---
title: Attribut length_is
description: L’attribut \ size \_ is \ vous permet de spécifier la taille maximale du tableau.
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f49ad63b2546d39dcc00d251f39143b7eec354c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416565"
---
# <a name="the-length_is-attribute"></a>La \[ longueur \_ est \] attribute

La \[ [**taille \_ est**](/windows/desktop/Midl/size-is) l' \] attribut vous permet de spécifier la taille maximale du tableau. Lorsqu’il s’agit du seul attribut, tous les éléments du tableau sont transmis. Au lieu d’envoyer tous les éléments du tableau, vous pouvez spécifier les éléments transmis à l’aide de la \[ [**longueur \_ est**](/windows/desktop/Midl/length-is) \] attribute, comme suit :

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(3.0)
]
interface arraytest
{
  void fArray3([in] short sSize,
               [in] short sLength
               [in, out, size_is(sSize), 
                 length_is(sLength)] char achArray[*]);
}
```

La taille décrit l’allocation lorsque la longueur décrit la transmission. Le nombre d’éléments transmis doit toujours être inférieur ou égal au nombre d’éléments alloués. La valeur associée à **Length \_** est toujours inférieure ou égale à **size \_ is**.

 

 