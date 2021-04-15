---
title: Méthode INapEnforcementClientConnection2 GetInstalledShvs (NapEnforcementClient. h)
description: Utilisé par l’agent NAP pour interroger les programmes de validation d’intégrité système (SHV) installés sur le client.
ms.assetid: b2e3ab29-90bf-4117-bc2e-2ff2827ee15c
keywords:
- Méthode GetInstalledShvs NAP
- Méthode GetInstalledShvs NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, méthode GetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa54d09a0c3d3c524262231982f662c497920a0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467067"
---
# <a name="inapenforcementclientconnection2getinstalledshvs-method"></a><span data-ttu-id="34243-106">INapEnforcementClientConnection2 :: GetInstalledShvs, méthode</span><span class="sxs-lookup"><span data-stu-id="34243-106">INapEnforcementClientConnection2::GetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="34243-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="34243-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="34243-108">La méthode **GetInstalledShvs** est utilisée par l’agent NAP pour interroger les programmes de validation d’intégrité système (SHV) installés sur le client.</span><span class="sxs-lookup"><span data-stu-id="34243-108">The **GetInstalledShvs** method is used by the NAP Agent to query the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="34243-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34243-109">Syntax</span></span>


```C++
HRESULT GetInstalledShvs(
  [out] SystemHealthEntityCount *count,
  [out] SystemHealthEntityId    **ids
) const;
```



## <a name="parameters"></a><span data-ttu-id="34243-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34243-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34243-111">*nombre* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="34243-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34243-112">Pointeur vers une valeur [SystemHealthEntityCount](nap-datatypes.md) qui spécifie le nombre de validateurs d’intégrité du système installés dans *IDS*.</span><span class="sxs-lookup"><span data-stu-id="34243-112">A pointer to a [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of installed SHVs in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="34243-113">*ID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="34243-113">*ids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34243-114">Pointeur vers un tableau de valeurs [SystemHealthEntityId](nap-datatypes.md) qui contiennent les ID SHV installés.</span><span class="sxs-lookup"><span data-stu-id="34243-114">A pointer to an array of [SystemHealthEntityId](nap-datatypes.md) values that contain the installed SHV IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34243-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="34243-115">Return value</span></span>

<span data-ttu-id="34243-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="34243-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="34243-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="34243-117">Return code</span></span>                                                                                   | <span data-ttu-id="34243-118">Description</span><span class="sxs-lookup"><span data-stu-id="34243-118">Description</span></span>                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="34243-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="34243-119"><dt>**S\_OK** </dt></span></span> </dl>         | <span data-ttu-id="34243-120">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="34243-120">Operation succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="34243-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="34243-121"><dt>**E\_INVALIDARG** </dt></span></span> </dl> | <span data-ttu-id="34243-122">Un argument non valide a été passé à la méthode.</span><span class="sxs-lookup"><span data-stu-id="34243-122">An invalid argument was passed to the method.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="34243-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34243-123">Requirements</span></span>



| <span data-ttu-id="34243-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34243-124">Requirement</span></span> | <span data-ttu-id="34243-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="34243-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34243-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34243-126">Minimum supported client</span></span><br/> | <span data-ttu-id="34243-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34243-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="34243-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="34243-128">Minimum supported server</span></span><br/> | <span data-ttu-id="34243-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="34243-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="34243-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="34243-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="34243-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="34243-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="34243-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="34243-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="34243-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="34243-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="34243-134">DLL</span><span class="sxs-lookup"><span data-stu-id="34243-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34243-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34243-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="34243-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34243-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34243-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="34243-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





