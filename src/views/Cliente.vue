<template>
    <div class="Cliente">
        <h1>Bienvenido Cliente</h1>
        <FormularioFactura />
        <Factura />

    </div>

</template>



<script>
import FormularioFactura from '@/components/formularioFactura.vue';
import Factura from '../components/factura.vue';


export default {
    name: "Vendedor-view",
    components: { FormularioFactura, Factura }
}
</script>



<style>

</style>