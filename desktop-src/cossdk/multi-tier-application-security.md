---
description: Sécurité des applications multiniveau
ms.assetid: ff84eeed-ddfd-40e8-8f42-625b4d49ecd5
title: Sécurité des applications multiniveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150f7894c7d11e832786e31ab028f9dbac35f6e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515156"
---
# <a name="multi-tier-application-security"></a><span data-ttu-id="1e6cf-103">Sécurité des applications multiniveau</span><span class="sxs-lookup"><span data-stu-id="1e6cf-103">Multi-Tier Application Security</span></span>

<span data-ttu-id="1e6cf-104">Vous pouvez faire face à des choix difficiles pour déterminer précisément où appliquer la sécurité dans une application multiniveau basée sur des composants : au niveau de la base de données ?</span><span class="sxs-lookup"><span data-stu-id="1e6cf-104">You can face difficult choices in deciding precisely where to enforce security in a multi-tier, component-based application: At the database?</span></span> <span data-ttu-id="1e6cf-105">Au niveau intermédiaire ?</span><span class="sxs-lookup"><span data-stu-id="1e6cf-105">At the middle tier?</span></span> <span data-ttu-id="1e6cf-106">Dans les composants ?</span><span class="sxs-lookup"><span data-stu-id="1e6cf-106">In the components?</span></span> <span data-ttu-id="1e6cf-107">Autre chose ?</span><span class="sxs-lookup"><span data-stu-id="1e6cf-107">Somewhere else?</span></span> <span data-ttu-id="1e6cf-108">Importe?</span><span class="sxs-lookup"><span data-stu-id="1e6cf-108">Everywhere?</span></span> <span data-ttu-id="1e6cf-109">À mesure que les mécanismes de sécurité augmentent le nombre et la complexité, les baisses de performances et le comportement de l’application deviennent moins prévisibles.</span><span class="sxs-lookup"><span data-stu-id="1e6cf-109">As security mechanisms increase in number and complexity, performance declines and application behavior becomes less predictable.</span></span> <span data-ttu-id="1e6cf-110">Toutefois, vous devez vous assurer que les données sont protégées, que les règles d’entreprise sont suivies et que l’activité importante est journalisée, et que votre application fonctionne toujours pour les clients comme prévu.</span><span class="sxs-lookup"><span data-stu-id="1e6cf-110">Nevertheless, you must ensure that data is protected, business rules are followed, and significant activity is logged, and still have your application work for clients as intended.</span></span> <span data-ttu-id="1e6cf-111">Vous devez être certain que tous les chemins d’accès client à l’aide de votre application sont corrects et que les points de contrôle de sécurité que vous avez en place seront suffisants.</span><span class="sxs-lookup"><span data-stu-id="1e6cf-111">You must be certain that every client path through your application is correct and that the security checkpoints you have in place will suffice.</span></span>

<span data-ttu-id="1e6cf-112">La décision la plus difficile est souvent d’assurer la sécurité au niveau de la base de données.</span><span class="sxs-lookup"><span data-stu-id="1e6cf-112">The hardest decision is often whether to enforce security at the database.</span></span> <span data-ttu-id="1e6cf-113">Historiquement, c’est là que la sécurité est la plus étroite, car elle est perçue comme un règne qui doit être véritablement sécurisé, et les administrateurs de base de données sont très réticents à faire confiance à une autre personne pour mettre en œuvre la sécurité.</span><span class="sxs-lookup"><span data-stu-id="1e6cf-113">Historically, this is where security is tightest because it is perceived as the one kingdom that needs to be truly secure, and database administrators are very reluctant to trust someone else to enforce security for them.</span></span> <span data-ttu-id="1e6cf-114">Toutefois, l’application de la sécurité au niveau de la base de données peut être très coûteuse et difficile à mettre à l’échelle, ce qui est précisément le point d’écrire des applications multiniveaux en premier lieu.</span><span class="sxs-lookup"><span data-stu-id="1e6cf-114">But enforcing security at the database can be quite expensive and difficult to scale, which is precisely the point of writing multi-tier applications in the first place.</span></span>

<span data-ttu-id="1e6cf-115">La règle générale à suivre avec les applications multiniveaux évolutives à l’aide de COM+ est que, chaque fois que cela est possible, vous devez appliquer une sécurité détaillée dans l’application COM+ au niveau intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="1e6cf-115">The general rule to follow with scalable multi-tier applications using COM+ is that, whenever possible, you should enforce detailed security in the COM+ application at the middle tier.</span></span> <span data-ttu-id="1e6cf-116">Cela vous permet de tirer pleinement parti des services évolutifs fournis par COM+.</span><span class="sxs-lookup"><span data-stu-id="1e6cf-116">Doing so enables you to fully leverage the scalable services provided by COM+.</span></span> <span data-ttu-id="1e6cf-117">S’authentifier au niveau de la base de données uniquement lorsque vous en avez absolument besoin et peser entièrement les implications en matière de performances.</span><span class="sxs-lookup"><span data-stu-id="1e6cf-117">Authenticate at the database only when you absolutely need to, and fully weigh the performance implications of doing so.</span></span>

<span data-ttu-id="1e6cf-118">Pour plus d’informations sur les problèmes à prendre en compte lorsque vous décidez de l’emplacement des contrôles de sécurité, consultez [décider où appliquer la sécurité](deciding-where-to-enforce-security.md).</span><span class="sxs-lookup"><span data-stu-id="1e6cf-118">For a discussion of issues to consider in deciding where to perform security checks, see [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

<span data-ttu-id="1e6cf-119">Pour plus d’informations sur certains scénarios de base pour la sécurisation des applications multiniveau, consultez [scénarios de base pour la sécurisation des données dans les applications multicouches](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span><span class="sxs-lookup"><span data-stu-id="1e6cf-119">For a discussion of some basic scenarios in securing multi-tier applications, see [Basic Scenarios for Securing Data in Multi-Tier Applications](basic-scenarios-for-securing-data-in-multi-tier-applications.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e6cf-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1e6cf-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e6cf-121">Authentification du client</span><span class="sxs-lookup"><span data-stu-id="1e6cf-121">Client Authentication</span></span>](client-authentication.md)
</dt> <dt>

[<span data-ttu-id="1e6cf-122">Emprunt d’identité et délégation du client</span><span class="sxs-lookup"><span data-stu-id="1e6cf-122">Client Impersonation and Delegation</span></span>](client-impersonation-and-delegation.md)
</dt> <dt>

[<span data-ttu-id="1e6cf-123">Sécurité de l’application de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1e6cf-123">Library Application Security</span></span>](library-application-security.md)
</dt> <dt>

[<span data-ttu-id="1e6cf-124">Sécurité des composants de programmation</span><span class="sxs-lookup"><span data-stu-id="1e6cf-124">Programmatic Component Security</span></span>](programmatic-component-security.md)
</dt> <dt>

[<span data-ttu-id="1e6cf-125">Administration de la sécurité basée sur les rôles</span><span class="sxs-lookup"><span data-stu-id="1e6cf-125">Role-Based Security Administration</span></span>](role-based-security-administration.md)
</dt> <dt>

[<span data-ttu-id="1e6cf-126">Utilisation de la stratégie de restriction logicielle dans COM+</span><span class="sxs-lookup"><span data-stu-id="1e6cf-126">Using the Software Restriction Policy in COM+</span></span>](using-the-software-restriction-policy-in-com-.md)
</dt> </dl>

 

 



