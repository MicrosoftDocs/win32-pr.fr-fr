---
title: Méthode INapComponentInfo GetFriendlyName (NapCommon. h)
description: Est utilisé par le système NAP pour obtenir le nom convivial d’un client d’intégrité.
ms.assetid: 28614f06-a250-4f92-abf2-422675efd8a0
keywords:
- Méthode GetFriendlyName NAP
- Méthode GetFriendlyName NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, méthode GetFriendlyName
topic_type:
- apiref
api_name:
- INapComponentInfo.GetFriendlyName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3848f8fb8365f91bceb5a44c498578f04a1776b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466774"
---
# <a name="inapcomponentinfogetfriendlyname-method"></a><span data-ttu-id="1112e-106">INapComponentInfo :: GetFriendlyName, méthode</span><span class="sxs-lookup"><span data-stu-id="1112e-106">INapComponentInfo::GetFriendlyName method</span></span>

> [!Note]  
> <span data-ttu-id="1112e-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1112e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1112e-108">La méthode de rappel **INapComponentInfo :: GetFriendlyName** est utilisée par le système NAP pour obtenir le nom convivial d’un client d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="1112e-108">The **INapComponentInfo::GetFriendlyName** callback method is used by the NAP System to get the friendly name of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="1112e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1112e-109">Syntax</span></span>


```C++
HRESULT GetFriendlyName(
  [out] MessageId *friendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="1112e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1112e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1112e-111">*FriendlyName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1112e-111">*friendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1112e-112">Pointeur vers un [**MessageID**](nap-datatypes.md) qui contient l’ID de ressource du nom convivial.</span><span class="sxs-lookup"><span data-stu-id="1112e-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the friendly name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1112e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1112e-113">Return value</span></span>

<span data-ttu-id="1112e-114">Retournez l’un de ces codes d’erreur en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="1112e-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="1112e-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1112e-115">Return code</span></span>                                                                                     | <span data-ttu-id="1112e-116">Description</span><span class="sxs-lookup"><span data-stu-id="1112e-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1112e-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1112e-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1112e-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="1112e-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="1112e-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1112e-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1112e-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="1112e-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1112e-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1112e-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1112e-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="1112e-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1112e-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1112e-123">Requirements</span></span>



| <span data-ttu-id="1112e-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1112e-124">Requirement</span></span> | <span data-ttu-id="1112e-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="1112e-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1112e-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1112e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1112e-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1112e-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1112e-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1112e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1112e-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1112e-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1112e-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="1112e-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1112e-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1112e-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="1112e-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="1112e-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1112e-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1112e-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1112e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1112e-134">See also</span></span>

<dl> <span data-ttu-id="1112e-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1112e-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="1112e-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="1112e-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





