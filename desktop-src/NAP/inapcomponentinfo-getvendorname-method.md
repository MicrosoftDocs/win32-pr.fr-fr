---
title: Méthode INapComponentInfo GetVendorName (NapCommon. h)
description: Est utilisé par le système NAP pour obtenir le nom du fournisseur d’un client d’intégrité.
ms.assetid: 7083b0b6-38fc-4c24-a5f7-fe0a1ebd5e88
keywords:
- Méthode GetVendorName NAP
- Méthode GetVendorName NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, méthode GetVendorName
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVendorName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3c82f4e7e4f76d827e71421c467a8a223428a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467070"
---
# <a name="inapcomponentinfogetvendorname-method"></a><span data-ttu-id="8fe61-106">INapComponentInfo :: GetVendorName, méthode</span><span class="sxs-lookup"><span data-stu-id="8fe61-106">INapComponentInfo::GetVendorName method</span></span>

> [!Note]  
> <span data-ttu-id="8fe61-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="8fe61-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8fe61-108">La méthode de rappel **INapComponentInfo :: GetVendorName** est utilisée par le système NAP pour obtenir le nom du fournisseur d’un client d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="8fe61-108">The **INapComponentInfo::GetVendorName** callback method is used by the NAP System to get the vendor name of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fe61-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fe61-109">Syntax</span></span>


```C++
HRESULT GetVendorName(
  [out] MessageId *vendorName
);
```



## <a name="parameters"></a><span data-ttu-id="8fe61-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fe61-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe61-111">*NomFournisseur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8fe61-111">*vendorName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fe61-112">Pointeur vers un [**MessageID**](nap-datatypes.md) qui contient l’ID de ressource du nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="8fe61-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the vendor name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fe61-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8fe61-113">Return value</span></span>

<span data-ttu-id="8fe61-114">Retournez l’un de ces codes d’erreur en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="8fe61-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="8fe61-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8fe61-115">Return code</span></span>                                                                                     | <span data-ttu-id="8fe61-116">Description</span><span class="sxs-lookup"><span data-stu-id="8fe61-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8fe61-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8fe61-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="8fe61-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="8fe61-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="8fe61-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8fe61-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="8fe61-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="8fe61-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="8fe61-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8fe61-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="8fe61-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="8fe61-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8fe61-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fe61-123">Requirements</span></span>



| <span data-ttu-id="8fe61-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fe61-124">Requirement</span></span> | <span data-ttu-id="8fe61-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fe61-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe61-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe61-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8fe61-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fe61-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8fe61-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fe61-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8fe61-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fe61-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8fe61-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="8fe61-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fe61-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fe61-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="8fe61-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="8fe61-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8fe61-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8fe61-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe61-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fe61-134">See also</span></span>

<dl> <span data-ttu-id="8fe61-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="8fe61-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="8fe61-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="8fe61-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





