<template>
    <div class="factura">
        <fieldset>

            <legend>Factura</legend>
            <form action="">

                <body>
                var idCliente;
                var nombreCliente ;
                var direccionCliente;
                var telefonoCliente;
                var nombreProducto;
                var precio;
                var cantidad;
                var total;
                var subtotal;
                var p=0;
                var iva;
                var subtotalP=0;
                var fecha= new Date();
                var imprimir;
                var numero_Factura=0;


                function generarFactura(){


                idCliente=document.getElementById("idCliente").value;
                nombreCliente=document.getElementById("nombreCliente").value;
                direccionCliente=document.getElementById("direccionCliente").value;
                telefonoCliente=document.getElementById("telefonoCliente").value;



                document.write(fecha.getDate() + "/" + (fecha.getMonth()+1) + "/" +
                fecha.getFullYear()+","+","+",");
                document.write("Identificacion del Cliente:"+'&nbsp;'+idCliente+"<br>"+"<br>");
                document.write("Nombre del Cliente:"+'&nbsp;'+nombreCliente+"<br>"+"<br>");
                document.write("Direccion:"+'&nbsp;'+direccionCliente+"<br>"+"<br>");
                document.write("Telefono:"+'&nbsp;'+telefonoCliente+"<br>"+"<br>"+"<br>");


                for (subtotal=0; nombreProducto != "*"; subtotal++) {


                nombreProducto=prompt('Ingrese Nombre del Producto');
                document.write("Nombre Producto: "+'&nbsp;'+nombreProducto+'&nbsp;'+'&nbsp;');

                precio=parseFloat(prompt('Ingrese Precio'));
                document.write("Precio: "+'&nbsp;'+precio+'&nbsp;'+'&nbsp;');

                cantidad=parseInt(prompt('Ingrese Cantidad'));
                document.write("Cantidad: "+'&nbsp;'+cantidad+'&nbsp;'+'&nbsp;');


                nombreProducto=prompt('Ingrese "*" Para terminar o cualquier tecla para continuar');

                subtotal=precio*cantidad;
                subtotalP=subtotalP+parseInt(subtotal);
                iva=subtotalP*0.19;
                total=subtotalP+iva;


                document.write("SubTotal :"+'&nbsp;'+subtotal+"<br>"+"<br>"+"<br>");


                }
                document.write("Subtotal : "+'&nbsp;'+subtotalP+"<br>"+"<br>");
                document.write("Iva 19% :"+'&nbsp;'+iva+"<br>"+"<br>");
                document.write("Total :"+'&nbsp;'+total+"<br>"+"<br>");
                document.write('<button onclick="window.print()">Imprimir Factura</button>');

                }

                generarFactura()
            </body>


                


                <h2>Factura</h2>

             

                <body>

                    Numero Id <br><input type="text" name="idCliente" id="idCliente" placeholder="idCliente" /><br><br>
                    Nombre Cliente <br><input type="text" name="nombreCliente" id="nombreCliente"
                        placeholder="Nombre" /><br><br>
                    Direccion <br><input type="text" name="direccionCliente" id="direccionCliente"
                        placeholder="Direccion" /><br><br>
                    Telefono <br><input type="text" name="telefonoCliente" id="telefonoCliente"
                        placeholder="Telefono" /><br><br>
                    <input type="button" name="Continuar" onclick="generarFactura()" value="Continuar" />

                </body>

             


            </form>

        </fieldset>

    </div>

</template>

<script>
export default {
    name: "factura-view"
}
</script>

<style>
head {
    text-align: center;
    color: black;
    margin: 30px 30px;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 24px;
    font-weight: bolder;
}

/*nav,
section,
article,*/
footer {
    margin: 2em;
    padding: 1em;
    border: 1px;
    border-style: solid;
}

body {
    background-image: url(../../img/depositphotos_58059017.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    background-attachment: fixed;
    font-style: inherit;
    font-size: medium;
    font-feature-settings: "abvm";
}

.text {
    text-align: center;
    color: blue;
    margin: 30px 30px;
    font-family: Arial, Helvetica, sans-serif;
    font-size: 18px;
    font-weight: bolder;
}

.factura {
    table-layout: fixed;
}

.fact-info>div>h5 {
    font-weight: bold;
}

.factura>thead {
    border-top: solid 3px #000;
    border-bottom: 3px solid #000;
}

.factura>thead>tr>th:nth-child(2),
.factura>tbod>tr>td:nth-child(2) {
    width: 300px;
}

.factura>thead>tr>th:nth-child(n+3) {
    text-align: right;
}

.factura>tbody>tr>td:nth-child(n+3) {
    text-align: right;
}

.factura>tfoot>tr>th,
.factura>tfoot>tr>th:nth-child(n+3) {
    font-size: 24px;
    text-align: right;
}

.cond {
    border-top: solid 2px #000;
}


input[type=text],
select {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
}

input[type=email],
select {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
}

input[type=date],
select {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
}

input[type=number],
select {
    width: 100%;
    padding: 12px 20px;
    margin: 8px 0;
    display: inline-block;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
}

input[type=submit] {
    width: 100%;
    background-color: #4CAF50;
    color: white;
    padding: 14px 20px;
    margin: 8px 0;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

input[type=submit]:hover {
    background-color: #45a049;
}

div {
    border-radius: 5px;
    background-color: #f2f2f2;
    padding: 20px;
}
</style>