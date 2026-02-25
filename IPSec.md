
## Enfoque General

Este sección muestro cómo **NetBox** puede adaptarse a escenarios reales donde el modelo de datos no cubre completamente la documentación de implementación de VPN, obligando al uso de **Custom Fields**.

 La sección de VPN funciona, pero no está tan normalizada como debería. Los "Custom Fields" existen para cubrir esa brecha, ya que NetBox no ofrece un modelo nativo para:
 * Rutas VPN
 * Peers remotos
 * Relación lógica ISP ↔ túnel (Futura Relacion)

Eso es una **decisión técnica**, no un error. - 

---
## Estructura que utilize para documentar los Túneles VPN

### 1. Campos personalizados (Custom Fields)

| **Campo**       | **Tipo de objeto (Ubicacion)** | **Tipo de dato**  | **Propósito**                         |
| --------------- | ------------------------------ | ----------------- | ------------------------------------- |
| `Output_ISP`    | Túnel                          | Objeto            | ISP o salida asociada al túnel        |
| `Rutas_Locales` | Túnel                          | Objetos múltiples | Redes locales anunciadas por el túnel |
| `Peer_Remoto`   | Túnel / Terminación de túnel   | Objeto            | Endpoint remoto de la VPN             |
![[Pasted image 20260225075931.png]]
___
### Ejemplos



### Visión a futuro

* Lograr vincular los circuitos o ISP con los tunes, me gustaria que tengan una relacion directa


---


