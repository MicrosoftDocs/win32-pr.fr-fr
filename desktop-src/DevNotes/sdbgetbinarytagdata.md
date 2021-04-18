---
description: Récupère les données binaires pour le TAGID spécifié.
ms.assetid: 18992406-67b4-4c48-9629-04d6bf1c5824
title: SdbGetBinaryTagData fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetBinaryTagData
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 028b073b149482b79b848216e44b8a425d6ffb56
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515925"
---
# <a name="sdbgetbinarytagdata-function"></a><span data-ttu-id="216f6-103">SdbGetBinaryTagData fonction)</span><span class="sxs-lookup"><span data-stu-id="216f6-103">SdbGetBinaryTagData function</span></span>

<span data-ttu-id="216f6-104">Récupère les données binaires pour le **TagId** spécifié.</span><span class="sxs-lookup"><span data-stu-id="216f6-104">Retrieves the binary data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="216f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="216f6-105">Syntax</span></span>


```C++
PVOID WINAPI SdbGetBinaryTagData(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="216f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="216f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="216f6-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="216f6-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216f6-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="216f6-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="216f6-109">*tiWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="216f6-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="216f6-110">**TagId** qui correspond aux données à récupérer.</span><span class="sxs-lookup"><span data-stu-id="216f6-110">The **TAGID** that corresponds to the data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="216f6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="216f6-111">Return value</span></span>

<span data-ttu-id="216f6-112">La fonction retourne un pointeur vers les données binaires ou **null** si le **TagId** n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="216f6-112">The function returns a pointer to the binary data or **NULL** if the **TAGID** is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="216f6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="216f6-113">Requirements</span></span>



| <span data-ttu-id="216f6-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="216f6-114">Requirement</span></span> | <span data-ttu-id="216f6-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="216f6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="216f6-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="216f6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="216f6-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="216f6-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="216f6-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="216f6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="216f6-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="216f6-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="216f6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="216f6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="216f6-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="216f6-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="216f6-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="216f6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="216f6-123">**SdbGetStringTagPtr**</span><span class="sxs-lookup"><span data-stu-id="216f6-123">**SdbGetStringTagPtr**</span></span>](sdbgetstringtagptr.md)
</dt> <dt>

[<span data-ttu-id="216f6-124">**SdbReadDWORDTag**</span><span class="sxs-lookup"><span data-stu-id="216f6-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="216f6-125">**SdbReadQWORDTag**</span><span class="sxs-lookup"><span data-stu-id="216f6-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="216f6-126">**SdbReadStringTag**</span><span class="sxs-lookup"><span data-stu-id="216f6-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




