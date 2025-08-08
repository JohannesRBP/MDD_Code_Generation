# 🧩 MDD : Graphical Modeling and Code Generation in C#

[![MIT license](https://img.shields.io/badge/license-MIT-brightgreen.svg)](http://opensource.org/licenses/MIT)
[![C#](https://img.shields.io/badge/language-C%23-blue.svg)](https://learn.microsoft.com/en-us/dotnet/csharp/)



## 🎯 Project Purpose

The goal is to create a graphical modeling tool that allows users to design enriched class diagrams and automatically generate:

- ✅ HTML pages for each class and association (Home, Create, List)
- ✅ C# class files with attributes, inheritance, and operations
- ✅ A dynamic HTML menu linking all generated components

This second phase of the project introduces improvements in the **metamodel**, **graphical metaphors**, **iconography**, and **code generation logic**.

---

## 🧠 What the Project Does

### 🧬 Metamodel Enhancements

- Modified multiplicities in inheritance and style relationships
- Added enumerations for cardinality
- Extended association properties with richer metadata

### 🎨 Graphical Metaphors

- New metaphor for identifier attributes
- Updated connectors for associations with decorators for cardinality and naming

### 🖼️ Iconography System

The modeling tool includes a rich icon set for:

- **Connectors**: Association, Composition, Inheritance, Reference
- **Tools**: Class, Attribute, Operation, Parameter, Enumeration, Identifier
- **Styles**: Font, color, alignment for enriched classes and their elements

---

## 🧱 Architecture & Code Generation

### 🧑‍💻 C# Class Generation

Each class is translated into a `.cs` file with:

- Class declaration (`public`, `abstract`, or `extends`)
- Identifier and regular attributes
- Constructor
- Getters and setters
- Operations with input/output parameters and placeholder logic (`// To Do`)
- Inherited members if subclass

### 🌐 HTML Page Generation

For each class or association, the system generates:

- `Home.html`: Navigation and links to Create/List pages
- `Alta.html`: Form for creating new instances
- `Lista.html`: Table listing instances with actions (Consult, Modify, Delete)

HTML styling is dynamically applied based on enrichment and style definitions.

### 📋 Menu Generation

A dynamic HTML menu is generated with links to all classes and N:M associations.

---

## 🧪 Example Output

### C# Abstract Class
```csharp
public abstract class Persona {
    private string DNI;
    private string nombre;
    private string apellidos;
    private int telefono;

    public Persona() {}

    public string GetDNI() => DNI;
    public void SetDNI(string dni) => DNI = dni;
    // ...
}
