# Reference
## Endpoints
<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getProducts</a>({ ...params }) -> WrestaurantApi.ProductsQueryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve el catálogo de productos de una sucursal, con paginación y filtros opcionales por grupo, clasificación y visibilidad en menú.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getProducts({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetProductsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getStations</a>({ ...params }) -> WrestaurantApi.StationsQueryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las estaciones (mesas, áreas, terminales) configuradas en una sucursal, con paginación y búsqueda opcional.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getStations({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetStationsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getGrupos</a>({ ...params }) -> WrestaurantApi.GruposQueryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve los grupos (categorías de productos) configurados en una sucursal, con paginación y búsqueda opcional por id, descripción o clasificación.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getGrupos({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetGruposRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getTurnos</a>({ ...params }) -> WrestaurantApi.TurnosQueryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve los turnos (cortes de caja) registrados en una sucursal, con paginación y búsqueda opcional.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getTurnos({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetTurnosRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getTempOrders</a>({ ...params }) -> WrestaurantApi.OrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las órdenes del turno actual por punto de Venta de una sucursal, con filtro opcional por folio, número de cheque o total.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getTempOrders({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetTempOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">createTempOrders</a>({ ...params }) -> WrestaurantApi.CreateOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Crea una nueva cuenta y retorna el id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.createTempOrders({
    licenseKey: "licenseKey",
    turnDependent: true,
    mesa: "5",
    idMesero: "001",
    estacion: "CAJA1",
    serie: "A",
    idEmpresa: "1",
    noPersonas: 2,
    productos: [{
            idProducto: "01052",
            descripcionProducto: "Hamburguesa doble carne",
            idGrupo: "0007",
            movimiento: 1,
            cantidad: 2,
            descripcionGrupo: "Hamburguesas",
            clasificacion: "ALIMENTOS",
            productoCompuestoPrincipal: 0,
            nombreCorto: "Hamb. doble",
            imagen: "",
            visibleMenu: true,
            idProdServSat: "50202306",
            comentario: "Sin pepinillos",
            precio: 89,
            precioSinImpuestos: 76.72,
            impuesto1: 12.28,
            impuesto2: 0,
            impuesto3: 0,
            descuento: 0,
            bloqueado: false,
            permitirprodcompenmodif: false
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.CreateOrderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">createClosedTempOrder</a>({ ...params }) -> WrestaurantApi.CreateClosedOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Crea una nueva venta cerrada con su pago y retorna el folio generado.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.createClosedTempOrder({
    licenseKey: "licenseKey",
    turnDependent: true,
    estacion: "CAJA1",
    serie: "A",
    idEmpresa: "1",
    noPersonas: 1,
    productos: [{
            idProducto: "01052",
            descripcionProducto: "Hamburguesa doble carne",
            idGrupo: "0007",
            movimiento: 1,
            cantidad: 1,
            descripcionGrupo: "Hamburguesas",
            clasificacion: "ALIMENTOS",
            productoCompuestoPrincipal: 0,
            nombreCorto: "Hamb. doble",
            imagen: "",
            visibleMenu: true,
            idProdServSat: "50202306",
            comentario: "",
            precio: 89,
            precioSinImpuestos: 76.72,
            impuesto1: 12.28,
            impuesto2: 0,
            impuesto3: 0,
            descuento: 0,
            bloqueado: false,
            permitirprodcompenmodif: false
        }],
    idFormaDePago: "001"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.CreateClosedOrderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getMeseros</a>({ ...params }) -> WrestaurantApi.MeserosResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve el listado de meseros configurados en una sucursal.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getMeseros({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetMeserosRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getEmpresas</a>({ ...params }) -> WrestaurantApi.EmpresasResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las empresas registradas en el Punto de Venta de una sucursal.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getEmpresas({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetEmpresasRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getOpenOrders</a>({ ...params }) -> WrestaurantApi.OpenOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve todas las cuentas activas (sin cancelar) del turno operativo actual (6:00 AM – 5:59:59 AM del día siguiente).
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getOpenOrders({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetOpenOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getTempOrderDetails</a>({ ...params }) -> WrestaurantApi.OrderDetailsQueryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las líneas de productos temporales de una sucursal, con paginación y filtros opcionales por folio de orden o búsqueda por producto.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getTempOrderDetails({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetTempOrderDetailsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getOrders</a>({ ...params }) -> WrestaurantApi.OrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las órdenes cerradas/históricas del Punto de Venta de una sucursal, con filtro opcional por folio, número de cheque o total.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getOrders({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getOrderDetails</a>({ ...params }) -> WrestaurantApi.OrderDetailsQueryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las líneas de productos de órdenes cerradas/históricas de una sucursal, con paginación y filtros opcionales por folio de orden o búsqueda por producto.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getOrderDetails({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetOrderDetailsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getDayOrders</a>({ ...params }) -> WrestaurantApi.OrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve todas las órdenes del día operativo actual (abiertas y cerradas), juntando las órdenes según los turnos que iniciaron y cerraron dentro de la ventana. Por defecto la ventana es 06:00–05:59:59 del día siguiente; el inicio es configurable vía dayStartHour.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getDayOrders({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetDayOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getPaymentMethods</a>({ ...params }) -> WrestaurantApi.PaymentMethodsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retorna todas las formas de pago disponibles en una sucursal específica.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.endpoints.getPaymentMethods({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetPaymentMethodsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EndpointsClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Impresoras
<details><summary><code>client.impresoras.<a href="/src/api/resources/impresoras/client/Client.ts">listPrinters</a>({ ...params }) -> WrestaurantApi.PrinterDto[]</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las impresoras del usuario. Filtra por licenseKey para limitar a un solo punto de venta.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.impresoras.listPrinters();

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.ListPrintersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ImpresorasClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.impresoras.<a href="/src/api/resources/impresoras/client/Client.ts">createPrinter</a>({ ...params }) -> WrestaurantApi.PrinterDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Registra una nueva impresora en uno de los puntos de venta del usuario.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.impresoras.createPrinter({
    licenseKey: "DS5D2368HCME4O9X",
    printerIp: "192.168.1.50",
    displayName: "Cocina",
    widthMm: 80,
    source: "windows",
    sourceId: "POS-01"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.CreatePrinterRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ImpresorasClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.impresoras.<a href="/src/api/resources/impresoras/client/Client.ts">getPrinter</a>({ ...params }) -> WrestaurantApi.PrinterDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve una impresora del usuario por su id.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.impresoras.getPrinter({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetPrinterRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ImpresorasClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.impresoras.<a href="/src/api/resources/impresoras/client/Client.ts">updatePrinter</a>({ ...params }) -> WrestaurantApi.PrinterDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Actualiza la configuración de una impresora existente del usuario.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.impresoras.updatePrinter({
    id: "id",
    printerIp: "192.168.1.51",
    displayName: "Cocina (caliente)",
    widthMm: 80,
    source: "windows",
    sourceId: "POS-01"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.UpdatePrinterRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ImpresorasClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.impresoras.<a href="/src/api/resources/impresoras/client/Client.ts">deletePrinter</a>({ ...params }) -> void</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Elimina de forma permanente una impresora del usuario.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.impresoras.deletePrinter({
    id: "id"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.DeletePrinterRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ImpresorasClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.impresoras.<a href="/src/api/resources/impresoras/client/Client.ts">printOrder</a>({ ...params }) -> WrestaurantApi.PrintOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Renderiza tickets ESC/POS y los envía a las impresoras de la sucursal. Cada grupo apunta a una impresora por su id (printerId). Marca isReprint=true para reimpresiones.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.impresoras.printOrder({
    licenseKey: "licenseKey",
    orderFolio: "169",
    isReprint: false,
    price: 128.5,
    paymentMethod: "CARD",
    businessName: "Mi Restaurante",
    businessSubtitle: "Sucursal Centro",
    groups: [{
            printerId: "00000000-b12a-405f-905d-dbf424c20000",
            jobType: "order",
            title: "COCINA",
            items: [{
                    idProduct: "01052",
                    name: "Hamburguesa doble carne",
                    quantity: 2,
                    price: 89,
                    modifiers: [{
                            idModifier: "50110",
                            name: "Sin cebolla",
                            price: 0
                        }],
                    notes: "Sin pepinillos"
                }]
        }]
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.PrintOrderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ImpresorasClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.impresoras.<a href="/src/api/resources/impresoras/client/Client.ts">getPrinters</a>({ ...params }) -> WrestaurantApi.PrinterAssignmentsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las impresoras configuradas para la sucursal (id, IP, nombre, ancho), para que el kiosko elija el printerId al imprimir.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```typescript
await client.impresoras.getPrinters({
    licenseKey: "licenseKey"
});

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `WrestaurantApi.GetPrintersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ImpresorasClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

