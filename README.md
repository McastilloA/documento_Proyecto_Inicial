<!-- Sección general -->
#### Integrantes:

 * Héctor Andrés Leyton Muñoz
 * Jeisson Andrés López Abril
 * Miguel Alejandro Castillo
<!-- Sección general -->


##### Actividad 1 - Creación del documento inicial del proyecto.



<!-- Sección actividad 1 -->
# Creación del documento inicial del proyecto.

### Diagrama EDT.
![gloomap_cbcb2b72](https://user-images.githubusercontent.com/43456634/160538464-70f36531-a2bf-43b8-80fa-9a1ee60164f6.png)

[*Ver imagen completa*](https://laiberocol-my.sharepoint.com/:i:/g/personal/mcasti40_ibero_edu_co/EZA9s4k9vyFHgFB1bCmvXZEBSEzLCsjhJ7kAo2eAbYN0cg?e=fSTTKS)

En esta actividad se elabora un documento de especificaciones del proyecto. En este documento se especifica la descripción del proyecto, el alcance, los objetivos del mismo y la estructura de desglose de actividades del trabajo (EDT). Donde el objetivo general es elaborar un software de control de ingreso para los establecimientos del municipio de Mosquera. Esta actividad se encuentra cargada en el repositorio en la carpeta planeación del mismo.
<!-- Sección actividad 1 -->

---------------------------------------------------------------------------------------------------------------------------------------------------------

##### Actividad 2 - Construir en el documento la planeación del proyecto.



<!-- Sección actividad 2 -->
# Construir en el documento la planeación del proyecto.

### Cronograma planeación de proyecto (Temporal).
![Screenshot from 2022-05-04 01-13-26](https://user-images.githubusercontent.com/43456634/166630972-d080c064-eb7c-4f13-b634-7d9a9b92b596.png)


En esta actividad se elabora la estimación en proyectos de software, la gestión de riesgos y las herramientas de gestión de proyectos. Donde el principal objetivo son los siguientes elementos:
* Estimación del proyecto (recursos y tiempos).
* Planeación temporal (Cronograma y diagrama de gantt).
* Desglose de riesgos del proyecto (diagrama RBS).
* Matriz de riesgos del mismo.

Esta actividad se encuentra cargada en el repositorio en la carpeta planeación del mismo.
<!-- Sección actividad 2 -->

---------------------------------------------------------------------------------------------------------------------------------------------------------

##### Actividad 3 - Creación del documento de historias de usuario.



<!-- Sección actividad 3 -->
# Creación del documento de historias de usuario.

### Planeacion historia de usuarios HU (Final).
![Screenshot from 2022-05-05 01-43-24](https://user-images.githubusercontent.com/43456634/166874556-8bbad8ca-b940-42f6-b254-560b1b2c83d0.png)


En esta actividad se construyen las historias de usuario asociadas al proyecto en las cuales se definan los criterios de aceptación asociados a cada historia de usuario con la finalidad de especificar los requerimientos del producto de software a desarrollar. Esta actividad se encuentra 
cargada en el repositorio en la carpeta historia_usuarios del mismo.
<!-- Sección actividad 3 -->

---------------------------------------------------------------------------------------------------------------------------------------------------------

##### Actividad 4 - Scripts de testing.



<!-- Sección actividad 4 -->
# Scripts de testing.

### Scripts, tecnicas TDD y tecnicas BDD.

Ejemplo tecnica BDD (Interfaz registrar usuarios)

![img_BDD](https://user-images.githubusercontent.com/43456634/169629934-4ca68310-952b-4cc9-9c73-20b53b4037e7.png)


Ejemplo tecnica TDD (Interfaz registrar usuarios)

```
<?php
require_once 'class_test.php';

if($_REQUEST){

	$test = new test();

    $test1 = $test->validaField($_REQUEST);   

    if($test1 == "OK"){
        
        $test2pass = $test->validaType("pass",$_REQUEST["pass"]);
        $test2nombre = $test->validaType("nombre",$_REQUEST["nombre"]);
        $test2apellido = $test->validaType("apellido",$_REQUEST["apellido"]);
        $test2correo = $test->validaType("correo",$_REQUEST["correo"]);
        
        if($test2pass == "OK" && $test2nombre == "OK" && $test2apellido == "OK" && $test2correo == "OK"){

            $test3 = $test->validarDatos($_REQUEST["nombre"],$_REQUEST["apellido"],$_REQUEST["correo"],$_REQUEST["user"],$_REQUEST["pass"],$_REQUEST["pass_confirm"]);
            
            if($test3 == "OK"){
                $test4 = $test->validarClave($_REQUEST["pass"]);
                
                if($test4 == "OK"){
                    echo "REGISTRO VÁLIDO";
                }else{
                    echo "REGISTRO NO VÁLIDO: " . $test4;
                }
            }else{
                echo "MESSAGE 3: " . $test3;
            } 

        }else{
            echo "MESSAGE 2: " . $test2pass.",". $test2nombre.",". $test2apellido.",". $test2correo;
        } 
    }else{
        echo "MESSAGE 1: " . $test1;
    } 

}else{

    die('data no permitida');
}
?>
```


En esta actividad se construyen los scripts de test unitarios (técnicas de TDD) y de aceptación (técnicas de BDD) basados en algunas historias de usuario cargadas en el repositorio. Esta actividad se encuentra cargada en el repositorio en la carpeta test del mismo.
<!-- Sección actividad 4 -->

---------------------------------------------------------------------------------------------------------------------------------------------------------












<!-- Sección general footer -->
###### *Todos los derechos son reservados a Miguel Alejandro Castillo - Héctor Andrés Leyton Muñoz - Jeisson Andrés López Abril*
<!-- Sección general footer -->
