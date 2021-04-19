---
description: Indique au système les modes de mise en conformité souhaités pour un ensemble d’opérations de protection contre la perte de données (DLP) de point de terminaison.
title: DlpInitializeEnforcementMode, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpInitializeEnforcementMode
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: cff3e1609f15f2cbbe6f6d9f76c6433ba3f4e5d7
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495523"
---
# <a name="dlpinitializeenforcementmode-function"></a><span data-ttu-id="12196-103">DlpInitializeEnforcementMode fonction)</span><span class="sxs-lookup"><span data-stu-id="12196-103">DlpInitializeEnforcementMode function</span></span>

<span data-ttu-id="12196-104">Indique au système les modes de mise en conformité souhaités pour un ensemble d’opérations de protection contre la perte de données (DLP) de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="12196-104">Notifies the system of the desired enforcement modes for a set of endpoint Data Loss Prevention (DLP) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="12196-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12196-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpInitializeEnforcementMode(_In_ DWORD Count, _In_reads_(Count) PDLP_APP_OP_ENLIGHTENED_LEVEL OperationEnforcement);
```



## <a name="parameters"></a><span data-ttu-id="12196-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12196-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12196-107">*Nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12196-107">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12196-108">**Valeur DWORD** spécifiant le nombre d’opérations incluses dans le tableau *OperationEnforcement* .</span><span class="sxs-lookup"><span data-stu-id="12196-108">A **DWORD** specifying the number of operations included in the *OperationEnforcement* array.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="12196-109">*OperationEnforcement* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="12196-109">*OperationEnforcement* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12196-110">Tableau de structures [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) qui spécifient le niveau d’application pour une opération DLP de point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="12196-110">An array of [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structures that specify the enforcement level for an endpoint DLP operation.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="12196-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="12196-111">Return value</span></span>

<span data-ttu-id="12196-112">Retourne un HRESULT incluant, sans s’y limiter, les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="12196-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="12196-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="12196-113">HRESULT</span></span> | <span data-ttu-id="12196-114">Description</span><span class="sxs-lookup"><span data-stu-id="12196-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="12196-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="12196-115">S_OK</span></span> | <span data-ttu-id="12196-116">La fonction s’est terminée avec succès</span><span class="sxs-lookup"><span data-stu-id="12196-116">The function completed successfully</span></span> |
| <span data-ttu-id="12196-117">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="12196-117">E_INVALIDARG</span></span> | <span data-ttu-id="12196-118">Un ou plusieurs des paramètres de fonction ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="12196-118">One or more of the function parameters are invalid.</span></span> |
| <span data-ttu-id="12196-119">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="12196-119">E_OUTOFMEMORY</span></span> | <span data-ttu-id="12196-120">L’allocation de mémoire pour l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="12196-120">Memory allocation for the operation failed.</span></span> |



## <a name="remarks"></a><span data-ttu-id="12196-121">Notes</span><span class="sxs-lookup"><span data-stu-id="12196-121">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="12196-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="12196-122">Requirements</span></span>



| <span data-ttu-id="12196-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12196-123">Requirement</span></span>          |    <span data-ttu-id="12196-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="12196-124">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12196-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12196-125">Minimum supported client</span></span><br/> | <span data-ttu-id="12196-126">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="12196-126">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="12196-127">DLL</span><span class="sxs-lookup"><span data-stu-id="12196-127">DLL</span></span><br/>                      | <span data-ttu-id="12196-128">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="12196-128">EndpointDlp.dll</span></span> |