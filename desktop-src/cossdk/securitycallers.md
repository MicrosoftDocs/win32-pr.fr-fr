---
description: Fournit l’accès aux informations sur les appelants individuels dans une collection d’appelants. La collection représente la chaîne d’appels se terminant par l’appel en cours, et chaque appelant de la collection représente l’identité d’un appelant.
ms.assetid: 164fe12d-eeb3-402f-8aa3-e3545904d9c4
title: SecurityCallers, classe (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SecurityCallers
api_type:
- COM
ms.openlocfilehash: c757b11bba6a30e8951915e1eace0811b6b6f732
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317853"
---
# <a name="securitycallers-class"></a><span data-ttu-id="f8cba-104">SecurityCallers (classe)</span><span class="sxs-lookup"><span data-stu-id="f8cba-104">SecurityCallers class</span></span>

<span data-ttu-id="f8cba-105">Fournit l’accès aux informations sur les appelants individuels dans une collection d’appelants.</span><span class="sxs-lookup"><span data-stu-id="f8cba-105">Provides access to information about individual callers in a collection of callers.</span></span> <span data-ttu-id="f8cba-106">La collection représente la chaîne d’appels se terminant par l’appel en cours, et chaque appelant de la collection représente l’identité d’un appelant.</span><span class="sxs-lookup"><span data-stu-id="f8cba-106">The collection represents the chain of calls ending with the current call, and each caller in the collection represents the identity of one caller.</span></span> <span data-ttu-id="f8cba-107">Seuls les appelants qui franchissent une limite où la sécurité est vérifiée sont inclus dans la chaîne d’appelants.</span><span class="sxs-lookup"><span data-stu-id="f8cba-107">Only callers who cross a boundary where security is checked are included in the chain of callers.</span></span> <span data-ttu-id="f8cba-108">(Dans l’environnement COM+, la sécurité est vérifiée au niveau des limites de l’application.) L’accès aux informations sur l’identité d’un appelant particulier est fourni par le biais de la classe [**SecurityIdentity**](securityidentity.md) , une collection d’identités.</span><span class="sxs-lookup"><span data-stu-id="f8cba-108">(In the COM+ environment, security is checked at application boundaries.) Access to information about a particular caller's identity is provided through the [**SecurityIdentity**](securityidentity.md) class, an identity collection.</span></span>

<span data-ttu-id="f8cba-109">Seules les applications COM+ qui utilisent la sécurité basée sur les rôles peuvent accéder à la classe **SecurityCallers** .</span><span class="sxs-lookup"><span data-stu-id="f8cba-109">Only COM+ applications that use role-based security can access the **SecurityCallers** class.</span></span> <span data-ttu-id="f8cba-110">Pour plus d’informations sur les rôles, consultez administration de la [sécurité basée sur les rôles](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="f8cba-110">For more information on roles, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="f8cba-111">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="f8cba-111">When to implement</span></span>

<span data-ttu-id="f8cba-112">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="f8cba-112">This class is implemented by COM+.</span></span>



| <span data-ttu-id="f8cba-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8cba-113">Requirement</span></span> | <span data-ttu-id="f8cba-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8cba-114">Value</span></span> |
|------------|------------------------------------------------------|
| <span data-ttu-id="f8cba-115">Interfaces</span><span class="sxs-lookup"><span data-stu-id="f8cba-115">Interfaces</span></span> | [<span data-ttu-id="f8cba-116">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="f8cba-116">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll) |



 

## <a name="when-to-use"></a><span data-ttu-id="f8cba-117">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="f8cba-117">When to use</span></span>

<span data-ttu-id="f8cba-118">Utilisez cette classe pour accéder aux méthodes de [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span><span class="sxs-lookup"><span data-stu-id="f8cba-118">Use this class to access the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="remarks"></a><span data-ttu-id="f8cba-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f8cba-119">Remarks</span></span>

<span data-ttu-id="f8cba-120">Vous ne pouvez pas créer directement un objet **SecurityCallers** .</span><span class="sxs-lookup"><span data-stu-id="f8cba-120">You cannot directly create a **SecurityCallers** object.</span></span> <span data-ttu-id="f8cba-121">Pour utiliser les méthodes de [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), vous devez obtenir une référence à son implémentation en appelant [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), en fournissant IID \_ ISecurityCallContext pour le paramètre *riid* .</span><span class="sxs-lookup"><span data-stu-id="f8cba-121">To use the methods of [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll), you must obtain a reference to its implementation by calling [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), supplying IID\_ISecurityCallContext for the *riid* parameter.</span></span> <span data-ttu-id="f8cba-122">Ensuite, appelez [**ISecurityCallContext :: obtenir l' \_ élément**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) qui demande un élément de contexte d’appel de sécurité qui est une collection d’identités de sécurité (par exemple, « DirectCaller » ou « OriginalCaller »).</span><span class="sxs-lookup"><span data-stu-id="f8cba-122">Next, call [**ISecurityCallContext::get\_Item**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-get_item) requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

<span data-ttu-id="f8cba-123">Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types des services COM+.</span><span class="sxs-lookup"><span data-stu-id="f8cba-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Services Type Library.</span></span> <span data-ttu-id="f8cba-124">Vous ne pouvez pas créer directement un objet SecurityCallers.</span><span class="sxs-lookup"><span data-stu-id="f8cba-124">You cannot directly create a SecurityCallers object.</span></span> <span data-ttu-id="f8cba-125">Pour utiliser ses propriétés, vous devez obtenir un référence à son implémentation à l’aide de [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="f8cba-125">To use its properties, you must obtain a refernece to its implementation using [**GetSecurityCallContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext).</span></span> <span data-ttu-id="f8cba-126">Ensuite, récupérez la propriété Item de l’objet, en demandant un élément de contexte d’appel de sécurité qui est une collection d’identités de sécurité (telle que « DirectCaller » ou « OriginalCaller »).</span><span class="sxs-lookup"><span data-stu-id="f8cba-126">Next, get the Item property of the object, requesting a security call context item that is a security identity collection (such as "DirectCaller" or "OriginalCaller").</span></span>

## <a name="requirements"></a><span data-ttu-id="f8cba-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8cba-127">Requirements</span></span>



| <span data-ttu-id="f8cba-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8cba-128">Requirement</span></span> | <span data-ttu-id="f8cba-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8cba-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f8cba-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8cba-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f8cba-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8cba-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="f8cba-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8cba-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f8cba-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8cba-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f8cba-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8cba-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8cba-135"><dt>ComSvcs. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8cba-135"><dt>ComSvcs.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8cba-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8cba-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8cba-137">**GetSecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="f8cba-137">**GetSecurityCallContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-igetsecuritycallcontext-getsecuritycallcontext)
</dt> <dt>

[<span data-ttu-id="f8cba-138">**ISecurityCallersColl**</span><span class="sxs-lookup"><span data-stu-id="f8cba-138">**ISecurityCallersColl**</span></span>](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll)
</dt> <dt>

[<span data-ttu-id="f8cba-139">Sécurité des composants de programmation</span><span class="sxs-lookup"><span data-stu-id="f8cba-139">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="f8cba-140">Administration de la sécurité basée sur les rôles</span><span class="sxs-lookup"><span data-stu-id="f8cba-140">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="f8cba-141">**SecurityCallContext**</span><span class="sxs-lookup"><span data-stu-id="f8cba-141">**SecurityCallContext**</span></span>](securitycallcontext.md)
</dt> <dt>

[<span data-ttu-id="f8cba-142">**SecurityIdentity**</span><span class="sxs-lookup"><span data-stu-id="f8cba-142">**SecurityIdentity**</span></span>](securityidentity.md)
</dt> </dl>

 

