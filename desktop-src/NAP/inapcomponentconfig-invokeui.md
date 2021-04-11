---
title: Méthode INapComponentConfig InvokeUI (NapCommon. h)
description: Lance une interface utilisateur personnalisée pour un composant de programme de validation d’intégrité système (SHV).
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- Méthode InvokeUI NAP
- Méthode InvokeUI NAP, interface INapComponentConfig
- INapComponentConfig interface NAP, méthode InvokeUI
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd86d683365286fc2130c1ac9edf21ff075d61a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941924"
---
# <a name="inapcomponentconfiginvokeui-method"></a><span data-ttu-id="19e73-106">INapComponentConfig :: InvokeUI, méthode</span><span class="sxs-lookup"><span data-stu-id="19e73-106">INapComponentConfig::InvokeUI method</span></span>

> [!Note]  
> <span data-ttu-id="19e73-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="19e73-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="19e73-108">La méthode **InvokeUI** lance une interface utilisateur personnalisée pour un composant de programme de validation d’intégrité système (SHV).</span><span class="sxs-lookup"><span data-stu-id="19e73-108">The **InvokeUI** method launches a customized user interface for a system health validator (SHV) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e73-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="19e73-109">Syntax</span></span>


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a><span data-ttu-id="19e73-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="19e73-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19e73-111">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="19e73-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19e73-112">Handle de la fenêtre parente ou propriétaire.</span><span class="sxs-lookup"><span data-stu-id="19e73-112">A handle to the parent or owner window.</span></span> <span data-ttu-id="19e73-113">Un handle de fenêtre valide doit être fourni.</span><span class="sxs-lookup"><span data-stu-id="19e73-113">A valid window handle must be supplied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19e73-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="19e73-114">Return value</span></span>

<span data-ttu-id="19e73-115">Retourne l’un des codes d’erreur suivants en fonction du résultat de cette opération.</span><span class="sxs-lookup"><span data-stu-id="19e73-115">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="19e73-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="19e73-116">Return code</span></span>                                                                                     | <span data-ttu-id="19e73-117">Description</span><span class="sxs-lookup"><span data-stu-id="19e73-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="19e73-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="19e73-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="19e73-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="19e73-119">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="19e73-120"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="19e73-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="19e73-121">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="19e73-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="19e73-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="19e73-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="19e73-123">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="19e73-123">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="19e73-124"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="19e73-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>       | <span data-ttu-id="19e73-125">Le SHV ne prend pas en charge une interface utilisateur personnalisée.</span><span class="sxs-lookup"><span data-stu-id="19e73-125">The SHV does not support a customized UI.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="19e73-126">Notes</span><span class="sxs-lookup"><span data-stu-id="19e73-126">Remarks</span></span>

<span data-ttu-id="19e73-127">Cet appel de méthode doit être bloqué jusqu’à ce que l’interface utilisateur SHV se termine.</span><span class="sxs-lookup"><span data-stu-id="19e73-127">This method call should block until the SHV user interface exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="19e73-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="19e73-128">Requirements</span></span>



| <span data-ttu-id="19e73-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="19e73-129">Requirement</span></span> | <span data-ttu-id="19e73-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="19e73-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="19e73-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19e73-131">Minimum supported client</span></span><br/> | <span data-ttu-id="19e73-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="19e73-132">None supported</span></span><br/>                                                                |
| <span data-ttu-id="19e73-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="19e73-133">Minimum supported server</span></span><br/> | <span data-ttu-id="19e73-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="19e73-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="19e73-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="19e73-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="19e73-136"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="19e73-136"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="19e73-137">MIDL</span><span class="sxs-lookup"><span data-stu-id="19e73-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19e73-138"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="19e73-138"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19e73-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19e73-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e73-140">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="19e73-140">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="19e73-141">**INapComponentConfig::IsUISupported**</span><span class="sxs-lookup"><span data-stu-id="19e73-141">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





