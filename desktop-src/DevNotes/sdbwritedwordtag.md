---
description: Écrit une valeur DWORD dans la base de données spécifiée.
ms.assetid: 2ecbfcac-5bb1-4129-9501-79210672aa1b
title: SdbWriteDWORDTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5b549a91037aa308b5b88d0e3e2a51e153002bd5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200934"
---
# <a name="sdbwritedwordtag-function"></a><span data-ttu-id="df0f1-103">SdbWriteDWORDTag fonction)</span><span class="sxs-lookup"><span data-stu-id="df0f1-103">SdbWriteDWORDTag function</span></span>

<span data-ttu-id="df0f1-104">Écrit une valeur **DWORD** dans la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="df0f1-104">Writes a **DWORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="df0f1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df0f1-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteDWORDTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ DWORD dwData
);
```



## <a name="parameters"></a><span data-ttu-id="df0f1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df0f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df0f1-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df0f1-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df0f1-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="df0f1-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="df0f1-109">*tTag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df0f1-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df0f1-110">BALIse pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="df0f1-110">The TAG for the entry.</span></span> <span data-ttu-id="df0f1-111">Cette BALIse doit être de **type \_ \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="df0f1-111">This TAG must be of type **TAG\_TYPE\_DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="df0f1-112">*dwData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df0f1-112">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df0f1-113">La valeur.</span><span class="sxs-lookup"><span data-stu-id="df0f1-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df0f1-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df0f1-114">Return value</span></span>

<span data-ttu-id="df0f1-115">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="df0f1-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="df0f1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df0f1-116">Requirements</span></span>



| <span data-ttu-id="df0f1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df0f1-117">Requirement</span></span> | <span data-ttu-id="df0f1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="df0f1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="df0f1-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df0f1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="df0f1-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df0f1-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="df0f1-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df0f1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="df0f1-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df0f1-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="df0f1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="df0f1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df0f1-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df0f1-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df0f1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df0f1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df0f1-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="df0f1-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="df0f1-127">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="df0f1-127">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="df0f1-128">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="df0f1-128">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="df0f1-129">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="df0f1-129">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




