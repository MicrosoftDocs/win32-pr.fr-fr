---
description: Associe une implémentation de ITransactionProxy avec le contexte actuel.
ms.assetid: 64009632-b536-41fb-95ac-b23e2cbf18da
title: 'IContextTransactionInfo :: RegisterTransactionProxy, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.RegisterTransactionProxy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7b559453b0d4ed75f92f7a421be4c3a47e07fdf7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317933"
---
# <a name="icontexttransactioninforegistertransactionproxy-method"></a><span data-ttu-id="8fed2-103">IContextTransactionInfo :: RegisterTransactionProxy, méthode</span><span class="sxs-lookup"><span data-stu-id="8fed2-103">IContextTransactionInfo::RegisterTransactionProxy method</span></span>

<span data-ttu-id="8fed2-104">Associe une implémentation de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) avec le contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="8fed2-104">Associates an [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation with the current context.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fed2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8fed2-105">Syntax</span></span>


```C++
HRESULT RegisterTransactionProxy(
  [in]  ITransactionProxy *pProxy,
  [out] GUID              *pGuid
);
```



## <a name="parameters"></a><span data-ttu-id="8fed2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8fed2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fed2-107">*pProxy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8fed2-107">*pProxy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fed2-108">Implémentation de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) à associer au contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="8fed2-108">An [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation to associate with the current context.</span></span>

</dd> <dt>

<span data-ttu-id="8fed2-109">*pguid* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8fed2-109">*pGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fed2-110">GUID qui identifie le proxy de transaction.</span><span class="sxs-lookup"><span data-stu-id="8fed2-110">A GUID that identifies the transaction proxy.</span></span> <span data-ttu-id="8fed2-111">COM+ utilise ce GUID lors de l’appel de [**ITransactionProxy :: Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) sur le proxy de transaction.</span><span class="sxs-lookup"><span data-stu-id="8fed2-111">COM+ uses this GUID when calling [**ITransactionProxy::Commit**](/windows/desktop/api/ComSvcs/nf-comsvcs-itransactionproxy-commit) on the transaction proxy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fed2-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8fed2-112">Return value</span></span>

<span data-ttu-id="8fed2-113">Cette méthode peut retourner les valeurs de retour standard E \_ INVALIDARG, e \_ OUTOFMEMORY et e \_ inattendue, ainsi que les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="8fed2-113">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, and E\_UNEXPECTED, as well as the following values.</span></span>



| <span data-ttu-id="8fed2-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8fed2-114">Return code</span></span>                                                                                                     | <span data-ttu-id="8fed2-115">Description</span><span class="sxs-lookup"><span data-stu-id="8fed2-115">Description</span></span>                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8fed2-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8fed2-116"><dt>**S\_OK**</dt></span></span> </dl>                            | <span data-ttu-id="8fed2-117">La commande s'est correctement terminée.</span><span class="sxs-lookup"><span data-stu-id="8fed2-117">The method completed successfully.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="8fed2-118"><dt>**CONTEXTE \_ E \_ ALREADYINTRANSACTION**</dt></span><span class="sxs-lookup"><span data-stu-id="8fed2-118"><dt>**CONTEXT\_E\_ALREADYINTRANSACTION**</dt></span></span> </dl> | <span data-ttu-id="8fed2-119">Le contexte actuel est déjà associé à une implémentation de [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) .</span><span class="sxs-lookup"><span data-stu-id="8fed2-119">The current context already has an associated [**ITransactionProxy**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactionproxy) implementation.</span></span><br/> |
| <dl> <span data-ttu-id="8fed2-120"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="8fed2-120"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                       | <span data-ttu-id="8fed2-121">Le contexte actuel héberge une transaction BYOT (Bring Your Own Transaction) ou une transaction non racine.</span><span class="sxs-lookup"><span data-stu-id="8fed2-121">The current context is hosting a Bring Your Own Transaction (BYOT) transaction or a non-root transaction.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="8fed2-122">Notes</span><span class="sxs-lookup"><span data-stu-id="8fed2-122">Remarks</span></span>

<span data-ttu-id="8fed2-123">La méthode **RegisterTransactionProxy** peut uniquement être appelée si le contexte actuel est un contexte de transaction racine.</span><span class="sxs-lookup"><span data-stu-id="8fed2-123">The **RegisterTransactionProxy** method can only be called if the current context is a root transaction context.</span></span> <span data-ttu-id="8fed2-124">Il ne peut pas être appelé si le contexte héberge une transaction BYOT ou une transaction non racine.</span><span class="sxs-lookup"><span data-stu-id="8fed2-124">It cannot be called if the context is hosting a BYOT transaction or a non-root transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fed2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8fed2-125">Requirements</span></span>



| <span data-ttu-id="8fed2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8fed2-126">Requirement</span></span> | <span data-ttu-id="8fed2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8fed2-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8fed2-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fed2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="8fed2-129">Windows XP avec les \[ applications de bureau SP2 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fed2-129">Windows XP with SP2 \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8fed2-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8fed2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="8fed2-131">Windows Server 2003 avec les \[ applications de bureau SP1 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8fed2-131">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8fed2-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8fed2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fed2-133">**IContextTransactionInfo**</span><span class="sxs-lookup"><span data-stu-id="8fed2-133">**IContextTransactionInfo**</span></span>](icontexttransactioninfo.md)
</dt> </dl>

 

 




