---
Description: Récupère la chaîne pour le TAGID spécifié.
ms.assetid: d67d386d-a2c5-46e2-8887-9ee20ea427f9
title: SdbReadStringTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadStringTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3f368d66e0fbc144a46683a04655cd7f650c3bce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942749"
---
# <a name="sdbreadstringtag-function"></a><span data-ttu-id="cc826-103">SdbReadStringTag fonction)</span><span class="sxs-lookup"><span data-stu-id="cc826-103">SdbReadStringTag function</span></span>

<span data-ttu-id="cc826-104">Récupère la chaîne pour le **TagId** spécifié.</span><span class="sxs-lookup"><span data-stu-id="cc826-104">Retrieves the string for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc826-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc826-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadStringTag(
  _In_  PDB    pdb,
  _In_  TAGID  tiWhich,
  _Out_ LPTSTR pwszBuffer,
  _In_  DWORD  cchBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="cc826-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc826-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc826-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc826-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc826-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="cc826-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="cc826-109">*tiWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc826-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc826-110">**TagId** qui correspond aux données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="cc826-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="cc826-111">*pwszBuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cc826-111">*pwszBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc826-112">Mémoire tampon qui reçoit la chaîne.</span><span class="sxs-lookup"><span data-stu-id="cc826-112">The buffer that receives the string.</span></span> <span data-ttu-id="cc826-113">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="cc826-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="cc826-114">*cchBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc826-114">*cchBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc826-115">Taille de la mémoire tampon *pwszBuffer* , en caractères.</span><span class="sxs-lookup"><span data-stu-id="cc826-115">The size of the *pwszBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc826-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc826-116">Return value</span></span>

<span data-ttu-id="cc826-117">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="cc826-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc826-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc826-118">Requirements</span></span>



| <span data-ttu-id="cc826-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc826-119">Requirement</span></span> | <span data-ttu-id="cc826-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc826-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc826-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc826-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cc826-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc826-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cc826-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc826-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cc826-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cc826-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cc826-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cc826-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc826-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc826-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc826-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc826-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc826-128">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="cc826-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="cc826-129">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="cc826-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="cc826-130">**SdbReadBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="cc826-130">**SdbReadBinaryTag**</span></span>](sdbreadbinarytag.md)
</dt> <dt>

[<span data-ttu-id="cc826-131">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="cc826-131">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> </dl>

 

 




