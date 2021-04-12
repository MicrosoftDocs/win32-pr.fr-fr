---
description: Lorsque la sécurité basée sur les rôles est utilisée, l’objet de contexte de l’appel de sécurité peut être utilisé pour accéder aux informations de sécurité relatives à l’appel en cours.
ms.assetid: 9fc0a9e5-934c-4510-8fbb-1fb2817aa0ea
title: Accès aux informations de contexte de l’appel de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d7e5160c766783b6d43822571d624e0a595c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201060"
---
# <a name="accessing-security-call-context-information"></a><span data-ttu-id="e710b-103">Accès aux informations de contexte de l’appel de sécurité</span><span class="sxs-lookup"><span data-stu-id="e710b-103">Accessing Security Call Context Information</span></span>

<span data-ttu-id="e710b-104">Lorsque la sécurité basée sur les rôles est utilisée, l’objet de contexte de l’appel de sécurité peut être utilisé pour accéder aux informations de sécurité relatives à l’appel en cours.</span><span class="sxs-lookup"><span data-stu-id="e710b-104">When role-based security is being used, the security call context object can be used to access security information about the current call.</span></span>

<span data-ttu-id="e710b-105">Les collections de propriétés suivantes sont disponibles à partir de l’objet de contexte de l’appel de sécurité :</span><span class="sxs-lookup"><span data-stu-id="e710b-105">The following collections of properties are available from the security call context object:</span></span>

-   [<span data-ttu-id="e710b-106">Collection SecurityCallContext</span><span class="sxs-lookup"><span data-stu-id="e710b-106">SecurityCallContext Collection</span></span>](#securitycallcontext-collection)
-   [<span data-ttu-id="e710b-107">SecurityCallers, collection</span><span class="sxs-lookup"><span data-stu-id="e710b-107">SecurityCallers Collection</span></span>](#securitycallers-collection)
-   [<span data-ttu-id="e710b-108">SecurityIdentity, collection</span><span class="sxs-lookup"><span data-stu-id="e710b-108">SecurityIdentity Collection</span></span>](#securityidentity-collection)
-   [<span data-ttu-id="e710b-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e710b-109">Related topics</span></span>](#related-topics)

## <a name="securitycallcontext-collection"></a><span data-ttu-id="e710b-110">Collection SecurityCallContext</span><span class="sxs-lookup"><span data-stu-id="e710b-110">SecurityCallContext Collection</span></span>



| <span data-ttu-id="e710b-111">Propriété</span><span class="sxs-lookup"><span data-stu-id="e710b-111">Property</span></span>                          | <span data-ttu-id="e710b-112">Description</span><span class="sxs-lookup"><span data-stu-id="e710b-112">Description</span></span>                                                                                                                            |
|-----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e710b-113">NumCallers</span><span class="sxs-lookup"><span data-stu-id="e710b-113">NumCallers</span></span><br/>             | <span data-ttu-id="e710b-114">Nombre d’appelants dans la chaîne d’appels.</span><span class="sxs-lookup"><span data-stu-id="e710b-114">The number of callers in the chain of calls.</span></span><br/>                                                                                |
| <span data-ttu-id="e710b-115">MinAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="e710b-115">MinAuthenticationLevel</span></span><br/> | <span data-ttu-id="e710b-116">Niveau d’authentification le moins sécurisé de tous les appelants de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="e710b-116">The least secure authentication level of all callers in the chain.</span></span><br/>                                                          |
| <span data-ttu-id="e710b-117">Appelants</span><span class="sxs-lookup"><span data-stu-id="e710b-117">Callers</span></span><br/>                | <span data-ttu-id="e710b-118">Informations sur l’identité des appelants en amont, sous la forme d’une collection [**SecurityCallers**](securitycallers.md) .</span><span class="sxs-lookup"><span data-stu-id="e710b-118">Information about the identity of upstream callers, in the form of a [**SecurityCallers**](securitycallers.md) collection.</span></span><br/> |
| <span data-ttu-id="e710b-119">DirectCaller</span><span class="sxs-lookup"><span data-stu-id="e710b-119">DirectCaller</span></span><br/>           | <span data-ttu-id="e710b-120">Appelant qui a appelé l’objet directement (sans appelants impliqués).</span><span class="sxs-lookup"><span data-stu-id="e710b-120">The caller that called the object directly (with no intervening callers).</span></span> <br/>                                                  |
| <span data-ttu-id="e710b-121">OriginalCaller</span><span class="sxs-lookup"><span data-stu-id="e710b-121">OriginalCaller</span></span><br/>         | <span data-ttu-id="e710b-122">Appelant à l’origine de la chaîne d’appels à l’objet.</span><span class="sxs-lookup"><span data-stu-id="e710b-122">The caller that originated the chain of calls to the object.</span></span> <br/>                                                               |



 

<span data-ttu-id="e710b-123">Pour plus d’informations sur l’utilisation de cette collection, Microsoft Visual Basic les développeurs doivent voir la classe [**SecurityCallContext**](securitycallcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="e710b-123">For more information about how to use this collection, Microsoft Visual Basic developers should see the [**SecurityCallContext**](securitycallcontext.md) class.</span></span> <span data-ttu-id="e710b-124">Les développeurs C et C++ doivent faire référence à [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span><span class="sxs-lookup"><span data-stu-id="e710b-124">C and C++ developers should refer to [**ISecurityCallContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallcontext).</span></span>

## <a name="securitycallers-collection"></a><span data-ttu-id="e710b-125">SecurityCallers, collection</span><span class="sxs-lookup"><span data-stu-id="e710b-125">SecurityCallers Collection</span></span>

<span data-ttu-id="e710b-126">La collection [**SecurityCallers**](securitycallers.md) représente des appelants qui peuvent être récupérés à l’aide d’un index compris entre 0 et 1 inférieur à NumCallers, inclus.</span><span class="sxs-lookup"><span data-stu-id="e710b-126">The [**SecurityCallers**](securitycallers.md) collection represents callers that can be retrieved by using an index between 0 and 1 less than NumCallers, inclusive.</span></span> <span data-ttu-id="e710b-127">Chaque appelant est représenté par un objet [**SecurityIdentity**](securityidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="e710b-127">Each caller is represented by a [**SecurityIdentity**](securityidentity.md) object.</span></span>

<span data-ttu-id="e710b-128">Pour plus d’informations sur cette collection, Visual Basic les développeurs doivent voir la classe [**SecurityCallers**](securitycallers.md) .</span><span class="sxs-lookup"><span data-stu-id="e710b-128">For more information about this collection, Visual Basic developers should see the [**SecurityCallers**](securitycallers.md) class.</span></span> <span data-ttu-id="e710b-129">Les développeurs C et C++ doivent faire référence à [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span><span class="sxs-lookup"><span data-stu-id="e710b-129">C and C++ developers should refer to [**ISecurityCallersColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecuritycallerscoll).</span></span>

## <a name="securityidentity-collection"></a><span data-ttu-id="e710b-130">SecurityIdentity, collection</span><span class="sxs-lookup"><span data-stu-id="e710b-130">SecurityIdentity Collection</span></span>



| <span data-ttu-id="e710b-131">Propriété</span><span class="sxs-lookup"><span data-stu-id="e710b-131">Property</span></span>                         | <span data-ttu-id="e710b-132">Description</span><span class="sxs-lookup"><span data-stu-id="e710b-132">Description</span></span>                                                                                                                                                          |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e710b-133">SID</span><span class="sxs-lookup"><span data-stu-id="e710b-133">SID</span></span><br/>                   | <span data-ttu-id="e710b-134">Identificateur de sécurité de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e710b-134">The security identifier for the caller.</span></span><br/>                                                                                                                   |
| <span data-ttu-id="e710b-135">AccountName</span><span class="sxs-lookup"><span data-stu-id="e710b-135">AccountName</span></span><br/>           | <span data-ttu-id="e710b-136">Nom de compte de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="e710b-136">The account name of the caller.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="e710b-137">AuthenticationService</span><span class="sxs-lookup"><span data-stu-id="e710b-137">AuthenticationService</span></span><br/> | <span data-ttu-id="e710b-138">Service d’authentification utilisé, tel que NTLMSSP, Kerberos ou SSL.</span><span class="sxs-lookup"><span data-stu-id="e710b-138">The authentication service used, such as NTLMSSP, Kerberos, or SSL.</span></span><br/>                                                                                       |
| <span data-ttu-id="e710b-139">AuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="e710b-139">AuthenticationLevel</span></span><br/>   | <span data-ttu-id="e710b-140">Niveau d’authentification utilisé, qui représente la quantité de protection utilisée lors de la communication avec l’objet.</span><span class="sxs-lookup"><span data-stu-id="e710b-140">The authentication level used, which represents the amount of protection used when communicating with the object.</span></span><br/>                                         |
| <span data-ttu-id="e710b-141">ImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="e710b-141">ImpersonationLevel</span></span><br/>    | <span data-ttu-id="e710b-142">Niveau d’emprunt d’identité défini par le client, si l’emprunt d’identité a été utilisé.</span><span class="sxs-lookup"><span data-stu-id="e710b-142">The level of impersonation set by the client, if impersonation was used.</span></span> <span data-ttu-id="e710b-143">Ce niveau indique la quantité d’autorité donnée au serveur par le client.</span><span class="sxs-lookup"><span data-stu-id="e710b-143">This level indicates the amount of authority given to the server by the client.</span></span> <br/> |



 

<span data-ttu-id="e710b-144">Pour plus d’informations sur cette collection, Visual Basic les développeurs doivent voir la classe [**SecurityIdentity**](securityidentity.md) .</span><span class="sxs-lookup"><span data-stu-id="e710b-144">For more information on this collection, Visual Basic developers should see the [**SecurityIdentity**](securityidentity.md) class.</span></span> <span data-ttu-id="e710b-145">Les développeurs C et C++ doivent faire référence à [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span><span class="sxs-lookup"><span data-stu-id="e710b-145">C and C++ developers should refer to [**ISecurityIdentityColl**](/windows/desktop/api/ComSvcs/nn-comsvcs-isecurityidentitycoll).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e710b-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e710b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e710b-147">Vérification de l’appartenance au rôle</span><span class="sxs-lookup"><span data-stu-id="e710b-147">Checking Role Membership</span></span>](checking-role-membership.md)
</dt> <dt>

[<span data-ttu-id="e710b-148">Détermination de l’activation ou non de la sécurité Role-Based</span><span class="sxs-lookup"><span data-stu-id="e710b-148">Determining Whether Role-Based Security Is Enabled</span></span>](determining-whether-role-based-security-is-enabled.md)
</dt> <dt>

[<span data-ttu-id="e710b-149">Sécurité des composants de programmation</span><span class="sxs-lookup"><span data-stu-id="e710b-149">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 




