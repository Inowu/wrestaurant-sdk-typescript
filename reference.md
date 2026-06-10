# Reference
## Endpoints
<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">listarProductos</a>({ ...params }) -> WrestaurantApi.ProductsQueryResponse</code></summary>
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
await client.endpoints.listarProductos({
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

**request:** `WrestaurantApi.GetApiV1ProductosLicenseKeyRequest` 
    
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

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">listarEstaciones</a>({ ...params }) -> WrestaurantApi.StationsQueryResponse</code></summary>
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
await client.endpoints.listarEstaciones({
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

**request:** `WrestaurantApi.GetApiV1EstacionesLicenseKeyRequest` 
    
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

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">listarOrdenesTemporales</a>({ ...params }) -> WrestaurantApi.OrdersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Devuelve las órdenes abiertas del Punto de Venta de una sucursal, con filtro opcional por folio, número de cheque o total.
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
await client.endpoints.listarOrdenesTemporales({
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

**request:** `WrestaurantApi.GetApiV1TempOrdenesLicenseKeyRequest` 
    
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

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">crearUnaOrdenNuevaCuenta</a>({ ...params }) -> WrestaurantApi.CreateOrderResponse</code></summary>
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
await client.endpoints.crearUnaOrdenNuevaCuenta({
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

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">crearUnaOrdenCerradaVentaRapida</a>({ ...params }) -> WrestaurantApi.CreateClosedOrderResponse</code></summary>
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
await client.endpoints.crearUnaOrdenCerradaVentaRapida({
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

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">listarMeseros</a>({ ...params }) -> WrestaurantApi.MeserosResponse</code></summary>
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
await client.endpoints.listarMeseros({
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

**request:** `WrestaurantApi.GetApiV1MeserosLicenseKeyRequest` 
    
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

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">listarEmpresas</a>({ ...params }) -> WrestaurantApi.EmpresasResponse</code></summary>
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
await client.endpoints.listarEmpresas({
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

**request:** `WrestaurantApi.GetApiV1EmpresasLicenseKeyRequest` 
    
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

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">listarOrdenesAbiertasDelTurnoActual</a>({ ...params }) -> WrestaurantApi.OpenOrdersResponse</code></summary>
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
await client.endpoints.listarOrdenesAbiertasDelTurnoActual({
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

**request:** `WrestaurantApi.GetApiV1TempOrdenesAbiertasLicenseKeyRequest` 
    
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

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">listarDetallesDeOrdenesTemporales</a>({ ...params }) -> WrestaurantApi.OrderDetailsQueryResponse</code></summary>
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
await client.endpoints.listarDetallesDeOrdenesTemporales({
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

**request:** `WrestaurantApi.GetApiV1TempOrdenesDetLicenseKeyRequest` 
    
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

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">listarTodasLasFormasDePagoEnUnaSucursal</a>({ ...params }) -> WrestaurantApi.PaymentMethodsResponse</code></summary>
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
await client.endpoints.listarTodasLasFormasDePagoEnUnaSucursal({
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

**request:** `WrestaurantApi.GetApiV1FormasdepagoLicenseKeyRequest` 
    
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

