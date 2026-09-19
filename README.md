# Anexos de datos

Series diarias del trabajo final de maestría **«Reconstrucción histórica de las
abstracciones y del balance hídrico en la cuenca del lago de Tota, Boyacá, Colombia»**,
de Oscar Iván Camargo Chaparro, Universidad Nacional de Colombia, Facultad de Ingeniería,
Departamento de Ingeniería Civil y Agrícola.

Los tres archivos se publican en **https://github.com/ocamargoc/balance-hidrico-lago-tota**, dirección que citan los anexos A y B
del documento.

## Los tres archivos

| Archivo | Qué contiene | Filas | Periodo |
|---|---|---:|---|
| `A1_serie_nivel_lago_1981_2024.csv` | Serie de nivel del lago en la estación Escaleras (35097070), con las cuatro capas de depuración y el nivel referido a cota | 16 071 | 1981-2024 |
| `B1_balance_hidrico_diario_1981_2024.csv` | Los cinco términos del balance hídrico a paso diario, con el nivel, el área y el volumen del lago | 16 071 | 1981-2024 |
| `B2_abstracciones_diarias_1981_2024.csv` | Serie diaria de abstracciones, en volumen y en caudal | 16 071 | 1981-2024 |

## Convención de los archivos

Texto plano en UTF-8, separador coma, punto decimal y fecha en formato ISO
(`1981-01-01`). Los volúmenes van en millones de metros cúbicos por día (Mm³/día),
los niveles en metros sobre el nivel del mar con tres decimales, el área en
kilómetros cuadrados y los caudales en litros por segundo. El campo vacío significa
que ese día no tiene valor.

## A1. Serie de nivel del lago

| Columna | Contenido |
|---|---|
| `fecha` | Día, en formato ISO |
| `lectura_original_cm` | Lectura de la mira tal como la publica el IDEAM |
| `pico_reemplazado` | `si` cuando el filtro de Hampel reemplazó un pico de un día |
| `lectura_sin_picos_cm` | Lectura después del filtro de picos |
| `ajuste_bloques_1981_2006_m` | Corrección del dígito de metros en marzo de 1981 y en abril y mayo de 2006 |
| `ajuste_1992_2004_m` | Corrección del dígito de metros entre el 22 de junio de 1992 y el 31 de mayo de 2004 |
| `lectura_corregida_cm` | Lectura con las tres correcciones aplicadas |
| `nivel_corregido_msnm` | Lectura corregida llevada a cota, con el cero de la mira en 3 013,776 m s.n.m. |
| `nivel_corregido_lleno_msnm` | Serie anterior con los vacíos llenados. **Es la que usa el documento** |
| `metodo_llenado` | Método con que se llenó el vacío, cuando lo hubo |
| `estado` | Nota sobre la verificación del tramo |

## B1. Balance hídrico diario

| Columna | Contenido |
|---|---|
| `fecha` | Día, en formato ISO |
| `nivel_msnm` | Nivel del lago, de la serie A1 |
| `area_km2` | Área del espejo de agua, de la curva cota-área |
| `volumen_Mm3` | Volumen almacenado, de la curva cota-volumen |
| `precipitacion_Mm3` | Precipitación directa sobre el espejo de agua |
| `afluente_corregido_Mm3` | Caudal afluente de las 31 subcuencas, con GR4J, descontada la derivación del Olarte |
| `evaporacion_Mm3` | Evaporación desde la superficie del lago, por el método de Penman |
| `descarga_orificio_Mm3` | Caudal por el orificio de la estructura de control |
| `descarga_herradura_Mm3` | Caudal por la herradura de la estructura de control |
| `descarga_total_Mm3` | Suma de las dos anteriores |
| `variacion_almacenamiento_Mm3` | Cambio del volumen entre dos días consecutivos |
| `abstracciones_Mm3` | Abstracciones despejadas del balance |
| `regimen_estructura` | Régimen hidráulico del día: sin descarga, superficie libre, orificio ahogado, u orificio y herradura |
| `evaluable` | `si` cuando el balance puede evaluarse ese día |

## B2. Abstracciones diarias

| Columna | Contenido |
|---|---|
| `fecha` | Día, en formato ISO |
| `abstracciones_Mm3_dia` | Abstracciones del día |
| `abstracciones_L_s` | Las mismas, en caudal medio del día |
| `evaluable` | `si` cuando el balance puede evaluarse ese día |


## Verificación

Sobre estos archivos, el balance puede evaluarse en **15 948 días**, el 99,2 % del
periodo, con **42 años válidos**. Las abstracciones acumulan **1 681,9 Mm³**, que en el
año equivalente del periodo son **38,49 Mm³/año**. Las tres cifras coinciden con las que
reporta el documento.

## Licencia y cita

Los datos se publican para que los resultados del trabajo puedan reproducirse y
verificarse. Al usarlos, citar el trabajo final de maestría.
