---
description: Une fois que vous avez activé les vérifications d’accès, pour votre application COM+, vous devez sélectionner le niveau auquel vous souhaitez que les vérifications d’accès soient effectuées.
ms.assetid: 9c044add-7761-4378-b7eb-bf4e84e913b3
title: Définition d’un niveau de sécurité pour les vérifications d’accès
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 646a49a4966bff7c593f12cb7481f4a4aad8859e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111279"
---
# <a name="setting-a-security-level-for-access-checks"></a><span data-ttu-id="8e431-103">Définition d’un niveau de sécurité pour les vérifications d’accès</span><span class="sxs-lookup"><span data-stu-id="8e431-103">Setting a Security Level for Access Checks</span></span>

<span data-ttu-id="8e431-104">Une fois que vous avez activé les [vérifications d’accès](enabling-access-checks-for-an-application.md), pour votre application com+, vous devez sélectionner le niveau auquel vous souhaitez que les vérifications d’accès soient effectuées.</span><span class="sxs-lookup"><span data-stu-id="8e431-104">After you have enabled [access checks](enabling-access-checks-for-an-application.md), for your COM+ application, you must select the level at which you wish to have access checks performed.</span></span>

<span data-ttu-id="8e431-105">**Pour sélectionner un niveau de sécurité**</span><span class="sxs-lookup"><span data-stu-id="8e431-105">**To select a security level**</span></span>

1.  <span data-ttu-id="8e431-106">Dans l’arborescence de la console de l’outil d’administration Services de composants, cliquez avec le bouton droit sur l’application COM+ pour laquelle vous souhaitez activer les vérifications d’accès, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="8e431-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="8e431-107">Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="8e431-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="8e431-108">Sous **niveau de sécurité**, sélectionnez l’une des options suivantes :</span><span class="sxs-lookup"><span data-stu-id="8e431-108">Under **Security level**, select one of the following:</span></span>

    -   <span data-ttu-id="8e431-109">**Effectuer des vérifications d’accès uniquement au niveau du processus**: ce paramètre indique que les utilisateurs dans les rôles affectés à l’application seront ajoutés au descripteur de sécurité du processus.</span><span class="sxs-lookup"><span data-stu-id="8e431-109">**Perform access checks only at the process level**— This setting indicates that users in roles that are assigned to the application will be added to the process security descriptor.</span></span> <span data-ttu-id="8e431-110">Cela a les effets et les implications suivants :</span><span class="sxs-lookup"><span data-stu-id="8e431-110">This has the following effects and implications:</span></span>

        <span data-ttu-id="8e431-111">La vérification des rôles affinée est désactivée au niveau du composant, de la méthode et de l’interface.</span><span class="sxs-lookup"><span data-stu-id="8e431-111">Fine-grained role checking is turned off at the component, method, and interface levels.</span></span> <span data-ttu-id="8e431-112">Les vérifications de sécurité sont effectuées uniquement au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="8e431-112">Security checks are performed only at the application level.</span></span>

        <span data-ttu-id="8e431-113">La propriété de sécurité n’est pas incluse dans le contexte pour les objets qui s’exécutent dans l’application.</span><span class="sxs-lookup"><span data-stu-id="8e431-113">The security property is not included on the context for any objects running within the application.</span></span> <span data-ttu-id="8e431-114">Cela peut affecter la manière dont les objets sont activés.</span><span class="sxs-lookup"><span data-stu-id="8e431-114">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="8e431-115">Consultez la [propriété contexte de sécurité](security-context-property.md).</span><span class="sxs-lookup"><span data-stu-id="8e431-115">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="8e431-116">Le contexte de l’appel de sécurité ne sera pas mis à disposition.</span><span class="sxs-lookup"><span data-stu-id="8e431-116">The security call context will not be made available.</span></span> <span data-ttu-id="8e431-117">La sécurité par programme qui s’appuie sur les informations de contexte d’appel de sécurité ne fonctionnera pas.</span><span class="sxs-lookup"><span data-stu-id="8e431-117">Programmatic security that relies on security call context information will not function.</span></span> <span data-ttu-id="8e431-118">Consultez les informations de contexte de l' [appel de sécurité](security-call-context-information.md).</span><span class="sxs-lookup"><span data-stu-id="8e431-118">See [Security Call Context Information](security-call-context-information.md).</span></span>

    -   <span data-ttu-id="8e431-119">**Effectuer des vérifications d’accès au niveau du processus et du composant**: ce paramètre indique que les contrôles du descripteur de sécurité au niveau du processus et les vérifications de sécurité basées sur les rôles sont effectués intégralement.</span><span class="sxs-lookup"><span data-stu-id="8e431-119">**Perform access checks at the process and component level**—This setting indicates that process-level security descriptor checks and full role-based security checks will be performed.</span></span> <span data-ttu-id="8e431-120">Cela a les effets et les implications suivants :</span><span class="sxs-lookup"><span data-stu-id="8e431-120">This has the following effects and implications:</span></span>

        <span data-ttu-id="8e431-121">Pour activer la vérification de rôle pour des composants particuliers, vous devez [activer les vérifications d’accès au niveau du composant](enabling-access-checks-at-the-component-level.md).</span><span class="sxs-lookup"><span data-stu-id="8e431-121">To enable role checking for particular components, you must [enable access checks at the component level](enabling-access-checks-at-the-component-level.md).</span></span>

        <span data-ttu-id="8e431-122">La propriété de sécurité est incluse dans le contexte des objets qui s’exécutent dans l’application.</span><span class="sxs-lookup"><span data-stu-id="8e431-122">The security property is included on the context for any objects running within the application.</span></span> <span data-ttu-id="8e431-123">Cela peut affecter la manière dont les objets sont activés.</span><span class="sxs-lookup"><span data-stu-id="8e431-123">This can potentially affect how objects are activated.</span></span> <span data-ttu-id="8e431-124">Consultez la [propriété contexte de sécurité](security-context-property.md).</span><span class="sxs-lookup"><span data-stu-id="8e431-124">See [Security Context Property](security-context-property.md).</span></span>

        <span data-ttu-id="8e431-125">Le contexte de l’appel de sécurité est disponible.</span><span class="sxs-lookup"><span data-stu-id="8e431-125">The security call context is available.</span></span> <span data-ttu-id="8e431-126">La sécurité basée sur les rôles par programmation est activée.</span><span class="sxs-lookup"><span data-stu-id="8e431-126">Programmatic role-based security is enabled.</span></span> <span data-ttu-id="8e431-127">Consultez les informations de contexte de l' [appel de sécurité](security-call-context-information.md).</span><span class="sxs-lookup"><span data-stu-id="8e431-127">See [Security Call Context Information](security-call-context-information.md).</span></span>

        > [!Note]  
        > <span data-ttu-id="8e431-128">Pour les applications de bibliothèque COM+, vous devez choisir de vérifier les niveaux au niveau du processus et au niveau du composant pour que les contrôles d’accès pertinents fonctionnent.</span><span class="sxs-lookup"><span data-stu-id="8e431-128">For COM+ library applications, you must choose to check both at process and at component levels for any meaningful access checking to work.</span></span> <span data-ttu-id="8e431-129">Les applications de bibliothèque s’appuient sur le processus hôte pour la sécurité au niveau du processus.</span><span class="sxs-lookup"><span data-stu-id="8e431-129">Library applications rely on the host process for process-level security.</span></span> <span data-ttu-id="8e431-130">Vous pouvez déterminer la manière dont l’application de bibliothèque interagit avec l’authentification effectuée par le processus hôte en [définissant l’authentification](enabling-authentication-for-a-library-application.md).</span><span class="sxs-lookup"><span data-stu-id="8e431-130">You can determine how the library application interacts with authentication performed by the host process by [setting authentication](enabling-authentication-for-a-library-application.md).</span></span> <span data-ttu-id="8e431-131">Pour plus d’informations, consultez [bibliothèque de sécurité des applications](library-application-security.md).</span><span class="sxs-lookup"><span data-stu-id="8e431-131">For more information, see [Library Application Security](library-application-security.md).</span></span>

         

4.  <span data-ttu-id="8e431-132">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="8e431-132">Click **OK**.</span></span>

<span data-ttu-id="8e431-133">Lors du prochain démarrage de l’application, la sécurité est automatiquement vérifiée au niveau spécifié.</span><span class="sxs-lookup"><span data-stu-id="8e431-133">The next time the application is started, security will automatically be checked at the specified level.</span></span> <span data-ttu-id="8e431-134">Seuls les utilisateurs affectés aux rôles affectés à l’application auront accès à l’application.</span><span class="sxs-lookup"><span data-stu-id="8e431-134">Only users assigned to roles assigned to the application will be given access to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e431-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e431-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e431-136">Assignation de rôles à des composants, des interfaces ou des méthodes</span><span class="sxs-lookup"><span data-stu-id="8e431-136">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="8e431-137">Configuration de la sécurité de Role-Based</span><span class="sxs-lookup"><span data-stu-id="8e431-137">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="8e431-138">Définition des rôles pour une application</span><span class="sxs-lookup"><span data-stu-id="8e431-138">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="8e431-139">Activation des vérifications d’accès pour une application</span><span class="sxs-lookup"><span data-stu-id="8e431-139">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="8e431-140">Activation des vérifications d’accès au niveau du composant</span><span class="sxs-lookup"><span data-stu-id="8e431-140">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> </dl>

 

 



