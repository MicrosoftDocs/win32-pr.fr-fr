---
description: Écrit une valeur de mot dans la base de données spécifiée.
ms.assetid: 8f921e14-4a82-4d8e-83fa-beb78118ecb8
title: SdbWriteWORDTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75a5b3eb430901de36d5aca325f928aae266bc39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523316"
---
# <a name="sdbwritewordtag-function"></a><span data-ttu-id="3806a-103">SdbWriteWORDTag fonction)</span><span class="sxs-lookup"><span data-stu-id="3806a-103">SdbWriteWORDTag function</span></span>

<span data-ttu-id="3806a-104">Écrit une valeur de **mot** dans la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3806a-104">Writes a **WORD** value to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="3806a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3806a-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteWORDTag(
  _In_ PDB  pdb,
  _In_ TAG  tTag,
  _In_ WORD wData
);
```



## <a name="parameters"></a><span data-ttu-id="3806a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3806a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3806a-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3806a-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3806a-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="3806a-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="3806a-109">*tTag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3806a-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3806a-110">BALIse pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="3806a-110">The TAG for the entry.</span></span> <span data-ttu-id="3806a-111">Cette BALIse doit être de **type \_ \_ mot de balise**.</span><span class="sxs-lookup"><span data-stu-id="3806a-111">This TAG must be of type **TAG\_TYPE\_WORD**.</span></span>

</dd> <dt>

<span data-ttu-id="3806a-112">*wData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3806a-112">*wData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3806a-113">La valeur.</span><span class="sxs-lookup"><span data-stu-id="3806a-113">The value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3806a-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3806a-114">Return value</span></span>

<span data-ttu-id="3806a-115">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="3806a-115">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3806a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3806a-116">Requirements</span></span>



| <span data-ttu-id="3806a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3806a-117">Requirement</span></span> | <span data-ttu-id="3806a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3806a-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3806a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3806a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3806a-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3806a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3806a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3806a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3806a-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3806a-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3806a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3806a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3806a-124"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3806a-124"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3806a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3806a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3806a-126">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="3806a-126">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="3806a-127">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3806a-127">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="3806a-128">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3806a-128">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="3806a-129">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="3806a-129">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> </dl>

 

 




