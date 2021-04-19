---
Description: Récupère les données binaires pour le TAGID spécifié.
ms.assetid: b349f2af-2505-4efc-bd59-203f7666ce61
title: SdbReadBinaryTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 024b432c3210b98721a0cf3058bad0f765287fde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511558"
---
# <a name="sdbreadbinarytag-function"></a><span data-ttu-id="47667-103">SdbReadBinaryTag fonction)</span><span class="sxs-lookup"><span data-stu-id="47667-103">SdbReadBinaryTag function</span></span>

<span data-ttu-id="47667-104">Récupère les données binaires pour le **TagId** spécifié.</span><span class="sxs-lookup"><span data-stu-id="47667-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="47667-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47667-105">Syntax</span></span>


```C++
BOOL WINAPI SdbReadBinaryTag(
  _In_  PDB   pdb,
  _In_  TAGID tiWhich,
  _Out_ PBYTE pBuffer,
  _In_  DWORD dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="47667-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47667-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47667-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47667-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47667-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="47667-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="47667-109">*tiWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47667-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47667-110">**TagId** qui correspond aux données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="47667-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="47667-111">*pbuffer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="47667-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47667-112">Mémoire tampon qui reçoit les données binaires.</span><span class="sxs-lookup"><span data-stu-id="47667-112">The buffer that receives the binary data.</span></span> <span data-ttu-id="47667-113">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="47667-113">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="47667-114">*dwBufferSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47667-114">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47667-115">Taille de la mémoire tampon *pbuffer* , en octets.</span><span class="sxs-lookup"><span data-stu-id="47667-115">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47667-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47667-116">Return value</span></span>

<span data-ttu-id="47667-117">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="47667-117">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="47667-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47667-118">Requirements</span></span>



| <span data-ttu-id="47667-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47667-119">Requirement</span></span> | <span data-ttu-id="47667-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="47667-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47667-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47667-121">Minimum supported client</span></span><br/> | <span data-ttu-id="47667-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47667-122">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="47667-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47667-123">Minimum supported server</span></span><br/> | <span data-ttu-id="47667-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47667-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="47667-125">DLL</span><span class="sxs-lookup"><span data-stu-id="47667-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47667-126"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47667-126"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47667-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47667-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47667-128">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="47667-128">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="47667-129">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="47667-129">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="47667-130">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="47667-130">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="47667-131">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="47667-131">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




