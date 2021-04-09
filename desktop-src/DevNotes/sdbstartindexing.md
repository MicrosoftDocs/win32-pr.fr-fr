---
description: Active la création et la modification d’index pour la base de données spécifiée.
ms.assetid: f780034e-6963-423c-8ffa-9fbe98dca7e1
title: SdbStartIndexing fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStartIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e3324b4cb0d42ca33ee7c3234a1acc099adcb743
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110427"
---
# <a name="sdbstartindexing-function"></a><span data-ttu-id="bcf4c-103">SdbStartIndexing fonction)</span><span class="sxs-lookup"><span data-stu-id="bcf4c-103">SdbStartIndexing function</span></span>

<span data-ttu-id="bcf4c-104">Active la création et la modification d’index pour la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-104">Enables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf4c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcf4c-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStartIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="bcf4c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcf4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcf4c-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bcf4c-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf4c-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="bcf4c-109">*iiWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bcf4c-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcf4c-110">Identificateur d’index.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcf4c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bcf4c-111">Return value</span></span>

<span data-ttu-id="bcf4c-112">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="bcf4c-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf4c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcf4c-113">Requirements</span></span>



| <span data-ttu-id="bcf4c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcf4c-114">Requirement</span></span> | <span data-ttu-id="bcf4c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcf4c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf4c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcf4c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf4c-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcf4c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bcf4c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcf4c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf4c-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bcf4c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bcf4c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="bcf4c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcf4c-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcf4c-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcf4c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcf4c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf4c-123">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="bcf4c-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="bcf4c-124">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="bcf4c-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="bcf4c-125">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="bcf4c-125">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




