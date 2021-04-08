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
# <a name="references-wmi"></a>Références (WMI)

Le mot clé **ref** MOF décrit un chemin d’accès à un objet et mappe à un \_ type d’automatisation VT BSTR. Le chemin d’accès à l’objet peut être un chemin d’accès complet à un serveur et un espace de noms, ou un chemin d’accès relatif à un autre objet dans le même espace de noms. Vous pouvez utiliser un mot clé de **référence** pour lier deux classes ou plus. WMI prend en charge deux types de chemins d’accès aux objets, qui permettent de définir des chemins d’accès généraux ou spécifiques dans WMI.

L’objectif principal du mot clé **ref** est de réduire le temps de transport et l’encodage entre les objets qui existent entièrement dans le référentiel WMI. Vous pouvez également utiliser le mot clé **ref** pour créer une association entre deux classes. Pour plus d’informations, consultez [déclaration d’une classe d’association](declaring-an-association-class.md). Si l’élément référencé se trouve dans le même fichier MOF, utilisez un alias pour initialiser **la valeur de référence.** Pour plus d’informations, consultez [création d’un alias](creating-an-alias.md).

> [!Note]  
> Quand un mot clé de **référence** est appliqué à une propriété de clé, vous pouvez distinguer les références d’objet par la valeur de la chaîne d’objet plutôt que par la valeur déréférencée.

 

MOF prend en charge le concept d’un chemin d’accès d’objet faiblement typé et fortement typé. Un chemin d’accès d’objet faiblement typé pointe vers un objet d’une classe non spécifiée et utilise le mot clé **ref** avec le mot clé [Object](object.md) . Un objet fortement typé pointe vers un objet d’une classe spécifique et utilise **ref** avec le nom de la classe. L’exemple suivant décrit une référence **RefToAnyClass** faiblement typée qui peut pointer vers n’importe quelle classe ou instance de classe, et une référence **RefToClassX** qui peut pointer uniquement vers une classe ou une instance **ClassX** :

``` syntax
class MyClass
{
    object ref RefToAnyClass;       // Weakly typed
    ClassX ref RefToClassX;         // Strongly typed
};
```

L’exemple suivant décrit deux instances et un objet Association qui référence les instances précédentes :

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

 

 



