---
description: Écrit des données binaires dans la base de données spécifiée.
ms.assetid: 935321b8-904e-46be-ad11-77d89670a072
title: SdbWriteBinaryTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e79de8549eb4c0a0f1b8a914c59d21ccfb3bcf7a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523324"
---
# <a name="sdbwritebinarytag-function"></a><span data-ttu-id="3e23f-103">SdbWriteBinaryTag fonction)</span><span class="sxs-lookup"><span data-stu-id="3e23f-103">SdbWriteBinaryTag function</span></span>

<span data-ttu-id="3e23f-104">Écrit des données binaires dans la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3e23f-104">Writes binary data to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e23f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e23f-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTag(
  _In_ PDB   pdb,
  _In_ TAG   tTag,
  _In_ PBYTE pBuffer,
  _In_ DWORD dwSize
);
```



## <a name="parameters"></a><span data-ttu-id="3e23f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3e23f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e23f-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e23f-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e23f-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="3e23f-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="3e23f-109">*tTag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e23f-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e23f-110">BALIse pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="3e23f-110">The TAG for the entry.</span></span> <span data-ttu-id="3e23f-111">Cette BALIse doit être de **type \_ \_ binaire**.</span><span class="sxs-lookup"><span data-stu-id="3e23f-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="3e23f-112">*pbuffer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e23f-112">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e23f-113">Mémoire tampon qui contient les données.</span><span class="sxs-lookup"><span data-stu-id="3e23f-113">The buffer that contains the data.</span></span> <span data-ttu-id="3e23f-114">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="3e23f-114">This parameter cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3e23f-115">*dwSize nul* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3e23f-115">*dwSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e23f-116">Taille de la mémoire tampon *pbuffer* , en octets.</span><span class="sxs-lookup"><span data-stu-id="3e23f-116">The size of the *pBuffer* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e23f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3e23f-117">Return value</span></span>

<span data-ttu-id="3e23f-118">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="3e23f-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e23f-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e23f-119">Requirements</span></span>



| <span data-ttu-id="3e23f-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e23f-120">Requirement</span></span> | <span data-ttu-id="3e23f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e23f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e23f-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e23f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3e23f-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e23f-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3e23f-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e23f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3e23f-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e23f-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3e23f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="3e23f-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e23f-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e23f-127"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e23f-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e23f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e23f-129">**SdbWriteBinaryTagFromFile**</span><span class="sxs-lookup"><span data-stu-id="3e23f-129">**SdbWriteBinaryTagFromFile**</span></span>](sdbwritebinarytagfromfile.md)
</dt> <dt>

[<span data-ttu-id="3e23f-130">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3e23f-130">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="3e23f-131">**SdbWriteQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3e23f-131">**SdbWriteQWORDTag**</span></span>](sdbwriteqwordtag.md)
</dt> <dt>

[<span data-ttu-id="3e23f-132">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="3e23f-132">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="3e23f-133">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3e23f-133">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




