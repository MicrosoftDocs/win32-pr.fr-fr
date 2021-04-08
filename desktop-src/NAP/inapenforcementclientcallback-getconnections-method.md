---
title: Méthode INapEnforcementClientCallback GetConnections (NapEnforcementClient. h)
description: Est appelé par le NapAgent et implémenté par le client de mise en œuvre pour retourner un ensemble de connexions.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- Méthode GetConnections NAP
- Méthode GetConnections NAP, interface INapEnforcementClientCallback
- INapEnforcementClientCallback interface NAP, méthode GetConnections
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acdc68dbc69cabe710414f3fa2501585f3e384e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844354"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a><span data-ttu-id="a91ca-106">INapEnforcementClientCallback :: GetConnections, méthode</span><span class="sxs-lookup"><span data-stu-id="a91ca-106">INapEnforcementClientCallback::GetConnections method</span></span>

> [!Note]  
> <span data-ttu-id="a91ca-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a91ca-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a91ca-108">La méthode de rappel **INapEnforcementClientCallback :: GetConnections** est appelée par le NapAgent et implémentée par le client de mise en œuvre pour retourner un ensemble de connexions.</span><span class="sxs-lookup"><span data-stu-id="a91ca-108">The **INapEnforcementClientCallback::GetConnections** callback method is called by the NapAgent and implemented by the enforcement client to return a set of connections.</span></span>

## <a name="syntax"></a><span data-ttu-id="a91ca-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a91ca-109">Syntax</span></span>


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a><span data-ttu-id="a91ca-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a91ca-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a91ca-111">*connexions* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a91ca-111">*connections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a91ca-112">Pointeur vers l’ensemble actuel de [**connexions**](connections-struct.md)gérées.</span><span class="sxs-lookup"><span data-stu-id="a91ca-112">A pointer to the current set of maintained [**Connections**](connections-struct.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a91ca-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a91ca-113">Return value</span></span>

<span data-ttu-id="a91ca-114">Cette méthode de rappel doit retourner l’un des codes d’erreur suivants.</span><span class="sxs-lookup"><span data-stu-id="a91ca-114">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="a91ca-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a91ca-115">Return code</span></span>                                                                                                | <span data-ttu-id="a91ca-116">Description</span><span class="sxs-lookup"><span data-stu-id="a91ca-116">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a91ca-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a91ca-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="a91ca-118">Retourne cette valeur si l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a91ca-118">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="a91ca-119"><dt>**\_serveur RPC \_ S \_ non disponible**</dt></span><span class="sxs-lookup"><span data-stu-id="a91ca-119"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="a91ca-120">Si cette valeur est retournée, l’application est supprimée de la liste de l’algorithme de hachage des transactions et l’entrée de cache NapAgent correspondante est vidée.</span><span class="sxs-lookup"><span data-stu-id="a91ca-120">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="a91ca-121">L’algorithme SHA défaillant peut alors se réinitialiser avec NapAgent.</span><span class="sxs-lookup"><span data-stu-id="a91ca-121">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a91ca-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a91ca-122">Requirements</span></span>



| <span data-ttu-id="a91ca-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a91ca-123">Requirement</span></span> | <span data-ttu-id="a91ca-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a91ca-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a91ca-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a91ca-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a91ca-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a91ca-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a91ca-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a91ca-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a91ca-128">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a91ca-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a91ca-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="a91ca-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a91ca-130"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a91ca-130"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a91ca-131">MIDL</span><span class="sxs-lookup"><span data-stu-id="a91ca-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a91ca-132"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a91ca-132"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a91ca-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a91ca-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a91ca-134">**INapEnforcementClientCallback**</span><span class="sxs-lookup"><span data-stu-id="a91ca-134">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





