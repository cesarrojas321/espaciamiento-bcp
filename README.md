# Espaciamiento BCP: la cuenta de campo

Calculadora del espaciamiento del rotor para bombas de cavidades progresivas (BCP).

**Página:** https://cesarrojas321.github.io/espaciamiento-bcp/

## Por qué existe

En campo, el espaciamiento del rotor se hace a mano: con el metro, la libreta y la cuenta de cabeza en la boca del pozo. Así lo hacía yo cuando trabajaba en campo con BCP, y así se sigue haciendo hoy. Es un paso crítico: si el rotor queda bajo, golpea el niple de paro; si queda alto, trabaja fuera del estator y se pierde producción.

Esta herramienta lleva esa cuenta a datos. Con lo que se mide en el pozo, en segundos dice qué hacer y deja el razonamiento a la vista para verificarlo y enseñarlo.

## Qué hace

**Datos de entrada** (lo que se mide al tocar el pin de paro):

- Largo de las cabillas (25 o 30 ft).
- Con qué cabilla se tocó el pin de paro.
- Cuántos pies de esa cabilla sobran sobre la brida.
- Pandeo (lo que se sube hasta recuperar el peso de la sarta) y espaciamiento a levantar.
- Medidas del cabezal: prensaestopa (stuffing box), cabezal, grampa y stick-up. Con eso se calcula la barra libre.

**Resultado:**

- Cuántas cabillas sacar y cuáles.
- Con qué niples de cabilla completar, con los tamaños disponibles.
- Barra libre sobre la brida y sobre la grampa.
- Repaseo: cuánto debe quedar sobre la brida al volver a tocar.
- Profundidad del fondo del rotor al tocar y en posición de trabajo.
- Esquema de la sarta antes y después, y la cuenta paso a paso.

**Decodificar la bomba:** con el modelo del estator (ej. 98-1580, 200K1450, 20-40-2100) da el caudal por rpm, a 100 rpm y por vuelta, la presión máxima y el caudal teórico y real a las rpm y eficiencia que se elijan (300 rpm y 85 % por defecto). Muestra de dónde sale cada número, el cálculo de cabeza (× 6 y sumar el 5 %) y una tabla rápida de bombas comunes, entre ellas la KUDU 200K1450 (SLB). Explica por qué el caudal real es menor que el teórico (espaciamiento, presión, desgaste, gas, sumergencia) y calcula la eficiencia real con la prueba del pozo.

| Código | Significado | Cuenta |
|---|---|---|
| Primer número | m³ por día a 100 rpm | bpd por rpm = número × 6,29 ÷ 100 |
| Segundo número | metros de columna de agua | psi = metros × 3,28 × 0,433 |
| Por vuelta | volumen de las cavidades (4 · d · E · Pe) | cm³ = m³/d por rpm × 10⁶ ÷ 1.440 |

## Método

| Paso | Cuenta |
|---|---|
| Levantado | pandeo + espaciamiento |
| Barra libre | prensaestopa + cabezal + grampa + stick-up |
| Barra pulida adentro | largo de la barra pulida − barra libre |
| Hueco | lo que queda de la última cabilla bajo la brida + cabillas sacadas |
| Niples | hueco − barra pulida adentro |
| Repaseo | barra libre − levantado |

## Caso de práctica

Un espaciamiento completo con números de campo: cabilla #134, cabillas 1-1/8" × 30 ft, pandeo 24", espaciamiento 48", barra libre 84". La herramienta reproduce cada paso de la cuenta:

- 3 cabillas sacadas
- 3 niples de 8 ft
- fondo del rotor a 4.023,46 ft
- repaseo de 12"

## Uso

Funciona en el teléfono y en la computadora, sin instalar nada y sin internet una vez abierta. Tiene modo claro y oscuro. Los datos quedan guardados solo en el dispositivo.

## Próximos pasos

- Guardar cada pozo con su historial de espaciamientos.
- Exportar el reporte de espaciamiento.
- Validarlo con más casos de campo.

---

Desarrollado por **César Rojas**, técnico en levantamiento artificial (BCP).
