---
description: Les magasins de stratégies d’autorisation, les applications et les étendues représentent différents niveaux d’organisation de la stratégie du gestionnaire d’autorisations.
ms.assetid: 235f236d-59c9-4a8c-aec6-60d1ddba4d5d
title: Magasins de stratégies, applications et étendues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4155d7bf60d34474d52c27efd50d2f53741fa73a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863026"
---
# <a name="policy-stores-applications-and-scopes"></a><span data-ttu-id="9c205-103">Magasins de stratégies, applications et étendues</span><span class="sxs-lookup"><span data-stu-id="9c205-103">Policy Stores, Applications, and Scopes</span></span>

<span data-ttu-id="9c205-104">Les magasins de stratégies d’autorisation, les applications et les étendues représentent différents niveaux d’organisation de la stratégie du gestionnaire d’autorisations.</span><span class="sxs-lookup"><span data-stu-id="9c205-104">Authorization policy stores, applications, and scopes represent different levels of organization of Authorization Manager policy.</span></span> <span data-ttu-id="9c205-105">Un magasin de stratégies peut contenir une ou plusieurs applications, et une application peut contenir une ou plusieurs étendues.</span><span class="sxs-lookup"><span data-stu-id="9c205-105">A policy store can contain one or more applications, and an application can contain one or more scopes.</span></span>

-   [<span data-ttu-id="9c205-106">Magasins de stratégies d’autorisation</span><span class="sxs-lookup"><span data-stu-id="9c205-106">Authorization Policy Stores</span></span>](#authorization-policy-stores)
-   [<span data-ttu-id="9c205-107">Applications</span><span class="sxs-lookup"><span data-stu-id="9c205-107">Applications</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="9c205-108">Étendues</span><span class="sxs-lookup"><span data-stu-id="9c205-108">Scopes</span></span>](#policy-stores-applications-and-scopes)
-   [<span data-ttu-id="9c205-109">La délégation</span><span class="sxs-lookup"><span data-stu-id="9c205-109">Delegation</span></span>](#delegation)
-   [<span data-ttu-id="9c205-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c205-110">Related topics</span></span>](#related-topics)

## <a name="authorization-policy-stores"></a><span data-ttu-id="9c205-111">Magasins de stratégies d’autorisation</span><span class="sxs-lookup"><span data-stu-id="9c205-111">Authorization Policy Stores</span></span>

<span data-ttu-id="9c205-112">Dans l’API du gestionnaire d’autorisations, un magasin de stratégies d’autorisation est représenté par un objet [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) .</span><span class="sxs-lookup"><span data-stu-id="9c205-112">In the Authorization Manager API, an authorization policy store is represented by an [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) object.</span></span> <span data-ttu-id="9c205-113">Le magasin de stratégies d’autorisation contient les définitions et les assignations des applications, des étendues, des opérations, des tâches, des rôles et des groupes d’utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9c205-113">The authorization policy store contains definitions and assignments of applications, scopes, operations, tasks, roles, and user groups.</span></span>

<span data-ttu-id="9c205-114">Un magasin de stratégies d’autorisation peut être stocké en tant que fichier XML ou Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9c205-114">An authorization policy store can be stored either as an XML file or in Active Directory.</span></span>

<span data-ttu-id="9c205-115">Une application doit initialiser un magasin de stratégies d’autorisation avant de modifier les informations dans le magasin ou d’utiliser la stratégie de stockage pour vérifier l’accès client aux ressources.</span><span class="sxs-lookup"><span data-stu-id="9c205-115">An application must initialize an authorization policy store before changing information in the store or using the store policy to check client access to resources.</span></span>

<span data-ttu-id="9c205-116">Un magasin de stratégies d’autorisation peut contenir un ou plusieurs objets [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) qui représentent chacun une stratégie d’autorisation pour une application spécifique.</span><span class="sxs-lookup"><span data-stu-id="9c205-116">An authorization policy store can contain one or more [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) objects that each represent authorization policy for a specific application.</span></span>

## <a name="applications"></a><span data-ttu-id="9c205-117">Applications</span><span class="sxs-lookup"><span data-stu-id="9c205-117">Applications</span></span>

<span data-ttu-id="9c205-118">Dans l’API du gestionnaire d’autorisations, une application est représentée par un objet [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) .</span><span class="sxs-lookup"><span data-stu-id="9c205-118">In the Authorization Manager API, an application is represented by an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object.</span></span> <span data-ttu-id="9c205-119">Un magasin de stratégies d’autorisation peut contenir des informations de stratégie d’autorisation pour de nombreuses applications.</span><span class="sxs-lookup"><span data-stu-id="9c205-119">An authorization policy store can contain authorization policy information for many applications.</span></span> <span data-ttu-id="9c205-120">L’utilisation d’objets **IAzApplication** vous permet de stocker différentes stratégies d’autorisation pour différentes applications dans un même magasin de stratégies.</span><span class="sxs-lookup"><span data-stu-id="9c205-120">Using **IAzApplication** objects allows you to store different authorization policy for different applications in a single policy store.</span></span>

<span data-ttu-id="9c205-121">Un magasin de stratégies d’autorisation doit contenir au moins une application.</span><span class="sxs-lookup"><span data-stu-id="9c205-121">An authorization policy store must contain at least one application.</span></span>

## <a name="scopes"></a><span data-ttu-id="9c205-122">Étendues</span><span class="sxs-lookup"><span data-stu-id="9c205-122">Scopes</span></span>

<span data-ttu-id="9c205-123">Dans l’API du gestionnaire d’autorisations, une étendue est représentée par un objet [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) .</span><span class="sxs-lookup"><span data-stu-id="9c205-123">In the Authorization Manager API, a scope is represented by an [**IAzScope**](/windows/desktop/api/Azroles/nn-azroles-iazscope) object.</span></span> <span data-ttu-id="9c205-124">Les étendues fournissent un niveau supplémentaire, facultatif d’organisation, pour une stratégie d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="9c205-124">Scopes provide an additional, optional level of organization for an authorization policy.</span></span> <span data-ttu-id="9c205-125">Une application peut contenir une ou plusieurs étendues, mais elle n’a pas besoin d’en contenir (le gestionnaire d’autorisations fournit une étendue par défaut à l’échelle de l’application).</span><span class="sxs-lookup"><span data-stu-id="9c205-125">An application can contain one or more scopes, but need not contain any (Authorization Manager provides a default, application-wide scope).</span></span>

<span data-ttu-id="9c205-126">Une étendue est une sous-division au sein d’une application qui sépare les ressources des autres ressources utilisées par cette application.</span><span class="sxs-lookup"><span data-stu-id="9c205-126">A scope is a subdivision within an application that separates resources from other resources that are used by that application.</span></span> <span data-ttu-id="9c205-127">Si vous disposez de groupes du gestionnaire d’autorisations, d’attributions de rôles, de définitions de rôles ou de définitions de tâches que vous ne souhaitez pas appliquer à l’ensemble de l’application, vous pouvez les créer au niveau de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="9c205-127">If you have Authorization Manager groups, role assignments, role definitions, or task definitions that you do not want to apply to an entire application, you can create them at the scope level.</span></span>

## <a name="delegation"></a><span data-ttu-id="9c205-128">La délégation</span><span class="sxs-lookup"><span data-stu-id="9c205-128">Delegation</span></span>

<span data-ttu-id="9c205-129">Les magasins de stratégies d’autorisation stockés dans Active Directory prennent en charge la délégation de l’administration.</span><span class="sxs-lookup"><span data-stu-id="9c205-129">Authorization policy stores that are stored in Active Directory support delegation of administration.</span></span> <span data-ttu-id="9c205-130">L’administration peut être déléguée à des utilisateurs et à des groupes au niveau du magasin, de l’application ou de l’étendue.</span><span class="sxs-lookup"><span data-stu-id="9c205-130">Administration can be delegated to users and groups at the store, application, or scope level.</span></span> <span data-ttu-id="9c205-131">Chaque niveau définit des rôles d’administration pour la stratégie à ce niveau.</span><span class="sxs-lookup"><span data-stu-id="9c205-131">Each level defines administrative roles for the policy at that level.</span></span> <span data-ttu-id="9c205-132">Pour déléguer le contrôle à un utilisateur ou à un groupe, affectez-le au rôle administrateur ; pour autoriser un utilisateur ou un groupe à lire la stratégie, attribuez-le au rôle lecteur.</span><span class="sxs-lookup"><span data-stu-id="9c205-132">To delegate control to a user or group, assign them to the administrator role; to allow a user or group to read the policy, assign them to the reader role.</span></span>

<span data-ttu-id="9c205-133">Les administrateurs d’un magasin, d’une application ou d’une étendue peuvent lire et modifier le magasin de stratégies au niveau délégué.</span><span class="sxs-lookup"><span data-stu-id="9c205-133">Administrators of a store, application, or scope can read and modify the policy store at the delegated level.</span></span> <span data-ttu-id="9c205-134">Les lecteurs peuvent lire le magasin de stratégies au niveau délégué, mais ne peuvent pas modifier le magasin.</span><span class="sxs-lookup"><span data-stu-id="9c205-134">Readers can read the policy store at the delegated level but cannot modify the store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c205-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c205-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c205-136">Création d’un objet du magasin de stratégies d’autorisation en C++</span><span class="sxs-lookup"><span data-stu-id="9c205-136">Creating an Authorization Policy Store Object in C++</span></span>](creating-an-authorization-policy-store-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="9c205-137">Création d’un objet d’application en C++</span><span class="sxs-lookup"><span data-stu-id="9c205-137">Creating an Application Object in C++</span></span>](creating-an-application-object-in-c--.md)
</dt> <dt>

[<span data-ttu-id="9c205-138">Délégation de la définition des autorisations en C++</span><span class="sxs-lookup"><span data-stu-id="9c205-138">Delegating the Defining of Permissions in C++</span></span>](delegating-the-defining-of-permissions-in-c--.md)
</dt> </dl>

 

 



