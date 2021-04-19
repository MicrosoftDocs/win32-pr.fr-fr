---
description: 'Lors de la création d’une instance avec des objets incorporés, effectuez les tâches suivantes :'
ms.assetid: 2abf6197-8b95-4c04-b154-508aa85fe12f
ms.tgt_platform: multiple
title: Création d’objets incorporés
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a76a70fa0e01068622a4f4cdbbbfb6c992b67f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536817"
---
# <a name="creating-embedded-objects"></a><span data-ttu-id="39f0a-103">Création d’objets incorporés</span><span class="sxs-lookup"><span data-stu-id="39f0a-103">Creating Embedded Objects</span></span>

<span data-ttu-id="39f0a-104">Lors de la création d’une instance avec des objets incorporés, effectuez les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="39f0a-104">When creating an instance with embedded objects, perform the following tasks:</span></span>

-   <span data-ttu-id="39f0a-105">Vous devez déclarer un objet incorporé comme fortement typé ou faiblement typé.</span><span class="sxs-lookup"><span data-stu-id="39f0a-105">You must declare an embedded object as strongly typed or weakly typed.</span></span>

    <span data-ttu-id="39f0a-106">Un objet fortement typé pointe vers un objet d’une classe spécifique et utilise le nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="39f0a-106">A strongly typed object points to an object of a specific class and uses the class name.</span></span> <span data-ttu-id="39f0a-107">Un objet faiblement typé pointe vers un objet d’une classe non spécifiée et utilise le mot clé **Object** .</span><span class="sxs-lookup"><span data-stu-id="39f0a-107">A weakly typed object points to an object of an unspecified class and uses the **object** keyword.</span></span> <span data-ttu-id="39f0a-108">Les deux objets sont mappés au type de **VT \_ inconnu** .</span><span class="sxs-lookup"><span data-stu-id="39f0a-108">Both objects map to the **VT\_UNKNOWN** type.</span></span>

-   <span data-ttu-id="39f0a-109">Vous pouvez utiliser **null** pour la valeur par défaut des objets et chemins d’accès incorporés dans les initialisations et les déclarations.</span><span class="sxs-lookup"><span data-stu-id="39f0a-109">You can use **NULL** for the default value of embedded objects and paths in initializations and declarations.</span></span>
-   <span data-ttu-id="39f0a-110">Lors de l’incorporation d’un chemin d’accès à un objet, ne placez pas d’espace blanc entre les éléments du chemin d’accès incorporé.</span><span class="sxs-lookup"><span data-stu-id="39f0a-110">When embedding an object path, do not place white space between the elements of the embedded path.</span></span> <span data-ttu-id="39f0a-111">Par exemple, le chemin d’accès à l’objet « Class1Index = 3 ; » ne contient pas d’espace entre le nom de la propriété « Class1index » et la valeur assignée, qui est « 3 ».</span><span class="sxs-lookup"><span data-stu-id="39f0a-111">For example, the object path "Class1Index=3;" contains no space between the property name "Class1index" and the value being assigned, which is "3".</span></span>

<span data-ttu-id="39f0a-112">La déclaration de classe suivante montre comment déclarer des objets incorporés fortement typés et faiblement typés.</span><span class="sxs-lookup"><span data-stu-id="39f0a-112">The following class declaration shows you how to declare strongly typed and weakly typed embedded objects.</span></span>

``` syntax
Class MyClass
{
    EmbedClass    Object1;          // Strongly typed
    object        Object2;          // Weakly typed
};
```

<span data-ttu-id="39f0a-113">Les exemples suivants décrivent comment déclarer des objets incorporés dans une déclaration de classe.</span><span class="sxs-lookup"><span data-stu-id="39f0a-113">The following examples describe how to declare embedded objects within a class declaration.</span></span>

``` syntax
Class Class1 
{ 
     [key] sint32 Class1Index;
};

Class Class2 
{
    [key] sint32 Class2Index;
    Class1 EmbedObject1 = instance of Class1{Class1Index=3;};
};

Class Class3
{
    [key] sint32 Class3Index;
    Class2 EmbedObject2 = instance of Class2 {Class2Index=4;};
};
```

<span data-ttu-id="39f0a-114">L’exemple suivant décrit l’initialisation d’une propriété qui est un objet fortement typé et une autre propriété qui est un tableau d’objets faiblement typés.</span><span class="sxs-lookup"><span data-stu-id="39f0a-114">The following example describes the initialization of one property that is a strongly typed object and another property that is an array of weakly typed objects.</span></span>

``` syntax
Class EmbedClass1
{
    [key] sint32 intval;
};

Class EmbedClass2
{
    [key] string sval;
};

Class ContainerClass
{
    [key] sint32 intval;
    EmbedClass1 SingleObject;
    Object ArrayObject[];
};

Instance of ContainerClass
{
    intval = 33;
    SingleObject = instance of EmbedClass1 {intval=99;};
    ArrayObject = {instance of EmbedClass2 {sval="something";},
                   instance of EmbedClass1 {intval=100;}};
};
```

 

 



