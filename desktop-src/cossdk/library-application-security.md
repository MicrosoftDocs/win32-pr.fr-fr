---
description: Étant donné qu’une application de bibliothèque COM+ est hébergée par un autre processus, qui peut avoir ses propres paramètres de sécurité, la sécurité pour les applications de bibliothèque nécessite une attention particulière.
ms.assetid: a966020c-a0bd-467c-b6d3-e09267cf5574
title: Sécurité de l’application de bibliothèque
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d2885173f3798d33ed26a5b447fde4429b9bf96
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523420"
---
# <a name="library-application-security"></a><span data-ttu-id="52acb-103">Sécurité de l’application de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="52acb-103">Library Application Security</span></span>

<span data-ttu-id="52acb-104">Étant donné qu’une application de bibliothèque COM+ est hébergée par un autre processus, qui peut avoir ses propres paramètres de sécurité, la sécurité pour les applications de bibliothèque nécessite une attention particulière.</span><span class="sxs-lookup"><span data-stu-id="52acb-104">Because a COM+ library application is hosted by another process, which may have its own security settings, security for library applications requires special consideration.</span></span>

<span data-ttu-id="52acb-105">Les contraintes suivantes s’appliquent à la sécurité de l’application de bibliothèque :</span><span class="sxs-lookup"><span data-stu-id="52acb-105">The following constraints apply to library application security:</span></span>

-   <span data-ttu-id="52acb-106">Les applications de bibliothèque s’exécutent sous le jeton de sécurité du processus client plutôt que sous leur propre identité d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="52acb-106">Library applications run under the client process security token rather than under their own user identity.</span></span> <span data-ttu-id="52acb-107">Ils n’ont que peu de privilèges que le client a.</span><span class="sxs-lookup"><span data-stu-id="52acb-107">They have only as much privilege as the client has.</span></span>
-   <span data-ttu-id="52acb-108">Les applications de bibliothèque ne contrôlent pas la sécurité au niveau du processus.</span><span class="sxs-lookup"><span data-stu-id="52acb-108">Library applications do not control process-level security.</span></span> <span data-ttu-id="52acb-109">Aucun utilisateur dans les rôles n’est ajouté au descripteur de sécurité pour le processus.</span><span class="sxs-lookup"><span data-stu-id="52acb-109">No users in roles will be added to the security descriptor for the process.</span></span> <span data-ttu-id="52acb-110">La seule façon pour une application de bibliothèque d’effectuer ses propres contrôles d’accès consiste à utiliser la sécurité au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="52acb-110">The only way for a library application to perform its own access checks is to use component-level security.</span></span> <span data-ttu-id="52acb-111">(Voir [limites de sécurité](security-boundaries.md).)</span><span class="sxs-lookup"><span data-stu-id="52acb-111">(See [Security Boundaries](security-boundaries.md).)</span></span>
-   <span data-ttu-id="52acb-112">Les applications de bibliothèque peuvent être configurées de façon à participer ou non à l’authentification du processus hôte, en activant ou désactivant l’authentification.</span><span class="sxs-lookup"><span data-stu-id="52acb-112">Library applications can be configured to either participate or not participate in host process authentication, by enabling or disabling authentication.</span></span> <span data-ttu-id="52acb-113">(Voir [activation de l’authentification pour une application de bibliothèque](enabling-authentication-for-a-library-application.md).)</span><span class="sxs-lookup"><span data-stu-id="52acb-113">(See [Enabling Authentication for a Library Application](enabling-authentication-for-a-library-application.md).)</span></span>
-   <span data-ttu-id="52acb-114">Les applications de bibliothèque ne peuvent pas définir un niveau d’emprunt d’identité ; ils utilisent ce processus hôte.</span><span class="sxs-lookup"><span data-stu-id="52acb-114">Library applications cannot set an impersonation level; they use that of the host process.</span></span>

## <a name="using-library-applications-to-limit-application-privilege"></a><span data-ttu-id="52acb-115">Utilisation d’applications de bibliothèque pour limiter le privilège de l’application</span><span class="sxs-lookup"><span data-stu-id="52acb-115">Using Library Applications to Limit Application Privilege</span></span>

<span data-ttu-id="52acb-116">Dans certains cas, vous souhaiterez peut-être configurer une application en tant qu’application de bibliothèque de manière à ce qu’elle s’exécute sous l’identité du processus d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="52acb-116">In some cases, you may want to configure an application specifically as a library application so that it runs under the identity of the hosting process.</span></span> <span data-ttu-id="52acb-117">Cela limite fondamentalement l’application afin qu’elle puisse accéder uniquement aux ressources auxquelles son client, le processus hôte, peut accéder.</span><span class="sxs-lookup"><span data-stu-id="52acb-117">Doing so fundamentally limits the application so that it can access only those resources that its client, the host process, can access.</span></span> <span data-ttu-id="52acb-118">Les threads sur lesquels s’exécutent les composants d’application de bibliothèque utilisent le jeton de processus par défaut. par conséquent, lorsqu’ils effectuent des appels en dehors de l’application ou accèdent à des ressources telles que des fichiers protégés par un descripteur de sécurité, ils semblent être le client.</span><span class="sxs-lookup"><span data-stu-id="52acb-118">The threads that the library application components run on will use the process token by default, and therefore when they make calls outside of the application or access resources such as files guarded with a security descriptor, they will appear to be the client.</span></span> <span data-ttu-id="52acb-119">Pour les applications qui effectuent des tâches sensibles, il peut s’agir d’un moyen simple de contrôler l’étendue de leurs actions.</span><span class="sxs-lookup"><span data-stu-id="52acb-119">For applications that perform sensitive work, this may be an easy way to control the scope of their actions.</span></span>

## <a name="effectively-securing-library-applications"></a><span data-ttu-id="52acb-120">Sécurisation efficace des applications de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="52acb-120">Effectively Securing Library Applications</span></span>

<span data-ttu-id="52acb-121">Il existe des considérations spéciales relatives à la configuration de la sécurité basée sur les rôles et de l’authentification pour les applications de bibliothèque afin qu’elles s’exécutent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="52acb-121">There are special considerations in configuring role-based security and authentication for library applications so that they perform as expected.</span></span> <span data-ttu-id="52acb-122">Pour plus d’informations, consultez [configuration de la sécurité pour les applications de bibliothèque](configuring-security-for-library-applications.md).</span><span class="sxs-lookup"><span data-stu-id="52acb-122">For details, see [Configuring Security for Library Applications](configuring-security-for-library-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="52acb-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="52acb-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52acb-124">Authentification du client</span><span class="sxs-lookup"><span data-stu-id="52acb-124">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="52acb-125">Emprunt d’identité et délégation du client</span><span class="sxs-lookup"><span data-stu-id="52acb-125">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="52acb-126">Sécurité des applications multiniveau</span><span class="sxs-lookup"><span data-stu-id="52acb-126">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> <dt>

[<span data-ttu-id="52acb-127">Sécurité des composants de programmation</span><span class="sxs-lookup"><span data-stu-id="52acb-127">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="52acb-128">Administration de la sécurité basée sur les rôles</span><span class="sxs-lookup"><span data-stu-id="52acb-128">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="52acb-129">Utilisation de la stratégie de restriction logicielle dans COM+</span><span class="sxs-lookup"><span data-stu-id="52acb-129">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



