---
description: 'TAGREF : contient l’index d’une entrée et ses informations de BALIse dans une base de données de shims.'
ms.assetid: e7d83dca-13a5-4396-b50b-0d068209c03c
title: TAGREF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e27a60847630e7bbd8e07ccf005dfd7b474d7a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096627"
---
# <a name="tagref"></a><span data-ttu-id="8dba1-103">TAGREF</span><span class="sxs-lookup"><span data-stu-id="8dba1-103">TAGREF</span></span>

<span data-ttu-id="8dba1-104">Contient l’index d’une entrée et ses informations sur les BALISes dans une base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="8dba1-104">Contains the index of an entry and its TAG information in a shim database.</span></span>


```C++
typedef DWORD TAGREF;
```



## <a name="remarks"></a><span data-ttu-id="8dba1-105">Notes </span><span class="sxs-lookup"><span data-stu-id="8dba1-105">Remarks</span></span>

<span data-ttu-id="8dba1-106">Un **TAGREF** est spécifique à une base de données de shims et valide sur plusieurs bases de données.</span><span class="sxs-lookup"><span data-stu-id="8dba1-106">A **TAGREF** is specific to a shim database and valid across multiple databases.</span></span> <span data-ttu-id="8dba1-107">Il peut s’agir d’une valeur entière qui représente l’index ou de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="8dba1-107">It can be an integer value that represents the index, or one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="8dba1-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF \_ null (0)</span><span class="sxs-lookup"><span data-stu-id="8dba1-108"><span id="TAGREF_NULL__0_"></span><span id="tagref_null__0_"></span>TAGREF\_NULL (0)</span></span>
</dt> <dd>

<span data-ttu-id="8dba1-109">Le **TAGREF** n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="8dba1-109">The **TAGREF** does not exist.</span></span> <span data-ttu-id="8dba1-110">Cette valeur est retournée par une fonction lorsqu’elle ne peut pas retourner un **TAGREF** valide.</span><span class="sxs-lookup"><span data-stu-id="8dba1-110">This value is returned from a function when it cannot return a valid **TAGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="8dba1-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>\_Racine TAGREF (0)</span><span class="sxs-lookup"><span data-stu-id="8dba1-111"><span id="TAGREF_ROOT__0_"></span><span id="tagref_root__0_"></span>TAGREF\_ROOT (0)</span></span>
</dt> <dd>

<span data-ttu-id="8dba1-112">Indique une BALIse de liste racine qui peut être utilisée comme parent pour obtenir un **TAGREF** enfant.</span><span class="sxs-lookup"><span data-stu-id="8dba1-112">Indicates a root list TAG that can be used as a parent to obtain a child **TAGREF**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8dba1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8dba1-113">Requirements</span></span>



| <span data-ttu-id="8dba1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8dba1-114">Requirement</span></span> | <span data-ttu-id="8dba1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8dba1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8dba1-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dba1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8dba1-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dba1-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8dba1-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8dba1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8dba1-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8dba1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8dba1-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8dba1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8dba1-121">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="8dba1-121">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> <dt>

[<span data-ttu-id="8dba1-122">**Référence**</span><span class="sxs-lookup"><span data-stu-id="8dba1-122">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="8dba1-123">Types de BALISes</span><span class="sxs-lookup"><span data-stu-id="8dba1-123">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="8dba1-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="8dba1-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




