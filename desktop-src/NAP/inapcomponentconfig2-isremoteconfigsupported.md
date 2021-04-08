---
title: Méthode INapComponentConfig2 IsRemoteConfigSupported (NapCommon. h)
description: Est implémenté par les validateurs d’intégrité système (SHV) pour indiquer si la configuration distante est prise en charge.
ms.assetid: c4b8e60b-ed60-49ec-b4d6-4e1575e4d1a5
keywords:
- Méthode IsRemoteConfigSupported NAP
- Méthode IsRemoteConfigSupported NAP, interface INapComponentConfig2
- INapComponentConfig2 interface NAP, méthode IsRemoteConfigSupported
topic_type:
- apiref
api_name:
- INapComponentConfig2.IsRemoteConfigSupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d144926aafff6f5ad7e243efe2a81a2955f497
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941923"
---
# <a name="inapcomponentconfig2isremoteconfigsupported-method"></a><span data-ttu-id="b2e0c-106">INapComponentConfig2 :: IsRemoteConfigSupported, méthode</span><span class="sxs-lookup"><span data-stu-id="b2e0c-106">INapComponentConfig2::IsRemoteConfigSupported method</span></span>

> [!Note]  
> <span data-ttu-id="b2e0c-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="b2e0c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b2e0c-108">La méthode **IsRemoteConfigSupported** est implémentée par les validateurs d’intégrité système (SHV) pour indiquer si la configuration distante est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b2e0c-108">The **IsRemoteConfigSupported** method is implemented by system health validators (SHVs) to indicate whether remote configuration is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e0c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b2e0c-109">Syntax</span></span>


```C++
HRESULT IsRemoteConfigSupported(
  [out] BOOL  *isSupported,
  [out] UINT8 *remoteConfigType
);
```



## <a name="parameters"></a><span data-ttu-id="b2e0c-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2e0c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2e0c-111">*IsSupported* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b2e0c-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2e0c-112">Pointeur vers un booléen dont la valeur est **true** si le composant prend en charge la configuration distante, et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b2e0c-112">A pointer to a BOOL that is set to **TRUE** if the component supports remote configuration, and **FALSE** if it does not.</span></span>

</dd> <dt>

<span data-ttu-id="b2e0c-113">*remoteConfigType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b2e0c-113">*remoteConfigType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2e0c-114">Indique le type de configuration à distance pris en charge à l’aide de la valeur de l’énumération [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) :</span><span class="sxs-lookup"><span data-stu-id="b2e0c-114">Indicates the type of remote configuration supported using value from the [**RemoteConfigurationType**](/windows/win32/api/naptypes/ne-naptypes-remoteconfigurationtype) enumeration:</span></span>



| <span data-ttu-id="b2e0c-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2e0c-115">Value</span></span>                                                                                                 | <span data-ttu-id="b2e0c-116">Signification</span><span class="sxs-lookup"><span data-stu-id="b2e0c-116">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b2e0c-117"><dt>remoteConfigTypeMachine</dt></span><span class="sxs-lookup"><span data-stu-id="b2e0c-117"><dt>remoteConfigTypeMachine</dt></span></span> </dl>    | <span data-ttu-id="b2e0c-118">[**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) est implémenté.</span><span class="sxs-lookup"><span data-stu-id="b2e0c-118">[**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) is implemented.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="b2e0c-119"><dt>remoteConfigTypeConfigBlob</dt></span><span class="sxs-lookup"><span data-stu-id="b2e0c-119"><dt>remoteConfigTypeConfigBlob</dt></span></span> </dl> | <span data-ttu-id="b2e0c-120">[**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) est implémenté.</span><span class="sxs-lookup"><span data-stu-id="b2e0c-120">[**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) is implemented.</span></span> <span data-ttu-id="b2e0c-121">[**INapComponentConfig :: GetConfig**](inapcomponentconfig-getconfig.md) et [**INapComponentConfig :: setconfig**](inapcomponentconfig-setconfig.md) peuvent être appelés à distance à l’aide de DCOM.</span><span class="sxs-lookup"><span data-stu-id="b2e0c-121">[**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md) and [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md) can be called remotely using DCOM.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2e0c-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b2e0c-122">Return value</span></span>

<span data-ttu-id="b2e0c-123">Retourne S \_ OK en cas de réussite, ou l’un des codes d’erreur Windows standard.</span><span class="sxs-lookup"><span data-stu-id="b2e0c-123">Returns S\_OK if successful, or one of the standard Windows error codes.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2e0c-124">Notes</span><span class="sxs-lookup"><span data-stu-id="b2e0c-124">Remarks</span></span>

<span data-ttu-id="b2e0c-125">Si ni [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) ni [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) n’est implémentée, la configuration distante de la SHV n’est pas possible.</span><span class="sxs-lookup"><span data-stu-id="b2e0c-125">If neither [**InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md) nor [**InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md) are implemented, remote configuration of the SHV is not possible.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2e0c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2e0c-126">Requirements</span></span>



| <span data-ttu-id="b2e0c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2e0c-127">Requirement</span></span> | <span data-ttu-id="b2e0c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2e0c-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e0c-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2e0c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e0c-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2e0c-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b2e0c-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2e0c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e0c-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2e0c-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b2e0c-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2e0c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2e0c-134"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2e0c-134"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="b2e0c-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="b2e0c-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b2e0c-136"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b2e0c-136"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2e0c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2e0c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e0c-138">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="b2e0c-138">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> </dl>

 

 





