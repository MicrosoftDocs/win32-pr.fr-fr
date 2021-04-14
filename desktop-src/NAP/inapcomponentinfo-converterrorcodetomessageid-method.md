---
title: Méthode INapComponentInfo ConvertErrorCodeToMessageId (NapCommon. h)
description: Est utilisé par le système NAP pour demander au client d’intégrité de convertir un code d’erreur HRESULT en ID de message.
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- Méthode ConvertErrorCodeToMessageId NAP
- Méthode ConvertErrorCodeToMessageId NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, méthode ConvertErrorCodeToMessageId
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed8eee06ed6bd553ffcce68e76e375dd706238
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466775"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a><span data-ttu-id="87748-106">INapComponentInfo :: ConvertErrorCodeToMessageId, méthode</span><span class="sxs-lookup"><span data-stu-id="87748-106">INapComponentInfo::ConvertErrorCodeToMessageId method</span></span>

> [!Note]  
> <span data-ttu-id="87748-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="87748-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="87748-108">La méthode de rappel **INapComponentInfo :: ConvertErrorCodeToMessageId** est utilisée par le système NAP pour demander au client d’intégrité de convertir un code d’erreur HRESULT en ID de message.</span><span class="sxs-lookup"><span data-stu-id="87748-108">The **INapComponentInfo::ConvertErrorCodeToMessageId** callback method is used by the NAP System to request the health client convert an HRESULT error code into a message ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="87748-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87748-109">Syntax</span></span>


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a><span data-ttu-id="87748-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87748-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87748-111">*ErrorCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87748-111">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87748-112">[**Code d’erreur**](nap-error-constants.md) du système NAP qui doit être converti en **MessageID**.</span><span class="sxs-lookup"><span data-stu-id="87748-112">The [**error code**](nap-error-constants.md) from the NAP System that is to be converted into a **MessageId**.</span></span>

</dd> <dt>

<span data-ttu-id="87748-113">*ID* \[ de la à\]</span><span class="sxs-lookup"><span data-stu-id="87748-113">*msgId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87748-114">Pointeur vers un [**MessageID**](nap-datatypes.md) qui contient l’ID de ressource de la chaîne localisée correspondante.</span><span class="sxs-lookup"><span data-stu-id="87748-114">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the corresponding localized string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87748-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87748-115">Return value</span></span>

<span data-ttu-id="87748-116">Retournez l’un de ces codes d’erreur en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="87748-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="87748-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="87748-117">Return code</span></span>                                                                                     | <span data-ttu-id="87748-118">Description</span><span class="sxs-lookup"><span data-stu-id="87748-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="87748-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="87748-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="87748-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="87748-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="87748-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="87748-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="87748-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="87748-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="87748-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="87748-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="87748-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="87748-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="87748-125">Notes</span><span class="sxs-lookup"><span data-stu-id="87748-125">Remarks</span></span>

<span data-ttu-id="87748-126">Le **MessageID** retourné est utilisé par le système NAP pour récupérer une chaîne localisée.</span><span class="sxs-lookup"><span data-stu-id="87748-126">The returned **MessageId** is used by the NAP System to retrieve a localized string.</span></span>

## <a name="requirements"></a><span data-ttu-id="87748-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87748-127">Requirements</span></span>



| <span data-ttu-id="87748-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87748-128">Requirement</span></span> | <span data-ttu-id="87748-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="87748-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="87748-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87748-130">Minimum supported client</span></span><br/> | <span data-ttu-id="87748-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87748-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="87748-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87748-132">Minimum supported server</span></span><br/> | <span data-ttu-id="87748-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87748-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="87748-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="87748-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="87748-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="87748-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="87748-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="87748-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87748-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87748-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87748-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87748-138">See also</span></span>

<dl> <span data-ttu-id="87748-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="87748-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="87748-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="87748-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





