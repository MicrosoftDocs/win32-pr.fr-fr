---
title: Méthode INapSystemHealthAgentCallback CompareSoHRequests (NapSystemHealthAgent. h)
description: Est utilisé par l’algorithme SHA pour comparer les demandes SoH.
ms.assetid: 14ba189a-e745-44b0-b729-522087d4e08b
keywords:
- Méthode CompareSoHRequests NAP
- Méthode CompareSoHRequests NAP, interface INapSystemHealthAgentCallback
- INapSystemHealthAgentCallback interface NAP, méthode CompareSoHRequests
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.CompareSoHRequests
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c6713f3de47cfbde6df67662f89ab3c094d0674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511157"
---
# <a name="inapsystemhealthagentcallbackcomparesohrequests-method"></a><span data-ttu-id="c0604-106">INapSystemHealthAgentCallback :: CompareSoHRequests, méthode</span><span class="sxs-lookup"><span data-stu-id="c0604-106">INapSystemHealthAgentCallback::CompareSoHRequests method</span></span>

> [!Note]  
> <span data-ttu-id="c0604-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="c0604-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c0604-108">La méthode **INapSystemHealthAgentCallback :: CompareSoHRequests** est utilisée par l’algorithme SHA pour comparer les demandes SOH.</span><span class="sxs-lookup"><span data-stu-id="c0604-108">The **INapSystemHealthAgentCallback::CompareSoHRequests** method is used by the SHA to compare SoH requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0604-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0604-109">Syntax</span></span>


```C++
HRESULT CompareSoHRequests(
  [in]  const SoHRequest *lhs,
  [in]  const SoHRequest *rhs,
  [out]       BOOL       *isEqual
);
```



## <a name="parameters"></a><span data-ttu-id="c0604-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0604-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0604-111">*LHS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c0604-111">*lhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0604-112">Pointeur vers le [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à gauche de l’opération de comparaison.</span><span class="sxs-lookup"><span data-stu-id="c0604-112">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the left of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="c0604-113">*RHS* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c0604-113">*rhs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0604-114">Pointeur vers le [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) à droite de l’opération de comparaison.</span><span class="sxs-lookup"><span data-stu-id="c0604-114">A pointer to the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) on the right of the comparison operation.</span></span>

</dd> <dt>

<span data-ttu-id="c0604-115">*IsEqual* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c0604-115">*isEqual* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0604-116">Pointeur vers un **booléen** qui a la **valeur true** si *LHS* et *RHS* sont sémantiquement égaux, et **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c0604-116">A pointer to a **BOOL** that is **TRUE** if *lhs* and *rhs* are semantically equal, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0604-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0604-117">Return value</span></span>

<span data-ttu-id="c0604-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="c0604-118">This method can return one of these values.</span></span>



| <span data-ttu-id="c0604-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c0604-119">Return code</span></span>                                                                               | <span data-ttu-id="c0604-120">Description</span><span class="sxs-lookup"><span data-stu-id="c0604-120">Description</span></span>                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="c0604-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c0604-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="c0604-122">Indique la réussite de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c0604-122">Indicates success.</span></span><br/>                         |
| <dl> <span data-ttu-id="c0604-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="c0604-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="c0604-124">La méthode n’a pas été implémentée par l’algorithme SHA.</span><span class="sxs-lookup"><span data-stu-id="c0604-124">The method was not implemented by the SHA.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0604-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c0604-125">Remarks</span></span>

<span data-ttu-id="c0604-126">Cette méthode de rappel est déclarée par le système NAP et doit être implémentée par l’enregistreur SHA.</span><span class="sxs-lookup"><span data-stu-id="c0604-126">This callback method is declared by the NAP system and is to be implemented by the SHA writer.</span></span>

<span data-ttu-id="c0604-127">L’algorithme SHA doit comparer le SoHs et retourner la **valeur true** si les SoHs sont sémantiquement égaux.</span><span class="sxs-lookup"><span data-stu-id="c0604-127">The SHA should compare the SoHs and return **TRUE** if the SoHs are semantically equal.</span></span> <span data-ttu-id="c0604-128">Le NapAgent utilise ces informations pour déterminer si un échange SoH doit être initié en raison de la modification de l’état de l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="c0604-128">The NapAgent uses this information to determine if an SoH exchange should be initiated due to change of state of the client machine.</span></span>

<span data-ttu-id="c0604-129">Si les Sha ont placé des ID incrémentiels ou des horodateurs dans leur SoH, les SoHs peuvent être sémantiquement égaux (c’est-à-dire qu’ils peuvent communiquer les mêmes informations d’intégrité), mais ils peuvent être inégaux en octets.</span><span class="sxs-lookup"><span data-stu-id="c0604-129">If SHAs have put incremental IDs or time-stamps into their SoH, then SoHs may be semantically equal (i.e. they may convey the same health information), but they may be byte-wise unequal.</span></span> <span data-ttu-id="c0604-130">L’SHA doit implémenter cette fonction pour vérifier l’égalité sémantique de SoHs.</span><span class="sxs-lookup"><span data-stu-id="c0604-130">SHAs should implement this function to check for semantic equality of SoHs.</span></span>

<span data-ttu-id="c0604-131">Si les utilisateurs de l’intégrité du système n’ont pas placé de datage ou d’ID dans leur SoHs, ils peuvent choisir de ne pas implémenter cette fonction et de retourner **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="c0604-131">If SHAs have not put any time-stamps or Ids into their SoHs, they may choose to not implement this function and return **E\_NOTIMPL**.</span></span> <span data-ttu-id="c0604-132">Dans ce cas, le NapAgent effectue une comparaison au niveau des octets sur [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="c0604-132">In this case, the NapAgent performs a byte-wise comparison on the [**SoHRequests**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0604-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0604-133">Requirements</span></span>



| <span data-ttu-id="c0604-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0604-134">Requirement</span></span> | <span data-ttu-id="c0604-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0604-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0604-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0604-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c0604-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0604-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c0604-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c0604-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c0604-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c0604-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c0604-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0604-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0604-141"><dt>NapSystemHealthAgent. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0604-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0604-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="c0604-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0604-143"><dt>NapSystemHealthAgent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0604-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0604-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0604-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0604-145">**INapSystemHealthAgentCallback**</span><span class="sxs-lookup"><span data-stu-id="c0604-145">**INapSystemHealthAgentCallback**</span></span>](inapsystemhealthagentcallback.md)
</dt> <dt>

[<span data-ttu-id="c0604-146">**Intégrité**</span><span class="sxs-lookup"><span data-stu-id="c0604-146">**SoH**</span></span>](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> </dl>

 

 





