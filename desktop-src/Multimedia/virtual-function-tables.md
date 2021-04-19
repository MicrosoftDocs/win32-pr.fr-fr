---
title: Tables de fonctions virtuelles
description: Tables de fonctions virtuelles
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a784a027f7e1120d8e7092aa5dd6c0f5c0e958b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511619"
---
# <a name="virtual-function-tables"></a><span data-ttu-id="38059-103">Tables de fonctions virtuelles</span><span class="sxs-lookup"><span data-stu-id="38059-103">Virtual Function Tables</span></span>

<span data-ttu-id="38059-104">Une table de fonctions virtuelles est un tableau de pointeurs vers les méthodes prises en charge par un objet.</span><span class="sxs-lookup"><span data-stu-id="38059-104">A virtual function table is an array of pointers to the methods an object supports.</span></span> <span data-ttu-id="38059-105">Si vous utilisez C, un objet apparaît sous la forme d’une structure dont le premier membre est un pointeur vers la table de fonctions virtuelles (**lpVtbl**); autrement dit, le premier membre pointe vers un tableau contenant des pointeurs de fonction.</span><span class="sxs-lookup"><span data-stu-id="38059-105">If you're using C, an object appears as a structure whose first member is a pointer to the virtual function table (**lpVtbl**); that is, the first member points to an array containing function pointers.</span></span> <span data-ttu-id="38059-106">Les méthodes prennent toutes un pointeur vers la table de fonctions comme premier paramètre.</span><span class="sxs-lookup"><span data-stu-id="38059-106">The methods all take a pointer to the function table as the first parameter.</span></span> <span data-ttu-id="38059-107">Ainsi, l’exemple suivant appelle la méthode **Read** d’un objet **pStream** :</span><span class="sxs-lookup"><span data-stu-id="38059-107">Thus, the following example calls the **Read** method of a **pStream** object:</span></span>


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



<span data-ttu-id="38059-108">En C + +, le pointeur vers la table de fonctions virtuelles, le pointeur *This* , est implicite.</span><span class="sxs-lookup"><span data-stu-id="38059-108">In C+ +, the pointer to the virtual function table, the *this* pointer, is implicit.</span></span> <span data-ttu-id="38059-109">L’exemple suivant est équivalent à l’exemple précédent lors de l’utilisation de C + + :</span><span class="sxs-lookup"><span data-stu-id="38059-109">The following is equivalent to the previous example when using C+ +:</span></span>


```C++
pStream->Read(parameters) 
 
```



 

 




