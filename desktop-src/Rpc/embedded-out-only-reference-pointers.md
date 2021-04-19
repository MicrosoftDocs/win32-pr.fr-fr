---
title: Pointeurs de référence Out-Only incorporés
description: Pointeurs de référence Out-Only incorporés
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072e9aa3cc3f0f673e4bb737016bc035a3ac496
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511315"
---
# <a name="embedded-out-only-reference-pointers"></a><span data-ttu-id="daa1e-103">Pointeurs de référence Out-Only incorporés</span><span class="sxs-lookup"><span data-stu-id="daa1e-103">Embedded Out-Only Reference Pointers</span></span>

<span data-ttu-id="daa1e-104">Lorsque vous utilisez des \[ [](/windows/desktop/Midl/out-idl) \] pointeurs de référence en sortie seule dans Microsoft RPC, les stubs de serveur générés allouent uniquement le premier niveau des pointeurs accessibles à partir du pointeur de référence.</span><span class="sxs-lookup"><span data-stu-id="daa1e-104">When you use \[[**out**](/windows/desktop/Midl/out-idl)\]-only reference pointers in Microsoft RPC, the generated server stubs allocate only the first level of pointers accessible from the reference pointer.</span></span> <span data-ttu-id="daa1e-105">Les pointeurs à des niveaux plus profonds ne sont pas alloués par les stubs, mais doivent être alloués par la couche d’application serveur.</span><span class="sxs-lookup"><span data-stu-id="daa1e-105">Pointers at deeper levels are not allocated by the stubs, but must be allocated by the server application layer.</span></span> <span data-ttu-id="daa1e-106">Par exemple, supposons qu’une interface spécifie un \[  \] tableau en dehors des pointeurs de référence :</span><span class="sxs-lookup"><span data-stu-id="daa1e-106">For example, suppose an interface specifies an \[**out**\]-only array of reference pointers:</span></span>

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

<span data-ttu-id="daa1e-107">Dans cet exemple, le stub serveur alloue de la mémoire pour 10 pointeurs et définit la valeur de chaque pointeur sur null.</span><span class="sxs-lookup"><span data-stu-id="daa1e-107">In this example, the server stub allocates memory for 10 pointers and sets the value of each pointer to null.</span></span> <span data-ttu-id="daa1e-108">L’application serveur doit allouer la mémoire pour les 10 entiers [**courts**](/windows/desktop/Midl/short) référencés par les pointeurs, puis définir les 10 pointeurs pour qu’ils pointent vers les entiers.</span><span class="sxs-lookup"><span data-stu-id="daa1e-108">The server application must allocate the memory for the 10 [**short**](/windows/desktop/Midl/short) integers referenced by the pointers and then set the 10 pointers to point to the integers.</span></span>

<span data-ttu-id="daa1e-109">Lorsque la \[ [](/windows/desktop/Midl/out-idl) \] structure de données en sortie seule comprend des pointeurs de référence imbriqués, les stubs de serveur allouent uniquement le premier pointeur accessible à partir du pointeur de référence.</span><span class="sxs-lookup"><span data-stu-id="daa1e-109">When the \[[**out**](/windows/desktop/Midl/out-idl)\]-only data structure includes nested reference pointers, the server stubs allocate only the first pointer accessible from the reference pointer.</span></span> <span data-ttu-id="daa1e-110">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="daa1e-110">For example:</span></span>

``` syntax
/* IDL file (fragment) */
typedef struct 
{
    [ref] small * psValue;
} STRUCT1_TYPE;

typedef struct 
{
    [ref] STRUCT1_TYPE * ps1;
} STRUCT_TOP_TYPE;

Proc2([out, ref] STRUCT_TOP_TYPE * psTop);
```

<span data-ttu-id="daa1e-111">Dans l’exemple précédent, les stubs de serveur allouent le pointeur *psTop* et le **\_ \_ type struct** de structure.</span><span class="sxs-lookup"><span data-stu-id="daa1e-111">In the preceding example, the server stubs allocate the pointer *psTop* and the structure **STRUCT\_TOP\_TYPE**.</span></span> <span data-ttu-id="daa1e-112">Le point de référence *ps1* dans le type de la **\_ partie \_ supérieure** de la structure a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="daa1e-112">The reference pointer *ps1* in **STRUCT\_TOP\_TYPE** is set to null.</span></span> <span data-ttu-id="daa1e-113">Le stub serveur n’alloue pas tous les niveaux de la structure de données, ni n’alloue le **\_ type STRUCT1** ou son pointeur incorporé, *psValue*.</span><span class="sxs-lookup"><span data-stu-id="daa1e-113">The server stub does not allocate every level of the data structure, nor does it allocate the **STRUCT1\_TYPE** or its embedded pointer, *psValue*.</span></span>

 

 