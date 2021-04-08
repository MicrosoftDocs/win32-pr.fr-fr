---
description: Le type de données OBJECT est un objet de classe WMI utilisé pour déclarer des associations faiblement typées et des objets incorporés.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c257b45833204a873292da467d484fab97b22b0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749516"
---
# <a name="object"></a><span data-ttu-id="3e42c-103">OBJECT</span><span class="sxs-lookup"><span data-stu-id="3e42c-103">OBJECT</span></span>

<span data-ttu-id="3e42c-104">Le type de données OBJECT est un objet de classe WMI utilisé pour déclarer des associations faiblement typées et des objets incorporés.</span><span class="sxs-lookup"><span data-stu-id="3e42c-104">The OBJECT data type is a WMI class object use to declare weakly typed associations and embedded objects.</span></span> <span data-ttu-id="3e42c-105">Vous ne définissez pas la classe spécifique d’un objet faiblement typé tant que vous n’avez pas créé une instance de la classe.</span><span class="sxs-lookup"><span data-stu-id="3e42c-105">You do not define the specific class for a weakly typed object until you create an instance of the class.</span></span> <span data-ttu-id="3e42c-106">Les objets incorporés définis avec le type de données OBJECT peuvent contenir des instances de n’importe quelle classe WMI.</span><span class="sxs-lookup"><span data-stu-id="3e42c-106">Embedded objects defined with the OBJECT data type can contain instances of any WMI class.</span></span> <span data-ttu-id="3e42c-107">Pour plus d’informations, consultez [objets incorporés](embedded-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3e42c-107">For more information, see [Embedded Objects](embedded-objects.md).</span></span>

<span data-ttu-id="3e42c-108">L’exemple suivant définit et crée des instances de deux classes, dont l’une contient un objet incorporé de type OBJECT :</span><span class="sxs-lookup"><span data-stu-id="3e42c-108">The following example defines and creates instances of two classes, one of which contains an embedded object of type OBJECT:</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

instance of __Namespace
{
    Name = "WMI" ;
} ;

#pragma namespace("\\\\.\\root\\WMI")

class CompositeClass
{
    [key] string aKey;   
    object EmbObj;       // Weakly typed
};

class EmbClass

{
  [key] string aKey;
};

instance of CompositeClass
{
    aKey = "CompositeClass Key";
    EmbObj = 
        instance of EmbClass
        {
           aKey = "key for embedded object";
        };
};
```

 

 



