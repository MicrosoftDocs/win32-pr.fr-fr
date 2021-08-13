---
description: Le type de données OBJECT est un objet de classe WMI utilisé pour déclarer des associations faiblement typées et des objets incorporés.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c26b8b6ff77f788aeed607057541d19d80fea4c105b53d492c1f1e8468b319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554928"
---
# <a name="object"></a>OBJECT

Le type de données OBJECT est un objet de classe WMI utilisé pour déclarer des associations faiblement typées et des objets incorporés. Vous ne définissez pas la classe spécifique d’un objet faiblement typé tant que vous n’avez pas créé une instance de la classe. Les objets incorporés définis avec le type de données OBJECT peuvent contenir des instances de n’importe quelle classe WMI. Pour plus d’informations, consultez [objets incorporés](embedded-objects.md).

L’exemple suivant définit et crée des instances de deux classes, dont l’une contient un objet incorporé de type OBJECT :

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

 

 



