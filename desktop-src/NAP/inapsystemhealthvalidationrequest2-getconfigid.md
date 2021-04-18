---
title: Méthode INapSystemHealthValidationRequest2 GetConfigID (NapSystemHealthValidator. h)
description: Utilisé par les programmes de validation d’intégrité système (SHV) pour récupérer l’ID de configuration dans une demande de validation.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- Méthode GetConfigID NAP
- Méthode GetConfigID NAP, interface INapSystemHealthValidationRequest2
- INapSystemHealthValidationRequest2 interface NAP, méthode GetConfigID
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512205"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a><span data-ttu-id="f0ba4-106">INapSystemHealthValidationRequest2 :: GetConfigID, méthode</span><span class="sxs-lookup"><span data-stu-id="f0ba4-106">INapSystemHealthValidationRequest2::GetConfigID method</span></span>

> [!Note]  
> <span data-ttu-id="f0ba4-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="f0ba4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f0ba4-108">La méthode **INapSystemHealthValidationRequest2 :: GetConfigId** est utilisée par les programmes de validation d’intégrité système (SHV) pour récupérer l’ID de configuration dans une demande de validation.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-108">The **INapSystemHealthValidationRequest2::GetConfigId** method is used by the System Health Validators (SHVs) to retrieve the configuration ID in a validation request.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ba4-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0ba4-109">Syntax</span></span>


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a><span data-ttu-id="f0ba4-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0ba4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0ba4-111">*configID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f0ba4-111">*configID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ba4-112">Au retour, pointeur vers UINT32 qui contient un ID de configuration de la SHV.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-112">On return, a pointer to UINT32 that contains a configuration ID of the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0ba4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f0ba4-113">Return value</span></span>

<span data-ttu-id="f0ba4-114">Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="f0ba4-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f0ba4-115">Return code</span></span>                                                                                  | <span data-ttu-id="f0ba4-116">Description</span><span class="sxs-lookup"><span data-stu-id="f0ba4-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="f0ba4-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ba4-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f0ba4-118">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-118">Operation successful.</span></span><br/>                |
| <dl> <span data-ttu-id="f0ba4-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f0ba4-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f0ba4-120">Le paramètre configID a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="f0ba4-120">The configID parameter was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f0ba4-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0ba4-121">Requirements</span></span>



| <span data-ttu-id="f0ba4-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f0ba4-122">Requirement</span></span> | <span data-ttu-id="f0ba4-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f0ba4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ba4-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0ba4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ba4-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0ba4-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="f0ba4-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f0ba4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ba4-127">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f0ba4-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f0ba4-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="f0ba4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0ba4-129"><dt>NapSystemHealthValidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0ba4-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0ba4-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="f0ba4-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f0ba4-131"><dt>NapSystemHealthValidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f0ba4-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="f0ba4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="f0ba4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0ba4-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0ba4-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="f0ba4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0ba4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ba4-135">**INapSystemHealthValidationRequest2**</span><span class="sxs-lookup"><span data-stu-id="f0ba4-135">**INapSystemHealthValidationRequest2**</span></span>](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





