---
description: Recherche le premier enregistrement DWORD de l’index spécifié qui répond aux critères spécifiés.
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: SdbFindFirstDWORDIndexedTag fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522815"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a><span data-ttu-id="79fa6-103">SdbFindFirstDWORDIndexedTag fonction)</span><span class="sxs-lookup"><span data-stu-id="79fa6-103">SdbFindFirstDWORDIndexedTag function</span></span>

<span data-ttu-id="79fa6-104">Recherche le premier enregistrement **DWORD** de l’index spécifié qui répond aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="79fa6-104">Finds the first **DWORD** record in the specified index that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="79fa6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79fa6-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
);
```



## <a name="parameters"></a><span data-ttu-id="79fa6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79fa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79fa6-107">fichier *PDB* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79fa6-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fa6-108">Handle de la base de données de shims.</span><span class="sxs-lookup"><span data-stu-id="79fa6-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="79fa6-109">*tWhich* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79fa6-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fa6-110">Type de l'index.</span><span class="sxs-lookup"><span data-stu-id="79fa6-110">The index type.</span></span> <span data-ttu-id="79fa6-111">Pour obtenir la liste des valeurs, consultez [**tag**](tag.md) .</span><span class="sxs-lookup"><span data-stu-id="79fa6-111">See [**TAG**](tag.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="79fa6-112">*tKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79fa6-112">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fa6-113">Type de clé.</span><span class="sxs-lookup"><span data-stu-id="79fa6-113">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="79fa6-114">*dwName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79fa6-114">*dwName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79fa6-115">Nom des données à trouver.</span><span class="sxs-lookup"><span data-stu-id="79fa6-115">The name of the data to be found.</span></span> <span data-ttu-id="79fa6-116">Cette valeur est convertie en clé.</span><span class="sxs-lookup"><span data-stu-id="79fa6-116">This value will be converted into a key.</span></span>

</dd> <dt>

<span data-ttu-id="79fa6-117">*pFindInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="79fa6-117">*pFindInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79fa6-118">Structure [**d' \_ informations de recherche**](find-info.md) qui reçoit l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="79fa6-118">A [**FIND\_INFO**](find-info.md) structure that receives the record.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79fa6-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79fa6-119">Return value</span></span>

<span data-ttu-id="79fa6-120">**TagId** de la première correspondance ou **balise \_ null** si aucune correspondance n’est trouvée.</span><span class="sxs-lookup"><span data-stu-id="79fa6-120">The **TAGID** of the first match or **TAG\_NULL** if no match is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="79fa6-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79fa6-121">Requirements</span></span>



| <span data-ttu-id="79fa6-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79fa6-122">Requirement</span></span> | <span data-ttu-id="79fa6-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="79fa6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="79fa6-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79fa6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="79fa6-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79fa6-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="79fa6-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79fa6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="79fa6-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79fa6-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="79fa6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="79fa6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79fa6-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79fa6-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79fa6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79fa6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79fa6-131">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="79fa6-131">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> </dl>

 

 




