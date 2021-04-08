---
description: Fournit l’accès à une collection d’informations de sécurité représentant l’identité d’un appelant. À l’aide de cette classe, vous pouvez trouver des informations sur un appelant particulier dans une chaîne d’appelants qui fait partie du contexte de l’appel de sécurité.
ms.assetid: c6b28695-1b08-490a-8d56-eb55d82f3e7a
title: SecurityIdentity, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityIdentity
api_type:
- COM
ms.openlocfilehash: 6775c06bc25bfb32a1c2c247868fd2a9fbc9aade
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103761557"
---
# <a name="securityidentity-class"></a><span data-ttu-id="1f60d-104">SecurityIdentity, classe</span><span class="sxs-lookup"><span data-stu-id="1f60d-104">SecurityIdentity class</span></span>

<span data-ttu-id="1f60d-105">Fournit l’accès à une collection d’informations de sécurité représentant l’identité d’un appelant.</span><span class="sxs-lookup"><span data-stu-id="1f60d-105">Provides access to a collection of security information representing a caller's identity.</span></span> <span data-ttu-id="1f60d-106">À l’aide de cette classe, vous pouvez trouver des informations sur un appelant particulier dans une chaîne d’appelants qui fait partie du contexte de l’appel de sécurité.</span><span class="sxs-lookup"><span data-stu-id="1f60d-106">Using this class, you can find out about a particular caller in a chain of callers that is part of the security call context.</span></span> <span data-ttu-id="1f60d-107">Pour plus d’informations sur la façon dont les informations de contexte de l’appel de sécurité sont accessibles, consultez sécurité des composants de programmation.</span><span class="sxs-lookup"><span data-stu-id="1f60d-107">For more information about how security call context information is accessed, see Programmatic Component Security.</span></span>

<span data-ttu-id="1f60d-108">Seules les applications COM+ qui utilisent la sécurité basée sur les rôles peuvent accéder à la classe **SecurityIdentity** .</span><span class="sxs-lookup"><span data-stu-id="1f60d-108">Only COM+ applications that use role-based security can access the **SecurityIdentity** class.</span></span> <span data-ttu-id="1f60d-109">Pour plus d’informations sur les rôles, consultez administration de la [sécurité basée sur les rôles](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="1f60d-109">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="1f60d-110">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="1f60d-110">When to implement</span></span>

<span data-ttu-id="1f60d-111">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="1f60d-111">This class is implemented by COM+.</span></span>



| <span data-ttu-id="1f60d-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f60d-112">Requirement</span></span> | <span data-ttu-id="1f60d-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f60d-113">Value</span></span> |
|------------|--------------------------------------------------------|
| <span data-ttu-id="1f60d-114">Interfaces</span><span class="sxs-lookup"><span data-stu-id="1f60d-114">Interfaces</span></span> | [<span data-ttu-id="1f60d-115">**ISecurityIdentityColl**</span><span class="sxs-lookup"><span data-stu-id="1f60d-115">**ISecurityIdentityColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="1f60d-116">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="1f60d-116">When to use</span></span>

<span data-ttu-id="1f60d-117">Utilisez cette classe pour accéder aux méthodes de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span><span class="sxs-lookup"><span data-stu-id="1f60d-117">Use this class to access the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="1f60d-118">Notes</span><span class="sxs-lookup"><span data-stu-id="1f60d-118">Remarks</span></span>

<span data-ttu-id="1f60d-119">Vous ne pouvez pas créer directement un objet **SecurityIdentity** .</span><span class="sxs-lookup"><span data-stu-id="1f60d-119">You cannot directly create a **SecurityIdentity** object.</span></span> <span data-ttu-id="1f60d-120">Pour utiliser les méthodes de [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), vous devez obtenir une référence à son implémentation en appelant [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), en fournissant IID \_ ISecurityCallContext pour le paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="1f60d-120">To use the methods of [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="1f60d-121">Ensuite, appelez [**ISecurityCallContext :: obtenir l' \_ élément**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) qui demande un élément de contexte d’appel de sécurité qui est une collection d’identités de sécurité (par exemple, « DirectCaller » ou « OriginalCaller »).</span><span class="sxs-lookup"><span data-stu-id="1f60d-121">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="1f60d-122">Appelez ensuite [**ISecurityIdentityColl :: obtenir l' \_ élément**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) pour récupérer un élément d’identité de sécurité (tel que « Name » ou « AuthenticationService »).</span><span class="sxs-lookup"><span data-stu-id="1f60d-122">Then call [**ISecurityIdentityColl::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecurityidentitycoll-get_item) to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

<span data-ttu-id="1f60d-123">Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+.</span><span class="sxs-lookup"><span data-stu-id="1f60d-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="1f60d-124">Vous ne pouvez pas créer directement un objet SecurityIdentity.</span><span class="sxs-lookup"><span data-stu-id="1f60d-124">You cannot directly create a SecurityIdentity object.</span></span> <span data-ttu-id="1f60d-125">Pour utiliser ses propriétés, vous devez obtenir un référence à son implémentation à l’aide de [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="1f60d-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="1f60d-126">Ensuite, récupérez la propriété Item de l’objet, en demandant un élément de contexte d’appel de sécurité qui est une collection d’identités de sécurité (telle que « DirectCaller » ou « OriginalCaller »).</span><span class="sxs-lookup"><span data-stu-id="1f60d-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span> <span data-ttu-id="1f60d-127">Ensuite, utilisez la propriété Item de l’objet SecurityIdentity pour récupérer un élément d’identité de sécurité (tel que « Name » ou « AuthenticationService »).</span><span class="sxs-lookup"><span data-stu-id="1f60d-127">Then, use the Item property of the SecurityIdentity object to retrieve a security identity item (such as "Name" or "AuthenticationService").</span></span>

## <a name="requirements"></a><span data-ttu-id="1f60d-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f60d-128">Requirements</span></span>



| <span data-ttu-id="1f60d-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f60d-129">Requirement</span></span> | <span data-ttu-id="1f60d-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f60d-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1f60d-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f60d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1f60d-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f60d-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1f60d-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f60d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1f60d-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f60d-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1f60d-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f60d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f60d-136"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f60d-136"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f60d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f60d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f60d-138">**GetSecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="1f60d-138">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="1f60d-139">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="1f60d-139">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="1f60d-140">Sécurité des composants de programmation</span><span class="sxs-lookup"><span data-stu-id="1f60d-140">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="1f60d-141">Administration de la sécurité basée sur les rôles</span><span class="sxs-lookup"><span data-stu-id="1f60d-141">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="1f60d-142">**SecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="1f60d-142">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="1f60d-143">**SecurityCallers**</span><span class="sxs-lookup"><span data-stu-id="1f60d-143">**SecurityCallers**</span></span>](securitycallers.md)
</dt> </dl>

 

