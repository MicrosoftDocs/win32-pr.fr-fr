---
description: L’exécution de cette étape permet d’effectuer des vérifications d’accès au processus ou une sécurité complète basée sur les rôles, en fonction du niveau de sécurité que vous sélectionnez et de l’activation ou non de la vérification d’accès pour des composants individuels.
ms.assetid: 266bdac1-41be-45a5-a8c7-f9c6fe08445c
title: Activation des vérifications d’accès pour une application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3d64a32b23467f85c368e088a870ebe5e4d683e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106532070"
---
# <a name="enabling-access-checks-for-an-application"></a><span data-ttu-id="de3b5-103">Activation des vérifications d’accès pour une application</span><span class="sxs-lookup"><span data-stu-id="de3b5-103">Enabling Access Checks for an Application</span></span>

<span data-ttu-id="de3b5-104">L’exécution de cette étape permet d’effectuer des vérifications d’accès au processus ou une sécurité complète basée sur les rôles, en fonction du niveau de sécurité que vous sélectionnez et de l’activation ou non de la vérification d’accès pour des composants individuels.</span><span class="sxs-lookup"><span data-stu-id="de3b5-104">Performing this step enables either process access checks or full role-based security, depending on what security level you select and whether you enable access checking for individual components.</span></span>

<span data-ttu-id="de3b5-105">**Pour activer les vérifications d’accès pour une application**</span><span class="sxs-lookup"><span data-stu-id="de3b5-105">**To enable access checks for an application**</span></span>

1.  <span data-ttu-id="de3b5-106">Dans l’arborescence de la console de l’outil d’administration Services de composants, cliquez avec le bouton droit sur l’application COM+ pour laquelle vous souhaitez activer les vérifications d’accès, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="de3b5-106">In the console tree of the Component Services administrative tool, right-click the COM+ application for which you want to enable access checks, and then click **Properties**.</span></span>

2.  <span data-ttu-id="de3b5-107">Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="de3b5-107">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="de3b5-108">Activez la case à cocher **appliquer les vérifications d’accès pour cette application** .</span><span class="sxs-lookup"><span data-stu-id="de3b5-108">Select the **Enforce access checks for this application** check box.</span></span>

4.  <span data-ttu-id="de3b5-109">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="de3b5-109">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="de3b5-110">À compter de Windows Server 2003, les vérifications d’accès sont activées par défaut lors de la création d’une application COM+.</span><span class="sxs-lookup"><span data-stu-id="de3b5-110">As of Windows Server 2003, access checks are enabled by default when creating a COM+ application.</span></span> <span data-ttu-id="de3b5-111">Les contrôles d’accès sont activés par défaut au niveau de l’application et sont désactivés par défaut au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="de3b5-111">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="de3b5-112">Auparavant, les contrôles d’accès étaient désactivés par défaut au niveau de l’application et activés par défaut au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="de3b5-112">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

<span data-ttu-id="de3b5-113">Après avoir activé les vérifications d’accès, vous devez sélectionner le niveau de sécurité approprié.</span><span class="sxs-lookup"><span data-stu-id="de3b5-113">After enabling access checks, you should select the appropriate security level.</span></span> <span data-ttu-id="de3b5-114">Consultez [définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="de3b5-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md).</span></span> <span data-ttu-id="de3b5-115">En outre, vous devez être sûr de définir des rôles et de les ajouter à l’application.</span><span class="sxs-lookup"><span data-stu-id="de3b5-115">Also, you must be sure to define roles and add them to the application.</span></span> <span data-ttu-id="de3b5-116">Si les vérifications d’accès sont activées mais qu’aucun rôle n’a été ajouté, tous les appels à l’application échouent.</span><span class="sxs-lookup"><span data-stu-id="de3b5-116">If access checks are enabled but no roles have been added, all calls to the application will fail.</span></span> <span data-ttu-id="de3b5-117">Consultez [définition des rôles pour une application](defining-roles-for-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="de3b5-117">See [Defining Roles for an Application](defining-roles-for-an-application.md).</span></span>

> [!Note]  
> <span data-ttu-id="de3b5-118">Lors du débogage de votre application, il peut être utile de désactiver la sécurité afin que vous puissiez vous concentrer sur d’autres aspects du comportement et de la conception de votre programme.</span><span class="sxs-lookup"><span data-stu-id="de3b5-118">When debugging your application, it might be helpful to disable security so that you can concentrate on other aspects of your program's behavior and design.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="de3b5-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="de3b5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de3b5-120">Assignation de rôles à des composants, des interfaces ou des méthodes</span><span class="sxs-lookup"><span data-stu-id="de3b5-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="de3b5-121">Configuration de la sécurité de Role-Based</span><span class="sxs-lookup"><span data-stu-id="de3b5-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="de3b5-122">Définition des rôles pour une application</span><span class="sxs-lookup"><span data-stu-id="de3b5-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="de3b5-123">Activation des vérifications d’accès au niveau du composant</span><span class="sxs-lookup"><span data-stu-id="de3b5-123">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="de3b5-124">Définition d’un niveau de sécurité pour les vérifications d’accès</span><span class="sxs-lookup"><span data-stu-id="de3b5-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



