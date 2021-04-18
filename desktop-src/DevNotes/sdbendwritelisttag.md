---
description: Termine les opérations d’écriture pour la liste spécifiée.
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: SdbEndWriteListTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f5f203e3b643fcae174eae3634b5d337a0d7276a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519199"
---
# <a name="sdbendwritelisttag-function"></a><span data-ttu-id="eadbc-103">SdbEndWriteListTag fonction)</span><span class="sxs-lookup"><span data-stu-id="eadbc-103">SdbEndWriteListTag function</span></span>

<span data-ttu-id="eadbc-104">Termine les opérations d’écriture pour la liste spécifiée.</span><span class="sxs-lookup"><span data-stu-id="eadbc-104">Ends the write operations for the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="eadbc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eadbc-105">Syntax</span></span>


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a><span data-ttu-id="eadbc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eadbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eadbc-107">fichier *PDB* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="eadbc-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="eadbc-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="eadbc-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="eadbc-109">*tiList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eadbc-109">*tiList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eadbc-110">[**TagId**](tagid.md) de la liste</span><span class="sxs-lookup"><span data-stu-id="eadbc-110">The [**TAGID**](tagid.md) of the list</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eadbc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eadbc-111">Return value</span></span>

<span data-ttu-id="eadbc-112">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="eadbc-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="eadbc-113">Notes</span><span class="sxs-lookup"><span data-stu-id="eadbc-113">Remarks</span></span>

<span data-ttu-id="eadbc-114">Appelez cette fonction après avoir écrit toutes les entrées de liste. il marquera la fin de la liste.</span><span class="sxs-lookup"><span data-stu-id="eadbc-114">Call this function after writing all list entries; it will mark the end of the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="eadbc-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eadbc-115">Requirements</span></span>



| <span data-ttu-id="eadbc-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eadbc-116">Requirement</span></span> | <span data-ttu-id="eadbc-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="eadbc-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eadbc-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eadbc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eadbc-119">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eadbc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="eadbc-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eadbc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eadbc-121">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eadbc-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="eadbc-122">DLL</span><span class="sxs-lookup"><span data-stu-id="eadbc-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eadbc-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eadbc-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eadbc-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eadbc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eadbc-125">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="eadbc-125">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="eadbc-126">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="eadbc-126">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="eadbc-127">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="eadbc-127">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




