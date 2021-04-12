---
title: Attributs first_is et last_is
description: Vous pouvez déterminer le nombre d’éléments transmis en spécifiant le premier et le dernier élément.
ms.assetid: bd4dcf42-64a7-4b05-ac55-be77c381eb2e
keywords:
- first_is
- last_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159a2696db8e175f921b797176baaa8f3aa0263c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316314"
---
# <a name="the-first_is-and-last_is-attributes"></a><span data-ttu-id="1acc9-105">Le \[ premier \_ est \] et le \[ dernier \_ est un \] attribut</span><span class="sxs-lookup"><span data-stu-id="1acc9-105">The \[first\_is\] and \[last\_is\] Attributes</span></span>

<span data-ttu-id="1acc9-106">Vous pouvez déterminer le nombre d’éléments transmis en spécifiant le premier et le dernier élément.</span><span class="sxs-lookup"><span data-stu-id="1acc9-106">You can determine the number of transmitted elements by specifying the first and last elements.</span></span> <span data-ttu-id="1acc9-107">Utilisez les \[ attributs [**First \_ is**](/windows/desktop/Midl/first-is) \] et \[ [**Last \_**](/windows/desktop/Midl/last-is) comme indiqué ci- \] dessous :</span><span class="sxs-lookup"><span data-stu-id="1acc9-107">Use the \[[**first\_is**](/windows/desktop/Midl/first-is)\] and \[[**last\_is**](/windows/desktop/Midl/last-is)\] attributes as shown:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(4.0)
]
interface arraytest
{

  void fArray4([in]               short sSize,
               [in]               short sLast,
               [in]               short sFirst,
               [in, 
                out,
                size_is(sSize),
                first_is(sFirst),
                last_is(sLast)]   char achArray[]) ;
}
```

 

 