---
Description: Récupère la valeur DWORD pour le TAGID spécifié.
ms.assetid: 6610e101-9068-4812-b0ca-528658b62535
title: SdbReadDWORDTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReadDWORDTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0f1f7acc113bc40388d62927b6d98f8ff7bdebf1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105928"
---
# <a name="sdbreaddwordtag-function"></a><span data-ttu-id="e1f92-103">SdbReadDWORDTag fonction)</span><span class="sxs-lookup"><span data-stu-id="e1f92-103">SdbReadDWORDTag function</span></span>

<span data-ttu-id="e1f92-104">Récupère la valeur **DWORD** pour le **TagId** spécifié.</span><span class="sxs-lookup"><span data-stu-id="e1f92-104">Retrieves the **DWORD** value for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f92-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1f92-105">Syntax</span></span>


```C++
DWORD WINAPI SdbReadDWORDTag(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich,
  _In_ DWORD dwDefault
);
```



## <a name="parameters"></a><span data-ttu-id="e1f92-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1f92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1f92-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1f92-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1f92-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="e1f92-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="e1f92-109">*tiWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1f92-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1f92-110">**TagId** qui correspond aux données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e1f92-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="e1f92-111">*dwDefault* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1f92-111">*dwDefault* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1f92-112">Valeur par défaut à retourner en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="e1f92-112">The default value to be returned on failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1f92-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1f92-113">Return value</span></span>

<span data-ttu-id="e1f92-114">La fonction retourne la valeur en cas de réussite ou *dwDefault* en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="e1f92-114">The function returns the value on success or *dwDefault* on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1f92-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1f92-115">Requirements</span></span>



| <span data-ttu-id="e1f92-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1f92-116">Requirement</span></span> | <span data-ttu-id="e1f92-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1f92-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f92-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1f92-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e1f92-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1f92-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e1f92-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e1f92-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e1f92-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e1f92-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e1f92-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e1f92-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1f92-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1f92-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1f92-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1f92-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f92-125">**SdbGetBinaryTagData**</span><span class="sxs-lookup"><span data-stu-id="e1f92-125">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="e1f92-126">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="e1f92-126">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="e1f92-127">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="e1f92-127">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="e1f92-128">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="e1f92-128">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




