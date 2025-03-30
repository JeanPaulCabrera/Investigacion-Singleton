# Singleton

## Tipo de Patrón: Creacional

### Utilidad del Patrón
El patrón Singleton se utiliza para garantizar que una clase tenga una única instancia y proporcionar un punto de acceso global a dicha instancia. Este patrón es útil cuando se requiere controlar el acceso a recursos compartidos, como conexiones a bases de datos, registros de configuración o gestores de memoria.

#### Ejemplo de Uso
Un caso común para el patrón Singleton es la gestión de la conexión a una base de datos. Si cada parte de un programa creara una nueva conexión a la base de datos, esto podría generar un consumo excesivo de recursos y posibles bloqueos. Utilizando Singleton, se asegura que solo exista una conexión activa en la aplicación.

## Diagrama UML
![Diagrama UML del Singleton](ruta/a/la/imagen/uml_singleton.png)

## Pseudocódigo
```pseudo
class Singleton:
    private static instance = null
    
    private Singleton():
        // Constructor privado para evitar instancias directas
    
    public static getInstance():
        if instance == null:
            instance = new Singleton()
        return instance

// Uso del Singleton
singleton1 = Singleton.getInstance()
singleton2 = Singleton.getInstance()
print(singleton1 == singleton2)  // True, ambas referencias apuntan a la misma instancia
```

## Patrones Relacionados
- **Factory Method**: Puede utilizarse junto con Singleton para controlar la creación de instancias.
- **Prototype**: Alternativa cuando se requiere la clonación en lugar de restringir instancias.
- **Dependency Injection**: Puede reducir la necesidad de Singleton proporcionando instancias compartidas de otra manera.

## Recursos Visuales
- ![Explicación en video sobre Singleton](ruta/a/video/singleton_tutorial.mp4)
- ![Ejemplo de implementación](ruta/a/imagen/singleton_example.png)

## Referencias (Formato APA)
- Gamma, E., Helm, R., Johnson, R., & Vlissides, J. (1994). *Design Patterns: Elements of Reusable Object-Oriented Software*. Addison-Wesley.
- Freeman, E., Freeman, E., Bates, B., & Sierra, K. (2004). *Head First Design Patterns*. O'Reilly Media.