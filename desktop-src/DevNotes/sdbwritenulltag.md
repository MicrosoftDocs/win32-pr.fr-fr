---
description: Écrit une entrée NULL dans la base de données spécifiée.
ms.assetid: 2a29389b-d4f6-4527-a429-c9459b095f2f
title: SdbWriteNULLTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteNULLTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 662d5c4db31f199df8b3b9f7368aba118ea6e8fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200933"
---
# <a name="sdbwritenulltag-function"></a><span data-ttu-id="3de10-103">SdbWriteNULLTag fonction)</span><span class="sxs-lookup"><span data-stu-id="3de10-103">SdbWriteNULLTag function</span></span>

<span data-ttu-id="3de10-104">Écrit une entrée **null** dans la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3de10-104">Writes a **NULL** entry to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="3de10-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3de10-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteNULLTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="3de10-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3de10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de10-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3de10-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de10-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="3de10-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="3de10-109">*tTag* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3de10-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3de10-110">BALIse pour l’entrée.</span><span class="sxs-lookup"><span data-stu-id="3de10-110">The TAG for the entry.</span></span> <span data-ttu-id="3de10-111">Cette BALIse doit être de type de **balise \_ \_ null**.</span><span class="sxs-lookup"><span data-stu-id="3de10-111">This TAG must be of type **TAG\_TYPE\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de10-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3de10-112">Return value</span></span>

<span data-ttu-id="3de10-113">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="3de10-113">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3de10-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3de10-114">Requirements</span></span>



| <span data-ttu-id="3de10-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3de10-115">Requirement</span></span> | <span data-ttu-id="3de10-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3de10-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3de10-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3de10-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3de10-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3de10-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3de10-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3de10-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3de10-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3de10-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3de10-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3de10-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3de10-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3de10-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de10-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3de10-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de10-124">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="3de10-124">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> <dt>

[<span data-ttu-id="3de10-125">**SdbWriteDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3de10-125">**SdbWriteDWORDTag**</span></span>](sdbwritedwordtag.md)
</dt> <dt>

[<span data-ttu-id="3de10-126">**SdbWriteStringTag**</span><span class="sxs-lookup"><span data-stu-id="3de10-126">**SdbWriteStringTag**</span></span>](sdbwritestringtag.md)
</dt> <dt>

[<span data-ttu-id="3de10-127">**SdbWriteWORDTag**</span><span class="sxs-lookup"><span data-stu-id="3de10-127">**SdbWriteWORDTag**</span></span>](sdbwritewordtag.md)
</dt> </dl>

 

 




