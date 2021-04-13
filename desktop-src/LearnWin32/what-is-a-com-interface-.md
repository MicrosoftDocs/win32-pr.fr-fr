---
title: Qu’est-ce qu’une interface COM ?
description: Qu’est-ce qu’une interface COM ?
ms.assetid: 36f27a58-cc63-4b67-bdcb-8f9a19650c6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da703569beae7a9aa2fc41bcea0214cc9aa488ad
ms.sourcegitcommit: 8eac40ea4d87a85e036ed5bbffec7b7a3dab39ec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2019
ms.locfileid: "104380463"
---
# <a name="what-is-a-com-interface"></a><span data-ttu-id="bd99e-103">Qu’est-ce qu’une interface COM ?</span><span class="sxs-lookup"><span data-stu-id="bd99e-103">What Is a COM Interface?</span></span>

<span data-ttu-id="bd99e-104">Si vous connaissez C# ou Java, les interfaces doivent être un concept familier.</span><span class="sxs-lookup"><span data-stu-id="bd99e-104">If you know C# or Java, interfaces should be a familiar concept.</span></span> <span data-ttu-id="bd99e-105">Une *interface* définit un ensemble de méthodes qu’un objet peut prendre en charge, sans dicter aucune information sur l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="bd99e-105">An *interface* defines a set of methods that an object can support, without dictating anything about the implementation.</span></span> <span data-ttu-id="bd99e-106">L’interface marque une limite claire entre le code qui appelle une méthode et le code qui implémente la méthode.</span><span class="sxs-lookup"><span data-stu-id="bd99e-106">The interface marks a clear boundary between code that calls a method and the code that implements the method.</span></span> <span data-ttu-id="bd99e-107">En termes d’informatique, l’appelant est *découplé* de l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="bd99e-107">In computer science terms, the caller is *decoupled* from the implementation.</span></span>

![Illustration montrant la limite de l’interface entre un objet et une application](images/com01.png)

<span data-ttu-id="bd99e-109">En C++, l’équivalent le plus proche d’une interface est une classe virtuelle pure, c’est-à-dire une classe qui contient uniquement des méthodes virtuelles pures et aucun autre membre.</span><span class="sxs-lookup"><span data-stu-id="bd99e-109">In C++, the nearest equivalent to an interface is a pure virtual class—that is, a class that contains only pure virtual methods and no other members.</span></span> <span data-ttu-id="bd99e-110">Voici un exemple hypothétique d’une interface :</span><span class="sxs-lookup"><span data-stu-id="bd99e-110">Here is a hypothetical example of an interface:</span></span>

```C++
// The following is not actual COM.

// Pseudo-C++:

interface IDrawable
{
    void Draw();
};
```

<span data-ttu-id="bd99e-111">L’idée de cet exemple est qu’un ensemble d’objets dans une bibliothèque de graphiques peuvent être dessinés.</span><span class="sxs-lookup"><span data-stu-id="bd99e-111">The idea of this example is that a set of objects in some graphics library are drawable.</span></span> <span data-ttu-id="bd99e-112">L' `IDrawable` interface définit les opérations que chaque objet pouvant être dessiné doit prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="bd99e-112">The `IDrawable` interface defines the operations that any drawable object must support.</span></span> <span data-ttu-id="bd99e-113">(Par Convention, les noms d’interface commencent par « I ».) Dans cet exemple, l' `IDrawable` interface définit une opération unique : `Draw` .</span><span class="sxs-lookup"><span data-stu-id="bd99e-113">(By convention, interface names start with "I".) In this example, the `IDrawable` interface defines a single operation: `Draw`.</span></span>

<span data-ttu-id="bd99e-114">Toutes les interfaces étant *abstraites*, un programme n’a pas pu créer une instance d’un `IDrawable` objet en tant que tel.</span><span class="sxs-lookup"><span data-stu-id="bd99e-114">All interfaces are *abstract*, so a program could not create an instance of an `IDrawable` object as such.</span></span> <span data-ttu-id="bd99e-115">Par exemple, le code suivant n’est pas compilé.</span><span class="sxs-lookup"><span data-stu-id="bd99e-115">For example, the following code would not compile.</span></span>

```C++
IDrawable draw;
draw.Draw();
```

<span data-ttu-id="bd99e-116">Au lieu de cela, la bibliothèque Graphics fournit des objets qui *implémentent* l' `IDrawable` interface.</span><span class="sxs-lookup"><span data-stu-id="bd99e-116">Instead, the graphics library provides objects that *implement* the `IDrawable` interface.</span></span> <span data-ttu-id="bd99e-117">Par exemple, la bibliothèque peut fournir un objet Shape pour les formes de dessin et un objet Bitmap pour dessiner des images.</span><span class="sxs-lookup"><span data-stu-id="bd99e-117">For example, the library might provide a shape object for drawing shapes and a bitmap object for drawing images.</span></span> <span data-ttu-id="bd99e-118">En C++, cette opération est effectuée en héritant d’une classe de base abstraite commune :</span><span class="sxs-lookup"><span data-stu-id="bd99e-118">In C++, this is done by inheriting from a common abstract base class:</span></span>

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

<span data-ttu-id="bd99e-119">Les `Shape` `Bitmap` classes et définissent deux types distincts d’objets dessinables.</span><span class="sxs-lookup"><span data-stu-id="bd99e-119">The `Shape` and `Bitmap` classes define two distinct types of drawable object.</span></span> <span data-ttu-id="bd99e-120">Chaque classe hérite de `IDrawable` et fournit sa propre implémentation de la `Draw` méthode.</span><span class="sxs-lookup"><span data-stu-id="bd99e-120">Each class inherits from `IDrawable` and provides its own implementation of the `Draw` method.</span></span> <span data-ttu-id="bd99e-121">Naturellement, les deux implémentations peuvent varier considérablement.</span><span class="sxs-lookup"><span data-stu-id="bd99e-121">Naturally, the two implementations might differ considerably.</span></span> <span data-ttu-id="bd99e-122">Par exemple, la `Shape::Draw` méthode peut pixelliser un ensemble de lignes, tout en `Bitmap::Draw` blitant un tableau de pixels.</span><span class="sxs-lookup"><span data-stu-id="bd99e-122">For example, the `Shape::Draw` method might rasterize a set of lines, while `Bitmap::Draw` would blit an array of pixels.</span></span>

<span data-ttu-id="bd99e-123">Un programme qui utilise cette bibliothèque de graphiques peut manipuler `Shape` des `Bitmap` objets et par le biais de `IDrawable` pointeurs, plutôt que d’utiliser `Shape` directement des `Bitmap` pointeurs ou.</span><span class="sxs-lookup"><span data-stu-id="bd99e-123">A program using this graphics library would manipulate `Shape` and `Bitmap` objects through `IDrawable` pointers, rather than using `Shape` or `Bitmap` pointers directly.</span></span>

```C++
IDrawable *pDrawable = CreateTriangleShape();

if (pDrawable)
{
    pDrawable->Draw();
}
```

<span data-ttu-id="bd99e-124">Voici un exemple qui effectue une boucle sur un tableau de `IDrawable` pointeurs.</span><span class="sxs-lookup"><span data-stu-id="bd99e-124">Here is an example that loops over an array of `IDrawable` pointers.</span></span> <span data-ttu-id="bd99e-125">Le tableau peut contenir un assortiment hétérogène de formes, de bitmaps et d’autres objets graphiques, à condition que chaque objet du tableau hérite de `IDrawable` .</span><span class="sxs-lookup"><span data-stu-id="bd99e-125">The array might contain a heterogeneous assortment of shapes, bitmaps, and other graphics objects, as long as each object in the array inherits `IDrawable`.</span></span>

```C++
void DrawSomeShapes(IDrawable **drawableArray, size_t count)
{
    for (size_t i = 0; i < count; i++)
    {
        drawableArray[i]->Draw();
    }
}
```

<span data-ttu-id="bd99e-126">Un point essentiel sur COM est que le code appelant ne voit jamais le type de la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="bd99e-126">A key point about COM is that the calling code never sees the type of the derived class.</span></span> <span data-ttu-id="bd99e-127">En d’autres termes, vous ne devez jamais déclarer une variable de type `Shape` ou `Bitmap` dans votre code.</span><span class="sxs-lookup"><span data-stu-id="bd99e-127">In other words, you would never declare a variable of type `Shape` or `Bitmap` in your code.</span></span> <span data-ttu-id="bd99e-128">Toutes les opérations sur les formes et les bitmaps sont effectuées à l’aide de `IDrawable` pointeurs.</span><span class="sxs-lookup"><span data-stu-id="bd99e-128">All operations on shapes and bitmaps are performed using `IDrawable` pointers.</span></span> <span data-ttu-id="bd99e-129">De cette façon, COM maintient une séparation stricte entre l’interface et l’implémentation.</span><span class="sxs-lookup"><span data-stu-id="bd99e-129">In this way, COM maintains a strict separation between interface and implementation.</span></span> <span data-ttu-id="bd99e-130">Les détails de l’implémentation `Shape` des `Bitmap` classes et peuvent changer, par exemple pour corriger des bogues ou ajouter de nouvelles fonctionnalités, sans aucune modification du code appelant.</span><span class="sxs-lookup"><span data-stu-id="bd99e-130">The implementation details of the `Shape` and `Bitmap` classes can change—for example, to fix bugs or add new capabilities—with no changes to the calling code.</span></span>

<span data-ttu-id="bd99e-131">Dans une implémentation C++, les interfaces sont déclarées à l’aide d’une classe ou d’une structure.</span><span class="sxs-lookup"><span data-stu-id="bd99e-131">In a C++ implementation, interfaces are declared using a class or structure.</span></span>

> [!Note]  
> <span data-ttu-id="bd99e-132">Les exemples de code de cette rubrique sont destinés à communiquer des concepts généraux, et non des pratiques réelles.</span><span class="sxs-lookup"><span data-stu-id="bd99e-132">The code examples in this topic are meant to convey general concepts, not real-world practice.</span></span> <span data-ttu-id="bd99e-133">La définition de nouvelles interfaces COM n’entre pas dans le cadre de cette série, mais vous ne devez pas définir une interface directement dans un fichier d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="bd99e-133">Defining new COM interfaces is beyond the scope of this series, but you would not define an interface directly in a header file.</span></span> <span data-ttu-id="bd99e-134">Au lieu de cela, une interface COM est définie à l’aide d’un langage appelé IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="bd99e-134">Instead, a COM interface is defined using a language called Interface Definition Language (IDL).</span></span> <span data-ttu-id="bd99e-135">Le fichier IDL est traité par un compilateur IDL, qui génère un fichier d’en-tête C++.</span><span class="sxs-lookup"><span data-stu-id="bd99e-135">The IDL file is processed by an IDL compiler, which generates a C++ header file.</span></span>

```C++
class IDrawable
{
public:
    virtual void Draw() = 0;
};
```

<span data-ttu-id="bd99e-136">Lorsque vous travaillez avec COM, il est important de se souvenir que les interfaces ne sont pas des objets.</span><span class="sxs-lookup"><span data-stu-id="bd99e-136">When you work with COM, it is important to remember that interfaces are not objects.</span></span> <span data-ttu-id="bd99e-137">Il s’agit de collections de méthodes que les objets doivent implémenter.</span><span class="sxs-lookup"><span data-stu-id="bd99e-137">They are collections of methods that objects must implement.</span></span> <span data-ttu-id="bd99e-138">Plusieurs objets peuvent implémenter la même interface, comme indiqué dans `Shape` les `Bitmap` exemples et.</span><span class="sxs-lookup"><span data-stu-id="bd99e-138">Several objects can implement the same interface, as shown with the `Shape` and `Bitmap` examples.</span></span> <span data-ttu-id="bd99e-139">En outre, un objet peut implémenter plusieurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="bd99e-139">Moreover, one object can implement several interfaces.</span></span> <span data-ttu-id="bd99e-140">Par exemple, la bibliothèque de graphiques peut définir une interface nommée `ISerializable` qui prend en charge l’enregistrement et le chargement d’objets graphiques.</span><span class="sxs-lookup"><span data-stu-id="bd99e-140">For example, the graphics library might define an interface named `ISerializable` that supports saving and loading graphics objects.</span></span> <span data-ttu-id="bd99e-141">Considérons maintenant les déclarations de classe suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd99e-141">Now consider the following class declarations:</span></span>

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

<span data-ttu-id="bd99e-142">Dans cet exemple, la `Bitmap` classe implémente `ISerializable` .</span><span class="sxs-lookup"><span data-stu-id="bd99e-142">In this example, the `Bitmap` class implements `ISerializable`.</span></span> <span data-ttu-id="bd99e-143">Le programme peut utiliser cette méthode pour enregistrer ou charger la bitmap.</span><span class="sxs-lookup"><span data-stu-id="bd99e-143">The program could use this method to save or load the bitmap.</span></span> <span data-ttu-id="bd99e-144">Toutefois, la `Shape` classe n’implémente pas `ISerializable` , donc elle n’expose pas cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="bd99e-144">However, the `Shape` class does not implement `ISerializable`, so it does not expose that functionality.</span></span> <span data-ttu-id="bd99e-145">Le diagramme suivant montre les relations d’héritage dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="bd99e-145">The following diagram shows the inheritance relations in this example.</span></span>

![Illustration montrant l’héritage de l’interface, avec les classes Shape et bitmap pointant vers IDrawable, mais uniquement bitmap pointant sur ISerializable](images/com02.png)

<span data-ttu-id="bd99e-147">Cette section a examiné la base conceptuelle des interfaces, mais jusqu’à présent, nous n’avons pas vu le code COM réel.</span><span class="sxs-lookup"><span data-stu-id="bd99e-147">This section has examined the conceptual basis of interfaces, but so far we have not seen actual COM code.</span></span> <span data-ttu-id="bd99e-148">Nous allons commencer par la première chose qu’une application COM doit faire : initialiser la bibliothèque COM.</span><span class="sxs-lookup"><span data-stu-id="bd99e-148">We'll start with the first thing that any COM application must do: Initialize the COM library.</span></span>

## <a name="next"></a><span data-ttu-id="bd99e-149">Suivant</span><span class="sxs-lookup"><span data-stu-id="bd99e-149">Next</span></span>

[<span data-ttu-id="bd99e-150">Initialisation de la bibliothèque COM</span><span class="sxs-lookup"><span data-stu-id="bd99e-150">Initializing the COM Library</span></span>](initializing-the-com-library.md)