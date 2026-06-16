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

<details><summary><code>client.endpoints.<a href="/src/api/resources/endpoints/client/Client.ts">getTempOrders</a>({ ...params }) -> WrestaurantApi.OrdersResponse</code></summary>
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

