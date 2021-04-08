---
description: Le mot clé ref MOF décrit un chemin d’accès à un objet et mappe à un \_ type d’automatisation VT BSTR.
ms.assetid: 9da25435-4ccc-4251-a4be-37239156e320
ms.tgt_platform: multiple
title: Références (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30722910de761f3d2111a3218cf364f49ccb3c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866586"
---
# <a name="references-wmi"></a><span data-ttu-id="52814-103">Références (WMI)</span><span class="sxs-lookup"><span data-stu-id="52814-103">References (WMI)</span></span>

<span data-ttu-id="52814-104">Le mot clé **ref** MOF décrit un chemin d’accès à un objet et mappe à un \_ type d’automatisation VT BSTR.</span><span class="sxs-lookup"><span data-stu-id="52814-104">The MOF **ref** key word describes an object path and maps to a VT\_BSTR Automation type.</span></span> <span data-ttu-id="52814-105">Le chemin d’accès à l’objet peut être un chemin d’accès complet à un serveur et un espace de noms, ou un chemin d’accès relatif à un autre objet dans le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="52814-105">The object path can be either a full path to a server and namespace, or a relative path to another object in the same namespace.</span></span> <span data-ttu-id="52814-106">Vous pouvez utiliser un mot clé de **référence** pour lier deux classes ou plus.</span><span class="sxs-lookup"><span data-stu-id="52814-106">You can use a **ref** key word to link two or more classes together.</span></span> <span data-ttu-id="52814-107">WMI prend en charge deux types de chemins d’accès aux objets, qui permettent de définir des chemins d’accès généraux ou spécifiques dans WMI.</span><span class="sxs-lookup"><span data-stu-id="52814-107">WMI supports two types of object paths, which use to define general or specific paths within WMI.</span></span>

<span data-ttu-id="52814-108">L’objectif principal du mot clé **ref** est de réduire le temps de transport et l’encodage entre les objets qui existent entièrement dans le référentiel WMI.</span><span class="sxs-lookup"><span data-stu-id="52814-108">The main purpose of the **ref** key word is to reduce transport time and encoding between objects that exist entirely within the WMI repository.</span></span> <span data-ttu-id="52814-109">Vous pouvez également utiliser le mot clé **ref** pour créer une association entre deux classes.</span><span class="sxs-lookup"><span data-stu-id="52814-109">You can also use the **ref** key word to create an association between two classes.</span></span> <span data-ttu-id="52814-110">Pour plus d’informations, consultez [déclaration d’une classe d’association](declaring-an-association-class.md).</span><span class="sxs-lookup"><span data-stu-id="52814-110">For more information, see [Declaring an Association Class](declaring-an-association-class.md).</span></span> <span data-ttu-id="52814-111">Si l’élément référencé se trouve dans le même fichier MOF, utilisez un alias pour initialiser **la valeur de référence.**</span><span class="sxs-lookup"><span data-stu-id="52814-111">If the referenced item is located within the same MOF file, use an alias to initialize the **ref** value.</span></span> <span data-ttu-id="52814-112">Pour plus d’informations, consultez [création d’un alias](creating-an-alias.md).</span><span class="sxs-lookup"><span data-stu-id="52814-112">For more information, see [Creating an Alias](creating-an-alias.md).</span></span>

> [!Note]  
> <span data-ttu-id="52814-113">Quand un mot clé de **référence** est appliqué à une propriété de clé, vous pouvez distinguer les références d’objet par la valeur de la chaîne d’objet plutôt que par la valeur déréférencée.</span><span class="sxs-lookup"><span data-stu-id="52814-113">When a **ref** key word is applied to a key property, you can distinguish object references by the object string value instead of by the dereferenced value.</span></span>

 

<span data-ttu-id="52814-114">MOF prend en charge le concept d’un chemin d’accès d’objet faiblement typé et fortement typé.</span><span class="sxs-lookup"><span data-stu-id="52814-114">MOF supports the concept of a weakly typed and strongly typed object path.</span></span> <span data-ttu-id="52814-115">Un chemin d’accès d’objet faiblement typé pointe vers un objet d’une classe non spécifiée et utilise le mot clé **ref** avec le mot clé [Object](object.md) .</span><span class="sxs-lookup"><span data-stu-id="52814-115">A weakly typed object path points to an object of an unspecified class and uses the **ref** key word with the [OBJECT](object.md) keyword.</span></span> <span data-ttu-id="52814-116">Un objet fortement typé pointe vers un objet d’une classe spécifique et utilise **ref** avec le nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="52814-116">A strongly typed object points to an object of a specific class and uses **ref** with the class name.</span></span> <span data-ttu-id="52814-117">L’exemple suivant décrit une référence **RefToAnyClass** faiblement typée qui peut pointer vers n’importe quelle classe ou instance de classe, et une référence **RefToClassX** qui peut pointer uniquement vers une classe ou une instance **ClassX** :</span><span class="sxs-lookup"><span data-stu-id="52814-117">The following example describes a weakly typed **RefToAnyClass** reference that can point to any class or class instance, and a **RefToClassX** reference that can point only to a **ClassX** class or instance:</span></span>

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

<span data-ttu-id="52814-118">L’exemple suivant décrit deux instances et un objet Association qui référence les instances précédentes :</span><span class="sxs-lookup"><span data-stu-id="52814-118">The following example describes two instances and an association object that references the previous instances:</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

Class A{
    [key] string aKey;
};

Class C{
    [key] string cKey;
};

// The following class creates an association 
// between the "A" class and the "C" class
    [Association] Class B{
    [key] A ref aRef;
    [Key, Min(1)] C ref cRef;
};

instance of a
{
    aKey = "This is the key for the A class";
};

instance of c
{
    cKey = "This is the key for the c class";
};
```

 

 



