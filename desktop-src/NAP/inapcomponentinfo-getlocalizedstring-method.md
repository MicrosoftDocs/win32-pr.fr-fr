---
title: Méthode INapComponentInfo GetLocalizedString (NapCommon. h)
description: Est utilisé par le système NAP pour récupérer les chaînes localisées.
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- Méthode GetLocalizedString NAP
- Méthode GetLocalizedString NAP, interface INapComponentInfo
- INapComponentInfo interface NAP, méthode GetLocalizedString
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781e4e8c93f58039c72a98f40a529243e5722d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942892"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a><span data-ttu-id="65de2-106">INapComponentInfo :: GetLocalizedString, méthode</span><span class="sxs-lookup"><span data-stu-id="65de2-106">INapComponentInfo::GetLocalizedString method</span></span>

> [!Note]  
> <span data-ttu-id="65de2-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="65de2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="65de2-108">La méthode de rappel **INapComponentInfo :: GetLocalizedString** est utilisée par le système NAP pour récupérer les chaînes localisées.</span><span class="sxs-lookup"><span data-stu-id="65de2-108">The **INapComponentInfo::GetLocalizedString** callback method is used by the NAP System to get localized strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="65de2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65de2-109">Syntax</span></span>


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a><span data-ttu-id="65de2-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65de2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65de2-111">*ID* \[ de la dans\]</span><span class="sxs-lookup"><span data-stu-id="65de2-111">*msgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65de2-112">[**MessageID**](nap-datatypes.md) qui contient l’ID de ressource de la chaîne à localiser.</span><span class="sxs-lookup"><span data-stu-id="65de2-112">A [**MessageId**](nap-datatypes.md) that contains the resource ID of the string to localize.</span></span>

</dd> <dt>

<span data-ttu-id="65de2-113">*chaîne* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="65de2-113">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65de2-114">Pointeur vers un pointeur vers un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient la version localisée du message.</span><span class="sxs-lookup"><span data-stu-id="65de2-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the localized version of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65de2-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65de2-115">Return value</span></span>

<span data-ttu-id="65de2-116">Retournez l’un de ces codes d’erreur en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="65de2-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="65de2-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="65de2-117">Return code</span></span>                                                                                     | <span data-ttu-id="65de2-118">Description</span><span class="sxs-lookup"><span data-stu-id="65de2-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="65de2-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="65de2-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="65de2-120">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="65de2-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="65de2-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="65de2-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="65de2-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="65de2-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="65de2-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="65de2-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="65de2-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="65de2-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="65de2-125">Notes</span><span class="sxs-lookup"><span data-stu-id="65de2-125">Remarks</span></span>

<span data-ttu-id="65de2-126">Les chaînes doivent être localisées en fonction de l’ID de langue du thread appelant.</span><span class="sxs-lookup"><span data-stu-id="65de2-126">Strings should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="65de2-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65de2-127">Requirements</span></span>



| <span data-ttu-id="65de2-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65de2-128">Requirement</span></span> | <span data-ttu-id="65de2-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="65de2-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="65de2-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65de2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="65de2-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65de2-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="65de2-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65de2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="65de2-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65de2-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="65de2-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="65de2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="65de2-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="65de2-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="65de2-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="65de2-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="65de2-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="65de2-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65de2-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65de2-138">See also</span></span>

<dl> <span data-ttu-id="65de2-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="65de2-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="65de2-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="65de2-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





