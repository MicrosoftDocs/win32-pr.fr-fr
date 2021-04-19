---
title: INapComponentInfo GetDescription, méthode (NapCommon. h)
description: Est utilisé par le système NAP pour obtenir la description d’un client d’intégrité.
ms.assetid: f8d1d5ea-0de6-426d-90eb-b035b5bd0bfd
keywords:
- GetDescription, méthode NAP
- GetDescription, méthode NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, GetDescription, méthode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetDescription
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 499aee6f7805925cc68c08b580db7b1b72763165
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511347"
---
# <a name="inapcomponentinfogetdescription-method"></a><span data-ttu-id="0cfed-106">INapComponentInfo :: GetDescription, méthode</span><span class="sxs-lookup"><span data-stu-id="0cfed-106">INapComponentInfo::GetDescription method</span></span>

> [!Note]  
> <span data-ttu-id="0cfed-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="0cfed-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0cfed-108">La méthode de rappel **INapComponentInfo :: GetDescription** est utilisée par le système NAP pour obtenir la description d’un client d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="0cfed-108">The **INapComponentInfo::GetDescription** callback method is used by the NAP System to get the description of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cfed-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0cfed-109">Syntax</span></span>


```C++
HRESULT GetDescription(
  [out] MessageId *description
);
```



## <a name="parameters"></a><span data-ttu-id="0cfed-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0cfed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cfed-111">*Description* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0cfed-111">*description* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfed-112">Pointeur vers un [**MessageID**](nap-datatypes.md) qui contient l’ID de ressource de la description.</span><span class="sxs-lookup"><span data-stu-id="0cfed-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the description.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cfed-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0cfed-113">Return value</span></span>

<span data-ttu-id="0cfed-114">Retournez l’un de ces codes d’erreur en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="0cfed-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="0cfed-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0cfed-115">Return code</span></span>                                                                                     | <span data-ttu-id="0cfed-116">Description</span><span class="sxs-lookup"><span data-stu-id="0cfed-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0cfed-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0cfed-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0cfed-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0cfed-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="0cfed-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0cfed-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0cfed-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="0cfed-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0cfed-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0cfed-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0cfed-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0cfed-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0cfed-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0cfed-123">Requirements</span></span>



| <span data-ttu-id="0cfed-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0cfed-124">Requirement</span></span> | <span data-ttu-id="0cfed-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0cfed-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cfed-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cfed-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0cfed-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cfed-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0cfed-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0cfed-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0cfed-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0cfed-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0cfed-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="0cfed-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0cfed-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0cfed-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="0cfed-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="0cfed-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0cfed-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0cfed-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cfed-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cfed-134">See also</span></span>

<dl> <span data-ttu-id="0cfed-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="0cfed-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="0cfed-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="0cfed-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





