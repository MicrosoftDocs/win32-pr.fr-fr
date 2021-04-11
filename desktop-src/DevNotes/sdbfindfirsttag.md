---
description: Recherche une correspondance de BALIse dans le parent spécifié et retourne le TAGID de la première correspondance.
ms.assetid: ecbe216c-1e46-4472-b1d1-e2ac7ace82ab
title: SdbFindFirstTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: dc8b752d536be83d90ded55474166d14521f0f7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950369"
---
# <a name="sdbfindfirsttag-function"></a><span data-ttu-id="69934-103">SdbFindFirstTag fonction)</span><span class="sxs-lookup"><span data-stu-id="69934-103">SdbFindFirstTag function</span></span>

<span data-ttu-id="69934-104">Recherche une correspondance de BALIse dans le parent spécifié et retourne le **TagId** de la première correspondance.</span><span class="sxs-lookup"><span data-stu-id="69934-104">Searches for a TAG match within the specified parent and returns the **TAGID** of the first match.</span></span>

## <a name="syntax"></a><span data-ttu-id="69934-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69934-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstTag(
  _In_ PDB   pdb,
  _In_ TAGID tiParent,
  _In_ TAG   tTag
);
```



## <a name="parameters"></a><span data-ttu-id="69934-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69934-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69934-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69934-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69934-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="69934-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="69934-109">*tiParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69934-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69934-110">**TagId** du début de la recherche.</span><span class="sxs-lookup"><span data-stu-id="69934-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="69934-111">Ce paramètre peut être **TagId \_ racine** ou **\_ \_ liste de types de balises**.</span><span class="sxs-lookup"><span data-stu-id="69934-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="69934-112">*tTag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69934-112">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69934-113">BALIse à mettre en correspondance.</span><span class="sxs-lookup"><span data-stu-id="69934-113">The TAG to be matched.</span></span> <span data-ttu-id="69934-114">Pour obtenir la liste des valeurs possibles, consultez [tag](tag.md) .</span><span class="sxs-lookup"><span data-stu-id="69934-114">See [TAG](tag.md) for a list of possible values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69934-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69934-115">Return value</span></span>

<span data-ttu-id="69934-116">**TagId** de la première correspondance.</span><span class="sxs-lookup"><span data-stu-id="69934-116">The **TAGID** of the first match.</span></span>

## <a name="requirements"></a><span data-ttu-id="69934-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69934-117">Requirements</span></span>



| <span data-ttu-id="69934-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69934-118">Requirement</span></span> | <span data-ttu-id="69934-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="69934-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69934-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69934-120">Minimum supported client</span></span><br/> | <span data-ttu-id="69934-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69934-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="69934-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69934-122">Minimum supported server</span></span><br/> | <span data-ttu-id="69934-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69934-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="69934-124">DLL</span><span class="sxs-lookup"><span data-stu-id="69934-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69934-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69934-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69934-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69934-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69934-127">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="69934-127">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="69934-128">**SdbTagRefToTagID**</span><span class="sxs-lookup"><span data-stu-id="69934-128">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




