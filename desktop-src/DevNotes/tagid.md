---
description: Contient l’index d’une entrée et ses informations sur les BALISes dans une base de données de shims.
ms.assetid: 2ff58e01-cc47-4612-a3bc-a87ccb343bd2
title: TAGID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e7d8b8a25633d3505936d105b0eef7ed38746ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950501"
---
# <a name="tagid"></a><span data-ttu-id="bc6d5-103">TAGID</span><span class="sxs-lookup"><span data-stu-id="bc6d5-103">TAGID</span></span>

<span data-ttu-id="bc6d5-104">Contient l’index d’une entrée et ses informations sur les BALISes dans une base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="bc6d5-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGID;
```



## <a name="remarks"></a><span data-ttu-id="bc6d5-105">Notes</span><span class="sxs-lookup"><span data-stu-id="bc6d5-105">Remarks</span></span>

<span data-ttu-id="bc6d5-106">Un **TagId** est spécifique à une base de données.</span><span class="sxs-lookup"><span data-stu-id="bc6d5-106">A **TAGID** is specific to a database.</span></span> <span data-ttu-id="bc6d5-107">Il peut s’agir d’une valeur entière qui représente l’index ou de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="bc6d5-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="bc6d5-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID \_ null (0)</span><span class="sxs-lookup"><span data-stu-id="bc6d5-108"><span id="TAGID_NULL__0_"></span><span id="tagid_null__0_"></span>TAGID\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="bc6d5-109">Le **TagId** n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="bc6d5-109">The **TAGID** does not exist.</span></span> <span data-ttu-id="bc6d5-110">Cette valeur est retournée par une fonction lorsqu’elle ne peut pas retourner un **TagId** valide.</span><span class="sxs-lookup"><span data-stu-id="bc6d5-110">This value is returned from a function when it cannot return a valid **TAGID**.</span></span>

</dd> <dt>

<span data-ttu-id="bc6d5-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>\_Racine TagId (0)</span><span class="sxs-lookup"><span data-stu-id="bc6d5-111"><span id="TAGID_ROOT__0_"></span><span id="tagid_root__0_"></span>TAGID\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="bc6d5-112">Indique une BALIse de liste racine qui peut être utilisée comme parent pour obtenir un **TagId** enfant.</span><span class="sxs-lookup"><span data-stu-id="bc6d5-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGID**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc6d5-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc6d5-113">Requirements</span></span>



| <span data-ttu-id="bc6d5-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc6d5-114">Requirement</span></span> | <span data-ttu-id="bc6d5-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc6d5-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bc6d5-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc6d5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bc6d5-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc6d5-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bc6d5-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc6d5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bc6d5-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc6d5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc6d5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc6d5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc6d5-121">**Référence**</span><span class="sxs-lookup"><span data-stu-id="bc6d5-121">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="bc6d5-122">Types de BALISes</span><span class="sxs-lookup"><span data-stu-id="bc6d5-122">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="bc6d5-123">**TAGREF**</span><span class="sxs-lookup"><span data-stu-id="bc6d5-123">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




