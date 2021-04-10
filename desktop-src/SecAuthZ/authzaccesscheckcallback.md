---
description: Fonction définie par l’application qui gère les entrées de contrôle d’accès (ACE) de rappel au cours d’une vérification d’accès.
ms.assetid: e8a510e6-0739-4765-ad07-3bcb1b9c905c
title: AuthzAccessCheckCallback fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzAccessCheckCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 82e100092dd7c59e9cc689aa8723365fae8bed29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104211084"
---
# <a name="authzaccesscheckcallback-callback-function"></a><span data-ttu-id="005d8-103">AuthzAccessCheckCallback fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="005d8-103">AuthzAccessCheckCallback callback function</span></span>

<span data-ttu-id="005d8-104">La fonction **AuthzAccessCheckCallback** est une fonction définie par l’application qui gère les [*entrées de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) (ACE) de rappel au cours d’une vérification d’accès.</span><span class="sxs-lookup"><span data-stu-id="005d8-104">The **AuthzAccessCheckCallback** function is an application-defined function that handles callback [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) during an access check.</span></span> <span data-ttu-id="005d8-105">**AuthzAccessCheckCallback** est un espace réservé pour le nom de la fonction définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="005d8-105">**AuthzAccessCheckCallback** is a placeholder for the application-defined function name.</span></span> <span data-ttu-id="005d8-106">L’application inscrit ce rappel en appelant [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span><span class="sxs-lookup"><span data-stu-id="005d8-106">The application registers this callback by calling [**AuthzInitializeResourceManager**](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager).</span></span>

## <a name="syntax"></a><span data-ttu-id="005d8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="005d8-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzAccessCheckCallback(
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PACE_HEADER                 pAce,
  _In_opt_ PVOID                       pArgs,
  _Inout_  PBOOL                       pbAceApplicable
);
```



## <a name="parameters"></a><span data-ttu-id="005d8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="005d8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="005d8-109">*hAuthzClientContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="005d8-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="005d8-110">Handle d’un contexte client.</span><span class="sxs-lookup"><span data-stu-id="005d8-110">A handle to a client context.</span></span>

</dd> <dt>

<span data-ttu-id="005d8-111">*rythme* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="005d8-111">*pAce* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="005d8-112">Pointeur vers l’entrée du contrôle d’accès à évaluer pour l’inclusion dans l’appel à la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) .</span><span class="sxs-lookup"><span data-stu-id="005d8-112">A pointer to the ACE to evaluate for inclusion in the call to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function.</span></span>

</dd> <dt>

<span data-ttu-id="005d8-113">*pArgs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="005d8-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="005d8-114">Données passées dans le paramètre *DynamicGroupArgs* de l’appel à [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) ou [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).</span><span class="sxs-lookup"><span data-stu-id="005d8-114">Data passed in the *DynamicGroupArgs* parameter of the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) or [**AuthzCachedAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck).</span></span>

</dd> <dt>

<span data-ttu-id="005d8-115">*pbAceApplicable* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="005d8-115">*pbAceApplicable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="005d8-116">Pointeur vers une variable booléenne qui reçoit les résultats de l’évaluation de la logique définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="005d8-116">A pointer to a Boolean variable that receives the results of the evaluation of the logic defined by the application.</span></span>

<span data-ttu-id="005d8-117">Les résultats sont **vrais** si la logique détermine que l’entrée du contrôle d’accès est applicable et sera incluse dans l’appel à [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); dans le cas contraire, les résultats sont **false**.</span><span class="sxs-lookup"><span data-stu-id="005d8-117">The results are **TRUE** if the logic determines that the ACE is applicable and will be included in the call to [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck); otherwise, the results are **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="005d8-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="005d8-118">Return value</span></span>

<span data-ttu-id="005d8-119">Si la fonction est réussie, la fonction retourne **true**.</span><span class="sxs-lookup"><span data-stu-id="005d8-119">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="005d8-120">Si la fonction ne peut pas effectuer l’évaluation, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="005d8-120">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="005d8-121">Utilisez [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour renvoyer une erreur à la fonction de vérification d’accès.</span><span class="sxs-lookup"><span data-stu-id="005d8-121">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="remarks"></a><span data-ttu-id="005d8-122">Notes</span><span class="sxs-lookup"><span data-stu-id="005d8-122">Remarks</span></span>

<span data-ttu-id="005d8-123">Les variables d’attribut de sécurité doivent être présentes dans le contexte client si elles sont référencées dans une expression conditionnelle ; sinon, le terme d’expression conditionnelle qui les référence prend la valeur Unknown.</span><span class="sxs-lookup"><span data-stu-id="005d8-123">Security attribute variables must be present in the client context if referred to in a conditional expression, otherwise the conditional expression term referencing them will evaluate to unknown.</span></span>

<span data-ttu-id="005d8-124">Pour plus d’informations, consultez la vue d’ensemble du [fonctionnement de AccessCheck](how-dacls-control-access-to-an-object.md) et de la [stratégie d’autorisation centralisée](centralized-authorization-policy.md) .</span><span class="sxs-lookup"><span data-stu-id="005d8-124">For more information, see the [How AccessCheck Works](how-dacls-control-access-to-an-object.md) and [Centralized Authorization Policy](centralized-authorization-policy.md) overviews.</span></span>

## <a name="requirements"></a><span data-ttu-id="005d8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="005d8-125">Requirements</span></span>



| <span data-ttu-id="005d8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="005d8-126">Requirement</span></span> | <span data-ttu-id="005d8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="005d8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="005d8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="005d8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="005d8-129">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="005d8-129">Windows XP \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="005d8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="005d8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="005d8-131">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="005d8-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="005d8-132">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="005d8-132">Redistributable</span></span><br/>          | <span data-ttu-id="005d8-133">Pack des outils d’administration Windows Server 2003 sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="005d8-133">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="005d8-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="005d8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="005d8-135">Fonctions de base Access Control</span><span class="sxs-lookup"><span data-stu-id="005d8-135">Basic Access Control Functions</span></span>](authorization-functions.md)
</dt> <dt>

[<span data-ttu-id="005d8-136">Stratégie d’autorisation centralisée</span><span class="sxs-lookup"><span data-stu-id="005d8-136">Centralized Authorization Policy</span></span>](centralized-authorization-policy.md)
</dt> <dt>

[<span data-ttu-id="005d8-137">Fonctionnement de AccessCheck</span><span class="sxs-lookup"><span data-stu-id="005d8-137">How AccessCheck Works</span></span>](how-dacls-control-access-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="005d8-138">**AuthzAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="005d8-138">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> <dt>

[<span data-ttu-id="005d8-139">**AuthzCachedAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="005d8-139">**AuthzCachedAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzcachedaccesscheck)
</dt> <dt>

[<span data-ttu-id="005d8-140">**AuthzInitializeRemoteResourceManager**</span><span class="sxs-lookup"><span data-stu-id="005d8-140">**AuthzInitializeRemoteResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeremoteresourcemanager)
</dt> <dt>

[<span data-ttu-id="005d8-141">**AuthzInitializeResourceManager**</span><span class="sxs-lookup"><span data-stu-id="005d8-141">**AuthzInitializeResourceManager**</span></span>](/windows/desktop/api/Authz/nf-authz-authzinitializeresourcemanager)
</dt> </dl>

 

