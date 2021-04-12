---
description: Contient l’index d’une entrée et ses informations sur les BALISes dans une base de données de shims.
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8631811f101850b68bdbad1097c19b9a41737bd2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523151"
---
# <a name="tagref"></a><span data-ttu-id="1a12c-103">TAGREF</span><span class="sxs-lookup"><span data-stu-id="1a12c-103">TAGREF</span></span>

<span data-ttu-id="1a12c-104">Contient l’index d’une entrée et ses informations sur les BALISes dans une base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="1a12c-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a><span data-ttu-id="1a12c-105">Notes</span><span class="sxs-lookup"><span data-stu-id="1a12c-105">Remarks</span></span>

<span data-ttu-id="1a12c-106">Un **TAGREF** est spécifique à une base de données de shims et valide sur plusieurs bases de données.</span><span class="sxs-lookup"><span data-stu-id="1a12c-106">A **TAGREF** is specific to a shim database and valid across multiple databases.</span></span> <span data-ttu-id="1a12c-107">Il peut s’agir d’une valeur entière qui représente l’index ou de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="1a12c-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="1a12c-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ null (0)</span><span class="sxs-lookup"><span data-stu-id="1a12c-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="1a12c-109">Le **TAGREF** n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="1a12c-109">The **TAGREF** does not exist.</span></span> <span data-ttu-id="1a12c-110">Cette valeur est retournée par une fonction lorsqu’elle ne peut pas retourner un **TAGREF** valide.</span><span class="sxs-lookup"><span data-stu-id="1a12c-110">This value is returned from a function when it cannot return a valid **TAGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="1a12c-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>\_Racine TAGREF (0)</span><span class="sxs-lookup"><span data-stu-id="1a12c-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="1a12c-112">Indique une BALIse de liste racine qui peut être utilisée comme parent pour obtenir un **TAGREF** enfant.</span><span class="sxs-lookup"><span data-stu-id="1a12c-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGREF**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a12c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a12c-113">Requirements</span></span>



| <span data-ttu-id="1a12c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a12c-114">Requirement</span></span> | <span data-ttu-id="1a12c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a12c-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a12c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a12c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1a12c-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a12c-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1a12c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a12c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1a12c-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a12c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a12c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a12c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a12c-121">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="1a12c-121">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> <dt>

[<span data-ttu-id="1a12c-122">**Référence**</span><span class="sxs-lookup"><span data-stu-id="1a12c-122">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="1a12c-123">Types de BALISes</span><span class="sxs-lookup"><span data-stu-id="1a12c-123">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="1a12c-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="1a12c-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




