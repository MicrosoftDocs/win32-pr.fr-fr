---
title: Attribut length_is
description: L’attribut \ size \_ is \ vous permet de spécifier la taille maximale du tableau.
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f49ad63b2546d39dcc00d251f39143b7eec354c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729789"
---
# <a name="the-length_is-attribute"></a><span data-ttu-id="e1568-104">La \[ longueur \_ est \] attribute</span><span class="sxs-lookup"><span data-stu-id="e1568-104">The \[length\_is\] Attribute</span></span>

<span data-ttu-id="e1568-105">La \[ [**taille \_ est**](/windows/desktop/Midl/size-is) l' \] attribut vous permet de spécifier la taille maximale du tableau.</span><span class="sxs-lookup"><span data-stu-id="e1568-105">The \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute lets you specify the maximum size of the array.</span></span> <span data-ttu-id="e1568-106">Lorsqu’il s’agit du seul attribut, tous les éléments du tableau sont transmis.</span><span class="sxs-lookup"><span data-stu-id="e1568-106">When this is the only attribute, all elements of the array are transmitted.</span></span> <span data-ttu-id="e1568-107">Au lieu d’envoyer tous les éléments du tableau, vous pouvez spécifier les éléments transmis à l’aide de la \[ [**longueur \_ est**](/windows/desktop/Midl/length-is) \] attribute, comme suit :</span><span class="sxs-lookup"><span data-stu-id="e1568-107">Instead of sending all elements of the array, you can specify the transmitted elements using the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute, as follows:</span></span>

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

<span data-ttu-id="e1568-108">La taille décrit l’allocation lorsque la longueur décrit la transmission.</span><span class="sxs-lookup"><span data-stu-id="e1568-108">Size describes allocation while length describes transmission.</span></span> <span data-ttu-id="e1568-109">Le nombre d’éléments transmis doit toujours être inférieur ou égal au nombre d’éléments alloués.</span><span class="sxs-lookup"><span data-stu-id="e1568-109">The number of elements transmitted must always be less than or equal to the number of elements allocated.</span></span> <span data-ttu-id="e1568-110">La valeur associée à **Length \_** est toujours inférieure ou égale à **size \_ is**.</span><span class="sxs-lookup"><span data-stu-id="e1568-110">The value associated with **length\_is** is always less than or equal to **size\_is**.</span></span>

 

 