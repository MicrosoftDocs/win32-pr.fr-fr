---
description: Récupère la version de l’API de protection contre la perte de données (DLP) du point de terminaison sur l’appareil actuel.
title: DlpGetEnforcementApiVersion, fonction (endpointdlp. h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpGetEnforcementApiVersion
api_type:
- DllExport
api_location:
- EndpointDlp.dll
ms.openlocfilehash: d2b38b6bdcfd761b8ae3c90ee5d3b430767ad29c
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495769"
---
# <a name="dlpgetenforcementapiversion-function"></a><span data-ttu-id="174f9-103">DlpGetEnforcementApiVersion fonction)</span><span class="sxs-lookup"><span data-stu-id="174f9-103">DlpGetEnforcementApiVersion function</span></span>

<span data-ttu-id="174f9-104">Récupère la version de l’API de protection contre la perte de données (DLP) du point de terminaison sur l’appareil actuel.</span><span class="sxs-lookup"><span data-stu-id="174f9-104">Retrieves the version of the endpoint Data Loss Prevention (DLP) API on the current device.</span></span>

## <a name="syntax"></a><span data-ttu-id="174f9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="174f9-105">Syntax</span></span>


```C++
HRESULT WINAPI DlpGetEnforcementApiVersion(_Out_ DWORD* MajorVersion, _Out_ DWORD* MinorVersion);
```



## <a name="parameters"></a><span data-ttu-id="174f9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="174f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="174f9-107">*MajorVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="174f9-107">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="174f9-108">**Valeur DWORD** spécifiant le numéro de version principale.</span><span class="sxs-lookup"><span data-stu-id="174f9-108">A **DWORD** specifying the major version number.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="174f9-109">*MajorVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="174f9-109">*MajorVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="174f9-110">**Valeur DWORD** spécifiant le numéro de version mineure.</span><span class="sxs-lookup"><span data-stu-id="174f9-110">A **DWORD** specifying the minor version number.</span></span>

</dd> </dl>


## <a name="return-value"></a><span data-ttu-id="174f9-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="174f9-111">Return value</span></span>

<span data-ttu-id="174f9-112">Retourne un HRESULT incluant, sans s’y limiter, les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="174f9-112">Returns an HRESULT including, but not limited to, the following values.</span></span>

| <span data-ttu-id="174f9-113">HRESULT</span><span class="sxs-lookup"><span data-stu-id="174f9-113">HRESULT</span></span> | <span data-ttu-id="174f9-114">Description</span><span class="sxs-lookup"><span data-stu-id="174f9-114">Description</span></span> |
|---------|-------------|
| <span data-ttu-id="174f9-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="174f9-115">S_OK</span></span> | <span data-ttu-id="174f9-116">La fonction s’est terminée avec succès</span><span class="sxs-lookup"><span data-stu-id="174f9-116">The function completed successfully</span></span> |




## <a name="remarks"></a><span data-ttu-id="174f9-117">Notes</span><span class="sxs-lookup"><span data-stu-id="174f9-117">Remarks</span></span>


## <a name="requirements"></a><span data-ttu-id="174f9-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="174f9-118">Requirements</span></span>



| <span data-ttu-id="174f9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="174f9-119">Requirement</span></span>          |    <span data-ttu-id="174f9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="174f9-120">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="174f9-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="174f9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="174f9-122">Windows 10, version 1809 (10,0 ; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="174f9-122">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |
| <span data-ttu-id="174f9-123">DLL</span><span class="sxs-lookup"><span data-stu-id="174f9-123">DLL</span></span><br/>                      | <span data-ttu-id="174f9-124">EndpointDlp.dll</span><span class="sxs-lookup"><span data-stu-id="174f9-124">EndpointDlp.dll</span></span> |