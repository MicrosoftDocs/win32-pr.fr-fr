---
description: La fonction AuthzGetCentralAccessPolicyCallback est une fonction définie par l’application qui récupère la stratégie d’accès centralisée. AuthzGetCentralAccessPolicyCallback est un espace réservé pour le nom de la fonction définie par l’application.
ms.assetid: 1D5831EF-ACA8-4EE9-A7C1-E1A3CB74CEC0
title: AuthzGetCentralAccessPolicyCallback fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzGetCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b96832fa647fde920a70ac3d6608c8ebb0048892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524742"
---
# <a name="authzgetcentralaccesspolicycallback-callback-function"></a><span data-ttu-id="0dc1d-104">AuthzGetCentralAccessPolicyCallback fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="0dc1d-104">AuthzGetCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="0dc1d-105">La fonction *AuthzGetCentralAccessPolicyCallback* est une fonction définie par l’application qui récupère la stratégie d’accès centralisée.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-105">The *AuthzGetCentralAccessPolicyCallback* function is an application-defined function that retrieves the central access policy.</span></span> <span data-ttu-id="0dc1d-106">*AuthzGetCentralAccessPolicyCallback* est un espace réservé pour le nom de la fonction définie par l’application.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-106">*AuthzGetCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dc1d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0dc1d-107">Syntax</span></span>


```C++
BOOL CALLBACK AuthzGetCentralAccessPolicyCallback (
  _In_     AUTHZ_CLIENT_CONTEXT_HANDLE hAuthzClientContext,
  _In_     PSID                        capid,
  _In_opt_ PVOID                       pArgs,
  _Out_    PBOOL                       pCentralAccessPolicyApplicable,
  _Out_    PVOID                       ppCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="0dc1d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0dc1d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dc1d-109">*hAuthzClientContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0dc1d-109">*hAuthzClientContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc1d-110">Handle vers le contexte client.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-110">Handle to the client context.</span></span>

</dd> <dt>

<span data-ttu-id="0dc1d-111">*capid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0dc1d-111">*capid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc1d-112">ID de la stratégie d’accès centralisée à récupérer.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-112">ID of the central access policy to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="0dc1d-113">*pArgs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0dc1d-113">*pArgs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc1d-114">Arguments facultatifs passés à la fonction [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) via le membre **OptionalArguments** de la structure [**de \_ \_ demande d’accès auth**](/windows/desktop/api/Authz/ns-authz-authz_access_request) .</span><span class="sxs-lookup"><span data-stu-id="0dc1d-114">Optional arguments that were passed to the [**AuthzAccessCheck**](/windows/desktop/api/Authz/nf-authz-authzaccesscheck) function through the **OptionalArguments** member of the [**AUTHZ\_ACCESS\_REQUEST**](/windows/desktop/api/Authz/ns-authz-authz_access_request) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0dc1d-115">*pCentralAccessPolicyApplicable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0dc1d-115">*pCentralAccessPolicyApplicable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc1d-116">Pointeur vers une valeur booléenne que le gestionnaire de ressources utilise pour indiquer si une stratégie d’accès centralisée doit être utilisée pendant l’évaluation de l’accès.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-116">Pointer to a Boolean value that the resource manager uses to indicate whether a central access policy should be used during access evaluation.</span></span>

</dd> <dt>

<span data-ttu-id="0dc1d-117">*ppCentralAccessPolicy* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0dc1d-117">*ppCentralAccessPolicy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dc1d-118">Pointeur vers la stratégie d’accès centralisée (CAP) à utiliser pour l’évaluation de l’accès.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-118">Pointer to the central access policy (CAP) to be used for evaluating access.</span></span> <span data-ttu-id="0dc1d-119">Si cette valeur est **null**, l’extrémité par défaut est appliquée.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-119">If this value is **NULL**, the default CAP is applied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dc1d-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0dc1d-120">Return value</span></span>

<span data-ttu-id="0dc1d-121">Si la fonction est réussie, la fonction retourne **true**.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-121">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="0dc1d-122">Si la fonction ne peut pas effectuer l’évaluation, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-122">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="0dc1d-123">Utilisez [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour renvoyer une erreur à la fonction de vérification d’accès.</span><span class="sxs-lookup"><span data-stu-id="0dc1d-123">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc1d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0dc1d-124">Requirements</span></span>



| <span data-ttu-id="0dc1d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0dc1d-125">Requirement</span></span> | <span data-ttu-id="0dc1d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0dc1d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="0dc1d-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dc1d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0dc1d-128">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dc1d-128">Windows 8 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0dc1d-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dc1d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0dc1d-130">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dc1d-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                   |
| <span data-ttu-id="0dc1d-131">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="0dc1d-131">Redistributable</span></span><br/>          | <span data-ttu-id="0dc1d-132">Pack des outils d’administration Windows Server 2003 sur Windows XP</span><span class="sxs-lookup"><span data-stu-id="0dc1d-132">Windows Server 2003 Administration Tools Pack on Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0dc1d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dc1d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dc1d-134">**\_demande d’accès à auth. \_**</span><span class="sxs-lookup"><span data-stu-id="0dc1d-134">**AUTHZ\_ACCESS\_REQUEST**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_access_request)
</dt> <dt>

[<span data-ttu-id="0dc1d-135">**\_informations d’initialisation authment \_**</span><span class="sxs-lookup"><span data-stu-id="0dc1d-135">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="0dc1d-136">**AuthzAccessCheck**</span><span class="sxs-lookup"><span data-stu-id="0dc1d-136">**AuthzAccessCheck**</span></span>](/windows/desktop/api/Authz/nf-authz-authzaccesscheck)
</dt> </dl>

 

