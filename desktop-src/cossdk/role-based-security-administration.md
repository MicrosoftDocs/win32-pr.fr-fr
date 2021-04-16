---
description: Administration de la sécurité Role-Based
ms.assetid: 7247758e-f486-4ce2-afca-f0d10fffe626
title: Administration de la sécurité Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714cede74e105a68b0a5fed2371858054add954e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524039"
---
# <a name="role-based-security-administration"></a><span data-ttu-id="056ef-103">Administration de la sécurité Role-Based</span><span class="sxs-lookup"><span data-stu-id="056ef-103">Role-Based Security Administration</span></span>

<span data-ttu-id="056ef-104">La sécurité basée sur les rôles est un service automatique fourni par COM+ qui vous permet de construire et d’appliquer de manière administrative une stratégie de contrôle d’accès pour votre application COM+.</span><span class="sxs-lookup"><span data-stu-id="056ef-104">Role-based security is an automatic service provided by COM+ that enables you to administratively construct and enforce an access control policy for your COM+ application.</span></span> <span data-ttu-id="056ef-105">Avec un modèle de configuration de sécurité flexible et extensible, la sécurité basée sur les rôles offre un avantage considérable sur l’application de la sécurité dans vos composants et offre les avantages suivants :</span><span class="sxs-lookup"><span data-stu-id="056ef-105">With a flexible and extensible security configuration model, role-based security offers a considerable advantage over enforcing all security within your components and provides the following benefits:</span></span>

-   <span data-ttu-id="056ef-106">Vous pouvez configurer la sécurité de manière administrative à l’aide de l’outil d’administration Services de composants ou des fonctions d’administration.</span><span class="sxs-lookup"><span data-stu-id="056ef-106">You can configure security administratively, using either the Component Services administrative tool or the Administrative functions.</span></span>
-   <span data-ttu-id="056ef-107">Vous n’avez pas besoin d’écrire une logique relative à la sécurité dans vos composants lorsque la protection des rôles au niveau de la méthode vous offre un contrôle d’accès suffisamment précis.</span><span class="sxs-lookup"><span data-stu-id="056ef-107">You don't have to write security-related logic into your components when role protection at the method level provides you with fine enough access control.</span></span>
-   <span data-ttu-id="056ef-108">Vous n’avez pas besoin de factoriser la sécurité dans la conception de l’interface ou du composant.</span><span class="sxs-lookup"><span data-stu-id="056ef-108">You don't have to factor security into interface or component design.</span></span> <span data-ttu-id="056ef-109">Au lieu de cela, vous pouvez définir la sécurité par méthode.</span><span class="sxs-lookup"><span data-stu-id="056ef-109">Instead, you can set security on a method-by-method basis.</span></span>
-   <span data-ttu-id="056ef-110">Vous pouvez vous concentrer sur la structure de la stratégie de sécurité que vous souhaitez appliquer et, par le biais des rôles, cette stratégie peut être clairement exprimée aux administrateurs qui déploient votre application.</span><span class="sxs-lookup"><span data-stu-id="056ef-110">You can focus on the structure of the security policy you want to enforce, and through roles, that policy can be clearly expressed to the administrators deploying your application.</span></span>
-   <span data-ttu-id="056ef-111">Vous pouvez facilement modifier une stratégie de sécurité pour l’adapter aux exigences de sécurité en constante évolution pour une application.</span><span class="sxs-lookup"><span data-stu-id="056ef-111">You can easily modify a security policy to adapt to evolving security requirements for an application.</span></span>
-   <span data-ttu-id="056ef-112">Vous pouvez créer des stratégies de sécurité plus granulaires par programmation, si nécessaire, à l’aide de la sécurité basée sur les rôles comme plateforme de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="056ef-112">You can build more granular security policies programmatically if you need to, using role-based security as a supporting platform.</span></span>
-   <span data-ttu-id="056ef-113">Vous pouvez tirer parti de la sécurité basée sur les rôles pour effectuer un audit détaillé, car vous pouvez obtenir des informations de sécurité de l’appelant pour une chaîne entière d’appels en amont.</span><span class="sxs-lookup"><span data-stu-id="056ef-113">You can leverage role-based security to do detailed auditing, because you can obtain caller security information for an entire chain of upstream calls.</span></span>

> [!Note]  
> <span data-ttu-id="056ef-114">Les utilisateurs du rôle administrateur pour l’application système doivent être membres du groupe Administrateurs local.</span><span class="sxs-lookup"><span data-stu-id="056ef-114">Users in the Administrator role for the System Application must be members of the local administrators group.</span></span> <span data-ttu-id="056ef-115">En outre, à compter de Windows Server 2003, la fonctionnalité d’authentification de l’application système COM+ comprend la valeur EOAC \_ Disable \_ AAA.</span><span class="sxs-lookup"><span data-stu-id="056ef-115">Also, as of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="056ef-116">Cette valeur, qui désactive les activations AAA (Activate-As-Activator), est utilisée dans l’appel de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) lors du lancement de l’application système.</span><span class="sxs-lookup"><span data-stu-id="056ef-116">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="056ef-117">La définition de la fonctionnalité d’authentification sur EOAC \_ Disable \_ AAA permet à une application qui s’exécute sous un compte privilégié (tel que LocalSystem) d’empêcher son identité d’être utilisée pour lancer des composants non fiables.</span><span class="sxs-lookup"><span data-stu-id="056ef-117">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

 

<span data-ttu-id="056ef-118">Consultez les rubriques suivantes de cette section pour plus d’informations sur le fonctionnement de la sécurité basée sur les rôles et sur les points à prendre en compte lors de l’utilisation de cette stratégie de sécurité pour créer une stratégie de sécurité pour une application :</span><span class="sxs-lookup"><span data-stu-id="056ef-118">See the following topics in this section for information about how role-based security works and issues to consider when using it to construct a security policy for an application:</span></span>

-   [<span data-ttu-id="056ef-119">Utilisation de rôles pour l’autorisation du client</span><span class="sxs-lookup"><span data-stu-id="056ef-119">Using Roles for Client Authorization</span></span>](using-roles-for-client-authorization.md)
-   [<span data-ttu-id="056ef-120">Conception efficace des rôles</span><span class="sxs-lookup"><span data-stu-id="056ef-120">Designing Roles Effectively</span></span>](designing-roles-effectively.md)
-   [<span data-ttu-id="056ef-121">Limites de sécurité</span><span class="sxs-lookup"><span data-stu-id="056ef-121">Security Boundaries</span></span>](security-boundaries.md)
-   [<span data-ttu-id="056ef-122">Informations de contexte de l’appel de sécurité</span><span class="sxs-lookup"><span data-stu-id="056ef-122">Security Call Context Information</span></span>](security-call-context-information.md)
-   [<span data-ttu-id="056ef-123">Propriété de contexte de sécurité</span><span class="sxs-lookup"><span data-stu-id="056ef-123">Security Context Property</span></span>](security-context-property.md)

<span data-ttu-id="056ef-124">Pour obtenir des descriptions détaillées des étapes nécessaires à la configuration de la sécurité basée sur les rôles pour une application, consultez Configuration de la [sécurité des Role-Based](configuring-role-based-security.md).</span><span class="sxs-lookup"><span data-stu-id="056ef-124">For detailed how-to descriptions of the steps involved in configuring role-based security for an application, see [Configuring Role-Based Security](configuring-role-based-security.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="056ef-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="056ef-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="056ef-126">Authentification du client</span><span class="sxs-lookup"><span data-stu-id="056ef-126">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="056ef-127">Emprunt d’identité et délégation du client</span><span class="sxs-lookup"><span data-stu-id="056ef-127">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="056ef-128">Sécurité de l’application de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="056ef-128">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="056ef-129">Sécurité des applications multiniveau</span><span class="sxs-lookup"><span data-stu-id="056ef-129">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="056ef-130">Sécurité des composants de programmation</span><span class="sxs-lookup"><span data-stu-id="056ef-130">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="056ef-131">Utilisation de la stratégie de restriction logicielle dans COM+</span><span class="sxs-lookup"><span data-stu-id="056ef-131">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 
