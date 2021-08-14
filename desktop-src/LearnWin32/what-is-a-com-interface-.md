---
title: Qu’est-ce qu’une interface COM ?
description: Qu’est-ce qu’une interface COM ?
ms.assetid: 36f27a58-cc63-4b67-bdcb-8f9a19650c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a6eac63fb6395e04f36c89826a392046c906a70105e19bb6b9514975d89197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387600"
---
# <a name="what-is-a-com-interface"></a>Qu’est-ce qu’une interface COM ?

Si vous connaissez C# ou Java, les interfaces doivent être un concept familier. Une *interface* définit un ensemble de méthodes qu’un objet peut prendre en charge, sans dicter aucune information sur l’implémentation. L’interface marque une limite claire entre le code qui appelle une méthode et le code qui implémente la méthode. En termes d’informatique, l’appelant est *découplé* de l’implémentation.

![Illustration montrant la limite de l’interface entre un objet et une application](images/com01.png)

En C++, l’équivalent le plus proche d’une interface est une classe virtuelle pure, c’est-à-dire une classe qui contient uniquement des méthodes virtuelles pures et aucun autre membre. Voici un exemple hypothétique d’une interface :

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

L’idée de cet exemple est qu’un ensemble d’objets dans une bibliothèque de graphiques peuvent être dessinés. L' `IDrawable` interface définit les opérations que chaque objet pouvant être dessiné doit prendre en charge. (Par Convention, les noms d’interface commencent par « I ».) Dans cet exemple, l' `IDrawable` interface définit une opération unique : `Draw` .

Toutes les interfaces étant *abstraites*, un programme n’a pas pu créer une instance d’un `IDrawable` objet en tant que tel. Par exemple, le code suivant n’est pas compilé.

```C++
IDrawable draw;
draw.Draw();
```

Au lieu de cela, la bibliothèque Graphics fournit des objets qui *implémentent* l' `IDrawable` interface. Par exemple, la bibliothèque peut fournir un objet Shape pour les formes de dessin et un objet Bitmap pour dessiner des images. En C++, cette opération est effectuée en héritant d’une classe de base abstraite commune :

```C++
class Shape : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};

class Bitmap : public IDrawable
{
public:
    virtual void Draw();    // Override Draw and provide implementation.
};
```

Les `Shape` `Bitmap` classes et définissent deux types distincts d’objets dessinables. Chaque classe hérite de `IDrawable` et fournit sa propre implémentation de la `Draw` méthode. Naturellement, les deux implémentations peuvent varier considérablement. Par exemple, la `Shape::Draw` méthode peut pixelliser un ensemble de lignes, tout en `Bitmap::Draw` blitant un tableau de pixels.

Un programme qui utilise cette bibliothèque de graphiques peut manipuler `Shape` des `Bitmap` objets et par le biais de `IDrawable` pointeurs, plutôt que d’utiliser `Shape` directement des `Bitmap` pointeurs ou.

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

Voici un exemple qui effectue une boucle sur un tableau de `IDrawable` pointeurs. Le tableau peut contenir un assortiment hétérogène de formes, de bitmaps et d’autres objets graphiques, à condition que chaque objet du tableau hérite de `IDrawable` .

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

Un point essentiel sur COM est que le code appelant ne voit jamais le type de la classe dérivée. En d’autres termes, vous ne devez jamais déclarer une variable de type `Shape` ou `Bitmap` dans votre code. Toutes les opérations sur les formes et les bitmaps sont effectuées à l’aide de `IDrawable` pointeurs. De cette façon, COM maintient une séparation stricte entre l’interface et l’implémentation. Les détails de l’implémentation `Shape` des `Bitmap` classes et peuvent changer, par exemple pour corriger des bogues ou ajouter de nouvelles fonctionnalités, sans aucune modification du code appelant.

Dans une implémentation C++, les interfaces sont déclarées à l’aide d’une classe ou d’une structure.

> [!Note]  
> Les exemples de code de cette rubrique sont destinés à communiquer des concepts généraux, et non des pratiques réelles. La définition de nouvelles interfaces COM n’entre pas dans le cadre de cette série, mais vous ne devez pas définir une interface directement dans un fichier d’en-tête. Au lieu de cela, une interface COM est définie à l’aide d’un langage appelé IDL (Interface Definition Language). Le fichier IDL est traité par un compilateur IDL, qui génère un fichier d’en-tête C++.

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

Lorsque vous travaillez avec COM, il est important de se souvenir que les interfaces ne sont pas des objets. Il s’agit de collections de méthodes que les objets doivent implémenter. Plusieurs objets peuvent implémenter la même interface, comme indiqué dans `Shape` les `Bitmap` exemples et. En outre, un objet peut implémenter plusieurs interfaces. Par exemple, la bibliothèque de graphiques peut définir une interface nommée `ISerializable` qui prend en charge l’enregistrement et le chargement d’objets graphiques. Considérons maintenant les déclarations de classe suivantes :

```C++
// An interface for serialization.
class ISerializable
{
public:
    virtual void Load(PCWSTR filename) = 0;    // Load from file.
    virtual void Save(PCWSTR filename) = 0;    // Save to file.
};

// Declarations of drawable object types.

class Shape : public IDrawable
{
    ...
};

class Bitmap : public IDrawable, public ISerializable
{
    ...
};
```

Dans cet exemple, la `Bitmap` classe implémente `ISerializable` . Le programme peut utiliser cette méthode pour enregistrer ou charger la bitmap. Toutefois, la `Shape` classe n’implémente pas `ISerializable` , donc elle n’expose pas cette fonctionnalité. Le diagramme suivant montre les relations d’héritage dans cet exemple.

![Illustration montrant l’héritage de l’interface, avec les classes Shape et bitmap pointant vers IDrawable, mais uniquement bitmap pointant sur ISerializable](images/com02.png)

Cette section a examiné la base conceptuelle des interfaces, mais jusqu’à présent, nous n’avons pas vu le code COM réel. Nous allons commencer par la première chose qu’une application COM doit faire : initialiser la bibliothèque COM.

## <a name="next"></a>Suivant

[Initialisation de la bibliothèque COM](initializing-the-com-library.md)