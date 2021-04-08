---
description: Une classe d’association est un type spécial de classe qui définit une relation entre deux autres classes.
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: Déclaration d’une classe d’association
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035000"
---
# <a name="declaring-an-association-class"></a><span data-ttu-id="541cd-103">Déclaration d’une classe d’association</span><span class="sxs-lookup"><span data-stu-id="541cd-103">Declaring an Association Class</span></span>

<span data-ttu-id="541cd-104">Une classe d’association est un type spécial de classe qui définit une relation entre deux autres classes.</span><span class="sxs-lookup"><span data-stu-id="541cd-104">An association class is a special type of class that defines a relationship between two other classes.</span></span>

<span data-ttu-id="541cd-105">La procédure suivante décrit comment créer une classe d’association à l’aide de code MOF.</span><span class="sxs-lookup"><span data-stu-id="541cd-105">The following procedure describes how to create an association class using MOF code.</span></span>

<span data-ttu-id="541cd-106">**Pour créer une classe d’association à l’aide de code MOF**</span><span class="sxs-lookup"><span data-stu-id="541cd-106">**To create an association class using MOF code**</span></span>

1.  <span data-ttu-id="541cd-107">Assignez le qualificateur d' **Association** à votre classe.</span><span class="sxs-lookup"><span data-stu-id="541cd-107">Assign the **Association** qualifier to your class.</span></span>

    <span data-ttu-id="541cd-108">Bien qu’il soit possible de créer une classe avec des références à des objets ou des classes, le fait d’utiliser le qualificateur **Association** indique non seulement que votre classe est une classe d’association, mais, comme meilleure pratique, garantit que votre classe fonctionne pleinement comme une classe d’association.</span><span class="sxs-lookup"><span data-stu-id="541cd-108">Although it is possible to create a class with references to objects or classes, using the **Association** qualifier not only makes it clear that your class is an association class, but, as a best practice, ensures that your class fully functions as an association class.</span></span>

2.  <span data-ttu-id="541cd-109">Créez deux références dans la classe décrivant les deux instances d’objet que vous souhaitez associer à l’aide du type **ref** .</span><span class="sxs-lookup"><span data-stu-id="541cd-109">Create two references within the class describing the two object instances you wish to associate together using the **ref** type.</span></span>

    <span data-ttu-id="541cd-110">Les références lient les deux objets de l’Association en contenant les chemins d’accès aux objets.</span><span class="sxs-lookup"><span data-stu-id="541cd-110">The references bind the two objects in the association by containing paths to the objects.</span></span> <span data-ttu-id="541cd-111">Bien que cela ne soit pas obligatoire, utilisez également les propriétés de référence en tant que propriétés de clé.</span><span class="sxs-lookup"><span data-stu-id="541cd-111">Although not required, use the reference properties as key properties as well.</span></span>

    <span data-ttu-id="541cd-112">Bien que vous puissiez créer des références relatives à l’espace de noms ou à des espaces de noms complets, WMI n’a qu’une prise en charge limitée des références entre espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="541cd-112">Although you can create fully qualified or namespace-relative references, WMI has only limited support for cross-namespace references.</span></span> <span data-ttu-id="541cd-113">Plus précisément, seuls les objets définis statiquement peuvent faire référence les uns aux autres dans les limites de l’espace de noms. les objets pris en charge de manière dynamique ne peuvent pas faire référence mutuellement.</span><span class="sxs-lookup"><span data-stu-id="541cd-113">Specifically, only statically defined objects can reference each other across namespace boundaries; dynamically supported objects cannot reference each other.</span></span>

    <span data-ttu-id="541cd-114">Si nécessaire, utilisez les qualificateurs **HasClassRef** et **Classref** conjointement avec le type de référence d' **objet** pour référencer une classe.</span><span class="sxs-lookup"><span data-stu-id="541cd-114">If necessary, use the **HasClassRef** and **Classref** qualifiers in conjunction with the **object ref** type to reference a class.</span></span>

    <span data-ttu-id="541cd-115">WMI prend en charge **l’utilisation** d’un point de référence de référence à une instance et l’autre référence d' **objet** à une classe.</span><span class="sxs-lookup"><span data-stu-id="541cd-115">WMI supports having one **ref** reference point to an instance, and the other **object** reference point to a class.</span></span> <span data-ttu-id="541cd-116">Dans ce cas, votre classe d’association décrirait une association qui lie des instances à des classes.</span><span class="sxs-lookup"><span data-stu-id="541cd-116">In this case, your association class would describe an association that binds instances to classes.</span></span>

    <span data-ttu-id="541cd-117">L’exemple de code suivant décrit la syntaxe d’utilisation de **HasClassRef** et de **Classref** avec un type d' **objet** .</span><span class="sxs-lookup"><span data-stu-id="541cd-117">The following code example describes the syntax for using **HasClassRef** and **Classref** with an **object** type.</span></span>

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    <span data-ttu-id="541cd-118">Dans l’exemple précédent, la référence **EP1** peut pointer vers les définitions de classe pour la classe **MyEndpoint** ou la classe **OtherContainer** .</span><span class="sxs-lookup"><span data-stu-id="541cd-118">In the previous example, the **ep1** reference can point to the class definitions for either the **MyEndpoint** class or the **OtherContainer** class.</span></span> <span data-ttu-id="541cd-119">Notez que même si vous devez taper la classe de référence faiblement, vous ne pouvez pas taper le qualificateur **Classref** lui-même de façon faible ; cela réduirait gravement l’efficacité du moteur de requête WMI.</span><span class="sxs-lookup"><span data-stu-id="541cd-119">Note that while you must weakly type the reference class, you cannot weakly type the **Classref** qualifier itself; doing so would severely reduce the efficiency of the WMI query engine.</span></span> <span data-ttu-id="541cd-120">Le typage faible consiste à créer une référence qui peut contenir n’importe quel type de données à l’aide du mot clé **Object** et du type de données **ref** .</span><span class="sxs-lookup"><span data-stu-id="541cd-120">Weak typing is creating a reference that can contain any data type by using the **object** keyword and **ref** data type.</span></span> <span data-ttu-id="541cd-121">Pour pouvoir utiliser **HasClassRef**, vous devez définir les versions de qualificateur appropriées pour qu’elles se propagent à toutes les instances et sous-classes.</span><span class="sxs-lookup"><span data-stu-id="541cd-121">To successfully use **HasClassRef**, you must set the relevant qualifier flavors to propagate to all instances and subclasses.</span></span>

3.  <span data-ttu-id="541cd-122">Créez d’autres propriétés si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="541cd-122">Create any other properties as necessary.</span></span>

    <span data-ttu-id="541cd-123">L’exemple de code suivant montre que WMI ne prend actuellement pas en charge les classes d’association ayant moins ou plus de deux propriétés de référence.</span><span class="sxs-lookup"><span data-stu-id="541cd-123">The following code example shows that WMI does not currently support association classes having less or more than two reference properties.</span></span>

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  <span data-ttu-id="541cd-124">Lorsque vous avez terminé, compilez votre code MOF avec le compilateur MOF.</span><span class="sxs-lookup"><span data-stu-id="541cd-124">When finished, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="541cd-125">Pour plus d’informations, consultez [compilation des fichiers MOF](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="541cd-125">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="541cd-126">L’exemple de code à l’étape 3 définit la classe d’association **MyAssocClass** .</span><span class="sxs-lookup"><span data-stu-id="541cd-126">The code example in Step 3 defines the **MyAssocClass** association class.</span></span> <span data-ttu-id="541cd-127">La classe **MyAssocClass** définit une relation entre **ClassX** et **classy**.</span><span class="sxs-lookup"><span data-stu-id="541cd-127">The **MyAssocClass** class defines a relationship between **ClassX** and **ClassY**.</span></span> <span data-ttu-id="541cd-128">Les propriétés **PathToClassX** et **PathToClassY** contiennent des chemins d’accès aux instances des classes à associer.</span><span class="sxs-lookup"><span data-stu-id="541cd-128">The **PathToClassX** and **PathToClassY** properties contain object paths to the instances of the classes to be associated.</span></span> <span data-ttu-id="541cd-129">Le mot clé **ToInstance** est l’un des nombreux indicateurs de version que WMI définit pour fournir des informations sur l’utilisation d’un qualificateur.</span><span class="sxs-lookup"><span data-stu-id="541cd-129">The keyword **ToInstance** is one of several flavor flags that WMI defines to provide information about the use of a qualifier.</span></span> <span data-ttu-id="541cd-130">Le mot clé **ToInstance** indique que WMI doit propager le qualificateur d' **Association** à toutes les instances de la classe d’association.</span><span class="sxs-lookup"><span data-stu-id="541cd-130">The **ToInstance** keyword indicates that WMI should propagate the **Association** qualifier to all instances of the association class.</span></span> <span data-ttu-id="541cd-131">En vérifiant ce qualificateur d’instance, le logiciel client peut déterminer qu’une instance appartient à une classe d’association, sans avoir à récupérer la définition de classe pour rechercher le qualificateur d' **Association** .</span><span class="sxs-lookup"><span data-stu-id="541cd-131">By checking this instance qualifier, the client software can determine that an instance belongs to an association class, without having to retrieve the class definition to look for the **Association** qualifier.</span></span> <span data-ttu-id="541cd-132">Pour plus d’informations, consultez [Description d’un qualificateur avec une version de qualificateur](describing-a-qualifier-with-a-qualifier-flavor.md) et des [références](references.md).</span><span class="sxs-lookup"><span data-stu-id="541cd-132">For more information, see [Describing a Qualifier With a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md) and [References](references.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="541cd-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="541cd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="541cd-134">Conception de classes format MOF (MOF)</span><span class="sxs-lookup"><span data-stu-id="541cd-134">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



