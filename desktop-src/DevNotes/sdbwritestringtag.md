---
description: Écrit une chaîne dans la base de données spécifiée.
ms.assetid: 72c62d91-0c1c-4ff8-8829-1c3ec1fa8648
title: SdbWriteStringTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4ac588d99408d0d7f13bc0fd13d8abe8a6580e69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860886"
---
# <a name="sdbwritestringtag-function"></a><span data-ttu-id="3db52-103">SdbWriteStringTag fonction)</span><span class="sxs-lookup"><span data-stu-id="3db52-103">SdbWriteStringTag function</span></span>

<span data-ttu-id="3db52-104">Écrit une chaîne dans la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3db52-104">Writes a string to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="3db52-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3db52-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteStringTag(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszData
);
```



## <a name="parameters"></a><span data-ttu-id="3db52-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3db52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3db52-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3db52-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3db52-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="3db52-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="3db52-109">*tTag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3db52-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3db52-110">BALIse pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="3db52-110">The TAG for the entry.</span></span> <span data-ttu-id="3db52-111">Cette BALIse doit être de **type \_ \_ STRINGREF**.</span><span class="sxs-lookup"><span data-stu-id="3db52-111">This TAG must be of type **TAG\_TYPE\_STRINGREF**.</span></span>

</dd> <dt>

<span data-ttu-id="3db52-112">*pwszData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3db52-112">*pwszData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3db52-113">Chaîne terminée par le caractère null.</span><span class="sxs-lookup"><span data-stu-id="3db52-113">The null-terminated string.</span></span> <span data-ttu-id="3db52-114">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="3db52-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3db52-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3db52-115">Return value</span></span>

<span data-ttu-id="3db52-116">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="3db52-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3db52-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3db52-117">Requirements</span></span>



| <span data-ttu-id="3db52-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3db52-118">Requirement</span></span> | <span data-ttu-id="3db52-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3db52-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3db52-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3db52-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3db52-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3db52-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3db52-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3db52-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3db52-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3db52-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3db52-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3db52-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3db52-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3db52-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3db52-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3db52-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3db52-127">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="3db52-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="3db52-128">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3db52-128">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="3db52-129">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3db52-129">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="3db52-130">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3db52-130">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




