---
description: Déclare un nouvel index dans la base de données spécifiée.
ms.assetid: 21a09201-8f84-4263-b258-77716826a3cd
title: SdbDeclareIndex fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbDeclareIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 68004a29d01288a2e1d177b8a33df32b919e73ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516387"
---
# <a name="sdbdeclareindex-function"></a><span data-ttu-id="b655a-103">SdbDeclareIndex fonction)</span><span class="sxs-lookup"><span data-stu-id="b655a-103">SdbDeclareIndex function</span></span>

<span data-ttu-id="b655a-104">Déclare un nouvel index dans la base de données spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b655a-104">Declares a new index in the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="b655a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b655a-105">Syntax</span></span>


```C++
BOOL WINAPI SdbDeclareIndex(
  _In_  PDB     pdb,
  _In_  TAG     tWhich,
  _In_  TAG     tKey,
  _In_  DWORD   dwEntries,
  _In_  BOOL    bUniqueKey,
  _Out_ INDEXID *piiIndex
);
```



## <a name="parameters"></a><span data-ttu-id="b655a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b655a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b655a-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b655a-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b655a-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="b655a-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="b655a-109">*tWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b655a-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b655a-110">Ce paramètre doit être **une \_ \_ liste de types de balises**.</span><span class="sxs-lookup"><span data-stu-id="b655a-110">This parameter must be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="b655a-111">*tKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b655a-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b655a-112">BALIse qui spécifie le type à utiliser comme clé.</span><span class="sxs-lookup"><span data-stu-id="b655a-112">The TAG that specifies the type to be used as the key.</span></span> <span data-ttu-id="b655a-113">Ce paramètre ne peut pas être une **\_ \_ liste de types de balises**.</span><span class="sxs-lookup"><span data-stu-id="b655a-113">This parameter cannot be **TAG\_TYPE\_LIST**.</span></span>

</dd> <dt>

<span data-ttu-id="b655a-114">*dwEntries* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b655a-114">*dwEntries* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b655a-115">Nombre d’entrées à allouer dans l’index.</span><span class="sxs-lookup"><span data-stu-id="b655a-115">The number of entries to allocate in the index.</span></span>

</dd> <dt>

<span data-ttu-id="b655a-116">*bUniqueKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b655a-116">*bUniqueKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b655a-117">Si ce paramètre a la **valeur true**, l’index est un index de clé unique.</span><span class="sxs-lookup"><span data-stu-id="b655a-117">If this parameter is **TRUE**, the index is a unique-key index.</span></span>

</dd> <dt>

<span data-ttu-id="b655a-118">*piiIndex* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b655a-118">*piiIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b655a-119">**IndexID contient** résultant de l’index nouvellement déclaré.</span><span class="sxs-lookup"><span data-stu-id="b655a-119">The resulting **INDEXID** of the newly declared index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b655a-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b655a-120">Return value</span></span>

<span data-ttu-id="b655a-121">La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="b655a-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="b655a-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b655a-122">Remarks</span></span>

<span data-ttu-id="b655a-123">Appelez cette fonction avant d’écrire des balises dans le nouvel index.</span><span class="sxs-lookup"><span data-stu-id="b655a-123">Call this function before writing tags to the new index.</span></span>

## <a name="requirements"></a><span data-ttu-id="b655a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b655a-124">Requirements</span></span>



| <span data-ttu-id="b655a-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b655a-125">Requirement</span></span> | <span data-ttu-id="b655a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b655a-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b655a-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b655a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b655a-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b655a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b655a-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b655a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b655a-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b655a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b655a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="b655a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b655a-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b655a-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b655a-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b655a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b655a-134">**INDEXID contient**</span><span class="sxs-lookup"><span data-stu-id="b655a-134">**INDEXID**</span></span>](indexid.md)
</dt> <dt>

[<span data-ttu-id="b655a-135">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="b655a-135">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="b655a-136">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="b655a-136">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="b655a-137">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="b655a-137">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




