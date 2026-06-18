# 💜 Planilla Anual de Finanzas · Contadora Lucy

## ¿Qué es este proyecto?

Una webapp de finanzas personales construida como un archivo HTML único, basada en la planilla Excel de Contadora Lucy (`Planilla Anual Finanzas ContadoraLucy.xlsx`).

Permite cargar ingresos, gastos fijos, gastos variables y ahorros mes a mes, con sincronización automática entre dispositivos.

**URL de la app:** https://comisionexpress.github.io/finanzas-lucy

---

## 🛠️ Tecnologías usadas

- **HTML + CSS + JavaScript** — todo en un único archivo `index.html`, sin frameworks
- **Firebase Authentication** — login con Google
- **Firebase Firestore** — base de datos en tiempo real para sincronizar entre dispositivos
- **GitHub Pages** — hosting gratuito

---

## 🔧 Configuración Firebase

El proyecto usa Firebase con las siguientes credenciales (ya integradas en `index.html`):

- **Proyecto Firebase:** `finanzas-lucy`
- **Auth Domain:** `finanzas-lucy.firebaseapp.com`
- **Consola Firebase:** https://console.firebase.google.com/project/finanzas-lucy

Para que el login con Google funcione, el dominio `comisionexpress.github.io` está autorizado en:
Firebase → Authentication → Settings → Dominios autorizados

---

## 📁 Estructura del archivo index.html

El archivo tiene estas secciones en orden:

1. **CSS** — estilos visuales (tema oscuro, colores por categoría)
2. **HTML** — pantalla de login, barra de sincronización, sidebar y páginas
3. **Firebase SDK** — importado desde CDN de Google
4. **JavaScript** — toda la lógica dentro de un `<script type="module">`

---

## 📊 Categorías de la planilla

### 💰 Ingresos
- Sueldo / Honorarios principales
- Ingresos actividad secundaria
- Cobros a clientes / Facturación
- Otros ingresos

### 🏠 Gastos Fijos
- Alquiler / Cuota hipoteca
- Expensas / ABL / Impuestos
- Electricidad, Gas
- Internet / Teléfono / Cable
- Obra social / Prepaga / Salud
- Colegio / Educación / Cuotas
- Cuota préstamo / tarjeta fija
- Seguro
- Otro gasto fijo recurrente

### 🛒 Gastos Variables
- Supermercado / Almacén / Verdulería
- Salidas a comer (restaurantes, delivery)
- Salidas con amigos / entretenimiento
- Ropa / Calzado / Accesorios
- Belleza / Peluquería / Estética
- Cursos / Libros / Capacitación
- Farmacia / Salud ocasional
- Regalos / Eventos / Cumpleaños
- Suscripciones (streaming, apps, gym)
- Transporte ocasional (remis, Uber, taxi)
- Gastos extras / imprevistos

### 🚀 Ahorro e Inversión
- Fondo de emergencia
- Ahorro (plazo fijo / FCI / billetera virtual)
- Inversión en negocio / capacitación
- Inversión (criptos / acciones / bonos)

---

## 🔄 Cómo actualizar la app

1. Editá el archivo `index.html` en GitHub (clic en el lápiz ✏️)
2. O descargá, editá localmente y volvé a subir
3. GitHub Pages se actualiza solo en 1-2 minutos

---

## 💾 Dónde se guardan los datos

Los datos se guardan en **Firestore** bajo esta estructura:

```
usuarios/
  {uid del usuario}/
    finanzas/
      2026  ← documento con todos los meses
```

Cada usuario solo puede ver y editar sus propios datos.

---

## 🚀 Funcionalidades actuales

- ✅ Login con Google
- ✅ 12 meses con todas las categorías
- ✅ Totales automáticos por mes
- ✅ Resumen anual con tabla comparativa
- ✅ Gráfico de barras por mes
- ✅ Notas por mes
- ✅ Sincronización en tiempo real entre dispositivos
- ✅ Indicador de estado de sincronización

## 🔮 Posibles mejoras futuras

- [ ] Exportar a PDF
- [ ] Agregar categorías personalizadas
- [ ] Gráfico de torta por categoría
- [ ] Comparar año anterior
- [ ] Presupuesto mensual vs real
