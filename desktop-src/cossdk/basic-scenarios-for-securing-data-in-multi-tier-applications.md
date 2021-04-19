---
description: Cette rubrique présente quelques scénarios de bloc de construction, illustrant les critères décrits dans décider où appliquer la sécurité.
ms.assetid: e9820e53-8891-4bff-a333-00ad2dbb03a4
title: Scénarios de base pour la sécurisation des données dans les applications multiniveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7929bcfeba96b43b7ec91513b42ffb7f46266613
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515568"
---
# <a name="basic-scenarios-for-securing-data-in-multi-tier-applications"></a><span data-ttu-id="82eab-103">Scénarios de base pour la sécurisation des données dans les applications multiniveau</span><span class="sxs-lookup"><span data-stu-id="82eab-103">Basic Scenarios for Securing Data in Multi-Tier Applications</span></span>

<span data-ttu-id="82eab-104">Cette rubrique présente quelques scénarios de bloc de construction, illustrant les critères décrits dans [décider où appliquer la sécurité](deciding-where-to-enforce-security.md).</span><span class="sxs-lookup"><span data-stu-id="82eab-104">This topic presents a few building-block scenarios, illustrating the criteria discussed in [Deciding Where to Enforce Security](deciding-where-to-enforce-security.md).</span></span>

## <a name="trusted-server-scenario"></a><span data-ttu-id="82eab-105">Scénario de serveur approuvé</span><span class="sxs-lookup"><span data-stu-id="82eab-105">Trusted Server Scenario</span></span>

-   <span data-ttu-id="82eab-106">La base de données fait confiance entièrement à l’application COM+ pour authentifier et autoriser les utilisateurs finaux à accéder aux données de la base de données.</span><span class="sxs-lookup"><span data-stu-id="82eab-106">The database fully trusts the COM+ application to authenticate and authorize end users to access data in the database.</span></span>
-   <span data-ttu-id="82eab-107">De préférence, la base de données est sécurisée par rapport à tout accès sauf via l’application.</span><span class="sxs-lookup"><span data-stu-id="82eab-107">Preferably, the database is secured against any access except through the application.</span></span>
-   <span data-ttu-id="82eab-108">L’application COM+ utilise la sécurité basée sur les rôles pour autoriser les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="82eab-108">The COM+ application uses role-based security to authorize users.</span></span>
-   <span data-ttu-id="82eab-109">Les connexions s’ouvrent sous l’identité de l’application COM+ et sont entièrement regroupées.</span><span class="sxs-lookup"><span data-stu-id="82eab-109">Connections are opened under the COM+ application's identity and are fully poolable.</span></span>
-   <span data-ttu-id="82eab-110">L’audit et la journalisation peuvent être effectuées par l’application COM+, ou ces informations peuvent être transmises à la base de données par l’application.</span><span class="sxs-lookup"><span data-stu-id="82eab-110">Auditing and logging can be done by the COM+ application, or this information can be passed into the database by the application.</span></span>

<span data-ttu-id="82eab-111">Ce scénario fonctionne mieux pour les données accessibles par des catégories prévisibles d’utilisateurs qui peuvent être encapsulées dans des rôles.</span><span class="sxs-lookup"><span data-stu-id="82eab-111">This scenario works best for data that can be accessed by predictable categories of users that can be encapsulated in roles.</span></span> <span data-ttu-id="82eab-112">Par exemple, seuls les « responsables », les « responsables » et les « comptables » sont autorisés à accéder aux comptes.</span><span class="sxs-lookup"><span data-stu-id="82eab-112">For example, only "Managers," "Tellers," and "Accountants" have permission to access accounts.</span></span> <span data-ttu-id="82eab-113">La logique métier de ce que chaque est autorisé à faire est appliquée dans la couche intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="82eab-113">The business logic of what precisely each is enabled to do is enforced in the middle tier.</span></span>

## <a name="impersonation-scenario"></a><span data-ttu-id="82eab-114">Scénario d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="82eab-114">Impersonation Scenario</span></span>

-   <span data-ttu-id="82eab-115">La base de données effectue sa propre authentification et autorisation des utilisateurs finaux pour limiter l’accès aux données de la base de données.</span><span class="sxs-lookup"><span data-stu-id="82eab-115">The database does its own authentication and authorization of end users to help limit access to data in the database.</span></span>
-   <span data-ttu-id="82eab-116">L’application COM+ emprunte l’identité des clients chaque fois qu’ils accèdent à la base de données.</span><span class="sxs-lookup"><span data-stu-id="82eab-116">The COM+ application impersonates clients whenever it is accessing the database.</span></span>
-   <span data-ttu-id="82eab-117">Les connexions sont établies par appel et ne peuvent pas être réutilisées.</span><span class="sxs-lookup"><span data-stu-id="82eab-117">Connections are made on a per-call basis and can't be reused.</span></span>

<span data-ttu-id="82eab-118">Ce scénario fonctionne mieux pour les données étroitement liées à de très petites classes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="82eab-118">This scenario works best for data that is closely bound to very small classes of users.</span></span> <span data-ttu-id="82eab-119">Par exemple, chaque employé peut accéder uniquement à son propre fichier personnel, et chaque responsable peut accéder uniquement aux fichiers de personnel de ses rapports.</span><span class="sxs-lookup"><span data-stu-id="82eab-119">For example, each employee can access only his own personnel file, and each manager can access only the personnel files of her reports.</span></span>

## <a name="hybrid-scenario"></a><span data-ttu-id="82eab-120">Scénario hybride</span><span class="sxs-lookup"><span data-stu-id="82eab-120">Hybrid Scenario</span></span>

<span data-ttu-id="82eab-121">Une combinaison des deux scénarios précédents, où l’emprunt d’identité est utilisé uniquement lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="82eab-121">A combination of the preceding two scenarios, where impersonation is used only when it is needed.</span></span>

<span data-ttu-id="82eab-122">Ce scénario fonctionne mieux dans les situations où vous avez des relations de données utilisateur hybrides.</span><span class="sxs-lookup"><span data-stu-id="82eab-122">This scenario works best in situations where you have hybrid user-data relationships.</span></span> <span data-ttu-id="82eab-123">Par exemple, vous avez des « responsables », des « responsables », des « comptables » et des milliers de clients Web individuels qui peuvent accéder à leurs propres comptes uniquement.</span><span class="sxs-lookup"><span data-stu-id="82eab-123">For example, you have "Managers," "Tellers," "Accountants," and thousands of individual Web clients who can access just their own accounts.</span></span> <span data-ttu-id="82eab-124">Vous pouvez séparer les chemins logiques via l’application, éventuellement avec des composants distincts, pour gérer la dernière classe d’utilisateurs, en particulier lorsque les hypothèses de performances pour ces utilisateurs sont différentes.</span><span class="sxs-lookup"><span data-stu-id="82eab-124">You can separate logic paths through the application, potentially with separate components, to handle the latter class of users, particularly where performance assumptions for those users are different.</span></span>

## <a name="trusted-scenario-using-microsoft-sql-server-roles"></a><span data-ttu-id="82eab-125">Scénario approuvé à l’aide de rôles de Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="82eab-125">Trusted Scenario Using Microsoft SQL Server Roles</span></span>

-   <span data-ttu-id="82eab-126">Microsoft SQL Server 7,0 et versions ultérieures peuvent autoriser l’accès à des lignes spécifiques à l’aide de rôles, mais il fait confiance à l’application COM+ pour authentifier et autoriser les utilisateurs et les mapper aux rôles appropriés dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="82eab-126">Microsoft SQL Server 7.0 and later can authorize access to specific rows using roles but trusts the COM+ application to authenticate and authorize users and to map them to the correct roles in the database.</span></span>
-   <span data-ttu-id="82eab-127">L’application COM+ autorise les utilisateurs à utiliser la sécurité basée sur les rôles, et les rôles d’application correspondent bien aux rôles de base de données.</span><span class="sxs-lookup"><span data-stu-id="82eab-127">The COM+ application authorizes users using role-based security, and the application roles correspond well to database roles.</span></span>
-   <span data-ttu-id="82eab-128">Des connexions spécifiques à un rôle de base de données particulier peuvent être ouvertes.</span><span class="sxs-lookup"><span data-stu-id="82eab-128">Connections can be opened that are specific to a particular database role.</span></span> <span data-ttu-id="82eab-129">Ces connexions peuvent être réutilisées si elles sont conservées par des objets regroupés dans les applications COM+.</span><span class="sxs-lookup"><span data-stu-id="82eab-129">These connections can be reused if they are held by pooled objects in the COM+ applications.</span></span> <span data-ttu-id="82eab-130">Pour plus d’informations sur la façon de procéder, consultez mise en [pool d’objets com+](com--object-pooling.md).</span><span class="sxs-lookup"><span data-stu-id="82eab-130">For details on how to do this, see [COM+ Object Pooling](com--object-pooling.md).</span></span>
-   <span data-ttu-id="82eab-131">L’audit et la journalisation peuvent être effectuées par l’application COM+, ou ces informations peuvent être transmises à la base de données par l’application.</span><span class="sxs-lookup"><span data-stu-id="82eab-131">Auditing and logging can be done by the COM+ application, or this information can be passed in to the database by the application.</span></span>

<span data-ttu-id="82eab-132">Ce scénario fonctionne mieux pour généralement les mêmes types d’utilisateurs et de données que dans le premier scénario de serveur approuvé, car l’application COM+ est toujours largement fiable pour gérer correctement l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="82eab-132">This scenario works best for generally the same kinds of users and data as in the first trusted server scenario because the COM+ application is still being largely trusted to handle authorization correctly.</span></span> <span data-ttu-id="82eab-133">Toutefois, il permet de protéger la base de données contre tout accès non autorisé, tout en autorisant l’accès à partir de plusieurs sources en dehors de l’application COM+, sans entraîner de pénalités de mise à l’échelle et de performances dans le scénario d’emprunt d’identité.</span><span class="sxs-lookup"><span data-stu-id="82eab-133">However, it does help protect the database against unauthorized access while allowing access potentially from multiple sources outside the COM+ application, without incurring the scaling and performance penalties present with the impersonation scenario.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82eab-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="82eab-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82eab-135">Choix de l’emplacement de l’application de la sécurité</span><span class="sxs-lookup"><span data-stu-id="82eab-135">Deciding Where to Enforce Security</span></span>](deciding-where-to-enforce-security.md)
</dt> <dt>

[<span data-ttu-id="82eab-136">Sécurité des applications multiniveau</span><span class="sxs-lookup"><span data-stu-id="82eab-136">Multi-Tier Application Security</span></span>](multi-tier-application-security.md)
</dt> </dl>

 

 



