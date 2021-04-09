---
description: Récupère la BALIse associée au TAGID spécifié.
ms.assetid: 194d2035-fc2c-445d-a730-90db2ccea8af
title: SdbGetTagFromTagID fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetTagFromTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: d81dac026a9b6acc921586aaded54c8c90ad5bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110650"
---
# <a name="sdbgettagfromtagid-function"></a><span data-ttu-id="0723c-103">SdbGetTagFromTagID fonction)</span><span class="sxs-lookup"><span data-stu-id="0723c-103">SdbGetTagFromTagID function</span></span>

<span data-ttu-id="0723c-104">Récupère la BALIse associée au **TagId** spécifié.</span><span class="sxs-lookup"><span data-stu-id="0723c-104">Retrieves the TAG associated with the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0723c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0723c-105">Syntax</span></span>


```C++
TAG WINAPI SdbGetTagFromTagID(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="0723c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0723c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0723c-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0723c-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0723c-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="0723c-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="0723c-109">*tiWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0723c-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0723c-110">**TagId** pour la balise.</span><span class="sxs-lookup"><span data-stu-id="0723c-110">The **TAGID** for the TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0723c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0723c-111">Return value</span></span>

<span data-ttu-id="0723c-112">La fonction retourne la BALIse.</span><span class="sxs-lookup"><span data-stu-id="0723c-112">The function returns the TAG.</span></span>

## <a name="requirements"></a><span data-ttu-id="0723c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0723c-113">Requirements</span></span>



| <span data-ttu-id="0723c-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0723c-114">Requirement</span></span> | <span data-ttu-id="0723c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0723c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0723c-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0723c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0723c-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0723c-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0723c-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0723c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0723c-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0723c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0723c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0723c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0723c-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0723c-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0723c-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0723c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0723c-123">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0723c-123">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="0723c-124">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="0723c-124">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




