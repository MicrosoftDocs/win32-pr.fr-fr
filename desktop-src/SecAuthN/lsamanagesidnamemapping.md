---
UID: ''
title: LsaManageSidNameMapping fonction)
description: Ajoute ou supprime les mappages de SID/noms de l’ensemble de mappages inscrit auprès du service de recherche LSA.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: ''
ms.topic: reference
req.header: Ntsecapi.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Secur32.lib
req.dll:
- Advapi32.dll
- API-MS-Win-DownLevel-AdvAPI32-l4-1-0.dll
- API-MS-Win-security-lsalookup-l2-1-1.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name:
- LsaManageSidNameMapping
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: fc0065c3964718d690149693f3c71ec4e9f676ec
ms.sourcegitcommit: 382c7259008374408368c173e0027fb641c848fe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/22/2020
ms.locfileid: "104314492"
---
# <a name="lsamanagesidnamemapping-function"></a><span data-ttu-id="c408a-103">LsaManageSidNameMapping fonction)</span><span class="sxs-lookup"><span data-stu-id="c408a-103">LsaManageSidNameMapping function</span></span>

## <a name="description"></a><span data-ttu-id="c408a-104">Description</span><span class="sxs-lookup"><span data-stu-id="c408a-104">Description</span></span>

<span data-ttu-id="c408a-105">La fonction **LsaManageSidNameMapping** ajoute ou supprime les mappages de sid/nom de l’ensemble de mappages inscrit auprès du service de recherche LSA.</span><span class="sxs-lookup"><span data-stu-id="c408a-105">The **LsaManageSidNameMapping** function adds or removes SID/name mappings from the mapping set registered with the LSA Lookup Service.</span></span>

```cpp
void WINAPI LsaManageSidNameMapping(
  _In_  LSA_SID_NAME_MAPPING_OPERATION_TYPE    OpType,
  _In_  PLSA_SID_NAME_MAPPING_OPERATION_INPUT  OpInput,
  _Out_ PLSA_SID_NAME_MAPPING_OPERATION_OUTPUT *OpOutput
);
```

## <a name="parameters"></a><span data-ttu-id="c408a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c408a-106">Parameters</span></span>

### <a name="optype-in"></a><span data-ttu-id="c408a-107">OpType [in]</span><span class="sxs-lookup"><span data-stu-id="c408a-107">OpType [in]</span></span>

<span data-ttu-id="c408a-108">Indique si une fonction est appelée pour ajouter ou supprimer un mappage SID/nom.</span><span class="sxs-lookup"><span data-stu-id="c408a-108">Indicates if a this function is being called to add or remove an SID/name mapping.</span></span>

### <a name="opinput-in"></a><span data-ttu-id="c408a-109">OpInput [in]</span><span class="sxs-lookup"><span data-stu-id="c408a-109">OpInput [in]</span></span>

<span data-ttu-id="c408a-110">Indique le domaine, le compte et les valeurs SID à utiliser au cours de cette opération.</span><span class="sxs-lookup"><span data-stu-id="c408a-110">Indicates the domain, account, and SID values to use during this operation.</span></span> <span data-ttu-id="c408a-111">Des indicateurs supplémentaires peuvent également être définis dans cette structure.</span><span class="sxs-lookup"><span data-stu-id="c408a-111">Additional flags can also be set within this structure.</span></span>

### <a name="opoutput-out"></a><span data-ttu-id="c408a-112">OpOutput [out]</span><span class="sxs-lookup"><span data-stu-id="c408a-112">OpOutput [out]</span></span>

<span data-ttu-id="c408a-113">Contient une valeur de [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) qui indique la réussite ou l’échec de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c408a-113">Contains a value of [LSA_SID_NAME_MAPPING_OPERATION_ERROR](/previous-versions/windows/desktop/legacy/dn280707(v=vs.85)) that indicates operation success or failure.</span></span>

| <span data-ttu-id="c408a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="c408a-114">Value</span></span> | <span data-ttu-id="c408a-115">Signification</span><span class="sxs-lookup"><span data-stu-id="c408a-115">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="c408a-116">**Success**</span><span class="sxs-lookup"><span data-stu-id="c408a-116">**Success**</span></span> | <span data-ttu-id="c408a-117">L’opération est terminée sans erreur.</span><span class="sxs-lookup"><span data-stu-id="c408a-117">Operation is complete without error.</span></span> |
| <span data-ttu-id="c408a-118">**NonMappingError**</span><span class="sxs-lookup"><span data-stu-id="c408a-118">**NonMappingError**</span></span> | <span data-ttu-id="c408a-119">Une erreur non liée au mappage de nom SID s’est produite.</span><span class="sxs-lookup"><span data-stu-id="c408a-119">An error unrelated to SID-name mapping has occurred.</span></span> |
| <span data-ttu-id="c408a-120">**NameCollision**</span><span class="sxs-lookup"><span data-stu-id="c408a-120">**NameCollision**</span></span> | <span data-ttu-id="c408a-121">Échec de l’opération en raison d’une collision de noms.</span><span class="sxs-lookup"><span data-stu-id="c408a-121">Operation failure due to name collision.</span></span> |
| <span data-ttu-id="c408a-122">**SidCollision**</span><span class="sxs-lookup"><span data-stu-id="c408a-122">**SidCollision**</span></span> | <span data-ttu-id="c408a-123">Échec de l’opération en raison d’une collision de SID.</span><span class="sxs-lookup"><span data-stu-id="c408a-123">Operation failure due to SID collision.</span></span> |
| <span data-ttu-id="c408a-124">**DomainNotFound**</span><span class="sxs-lookup"><span data-stu-id="c408a-124">**DomainNotFound**</span></span> | <span data-ttu-id="c408a-125">Domaine correspondant introuvable.</span><span class="sxs-lookup"><span data-stu-id="c408a-125">Corresponding domain not found.</span></span> |
| <span data-ttu-id="c408a-126">**DomainSidPrefixMismatch**</span><span class="sxs-lookup"><span data-stu-id="c408a-126">**DomainSidPrefixMismatch**</span></span> | <span data-ttu-id="c408a-127">Le SID fourni n’a pas le préfixe de domaine correct.</span><span class="sxs-lookup"><span data-stu-id="c408a-127">Provided SID doesn't have the correct domain prefix.</span></span> |
| <span data-ttu-id="c408a-128">**MappingNotFound**</span><span class="sxs-lookup"><span data-stu-id="c408a-128">**MappingNotFound**</span></span> | <span data-ttu-id="c408a-129">Mappage introuvable dans le cache.</span><span class="sxs-lookup"><span data-stu-id="c408a-129">Mapping not found in the cache.</span></span> |

## <a name="returns"></a><span data-ttu-id="c408a-130">Retours</span><span class="sxs-lookup"><span data-stu-id="c408a-130">Returns</span></span>

<span data-ttu-id="c408a-131">Si le mappage est correctement inséré, la valeur de retour est STATUS_SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="c408a-131">If the mapping is inserted successfully, the return value is STATUS_SUCCESS.</span></span>
<span data-ttu-id="c408a-132">Sinon, si la fonction échoue en raison de conflits de noms ou de SID, STATUS_INVALID_PARAMETER erreur est retournée.</span><span class="sxs-lookup"><span data-stu-id="c408a-132">Otherwise, if the function fails due to SID or name conflicts, STATUS_INVALID_PARAMETER error will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="c408a-133">Notes</span><span class="sxs-lookup"><span data-stu-id="c408a-133">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="c408a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c408a-134">See also</span></span>
