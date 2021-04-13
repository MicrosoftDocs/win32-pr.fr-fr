---
title: INapComponentInfo GetVersion, méthode (NapCommon. h)
description: Est utilisé par le système NAP pour obtenir la version d’un client de contrôle d’intégrité.
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- Méthode GetVersion NAP
- GetVersion, méthode NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, GetVersion, méthode
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVersion
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa1d62c22acf778430bfc2f9dc0e969887c7b306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519178"
---
# <a name="inapcomponentinfogetversion-method"></a><span data-ttu-id="983d5-106">INapComponentInfo :: GetVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="983d5-106">INapComponentInfo::GetVersion method</span></span>

> [!Note]  
> <span data-ttu-id="983d5-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="983d5-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="983d5-108">La méthode de rappel **INapComponentInfo :: GetVersion** est utilisée par le système NAP pour obtenir la version d’un client de contrôle d’intégrité.</span><span class="sxs-lookup"><span data-stu-id="983d5-108">The **INapComponentInfo::GetVersion** callback method is used by the NAP System to get the version of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="983d5-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="983d5-109">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a><span data-ttu-id="983d5-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="983d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="983d5-111">*version* \[ de à\]</span><span class="sxs-lookup"><span data-stu-id="983d5-111">*version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="983d5-112">Pointeur vers un [**MessageID**](nap-datatypes.md) qui contient l’ID de ressource de la version.</span><span class="sxs-lookup"><span data-stu-id="983d5-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="983d5-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="983d5-113">Return value</span></span>

<span data-ttu-id="983d5-114">Retournez l’un de ces codes d’erreur en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="983d5-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="983d5-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="983d5-115">Return code</span></span>                                                                                     | <span data-ttu-id="983d5-116">Description</span><span class="sxs-lookup"><span data-stu-id="983d5-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="983d5-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="983d5-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="983d5-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="983d5-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="983d5-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="983d5-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="983d5-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="983d5-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="983d5-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="983d5-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="983d5-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="983d5-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="983d5-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="983d5-123">Requirements</span></span>



| <span data-ttu-id="983d5-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="983d5-124">Requirement</span></span> | <span data-ttu-id="983d5-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="983d5-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="983d5-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="983d5-126">Minimum supported client</span></span><br/> | <span data-ttu-id="983d5-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="983d5-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="983d5-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="983d5-128">Minimum supported server</span></span><br/> | <span data-ttu-id="983d5-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="983d5-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="983d5-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="983d5-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="983d5-131"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="983d5-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="983d5-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="983d5-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="983d5-133"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="983d5-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="983d5-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="983d5-134">See also</span></span>

<dl> <span data-ttu-id="983d5-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="983d5-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="983d5-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="983d5-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





