# IFTS Nº 29
# Estadística y probabilidades para el desarrollo del software
## Informe "Roles Junior en IT: Qué Busca el Mercado y Qué Ofrece"
### Análisis de datos sobre encuesta de salarios Sysarmy - Primer trimestre de 2024

#### Introducción:
En este informe se presenta un análisis de los datos recopilados sobre profesionales IT en posiciones Junior, enfocado en aspectos clave como tecnologías utilizadas, nivel académico alcanzado, los beneficios laborales ofrecidos, el salario y los años de experiencia laboral. Este análisis busca identificar patrones significativos que permitan comprender mejor las condiciones del mercado laboral y las habilidades más demandadas para los Juniors.


#### Hipótesis y Contexto:

##### Hipótesis:
"En el mercado actual, los roles Junior están sujetos a una creciente competitividad, donde los empleadores exigen niveles de formación específicos o académicos formales para diferenciar a los candidatos en un entorno saturado."

##### Marco Contextual:
En foros, redes sociales y otros medios informales, se discute frecuentemente que el mercado laboral para roles de nivel Junior está saturado. Esto ha llevado a que los empleadores, ante una alta cantidad de postulantes, aumenten sus expectativas y exijan no solo habilidades prácticas, sino también formaciones académicas específicas o formales como requisito para la contratación.

En este análisis, buscamos responder preguntas clave para entender qué solicitan las empresas en el nivel Junior, específicamente:
- ¿Qué habilidades, tecnologías y lenguajes son más comunes entre los Junior empleados formalmente?
- ¿Qué nivel de educación tienen los Junior contratados y cuál es el estado de esos estudios (completos/incompletos/en curso)?
- ¿Cuántos Junior lograron insertarse laboralmente con poca o ninguna experiencia previa?

El objetivo es contrastar estas observaciones con la percepción generalizada de que el mercado para Junior está saturado y explorar qué tan altas son las barreras de entrada para los postulantes interesados en roles de nivel inicial.

#### Metodología:
Datos utilizados:
Para este trabajo, partimos de los resultados de la última encuesta salarial de Openqube, publicada en el blog de Sysarmy, que nos fue proporcionada como base de análisis por la cátedra. Esta encuesta, ampliamente reconocida en el ámbito IT, recopila información sobre salarios, tecnologías utilizadas, beneficios laborales y otros aspectos clave del mercado laboral.

#### Herramientas:
El análisis fue realizado utilizando Python y Google Colab, junto con las siguientes librerías:
- io: Para la manipulación de archivos y datos de entrada.
- pandas: Para la limpieza, transformación y análisis de los datos.
- seaborn y matplotlib.pyplot: Para la visualización gráfica.
- numpy y scipy: Para el manejo y análisis de datos numéricos y estadísticos.
- 
#### Variables analizadas:
El documento original contenía 43 columnas, pero nuestro análisis se centró en aquellas que resultaban directamente relevantes para la hipótesis planteada. Las columnas seleccionadas fueron:
- ultimo_salario_mensual_o_retiro_bruto
- ultimo_salario_mensual_neto
- recibis_algun_tipo_de_bono
- contas_con_beneficios_adicionales
- anos_de_experiencia
- anos_en_el_puesto_actual
- plataformas_que_utilizas_en_tu_puesto_actual
- lenguajes_de_programacion_o_tecnologias_que_utilices_en_tu_puesto_actual
- frameworksherramientas_y_librerias_que_utilices_en_tu_puesto_actual
- base_de_datos
- modalidad_de_trabajo
- maximo_nivel_de_estudios
- estado
- genero
- sueldo_dolarizado
- seniority

#### Detalles a remarcar:
Durante la exploración inicial del dataset, se identificaron inconsistencias significativas en algunos registros. Para asegurar la calidad y relevancia de los datos, se tomaron las siguientes decisiones:

##### Relación sueldo bruto/neto:
Se detectaron disparidades notorias en la relación entre el sueldo bruto y neto. Por ejemplo, algunos encuestados reportaron valores que no correspondían a retenciones impositivas razonables. Estos registros fueron excluidos del análisis.

##### Edad:
Se recortaron registros de personas mayores de 73 años, considerando que esta edad excede el rango típico de la población activa en roles Junior.

##### Salarios extremadamente altos:
En los gráficos comparativos, se eliminaron registros con salarios netos inusualmente altos. Estos casos correspondían a cargos y niveles de experiencia incompatibles con la categoría 
Junior.

##### Inconsistencias en antigüedad y experiencia:
Hubo casos en los que los datos sobre años de experiencia, años en el cargo actual y antigüedad dentro de la empresa no eran coherentes. Por ejemplo, un encuestado reportó 0 años de experiencia, 19 años en la empresa y 0 años en el puesto actual. Dado que estas combinaciones no podían interpretarse con certeza, decidimos excluir la columna de "antigüedad dentro de la empresa" y trabajar únicamente con las columnas de "años de experiencia" y "años en el puesto actual", que mostraron mayor coherencia.
Estas acciones permitieron depurar el dataset, garantizando que los análisis y conclusiones se basen en datos representativos y confiables.

#### Análisis Relacionado a la Hipótesis
1. Nivel Académico y Experiencia
Analizar si las empresas están contratando Junior con niveles académicos avanzados (universitario o superior) o si se observa una mayor proporción de personas con estudios incompletos o en curso.
Investigar cuántos Junior tienen poca o ninguna experiencia laboral previa y si eso es una barrera para su inserción.
2. Habilidades y Tecnologías Solicitadas al Junior
Analizar las tecnologías más comunes entre los Junior activos en el mercado laboral.
Si su nivel máximo académico es el secundario (completo/incompleto), ¿qué tecnologías les solicitan?
3. Beneficios y Condiciones Laborales
Analizar los beneficios que suelen ofrecerse en roles Junior (e.g., capacitaciones, bonos, obra social, trabajo remoto) para identificar patrones que confirmen, desde otra perspectiva, las habilidades y conocimientos que son más valorados por el mercado.
Evaluar si los beneficios varían de manera significativa en función de las tecnologías utilizadas, las industrias o las competencias demandadas.
4. Salarios y Variables Relacionadas
Estimar rangos salariales promedio para Junior.
Verificar si el salario está influenciado por variables como tecnologías, experiencia, o nivel académico.



