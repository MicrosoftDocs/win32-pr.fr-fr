---
description: Recherche une BALIse enfant dans le parent spécifié et retourne le TAGID du premier enfant.
ms.assetid: 67538c7e-6360-40fa-b50f-dcbc7a6a147d
title: SdbGetFirstChild fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFirstChild
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: abc06ae0e4b5d842a968d0f3fbeb7a15702660b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522804"
---
# <a name="sdbgetfirstchild-function"></a><span data-ttu-id="ccb1a-103">SdbGetFirstChild fonction)</span><span class="sxs-lookup"><span data-stu-id="ccb1a-103">SdbGetFirstChild function</span></span>

<span data-ttu-id="ccb1a-104">Recherche une BALIse enfant dans le parent spécifié et retourne le **TagId** du premier enfant.</span><span class="sxs-lookup"><span data-stu-id="ccb1a-104">Searches for a child TAG within the specified parent and returns the **TAGID** of the first child.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb1a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ccb1a-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetFirstChild(
  _In_ PDB   pdb,
  _In_ TAGID tiParent
);
```



## <a name="parameters"></a><span data-ttu-id="ccb1a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ccb1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccb1a-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccb1a-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccb1a-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="ccb1a-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="ccb1a-109">*tiParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ccb1a-109">*tiParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ccb1a-110">**TagId** du début de la recherche.</span><span class="sxs-lookup"><span data-stu-id="ccb1a-110">The **TAGID** of the search start.</span></span> <span data-ttu-id="ccb1a-111">Ce paramètre peut être **TagId \_ racine** ou **\_ \_ liste de types de balises**.</span><span class="sxs-lookup"><span data-stu-id="ccb1a-111">This parameter can be **TAGID\_ROOT** or **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccb1a-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ccb1a-112">Return value</span></span>

<span data-ttu-id="ccb1a-113">Le **TagId** du premier enfant ou **TagId \_ null** n’est pas un enfant trouvé.</span><span class="sxs-lookup"><span data-stu-id="ccb1a-113">The **TAGID** of the first child or **TAGID\_NULL** is no child is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccb1a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccb1a-114">Requirements</span></span>



| <span data-ttu-id="ccb1a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccb1a-115">Requirement</span></span> | <span data-ttu-id="ccb1a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccb1a-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb1a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccb1a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ccb1a-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccb1a-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ccb1a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ccb1a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ccb1a-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ccb1a-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ccb1a-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ccb1a-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccb1a-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccb1a-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccb1a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccb1a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccb1a-124">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="ccb1a-124">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> <dt>

[<span data-ttu-id="ccb1a-125">**SdbFindNextTag**</span><span class="sxs-lookup"><span data-stu-id="ccb1a-125">**SdbFindNextTag**</span></span>](sdbfindnexttag.md)
</dt> <dt>

[<span data-ttu-id="ccb1a-126">**SdbGetNextChild**</span><span class="sxs-lookup"><span data-stu-id="ccb1a-126">**SdbGetNextChild**</span></span>](sdbgetnextchild.md)
</dt> </dl>

 

 




