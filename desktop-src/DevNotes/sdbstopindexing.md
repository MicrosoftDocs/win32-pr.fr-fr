---
description: Désactive la création et la modification d’index pour la base de données spécifiée.
ms.assetid: d079eae2-574e-4ac1-a0f9-11796e56a790
title: SdbStopIndexing fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStopIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3c9c6b34c265d611b57a3e73bb0c8fb1822fe752
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523327"
---
# <a name="sdbstopindexing-function"></a><span data-ttu-id="c46c7-103">SdbStopIndexing fonction)</span><span class="sxs-lookup"><span data-stu-id="c46c7-103">SdbStopIndexing function</span></span>

<span data-ttu-id="c46c7-104">Désactive la création et la modification d’index pour la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c46c7-104">Disables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="c46c7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c46c7-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStopIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="c46c7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c46c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c46c7-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c46c7-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c46c7-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="c46c7-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="c46c7-109">*iiWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c46c7-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c46c7-110">Identificateur d’index.</span><span class="sxs-lookup"><span data-stu-id="c46c7-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c46c7-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c46c7-111">Return value</span></span>

<span data-ttu-id="c46c7-112">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="c46c7-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c46c7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c46c7-113">Requirements</span></span>



| <span data-ttu-id="c46c7-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c46c7-114">Requirement</span></span> | <span data-ttu-id="c46c7-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c46c7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c46c7-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c46c7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c46c7-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c46c7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c46c7-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c46c7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c46c7-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c46c7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c46c7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c46c7-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c46c7-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c46c7-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c46c7-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c46c7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c46c7-123">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="c46c7-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="c46c7-124">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="c46c7-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="c46c7-125">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="c46c7-125">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> </dl>

 

 




