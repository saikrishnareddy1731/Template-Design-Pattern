# Template Design Pattern in Java

The **Template Pattern** is a behavioral design pattern that defines the **skeleton of an algorithm** in a method, deferring some steps to subclasses.  
It lets subclasses redefine certain steps of an algorithm without changing the algorithm’s structure.

---

## 📖 Concept
- **Abstract Class (Game)** → Defines the template method (`play`) which contains the skeleton of the algorithm.  
- **Concrete Classes (Cricket, Football)** → Implement the abstract steps of the algorithm (`initialize`, `startPlay`, `endPlay`).  
- **Template Method** → Declared as `final` in the abstract class to prevent overriding.

---

## 📂 UML Diagram (Mermaid)
```mermaid
classDiagram
    class Game {
        <<abstract>>
        +initialize()
        +startPlay()
        +endPlay()
        +play()
    }

    class Cricket {
        +initialize()
        +startPlay()
        +endPlay()
    }

    class Football {
        +initialize()
        +startPlay()
        +endPlay()
    }

    Game <|-- Cricket
    Game <|-- Football
