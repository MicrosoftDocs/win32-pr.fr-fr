---
description: Écrit une valeur QWORD dans la base de données spécifiée.
ms.assetid: 8ce566ea-a941-45fa-b031-26c3144ca02c
title: SdbWriteQWORDTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteQWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 58dcaad3487bb1f59a75dd6a671ecb43c9cf1751
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748092"
---
# <a name="sdbwriteqwordtag-function"></a><span data-ttu-id="5e124-103">SdbWriteQWORDTag fonction)</span><span class="sxs-lookup"><span data-stu-id="5e124-103">SdbWriteQWORDTag function</span></span>

<span data-ttu-id="5e124-104">Écrit une valeur **QWord** dans la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5e124-104">Writes a **QWORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e124-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e124-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteQWORDTag(
  _In_ PDB       pdb,
  _In_ TAG       tTag,
  _In_ ULONGLONG qwData
);
```



## <a name="parameters"></a><span data-ttu-id="5e124-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e124-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e124-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e124-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e124-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="5e124-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="5e124-109">*tTag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e124-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e124-110">BALIse pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="5e124-110">The TAG for the entry.</span></span> <span data-ttu-id="5e124-111">Cette BALIse doit être de type de **balise \_ \_ QWord**.</span><span class="sxs-lookup"><span data-stu-id="5e124-111">This TAG must be of type **TAG\_TYPE\_QWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="5e124-112">*qwData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5e124-112">*qwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e124-113">La valeur.</span><span class="sxs-lookup"><span data-stu-id="5e124-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e124-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e124-114">Return value</span></span>

<span data-ttu-id="5e124-115">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="5e124-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e124-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e124-116">Requirements</span></span>



| <span data-ttu-id="5e124-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e124-117">Requirement</span></span> | <span data-ttu-id="5e124-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e124-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5e124-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e124-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5e124-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e124-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5e124-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e124-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5e124-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e124-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5e124-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5e124-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e124-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e124-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e124-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e124-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e124-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="5e124-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="5e124-127">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="5e124-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="5e124-128">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="5e124-128">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="5e124-129">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="5e124-129">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




