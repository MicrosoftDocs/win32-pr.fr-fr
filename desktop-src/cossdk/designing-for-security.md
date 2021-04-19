---
description: Conception pour la sécurité
ms.assetid: 436f9d86-fbfa-4d5a-8580-fa1d4065c0aa
title: Conception pour la sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69bc59b06cfcb7432806e548cc9808199b194e6e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515365"
---
# <a name="designing-for-security"></a><span data-ttu-id="71249-103">Conception pour la sécurité</span><span class="sxs-lookup"><span data-stu-id="71249-103">Designing for Security</span></span>

<span data-ttu-id="71249-104">Votre stratégie de bout en bout pour la sécurité dépend évidemment du type d’application distribuée que vous développez.</span><span class="sxs-lookup"><span data-stu-id="71249-104">Your end-to-end strategy for security obviously depends on the type of distributed application you are developing.</span></span> <span data-ttu-id="71249-105">Voici plusieurs suggestions pour résoudre la sécurité en ce qui concerne la logique d’application de couche intermédiaire :</span><span class="sxs-lookup"><span data-stu-id="71249-105">Following are several suggestions for addressing security with respect to middle-tier application logic:</span></span>

-   <span data-ttu-id="71249-106">Pour obtenir de l’efficacité et des performances, authentifiez-vous comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="71249-106">For efficiency and performance, authenticate as close to the user as you can.</span></span> <span data-ttu-id="71249-107">Si votre application implique une architecture de la logique du navigateur au niveau de la base de données, envisagez de mapper les clients du navigateur aux identités de domaine, d’exécuter l’application COM+ avec des identités spécifiques à chaque application et de configurer les tables de la couche données pour qu’elles soient accessibles uniquement par une identité d’application particulière.</span><span class="sxs-lookup"><span data-stu-id="71249-107">If your application involves a browser-to-business-logic-to-database architecture, consider mapping the browser clients to domain identities, run the COM+ application under identities specific to each application, and configure tables in the data tier to be accessible only by a particular application identity.</span></span> <span data-ttu-id="71249-108">Ce scénario de serveur approuvé est plus évolutif et moins problématique que l’utilisation du SGBD pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="71249-108">This trusted server scenario is more scalable and less problematic than using the DBMS for authenticating.</span></span>
-   <span data-ttu-id="71249-109">Si vous concevez un composant qui sera utilisé dans une application distribuée à l’aide de la sécurité basée sur les rôles, vous pouvez utiliser la fonctionnalité de [sécurité com+](com--security.md) .</span><span class="sxs-lookup"><span data-stu-id="71249-109">If you are designing a component that will be used in a distributed application using role-based security, you can use the [COM+ security](com--security.md) functionality.</span></span> <span data-ttu-id="71249-110">Cette fonctionnalité vous permet d’appeler des méthodes telles que [**IObjectContext :: IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) et [**IObjectContext :: IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) pour aider à protéger des blocs de code d’un accès non autorisé.</span><span class="sxs-lookup"><span data-stu-id="71249-110">This functionality allows you to call methods such as [**IObjectContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-iscallerinrole) and [**IObjectContext::IsSecurityEnabled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-issecurityenabled) to help protect blocks of code from unauthorized access.</span></span> <span data-ttu-id="71249-111">Vous pouvez également utiliser le contexte de l’appel de sécurité pour obtenir des informations sur les appelants d’un objet.</span><span class="sxs-lookup"><span data-stu-id="71249-111">You can also use the security call context to get information about an object's callers.</span></span>
-   <span data-ttu-id="71249-112">Si vous concevez un composant qui sera utilisé dans une application distribuée sans utiliser la sécurité basée sur les rôles, la sécurité est automatiquement vérifiée uniquement au niveau du processus.</span><span class="sxs-lookup"><span data-stu-id="71249-112">If you are designing a component that will be used in a distributed application without using role-based security, security is automatically checked only at the process level.</span></span> <span data-ttu-id="71249-113">Les autorisations de processus d’accès déterminent qui est autorisé à accéder à l’application.</span><span class="sxs-lookup"><span data-stu-id="71249-113">Process access permissions determine who is given access to the application.</span></span> <span data-ttu-id="71249-114">Si vous avez besoin d’un contrôle plus fin sur les paramètres de sécurité au niveau du processus ou au niveau de l’interface, utilisez la fonctionnalité de sécurité par programme fournie par COM.</span><span class="sxs-lookup"><span data-stu-id="71249-114">If you need finer grain control over security settings at the process or at the interface level, use the programmatic security functionality provided by COM.</span></span>
-   <span data-ttu-id="71249-115">Si un composant qui utilise la sécurité COM+ est exécuté sans être intégré à une application COM+, les exceptions sont levées.</span><span class="sxs-lookup"><span data-stu-id="71249-115">If a component using COM+ programmatic security is run without being integrated into a COM+ application, exceptions will be thrown.</span></span> <span data-ttu-id="71249-116">Par conséquent, si vous souhaitez que ce composant soit correctement intégré à une application qui ne fait pas partie de l’environnement COM+, vous devez gérer toutes les exceptions de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="71249-116">Therefore, if you want such a component to be successfully integrated into an application that is not part of the COM+ environment, you must handle all exceptions appropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71249-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71249-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71249-118">Conception pour la disponibilité</span><span class="sxs-lookup"><span data-stu-id="71249-118">Designing for Availability</span></span>](designing-for-availability.md)
</dt> <dt>

[<span data-ttu-id="71249-119">Conception pour le déploiement</span><span class="sxs-lookup"><span data-stu-id="71249-119">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> <dt>

[<span data-ttu-id="71249-120">Conception pour l’évolutivité</span><span class="sxs-lookup"><span data-stu-id="71249-120">Designing for Scalability</span></span>](designing-for-scalability.md)
</dt> <dt>

[<span data-ttu-id="71249-121">Sécurité des composants de programmation</span><span class="sxs-lookup"><span data-stu-id="71249-121">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> </dl>

 

 



