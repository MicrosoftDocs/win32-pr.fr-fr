---
description: Valide les index nouvellement créés dans la base de données spécifiée.
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: SdbCommitIndexes fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCommitIndexes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0709a913dc78cefdf405a0a3bd29030801941c37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110282"
---
# <a name="sdbcommitindexes-function"></a><span data-ttu-id="c67ec-103">SdbCommitIndexes fonction)</span><span class="sxs-lookup"><span data-stu-id="c67ec-103">SdbCommitIndexes function</span></span>

<span data-ttu-id="c67ec-104">Valide les index nouvellement créés dans la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c67ec-104">Commits newly created indexes to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="c67ec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c67ec-105">Syntax</span></span>


```C++
BOOL WINAPI SdbCommitIndexes(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="c67ec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c67ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c67ec-107">fichier *PDB* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c67ec-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c67ec-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="c67ec-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c67ec-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c67ec-109">Return value</span></span>

<span data-ttu-id="c67ec-110">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="c67ec-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c67ec-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c67ec-111">Requirements</span></span>



| <span data-ttu-id="c67ec-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c67ec-112">Requirement</span></span> | <span data-ttu-id="c67ec-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="c67ec-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c67ec-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c67ec-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c67ec-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c67ec-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c67ec-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c67ec-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c67ec-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c67ec-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c67ec-118">DLL</span><span class="sxs-lookup"><span data-stu-id="c67ec-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c67ec-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c67ec-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c67ec-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c67ec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c67ec-121">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="c67ec-121">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="c67ec-122">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="c67ec-122">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="c67ec-123">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="c67ec-123">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




