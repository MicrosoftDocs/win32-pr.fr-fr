---
title: Méthode INapComponentConfig IsUISupported (NapCommon. h)
description: Spécifie si le composant prend en charge une interface utilisateur personnalisée.
ms.assetid: 044f8014-f041-4e9c-922a-2691b799ba84
keywords:
- Méthode IsUISupported NAP
- Méthode IsUISupported NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, méthode IsUISupported
topic_type:
- apiref
api_name:
- INapComponentConfig.IsUISupported
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab7d3f6b87ba5e483b466e6746f0f63d039cb205
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509921"
---
# <a name="inapcomponentconfigisuisupported-method"></a><span data-ttu-id="e0ba3-106">INapComponentConfig :: IsUISupported, méthode</span><span class="sxs-lookup"><span data-stu-id="e0ba3-106">INapComponentConfig::IsUISupported method</span></span>

> [!Note]  
> <span data-ttu-id="e0ba3-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="e0ba3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e0ba3-108">La méthode **IsUISupported** spécifie si le composant prend en charge une interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="e0ba3-108">The **IsUISupported** method specifies whether the component supports a customized user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0ba3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0ba3-109">Syntax</span></span>


```C++
HRESULT IsUISupported(
  [out] BOOL *isSupported
) const;
```



## <a name="parameters"></a><span data-ttu-id="e0ba3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0ba3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0ba3-111">*IsSupported* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e0ba3-111">*isSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e0ba3-112">Pointeur vers un booléen dont la valeur est **true** si le composant prend en charge une interface utilisateur personnalisée et la valeur **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e0ba3-112">A pointer to a BOOL that is set to **TRUE** if the component supports a customized user interface and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0ba3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e0ba3-113">Return value</span></span>

<span data-ttu-id="e0ba3-114">Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="e0ba3-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="e0ba3-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e0ba3-115">Return code</span></span>                                                                                     | <span data-ttu-id="e0ba3-116">Description</span><span class="sxs-lookup"><span data-stu-id="e0ba3-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="e0ba3-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e0ba3-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="e0ba3-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="e0ba3-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="e0ba3-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="e0ba3-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="e0ba3-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="e0ba3-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="e0ba3-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e0ba3-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="e0ba3-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e0ba3-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e0ba3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="e0ba3-123">Remarks</span></span>

<span data-ttu-id="e0ba3-124">L’interface utilisateur personnalisée d’un composant doit être lancée à l’aide de [**INapComponentConfig :: InvokeUI**](inapcomponentconfig-invokeui.md).</span><span class="sxs-lookup"><span data-stu-id="e0ba3-124">A component's customized user interface should be launched using [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e0ba3-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e0ba3-125">Requirements</span></span>



| <span data-ttu-id="e0ba3-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e0ba3-126">Requirement</span></span> | <span data-ttu-id="e0ba3-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="e0ba3-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0ba3-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0ba3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e0ba3-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0ba3-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e0ba3-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e0ba3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e0ba3-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e0ba3-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e0ba3-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e0ba3-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0ba3-133"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0ba3-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0ba3-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="e0ba3-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e0ba3-135"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e0ba3-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0ba3-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e0ba3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0ba3-137">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="e0ba3-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="e0ba3-138">**INapComponentConfig::InvokeUI**</span><span class="sxs-lookup"><span data-stu-id="e0ba3-138">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)
</dt> </dl>

 

 





