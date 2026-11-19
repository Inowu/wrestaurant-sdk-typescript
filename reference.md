# Reference
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

**request:** `WrestaurantApi.ListPrintersImpresorasRequest` 
    
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
    sourceId: "POS-01",
    kind: "thermal"
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

**request:** `WrestaurantApi.GetPrinterImpresorasRequest` 
    
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
    displayName: "Etiquetas barra",
    widthMm: 58,
    source: "windows",
    sourceId: "POS-01",
    kind: "label",
    label: {
        widthMm: 57.15,
        heightMm: 31.75,
        gapMm: 3.5,
        gapOffsetMm: 1.5,
        speed: 3,
        density: 8,
        direction: 0,
        copies: 1
    }
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

**request:** `WrestaurantApi.DeletePrinterImpresorasRequest` 
    
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
            sections: [{
                    label: "TITULAR",
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
                }, {
                    label: "INVITADO 1",
                    items: [{
                            idProduct: "01060",
                            name: "Ensalada C\u00E9sar",
                            quantity: 1,
                            price: 75,
                            modifiers: [{
                                    price: 1.1
                                }]
                        }]
                }]
        }],
    customer: {
        code: "A17",
        name: "Cliente Demo",
        type: "Socio",
        roomName: "Sala Terraza"
    },
    orderNote: "Sin popote"
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

<details><summary><code>client.impresoras.<a href="/src/api/resources/impresoras/client/Client.ts">printTest</a>({ ...params }) -> WrestaurantApi.PrintOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Envía un ticket o etiqueta de prueba a una sola impresora para comprobar que la configuración llega al papel. Usa la misma ruta que una impresión real.
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
await client.impresoras.printTest({
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

**request:** `WrestaurantApi.PrintTestRequest` 
    
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

**request:** `WrestaurantApi.GetPrintersImpresorasRequest` 
    
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

## Puntos de venta
<details><summary><code>client.puntosDeVenta.<a href="/src/api/resources/puntosDeVenta/client/Client.ts">getTicketHeader</a>({ ...params }) -> WrestaurantApi.TicketHeaderDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve los datos del negocio que se imprimen en el encabezado del ticket de cuenta de esta sucursal.

Estos datos no se leen del Punto de Venta. Es una configuración dentro del dashboard en WRestaurantAPI.
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
await client.puntosDeVenta.getTicketHeader({
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

**request:** `WrestaurantApi.GetTicketHeaderPuntosDeVentaRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PuntosDeVentaClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.puntosDeVenta.<a href="/src/api/resources/puntosDeVenta/client/Client.ts">updateTicketHeader</a>({ ...params }) -> WrestaurantApi.TicketHeaderDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Guarda los datos del negocio que se imprimen en el encabezado del ticket de cuenta de esta sucursal.

Se reemplaza el encabezado completo: los campos que se omitan quedan vacíos. Un campo vacío simplemente no se imprime, salvo `telefono`, cuya etiqueta "TEL:" aparece siempre.

Hay que configurarlo antes de la primera impresión. Sin él, el ticket se imprime sin el bloque del negocio.
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
await client.puntosDeVenta.updateTicketHeader({
    licenseKey: "licenseKey",
    body: {}
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

**request:** `WrestaurantApi.UpdateTicketHeaderPuntosDeVentaRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `PuntosDeVentaClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Productos
<details><summary><code>client.productos.<a href="/src/api/resources/productos/client/Client.ts">getProducts</a>({ ...params }) -> WrestaurantApi.ProductsQueryResponse</code></summary>
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
await client.productos.getProducts({
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

**request:** `WrestaurantApi.GetProductsProductosRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.productos.<a href="/src/api/resources/productos/client/Client.ts">createProducts</a>({ ...params }) -> WrestaurantApi.CreateProductsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Da de alta uno o varios productos (hasta 200 por solicitud) en una sola operación.

La clave (`idProducto`) es opcional. Si se envía, se usa tal cual y no debe existir ya. Si se omite, se genera automaticamente sin repetir ninguna clave existente. La respuesta devuelve la clave de cada producto en el mismo orden de la solicitud.

Se crean todos o ninguno. Si algún producto es inválido (clave ya existente o repetida, grupo, subgrupo, área o unidad inexistentes, o un subgrupo que no pertenece al grupo) la solicitud completa se rechaza con `400` y `errors` indica cada problema por su posición, por ejemplo `Productos[2].Subgrupos`.

Los impuestos son tasas en porcentaje (`16` = 16%); si se omiten se usan las tasas por defecto del Punto de Venta. El precio sin impuestos se calcula automáticamente.

Además, la operación:
- Registra el producto para venta a domicilio y kiosko, y su configuración de monedero (inactiva).
- Agrega una entrada de auditoría por producto en la bitácora del sistema.
- Marca los productos para sincronización con otros sistemas conectados.
- Avisa a las terminales del Punto de Venta que recarguen su catálogo.

Se recomienda enviar el encabezado `Idempotency-Key`: reintentar sin él crea de nuevo los productos cuya clave se generó, con claves distintas.
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
await client.productos.createProducts({
    licenseKey: "licenseKey",
    idEmpresa: "1",
    productos: [{
            descripcion: "AGUA DE JAMAICA 1 LT",
            idGrupo: "03",
            subgrupos: ["11"],
            nombreCorto: "JAMAICA 1LT",
            precio: 55,
            idArea: "1",
            idUnidad: "PZA",
            bloqueado: false,
            visibleMenu: false,
            usarComedor: true,
            usarDomicilio: true,
            usarRapido: true
        }, {
            idProducto: "CEB001",
            descripcion: "CERVEZA CEBADA",
            idGrupo: "03",
            subgrupos: ["13"],
            nombreCorto: "",
            precio: 150,
            impuesto1: 16,
            impuesto2: 8,
            impuesto3: 0,
            idArea: "1",
            idUnidad: "PZA",
            bloqueado: false,
            visibleMenu: false,
            usarComedor: true,
            usarDomicilio: true,
            usarRapido: true
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

**request:** `WrestaurantApi.CreateProductsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.productos.<a href="/src/api/resources/productos/client/Client.ts">updateProduct</a>({ ...params }) -> WrestaurantApi.UpdateProductResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Actualiza los datos principales de un producto existente: descripción, grupo, nombre corto, precio, impuestos, bloqueo, visibilidad en menú electrónico y si permite producto compuesto en modificador.

Es una actualización de reemplazo completo: se deben enviar todos los campos en cada solicitud (los valores omitidos no se conservan). El producto debe existir previamente — este endpoint no crea productos nuevos.

Además del cambio en sí, la operación aplica automáticamente estos efectos:
- Si el precio cambió, se registra en el historial de cambios de precio.
- Si el producto también está registrado como modificador de sí mismo, su precio se sincroniza.
- Se agrega una entrada de auditoría en la bitácora del sistema.
- Se marca el producto para sincronización con otros sistemas conectados.
- Avisa a las terminales del Punto de Venta que recarguen su catálogo.

No modifica grupos de modificadores, paquetes, costos, comentarios, asignaciones de estación/almacén ni configuración de monedero del producto — esa configuración, si existe, se conserva sin cambios.
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
await client.productos.updateProduct({
    licenseKey: "licenseKey",
    idProducto: "idProducto",
    idEmpresa: "1",
    descripcionProducto: "TECATE LIGHT (ACTUALIZADO)",
    idGrupo: "001",
    nombreCorto: "TECATE LIGHT (UPD)",
    visibleMenu: true,
    precio: 45,
    impuesto1: 16,
    impuesto2: 0,
    impuesto3: 0,
    bloqueado: false,
    permitirprodcompenmodif: true
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

**request:** `WrestaurantApi.UpdateProductRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.productos.<a href="/src/api/resources/productos/client/Client.ts">getBestSellers</a>({ ...params }) -> WrestaurantApi.BestSellersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Ranking de productos por unidades vendidas en cuentas cerradas, sin contar modificadores ni cuentas canceladas.

`clasificacion`: 1 = bebidas, 2 = alimentos, 3 = otros (omitido = todas). `dias` limita a las ventas de los últimos N días (omitido = todo el historial). `top` entre 1 y 50 (por omisión 1).
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
await client.productos.getBestSellers({
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

**request:** `WrestaurantApi.GetBestSellersProductosRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.productos.<a href="/src/api/resources/productos/client/Client.ts">getRecetas</a>({ ...params }) -> WrestaurantApi.RecetaResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve los insumos que componen la receta de un producto, con la cantidad que descuenta cada venta, sus costos por empresa y el almacén del que se descuenta en cada área del restaurante. Un producto sin receta responde con la lista de insumos vacía.
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
await client.productos.getRecetas({
    licenseKey: "licenseKey",
    idProducto: "idProducto"
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

**request:** `WrestaurantApi.GetRecetasProductosRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ProductosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Estaciones
<details><summary><code>client.estaciones.<a href="/src/api/resources/estaciones/client/Client.ts">getStations</a>({ ...params }) -> WrestaurantApi.StationsQueryResponse</code></summary>
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
await client.estaciones.getStations({
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

**request:** `WrestaurantApi.GetStationsEstacionesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EstacionesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Grupos
<details><summary><code>client.grupos.<a href="/src/api/resources/grupos/client/Client.ts">getGrupos</a>({ ...params }) -> WrestaurantApi.GruposQueryResponse</code></summary>
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
await client.grupos.getGrupos({
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

**request:** `WrestaurantApi.GetGruposGruposRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GruposClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.grupos.<a href="/src/api/resources/grupos/client/Client.ts">getSubgrupos</a>({ ...params }) -> WrestaurantApi.SubgruposResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve los subgrupos del menú (cada uno pertenece a un solo grupo; las descripciones se repiten entre grupos, así que identifique por `idSubgrupo`) y, para cada producto, el subgrupo en que está archivado (nulo si ninguno) y si se vende en comedor.
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
await client.grupos.getSubgrupos({
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

**request:** `WrestaurantApi.GetSubgruposGruposRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `GruposClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Insumos
<details><summary><code>client.insumos.<a href="/src/api/resources/insumos/client/Client.ts">getInsumos</a>({ ...params }) -> WrestaurantApi.InsumosQueryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve el catálogo de insumos (materia prima) de una sucursal, ordenado por descripción, con paginación, búsqueda y filtros opcionales por grupo, empresa y estatus. Cada insumo incluye su unidad de medida, grupo, costo, costo promedio, costo con impuestos, tasas de impuesto (en porcentaje), merma y configuración de inventario.

Solo se incluyen insumos simples: los insumos elaborados (recetas) no forman parte de este listado.
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
await client.insumos.getInsumos({
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

**request:** `WrestaurantApi.GetInsumosInsumosRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `InsumosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.insumos.<a href="/src/api/resources/insumos/client/Client.ts">getInsumoGrupos</a>({ ...params }) -> WrestaurantApi.InsumoGruposQueryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve los grupos de insumos configurados en una sucursal, ordenados por descripción, con paginación y búsqueda opcional. Cada grupo incluye su clasificación (alimentos, bebidas u otros), su cuenta contable y su tipo de pedido, con id y descripción.

El `idGrupo` de cada grupo es el valor que aceptan `GET /insumos` y `GET /insumos/elaborados` para filtrar por grupo.
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
await client.insumos.getInsumoGrupos({
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

**request:** `WrestaurantApi.GetInsumoGruposInsumosRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `InsumosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.insumos.<a href="/src/api/resources/insumos/client/Client.ts">getInsumosElaborados</a>({ ...params }) -> WrestaurantApi.InsumosElaboradosQueryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve los insumos elaborados (recetas o preparaciones que a su vez se usan como insumo) de una sucursal, ordenados por descripción, con paginación, búsqueda y filtros opcionales por grupo, empresa y estatus. Cada insumo incluye su unidad de medida, rendimiento, tiempos de preparación y de alerta, área de producción, costo, costo promedio, costo con impuestos, tasas de impuesto (en porcentaje) y merma.

Los insumos simples (materia prima) se consultan con `GET /insumos`.
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
await client.insumos.getInsumosElaborados({
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

**request:** `WrestaurantApi.GetInsumosElaboradosInsumosRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `InsumosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Turnos
<details><summary><code>client.turnos.<a href="/src/api/resources/turnos/client/Client.ts">getTurnos</a>({ ...params }) -> WrestaurantApi.TurnosQueryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve los turnos (cortes de caja) registrados en una sucursal, con paginación y búsqueda opcional. Admite filtros de fecha (inclusivos, formato ISO 8601) sobre la apertura (`aperturaStart`/`aperturaEnd`) y sobre el cierre (`cierreStart`/`cierreEnd`); cada límite es opcional y pueden combinarse. Nota: los turnos abiertos no tienen fecha de cierre, por lo que cualquier filtro sobre `cierre` los excluye.
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
await client.turnos.getTurnos({
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

**request:** `WrestaurantApi.GetTurnosTurnosRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TurnosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.turnos.<a href="/src/api/resources/turnos/client/Client.ts">closeShift</a>({ ...params }) -> WrestaurantApi.CloseShiftResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cierra un turno abierto: consolida las cuentas pagadas/canceladas en las tablas permanentes, libera mesas y marca el turno como cerrado. Requiere el idTurno exacto para evitar cerrar el turno equivocado cuando hay varios abiertos.
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
await client.turnos.closeShift({
    licenseKey: "licenseKey",
    idTurno: 22,
    estacion: "CAJA1",
    idEmpresa: "1",
    serie: "A"
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

**request:** `WrestaurantApi.CloseShiftRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TurnosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.turnos.<a href="/src/api/resources/turnos/client/Client.ts">openShift</a>({ ...params }) -> WrestaurantApi.OpenShiftResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Abre un nuevo turno para la estación y empresa indicadas. Devuelve el idTurno asignado junto con los datos de apertura (fondo, cajero, mesero, fondo en dólares). Falla con un error si ya existe un turno abierto para esa estación/empresa; ciérralo primero con turnos_cierre.
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
await client.turnos.openShift({
    licenseKey: "licenseKey",
    estacion: "CAJA1",
    idEmpresa: "1",
    idMesero: "",
    cajero: "",
    fondo: 0,
    fondoDolares: 0
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

**request:** `WrestaurantApi.OpenShiftRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TurnosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Asistencias
<details><summary><code>client.asistencias.<a href="/src/api/resources/asistencias/client/Client.ts">getAsistencias</a>({ ...params }) -> WrestaurantApi.AsistenciasQueryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve los registros de asistencia (entrada/salida) de los empleados de una sucursal, ordenados por empleado y hora de entrada, con paginación y búsqueda opcional por id o nombre del empleado. Cada registro incluye el nombre del empleado y su tipo (`1` = mesero, `2` = usuario), resueltos contra los catálogos correspondientes del Punto de Venta.

Por defecto se consulta el día operativo actual de SoftRestaurant: de las 06:00 a las 05:59:59 del día siguiente. El inicio de esa ventana es configurable vía `dayStartHour`, o puede reemplazarse por un rango explícito con `entradaStart` y `entradaEnd` (formato ISO 8601, ambos límites inclusivos y opcionales por separado). La ventana efectivamente aplicada se devuelve en `entradaStart`/`entradaEnd` de la respuesta.

Los registros cuya salida aún no se ha marcado se devuelven con `salida: null`, `abierta: true` y `duracionMinutos: null`. Usa `abiertas=true` para obtener solo a quienes siguen sin marcar salida, o `abiertas=false` para solo los turnos ya cerrados. Usa `tipo` para limitar la consulta a un solo catálogo de empleados.
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
await client.asistencias.getAsistencias({
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

**request:** `WrestaurantApi.GetAsistenciasAsistenciasRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AsistenciasClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Ordenes
<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">getTempOrders</a>({ ...params }) -> WrestaurantApi.OrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las órdenes del turno actual del Punto de Venta de una sucursal, con sus productos, formas de pago e impuestos.

Usa `folio` para traer una orden concreta: es una coincidencia exacta, no una búsqueda parcial. Omítelo para no filtrar por folio.

El parámetro `search` busca coincidencias parciales en folio, número de cheque, mesa y total.

Usa `facturado=true` para incluir solo órdenes ya facturadas, o `facturado=false` para incluir solo las no facturadas; si se omite, no se filtra por estado de facturación.

Retorna solo cuentas del turno en curso, no admite filtros de fecha.
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
await client.ordenes.getTempOrders({
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

**request:** `WrestaurantApi.GetTempOrdersOrdenesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">createTempOrders</a>({ ...params }) -> WrestaurantApi.CreateOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Crea una nueva cuenta y retorna el id.

`productos` puede ir vacío: la cuenta se abre sin artículos, igual que desde el punto de venta, y se le agregan después con `temp_ordenes/productos`.
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
await client.ordenes.createTempOrders({
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
            clasificacion: "2",
            modificador: 0,
            productoCompuestoPrincipal: 0,
            nombreCorto: "Hamb. doble",
            imagen: "",
            visibleMenu: true,
            idProdServSat: "50202306",
            comentario: "Sin pepinillos",
            precio: 89,
            precioSinImpuestos: 76.7241,
            impuesto1: 16,
            impuesto2: 0,
            impuesto3: 0,
            descuento: 0,
            bloqueado: false,
            permitirprodcompenmodif: false
        }, {
            idProducto: "14001",
            descripcionProducto: "Limonada natural",
            idGrupo: "0014",
            movimiento: 2,
            cantidad: 1,
            descripcionGrupo: "Refrescos",
            clasificacion: "1",
            modificador: 0,
            productoCompuestoPrincipal: 0,
            nombreCorto: "Limonada",
            imagen: "",
            visibleMenu: true,
            idProdServSat: "50202306",
            comentario: "",
            precio: 45,
            precioSinImpuestos: 38.7931,
            impuesto1: 16,
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

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">createClosedTempOrder</a>({ ...params }) -> WrestaurantApi.CreateClosedOrderResponse</code></summary>
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
await client.ordenes.createClosedTempOrder({
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
            clasificacion: "2",
            modificador: 0,
            productoCompuestoPrincipal: 0,
            nombreCorto: "Hamb. doble",
            imagen: "",
            visibleMenu: true,
            idProdServSat: "50202306",
            comentario: "",
            precio: 89,
            precioSinImpuestos: 76.7241,
            impuesto1: 16,
            impuesto2: 0,
            impuesto3: 0,
            descuento: 0,
            bloqueado: false,
            permitirprodcompenmodif: false
        }],
    idFormaDePago: "001",
    mesa: "5"
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

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">applyOrderDiscount</a>({ ...params }) -> WrestaurantApi.ApplyDiscountResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Aplica un descuento a toda una cuenta abierta, expresado como porcentaje del subtotal (modo "porcentaje") o como importe fijo (modo "importe").

Cuando el modo es "importe", `base` indica de qué cifra se resta ese importe: "subtotal" (por omisión) lo resta del subtotal sin impuestos, y "total" lo resta del total con impuestos. Sobre una cuenta de $35.00 con IVA, un importe de $10.00 deja el total en $23.40 con base "subtotal" y en $25.00 con base "total". En modo "porcentaje" el parámetro se ignora.

El descuento reemplaza cualquier descuento general previo de la cuenta — no se acumula. Para cancelar un descuento, envíe valor 0: los totales vuelven exactamente a sus valores originales.

La cuenta debe estar abierta: no pagada, no cancelada, no en uso en una estación, y sin imprimir (una cuenta impresa solo admite descuento si fue reabierta).

Además del descuento, la operación aplica automáticamente estos efectos:
- Recalcula todos los totales de la cuenta (subtotal, impuestos, total, alimentos/bebidas/otros).
- Reparte el descuento entre alimentos, bebidas y otros en proporción a su peso en el subtotal.
- Marca la cuenta para sincronización de descuentos con SoftRestaurant.
- Un descuento del 100% se registra como CORTESÍA: `totalDescuentos` conserva sólo los descuentos por producto y el importe general pasa a `totalCortesias`.
Los descuentos por producto ya aplicados a las líneas se conservan y se descuentan antes de este: el porcentaje general opera sobre el subtotal ya neteado.
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
await client.ordenes.applyOrderDiscount({
    licenseKey: "licenseKey",
    folio: 1,
    modo: "porcentaje",
    base: "subtotal",
    valor: 10,
    comentario: "Descuento de gerencia",
    idTipoDescuento: "",
    usuario: "ADMIN"
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

**request:** `WrestaurantApi.ApplyOrderDiscountRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">applyItemDiscounts</a>({ ...params }) -> WrestaurantApi.ApplyDiscountResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Aplica un descuento a una o más líneas de una cuenta abierta. Acepta los mismos parámetros y sigue las mismas reglas que el descuento general, pero referidos a cada línea en lugar de a toda la cuenta: `modo` ("porcentaje" o "importe") y, cuando el modo es "importe", `base` ("subtotal" o "total").

En modo "importe" el valor es POR UNIDAD. Una línea de 3 piezas a $100 con importe $50 sobre "total" descuenta $150 en total, porque cada pieza baja $50; el punto de venta lo guarda como un 50% en esa línea. Con base "subtotal" el importe se resta del precio unitario sin impuestos.

Cada línea se resuelve por separado: una misma petición puede combinar líneas con `modo` "porcentaje" y líneas con `modo` "importe", y usar bases distintas entre ellas.

Cada línea se identifica por su movimiento y su idProducto. El valor enviado reemplaza el descuento previo de esa línea — no se acumula. Para cancelar el descuento de una línea, envíe valor 0.

El descuento se guarda en la línea como porcentaje: el detalle de la cuenta no tiene columnas para el importe ni para la base, así que un importe se convierte a su porcentaje equivalente y sólo ese porcentaje queda almacenado.

Un descuento del 100% en una línea se registra como CORTESÍA, no como descuento — igual que un descuento general del 100%. Aplica también si el importe enviado iguala el precio unitario.

La operación es atómica: si alguna línea del cuerpo no existe en la cuenta, no se aplica ningún descuento y se devuelve un error. Las líneas no mencionadas conservan su descuento actual.

La cuenta debe estar abierta: no pagada, no cancelada, no en uso en una estación, y sin imprimir (una cuenta impresa solo admite descuento si fue reabierta).

Al terminar se recalculan todos los totales de la cuenta y se agrega una entrada de auditoría en la bitácora del sistema. Si la cuenta también tiene un descuento general, este se recalcula sobre el nuevo subtotal.
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
await client.ordenes.applyItemDiscounts({
    licenseKey: "licenseKey",
    folio: 1,
    comentario: "Producto con demora",
    idTipoDescuento: "",
    usuario: "ADMIN",
    items: [{
            movimiento: 1,
            idProducto: "001002",
            modo: "porcentaje",
            base: "subtotal",
            valor: 5
        }, {
            movimiento: 4,
            idProducto: "003002",
            modo: "porcentaje",
            base: "subtotal",
            valor: 50
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

**request:** `WrestaurantApi.ApplyItemDiscountsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">addOrderItems</a>({ ...params }) -> WrestaurantApi.AddOrderItemsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Agrega una o más líneas a una cuenta que ya está abierta. La operación sólo toca la cuenta temporal — no genera una venta ni reimprime nada.

El campo `movimiento` de cada producto sólo define el orden dentro de esta petición y a qué producto base pertenece cada modificador: debe empezar en 1 y ser consecutivo. El movimiento real dentro de la cuenta lo asigna el punto de venta continuando desde la última línea existente, y se devuelve en `movimientos` — son esos valores los que se usan después para descontar o cancelar cada línea.

Recuerde que `impuesto1`, `impuesto2` e `impuesto3` son TASAS en porcentaje (`16.00` = 16%), no importes.

La cuenta debe estar abierta: no pagada, no cancelada, no en uso en una estación, y sin imprimir (una cuenta impresa solo admite cambios si fue reabierta).

Al terminar se recalculan todos los totales de la cuenta. Si la cuenta ya tenía un descuento general, este se conserva y se vuelve a aplicar sobre el nuevo subtotal; los descuentos por producto de las líneas existentes tampoco se pierden.
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
await client.ordenes.addOrderItems({
    licenseKey: "licenseKey",
    folio: 1,
    usuario: "ADMIN",
    productos: [{
            idProducto: "27004",
            descripcionProducto: "",
            idGrupo: "",
            movimiento: 1,
            cantidad: 1,
            descripcionGrupo: "",
            clasificacion: "",
            modificador: 0,
            productoCompuestoPrincipal: 0,
            nombreCorto: "",
            imagen: "",
            visibleMenu: false,
            idProdServSat: "",
            comentario: "",
            precio: 260,
            precioSinImpuestos: 224.1379,
            impuesto1: 16,
            impuesto2: 0,
            impuesto3: 0,
            descuento: 0,
            bloqueado: false,
            permitirprodcompenmodif: false
        }, {
            idProducto: "27007",
            descripcionProducto: "",
            idGrupo: "",
            movimiento: 2,
            cantidad: 1,
            descripcionGrupo: "",
            clasificacion: "",
            modificador: 1,
            productoCompuestoPrincipal: 0,
            nombreCorto: "",
            imagen: "",
            visibleMenu: false,
            idProdServSat: "",
            comentario: "Sin cebolla",
            precio: 0,
            precioSinImpuestos: 0,
            impuesto1: 16,
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

**request:** `WrestaurantApi.AddOrderItemsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">cancelOrderItems</a>({ ...params }) -> WrestaurantApi.CancelOrderItemsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cancela una o más líneas de una cuenta abierta. Cada línea se identifica por su movimiento y su idProducto; la línea se retira de la cuenta y la cancelación queda registrada para el personal de cocina y para el reporte de cancelaciones de la sucursal.

Cancelar un producto base arrastra sus modificadores: se cancelan junto con él y aparecen en `movimientos`, por lo que `itemsCancelados` puede ser mayor que el número de líneas enviadas. Cancelar un modificador por separado sí es posible y no afecta al producto base.

La operación es atómica: si alguna línea del cuerpo no existe en la cuenta, no se cancela nada y se devuelve un error.

`razon` es el motivo de la cancelación en texto libre. Si la sucursal exige motivo (`forzarmotivocancela`), es obligatorio y no puede ir vacío. El punto de venta ofrece un catálogo de motivos sugeridos (SERVICIO LENTO, ERROR DE CAPTURA, MAL SABOR, CAMBIO DE OPINIÓN CLIENTE), pero son sólo texto y no llevan clave: envíe la descripción tal cual, o cualquier otro texto (máximo 200 caracteres).

Lo que queda guardado no es exactamente lo enviado: el punto de venta añade la mesa al final, con el formato `ERROR DE CAPTURA Mesa: CL-GE9-1`, porque su registro de cancelaciones no tiene columna de mesa. Esta API reproduce el mismo formato. En una venta sin mesa se guarda sólo el motivo.

La cuenta debe estar abierta: no pagada, no cancelada, no en uso en una estación, y sin imprimir (una cuenta impresa solo admite cambios si fue reabierta).

Además de retirar las líneas, la operación:
- Renumera las líneas restantes de forma consecutiva desde 1, igual que hace SoftRestaurant. Los movimientos devueltos son los que tenían ANTES de la renumeración.
- Marca los productos correspondientes como cancelados en producción para que cocina lo vea.
- Recalcula todos los totales de la cuenta, conservando el descuento general y los descuentos por producto de las líneas que sobreviven.
- Agrega una entrada de auditoría en la bitácora del sistema.

Cancelar todas las líneas deja la cuenta ABIERTA y vacía con totales en cero; no cancela la cuenta.
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
await client.ordenes.cancelOrderItems({
    licenseKey: "licenseKey",
    folio: 1,
    items: [{
            movimiento: 2,
            idProducto: "27004"
        }],
    razon: "CAMBIO DE OPINION CLIENTE",
    usuario: "ADMIN"
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

**request:** `WrestaurantApi.CancelOrderItemsRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">renameOrder</a>({ ...params }) -> WrestaurantApi.RenameOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cambia el nombre (mesa) de una cuenta abierta y registra el cambio en la bitácora del punto de venta.

El nombre no puede estar en uso por otra cuenta abierta sin pagar (`code: TABLE_IN_USE`). La cuenta debe estar abierta: no pagada, no cancelada, no en uso en una estación, y sin imprimir (una cuenta impresa solo admite cambios si fue reabierta).
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
await client.ordenes.renameOrder({
    licenseKey: "licenseKey",
    folio: 1
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

**request:** `WrestaurantApi.RenameOrderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">assignOrderClient</a>({ ...params }) -> WrestaurantApi.AssignOrderClientResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Vincula un cliente del punto de venta a una cuenta abierta y, si el cliente tiene un descuento, lo aplica a la cuenta. Obtenga la clave del cliente con `GET /clientes`.

El descuento del cliente reemplaza el descuento general que tuviera la cuenta; la respuesta incluye el descuento anterior y los totales actualizados.

Se rechaza si el cliente no existe (`code: CLIENT_NOT_FOUND`), está suspendido (`code: CLIENT_INACTIVE`), o tiene descuento y la sucursal no permite descuentos (`code: DISCOUNTS_DISABLED`). La cuenta debe estar abierta: no pagada, no cancelada, no en uso en una estación, y sin imprimir (una cuenta impresa solo admite cambios si fue reabierta).
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
await client.ordenes.assignOrderClient({
    licenseKey: "licenseKey",
    folio: 1,
    idCliente: "000002",
    usuario: "02"
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

**request:** `WrestaurantApi.AssignOrderClientRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">getOpenOrders</a>({ ...params }) -> WrestaurantApi.OpenOrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve todas las cuentas activas (sin cancelar) del turno operativo actual (6:00 AM – 5:59:59 AM del día siguiente).

`idMesero` limita el resultado a las cuentas de ese mesero. `soloPendientes=true` excluye las cuentas ya pagadas, que permanecen en la lista hasta el cierre del turno.
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
await client.ordenes.getOpenOrders({
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

**request:** `WrestaurantApi.GetOpenOrdersOrdenesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">getTempOrderDetails</a>({ ...params }) -> WrestaurantApi.OrderDetailsQueryResponse</code></summary>
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
await client.ordenes.getTempOrderDetails({
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

**request:** `WrestaurantApi.GetTempOrderDetailsOrdenesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">printOpenOrder</a>({ ...params }) -> WrestaurantApi.PrintOpenOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Imprime la cuenta de una orden abierta. Se comporta distinto según si la cuenta ya se había impreso:

- **Primera impresión**: la cuenta recibe su número de cheque, tomado del consecutivo de la sucursal, y queda marcada como impresa. Ese número es el que identifica la venta en los reportes y en la facturación.
- **Reimpresión**: la cuenta conserva su número de cheque; sólo se incrementa el contador de impresiones y la reimpresión queda registrada en la bitácora del punto de venta, con el usuario enviado en `usuario`.

No hace falta indicar cuál de las dos es: la decide el punto de venta según el estado de la cuenta. El resultado se informa en `esReimpresion`.
Imprimir NO cobra la cuenta. La orden sigue abierta, puede cerrarse con `POST /temp_ordenes/cerrar/{licenseKey}/{folio}`; una cuenta impresa sólo admite cambios si fue reabierta. Tampoco asigna turno ni folio de nota de consumo: eso ocurre al cobrar.
Es el endpoint para entregar otra copia del ticket después de cobrar: esa llamada es una reimpresión.
Antes de imprimir se recalculan los totales de la cuenta, conservando el descuento general y los descuentos por producto.
Requiere un turno abierto en la estación de la cuenta, y que la cuenta no esté cancelada ni en uso en una estación.
`imprimirTicket` (por omisión `true`) controla la impresión física del ticket. Envíe `false` para registrar la impresión en el punto de venta sin sacar papel. La impresión física no forma parte de la transacción: si falla, la cuenta queda impresa igualmente y el detalle se devuelve en `impresion`, sin cambiar el código de respuesta.
`includeOrderComments` (por omisión `false`) agrega al ticket el comentario de cada producto, impreso debajo del renglón al que pertenece. El comentario se lee de `tempcheqdet.comentario` de la propia cuenta, no de esta llamada, así que refleja lo que el punto de venta tiene guardado — incluido un cambio hecho desde SoftRestaurant. Un producto sin comentario no imprime renglón extra.
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
await client.ordenes.printOpenOrder({
    licenseKey: "licenseKey",
    folio: 1,
    imprimirTicket: true,
    usuario: "05",
    includeOrderComments: true
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

**request:** `WrestaurantApi.PrintOpenOrderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ordenes.<a href="/src/api/resources/ordenes/client/Client.ts">closeOpenOrder</a>({ ...params }) -> WrestaurantApi.CloseOpenOrderResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Cobra una orden abierta y la convierte en una venta: registra las formas de pago, marca la cuenta como pagada y la asigna al turno abierto de su estación. A partir de ese momento la orden ya no admite cambios, y el cierre de turno la migrará al histórico de órdenes.

**Pagos.** Envíe una o más formas de pago en `pagos` (hasta 10). La suma de `importe × tipoDeCambio` debe cubrir el total de la cuenta; si es menor, no se cobra nada y se devuelve un error con el total esperado. El excedente se entrega como cambio y se descuenta del pago en efectivo, igual que en el punto de venta: por eso un excedente sin ningún pago en efectivo se rechaza, ya que sería un cobro de más y no un cambio.

**Cobrar una cuenta no impresa se rechaza cuando la sucursal no permite cobrar sin imprimir; donde sí lo permite, la cuenta se cobra sin número de cheque, igual que en el punto de venta. El valor de esa configuración se devuelve en `pagarSinImprimir`.

**Cuentas sin productos.** Una cuenta vacía se puede cobrar: el total es 0.00 y se registra un pago de 0.00.

**Mesas.** Al cobrar, la cuenta libera la mesa que tenía asignada (`idMesa` al abrirla, o asignada desde el punto de venta). Si la mesa tiene otra cuenta abierta, sigue ocupada.

Requiere un turno abierto en la estación de la cuenta, y que la cuenta no esté pagada, cancelada ni en uso en una estación. Los totales se recalculan antes de cobrar, conservando el descuento general y los descuentos por producto.
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
await client.ordenes.closeOpenOrder({
    licenseKey: "licenseKey",
    folio: 1,
    pagos: [{
            idFormaDePago: "EF",
            importe: 500,
            propina: 0,
            tipoDeCambio: 1
        }, {
            idFormaDePago: "TARJC",
            importe: 620,
            propina: 50,
            referencia: "4242",
            tipoDeCambio: 1
        }],
    usuario: "05"
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

**request:** `WrestaurantApi.CloseOpenOrderRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `OrdenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Meseros
<details><summary><code>client.meseros.<a href="/src/api/resources/meseros/client/Client.ts">authenticateMesero</a>({ ...params }) -> WrestaurantApi.AuthenticatedMeseroDto</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Identifica al mesero al que pertenece un NIP. El NIP se valida en el punto de venta y nunca viaja en la respuesta.

Solo meseros activos. Un NIP que no identifica a un único mesero recibe `code: NIP_NOT_RECOGNIZED`.
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
await client.meseros.authenticateMesero({
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

**request:** `WrestaurantApi.AuthenticateMeseroRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MeserosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.meseros.<a href="/src/api/resources/meseros/client/Client.ts">getMeseros</a>({ ...params }) -> WrestaurantApi.MeserosResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve el listado de meseros configurados en una sucursal. Acepta búsqueda por texto libre sobre idmesero, nombre y perfil (search), o coincidencia exacta sobre idmesero (idMesero). Si se envía idMesero se ignora search.
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
await client.meseros.getMeseros({
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

**request:** `WrestaurantApi.GetMeserosMeserosRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MeserosClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## TiposDescuento
<details><summary><code>client.tiposDescuento.<a href="/src/api/resources/tiposDescuento/client/Client.ts">getTiposDescuento</a>({ ...params }) -> WrestaurantApi.TiposDescuentoResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve el catálogo de tipos de descuento visibles de la sucursal. La clave idTipoDescuento de cada elemento es la que se envía al aplicar un descuento.

Cuando maximoActivado es true, el campo descuento funciona como tope: un descuento mayor a ese porcentaje será rechazado por el punto de venta.
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
await client.tiposDescuento.getTiposDescuento({
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

**request:** `WrestaurantApi.GetTiposDescuentoTiposDescuentoRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `TiposDescuentoClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Mesas
<details><summary><code>client.mesas.<a href="/src/api/resources/mesas/client/Client.ts">getMesaAreas</a>({ ...params }) -> WrestaurantApi.MesaAreasResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve todas las áreas del restaurante configuradas en el punto de venta, incluidas las que no tienen mesas o no tienen ninguna mesa en uso. Cada área indica su mapa actual, cuántas mesas tiene y cuántas están en uso.

`idArea` es el valor que acepta `idAreaRestaurant` al abrir una orden. Envía idEmpresa para contar solo las mesas de esa empresa; la lista de áreas no cambia.
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
await client.mesas.getMesaAreas({
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

**request:** `WrestaurantApi.GetMesaAreasMesasRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MesasClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.mesas.<a href="/src/api/resources/mesas/client/Client.ts">getMesas</a>({ ...params }) -> WrestaurantApi.MesasResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las mesas de la sucursal agrupadas por área. Cada mesa indica si está en uso y las cuentas abiertas asignadas (folio, nombre, mesero), además de su posición en el mapa actual del área cuando está colocada en él.

Envía idEmpresa para devolver solo las mesas de esa empresa.
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
await client.mesas.getMesas({
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

**request:** `WrestaurantApi.GetMesasMesasRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `MesasClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Empresas
<details><summary><code>client.empresas.<a href="/src/api/resources/empresas/client/Client.ts">getEmpresas</a>({ ...params }) -> WrestaurantApi.EmpresasResponse</code></summary>
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
await client.empresas.getEmpresas({
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

**request:** `WrestaurantApi.GetEmpresasEmpresasRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `EmpresasClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Cheques
<details><summary><code>client.cheques.<a href="/src/api/resources/cheques/client/Client.ts">getOrders</a>({ ...params }) -> WrestaurantApi.OrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las órdenes cerradas/históricas del Punto de Venta de una sucursal, con filtro opcional por folio, número de cheque o total. Usa `facturado=true` para incluir solo órdenes ya facturadas, o `facturado=false` para incluir solo las no facturadas; si se omite, no se filtra por estado de facturación. Admite filtros de fecha (inclusivos, formato ISO 8601): `fechaStart`/`fechaEnd` sobre la fecha de apertura de la orden y `cierreStart`/`cierreEnd` sobre su fecha de cierre. Además, `turnoAperturaStart`/`turnoAperturaEnd` filtran por turno: devuelven las órdenes de TODOS los turnos abiertos dentro de ese rango de fechas, sin necesidad de enviar la lista de ids. Para filtrar por una lista explícita de ids de turno (potencialmente grande), usa `POST /ordenes/buscar/{licenseKey}`.
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
await client.cheques.getOrders({
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

**request:** `WrestaurantApi.GetOrdersChequesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ChequesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.cheques.<a href="/src/api/resources/cheques/client/Client.ts">searchOrders</a>({ ...params }) -> WrestaurantApi.OrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las órdenes cerradas/históricas cuyos ids de turno estén en la lista `idTurnos` enviada en el cuerpo (hasta 10,000 ids), con los mismos filtros opcionales de `GET /ordenes/{licenseKey}` (`search`, `facturado`, `fechaStart`/`fechaEnd`, `cierreStart`/`cierreEnd`) y paginación. Usa este endpoint cuando necesites filtrar por una lista explícita de turnos demasiado grande para la URL de un GET (~500 ids); si los turnos que te interesan corresponden a un rango de fechas, es más simple usar `GET /ordenes/{licenseKey}` con `turnoAperturaStart`/`turnoAperturaEnd`.
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
await client.cheques.searchOrders({
    licenseKey: "licenseKey",
    idTurnos: [18, 19, 22],
    page: 1,
    pageSize: 20,
    facturado: false,
    cierreStart: "2026-07-01T00:00:00Z",
    cierreEnd: "2026-07-15T23:59:59Z"
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

**request:** `WrestaurantApi.SearchOrdersRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ChequesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.cheques.<a href="/src/api/resources/cheques/client/Client.ts">getOrderDetails</a>({ ...params }) -> WrestaurantApi.OrderDetailsQueryResponse</code></summary>
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
await client.cheques.getOrderDetails({
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

**request:** `WrestaurantApi.GetOrderDetailsChequesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ChequesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.cheques.<a href="/src/api/resources/cheques/client/Client.ts">getDayOrders</a>({ ...params }) -> WrestaurantApi.OrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve todas las órdenes del día operativo actual (abiertas y cerradas), juntando las órdenes según los turnos que iniciaron y cerraron dentro de la ventana. Por defecto la ventana es 06:00–05:59:59 del día siguiente; el inicio es configurable vía dayStartHour. Usa `facturado=true` para incluir solo órdenes ya facturadas, o `facturado=false` para incluir solo las no facturadas; si se omite, no se filtra por estado de facturación.
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
await client.cheques.getDayOrders({
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

**request:** `WrestaurantApi.GetDayOrdersChequesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ChequesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Formas de pago
<details><summary><code>client.formasDePago.<a href="/src/api/resources/formasDePago/client/Client.ts">getPaymentMethods</a>({ ...params }) -> WrestaurantApi.PaymentMethodsResponse</code></summary>
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
await client.formasDePago.getPaymentMethods({
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

**request:** `WrestaurantApi.GetPaymentMethodsFormasDePagoRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FormasDePagoClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Facturas
<details><summary><code>client.facturas.<a href="/src/api/resources/facturas/client/Client.ts">getFacturaXml</a>({ ...params }) -> core.BinaryResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Descarga el contenido XML (CFDI) de la factura asociada a un número de cheque, dentro de una empresa del Punto de Venta.
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
await client.facturas.getFacturaXml({
    licenseKey: "licenseKey",
    numCheque: 1
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

**request:** `WrestaurantApi.GetFacturaXmlFacturasRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `FacturasClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Clientes
<details><summary><code>client.clientes.<a href="/src/api/resources/clientes/client/Client.ts">getClientes</a>({ ...params }) -> WrestaurantApi.ClientesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve, paginados, los clientes registrados en el Punto de Venta de una sucursal. `search` busca coincidencias parciales en nombre, email, RFC y CURP; `curp` filtra por coincidencia exacta y, si se envía, `search` se ignora.
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
await client.clientes.getClientes({
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

**request:** `WrestaurantApi.GetClientesClientesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `ClientesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Almacenes
<details><summary><code>client.almacenes.<a href="/src/api/resources/almacenes/client/Client.ts">getAlmacenes</a>({ ...params }) -> WrestaurantApi.AlmacenesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lista el catálogo de almacenes configurados en el punto de venta.
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
await client.almacenes.getAlmacenes({
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

**request:** `WrestaurantApi.GetAlmacenesAlmacenesRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `AlmacenesClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Inventario
<details><summary><code>client.inventario.<a href="/src/api/resources/inventario/client/Client.ts">getInventariosFisicos</a>({ ...params }) -> WrestaurantApi.InventariosFisicosResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Lista los inventarios físicos capturados en el punto de venta, del folio más reciente al más antiguo. Cada inventario compara la existencia teórica contra la física en hasta dos almacenes.
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
await client.inventario.getInventariosFisicos({
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

**request:** `WrestaurantApi.GetInventariosFisicosInventarioRequest` 
    
</dd>
</dl>

<dl>
<dd>

**requestOptions:** `InventarioClient.RequestOptions` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

