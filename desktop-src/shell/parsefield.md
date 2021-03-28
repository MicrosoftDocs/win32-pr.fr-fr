---
description: Lit une ligne à partir de Setup. inf et extrait le champ spécifié de la chaîne.
ms.assetid: 621e85f8-af30-4f1f-bab1-b7f824daa363
title: Fonction ParseField (util. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ParseField
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 45c7d5bc692f969ba821b5d3243b312d0883658e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203445"
---
# <a name="parsefield-function"></a><span data-ttu-id="c042e-103">ParseField fonction)</span><span class="sxs-lookup"><span data-stu-id="c042e-103">ParseField function</span></span>

<span data-ttu-id="c042e-104">\[La fonction **ParseField** est actuellement censée être utilisée dans la prochaine version du système d’exploitation Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="c042e-104">\[The **ParseField** function is currently expected to be available for use in the next version of the Microsoft Windows operating system.</span></span> <span data-ttu-id="c042e-105">Il peut être modifié ou non disponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="c042e-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="c042e-106">Lit une ligne à partir de Setup. inf et extrait le champ spécifié de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="c042e-106">Reads a line from Setup.inf and extracts the specified field from the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c042e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c042e-107">Syntax</span></span>


```C++
bool ParseField(
  _In_ LPCTSTR *szData,
  _In_ int     n,
  _In_ LPTSTR  *szBuf,
  _In_ int     iBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="c042e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c042e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c042e-109">*szData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c042e-109">*szData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c042e-110">Tapez : \**LPCTSTR \** _</span><span class="sxs-lookup"><span data-stu-id="c042e-110">Type: \**LPCTSTR\** _</span></span>

<span data-ttu-id="c042e-111">Pointeur vers la ligne de Setup. inf.</span><span class="sxs-lookup"><span data-stu-id="c042e-111">A pointer to the line from Setup.inf.</span></span>

</dd> <dt>

<span data-ttu-id="c042e-112">_n \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c042e-112">_n\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c042e-113">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="c042e-113">Type: **int**</span></span>

<span data-ttu-id="c042e-114">**Entier** qui indique le champ à extraire.</span><span class="sxs-lookup"><span data-stu-id="c042e-114">**INT** that indicates which field to extract.</span></span>

<dt>



 <span data-ttu-id="c042e-115"> (0)</span><span class="sxs-lookup"><span data-stu-id="c042e-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c042e-116">Indique le champ avant un signe égal (=).</span><span class="sxs-lookup"><span data-stu-id="c042e-116">Indicates the field before an equals sign (=).</span></span>

</dd> <dt>



 <span data-ttu-id="c042e-117">(1)</span><span class="sxs-lookup"><span data-stu-id="c042e-117">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c042e-118">Indique le premier champ.</span><span class="sxs-lookup"><span data-stu-id="c042e-118">Indicates the first field.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c042e-119">*szBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c042e-119">*szBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c042e-120">Type : \**LPTStr \** _</span><span class="sxs-lookup"><span data-stu-id="c042e-120">Type: \**LPTSTR\** _</span></span>

<span data-ttu-id="c042e-121">Pointeur vers la mémoire tampon qui reçoit le champ extrait.</span><span class="sxs-lookup"><span data-stu-id="c042e-121">A pointer to the buffer that receives the extracted field.</span></span>

</dd> <dt>

<span data-ttu-id="c042e-122">_iBufLen \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c042e-122">_iBufLen\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c042e-123">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="c042e-123">Type: **int**</span></span>

<span data-ttu-id="c042e-124">**Entier** qui reçoit la taille de la mémoire tampon qui reçoit le champ extrait.</span><span class="sxs-lookup"><span data-stu-id="c042e-124">**INT** that receives the size of the buffer that receives the extracted field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c042e-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c042e-125">Return value</span></span>

<span data-ttu-id="c042e-126">Type : **bool**</span><span class="sxs-lookup"><span data-stu-id="c042e-126">Type: **bool**</span></span>

<span data-ttu-id="c042e-127">Retourne la **valeur true** si la fonction a réussi et **false** si elle échoue.</span><span class="sxs-lookup"><span data-stu-id="c042e-127">Returns **TRUE** if the function is successful and **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="c042e-128">Notes</span><span class="sxs-lookup"><span data-stu-id="c042e-128">Remarks</span></span>

<span data-ttu-id="c042e-129">Les champs de la chaîne doivent être séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="c042e-129">The fields in the string must be separated by commas.</span></span>

<span data-ttu-id="c042e-130">Les espaces de début et de fin sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="c042e-130">Leading and trailing spaces are removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="c042e-131">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c042e-131">Requirements</span></span>



| <span data-ttu-id="c042e-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c042e-132">Requirement</span></span> | <span data-ttu-id="c042e-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c042e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c042e-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c042e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c042e-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c042e-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c042e-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c042e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c042e-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c042e-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c042e-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="c042e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c042e-139"><dt>Util. h</dt></span><span class="sxs-lookup"><span data-stu-id="c042e-139"><dt>Util.h</dt></span></span> </dl>                             |
| <span data-ttu-id="c042e-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c042e-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="c042e-141"><dt>Shell32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c042e-141"><dt>Shell32.lib</dt></span></span> </dl>                        |
| <span data-ttu-id="c042e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="c042e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c042e-143"><dt>Shell32.dll (version 5,0 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c042e-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




