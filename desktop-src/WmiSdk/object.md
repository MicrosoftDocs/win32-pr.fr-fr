---
description: Le type de données OBJECT est un objet de classe WMI utilisé pour déclarer des associations faiblement typées et des objets incorporés.
ms.assetid: 1ad99b92-dfd4-4147-abf5-045edceaa97d
ms.tgt_platform: multiple
title: OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c257b45833204a873292da467d484fab97b22b0a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403682"
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

 

 



