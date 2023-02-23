<template>
    <div>
            <p> {{ name }}</p>

            <!-- ref a "el" es asociarlo a la variable "el" en script-->
            <input ref="el" type="text" placeholder="Name" v-model="name"/>
            <div>
                <!-- @ reemplaza el OnEvent, o  -->
                <!-- addEventhandler -->
                <button 
                @click="submitForm"
                v-bind:disabled = "name.length==0"
                >
                <!-- v-bind:disabled = "name.length==0" forma larga -->
                Submit Form</button>
            </div>

    </div>
</template>

<!-- el export default y setup puede ser reemplazado -->
<!-- por atributo "setup en script" -->
<script>

    import { ref, onMounted} from 'vue'
    
    export default
    {
        // TODO SE DEBE RETURNEAR!
        setup()
        {
            const name = ref('')
            const el = ref()
            const submitForm = () =>
            {
                console.log(`Form submitted: Name = ${name.value}`)
            }

            // Mounted significada que un componente
            // se INICIALIZÓ y se MOSTRÓ el template en el DOM
            onMounted
            (
                () =>
                {
                    // console.log(el.value)
                    el.value.focus () // Hacemos que se seleccione automaticamente
                }
            )

            // EL RETURN ES DE SETUP SIEMPRE!
            return {name, submitForm, el}        
        }      
    }

</script>



<!-- <style>
    input[type='text']
    { 
        padding:5 px;
        color: #986;
    }

    button
    {
        margin-top: 20px;
    }
</style> -->