---
description: Assignation de rôles à des composants, des interfaces ou des méthodes
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: Assignation de rôles à des composants, des interfaces ou des méthodes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393143"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a><span data-ttu-id="be98a-103">Assignation de rôles à des composants, des interfaces ou des méthodes</span><span class="sxs-lookup"><span data-stu-id="be98a-103">Assigning Roles to Components, Interfaces, or Methods</span></span>

<span data-ttu-id="be98a-104">Vous pouvez affecter explicitement un rôle à n’importe quel élément d’une application COM+ qui est visible à l’aide de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="be98a-104">You can explicitly assign a role to any item within a COM+ application that is visible through the Component Services administrative tool.</span></span> <span data-ttu-id="be98a-105">Cela garantit que tous les utilisateurs membres du rôle seront autorisés à accéder à cet élément et à tous les autres éléments qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="be98a-105">Doing so ensures that any users that are members of the role will be permitted access to that item and any other items that it contains.</span></span> <span data-ttu-id="be98a-106">Par exemple, si vous affectez le rôle « Readers » à un composant, n’importe quel membre de « Readers » est autorisé à accéder à ce composant et à toutes les interfaces et méthodes qu’il expose.</span><span class="sxs-lookup"><span data-stu-id="be98a-106">For example, if you assign the role "Readers" to a component, any member of "Readers" is allowed access to that component and any interfaces and methods it exposes.</span></span> <span data-ttu-id="be98a-107">« Readers » s’affichera en tant que rôle hérité pour l’une de ces interfaces et méthodes.</span><span class="sxs-lookup"><span data-stu-id="be98a-107">"Readers" will show up as an Inherited role for any of those interfaces and methods.</span></span>

<span data-ttu-id="be98a-108">Une méthode est accessible aux appelants uniquement si vous lui assignez un rôle, soit en affectant explicitement le rôle directement à la méthode, soit en affectant un rôle à l’interface de la méthode ou au composant de la méthode, auquel cas le rôle est hérité par la méthode.</span><span class="sxs-lookup"><span data-stu-id="be98a-108">A method is accessible to callers only if you assign a role to it, either by explicitly assigning the role directly to the method or by assigning a role to the method's interface or the method's component, in which case the role will be inherited by the method.</span></span> <span data-ttu-id="be98a-109">Si aucun rôle n’est assigné et si les contrôles d’accès sont activés, tous les appels à la méthode échouent.</span><span class="sxs-lookup"><span data-stu-id="be98a-109">If no role is assigned and if access checks are enabled, all calls to the method will fail.</span></span>

<span data-ttu-id="be98a-110">Avant de pouvoir assigner un rôle, vous devez le [définir](defining-roles-for-an-application.md) pour l’application.</span><span class="sxs-lookup"><span data-stu-id="be98a-110">Before you can assign a role, you must [define](defining-roles-for-an-application.md) it for the application.</span></span> <span data-ttu-id="be98a-111">Tous les rôles définis pour l’application s’affichent dans la fenêtre **rôles explicitement définis pour les éléments sélectionnés** dans l’onglet **sécurité** pour les composants, les méthodes et les interfaces de l’application.</span><span class="sxs-lookup"><span data-stu-id="be98a-111">All roles defined for the application will appear in the **Roles explicitly set for selected item(s)** window on the **Security** tab for any components, methods, and interfaces within the application.</span></span>

<span data-ttu-id="be98a-112">**Pour assigner des rôles à un composant, une méthode ou une interface**</span><span class="sxs-lookup"><span data-stu-id="be98a-112">**To assign roles to a component, method, or interface**</span></span>

1.  <span data-ttu-id="be98a-113">Dans l’arborescence de la console de l’outil d’administration Services de composants, localisez l’application COM+ pour laquelle le rôle a été défini.</span><span class="sxs-lookup"><span data-stu-id="be98a-113">In the console tree of the Component Services administrative tool, locate the COM+ application for which the role has been defined.</span></span> <span data-ttu-id="be98a-114">Développez l’arborescence pour afficher les composants, les interfaces ou les méthodes de l’application, en fonction de ce à quoi vous affectez le rôle.</span><span class="sxs-lookup"><span data-stu-id="be98a-114">Expand the tree to view the application's components, interfaces, or methods, depending on what you are assigning the role to.</span></span>

2.  <span data-ttu-id="be98a-115">Cliquez avec le bouton droit sur l’élément auquel vous souhaitez affecter le rôle, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="be98a-115">Right-click the item to which you want to assign the role, and then click **Properties**.</span></span>

3.  <span data-ttu-id="be98a-116">Dans la boîte de dialogue Propriétés, cliquez sur l’onglet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="be98a-116">In the properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="be98a-117">Dans la zone **rôles définis explicitement pour le ou les éléments sélectionnés** , sélectionnez les rôles que vous souhaitez affecter à l’élément.</span><span class="sxs-lookup"><span data-stu-id="be98a-117">In the **Roles explicitly set for selected item(s)** box, select the roles that you want to assign to the item.</span></span>

5.  <span data-ttu-id="be98a-118">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="be98a-118">Click **OK**.</span></span>

<span data-ttu-id="be98a-119">Tous les rôles que vous avez définis explicitement pour un élément sont hérités par les éléments de niveau inférieur qu’il contient et s’affichent dans la fenêtre **rôles hérités par élément sélectionné** pour ces éléments.</span><span class="sxs-lookup"><span data-stu-id="be98a-119">Any roles that you have explicitly set for an item will be inherited by any lower-level items it contains and will show up in the **Roles inherited by selected item(s)** window for those items.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be98a-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="be98a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be98a-121">Configuration de la sécurité de Role-Based</span><span class="sxs-lookup"><span data-stu-id="be98a-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="be98a-122">Définition des rôles pour une application</span><span class="sxs-lookup"><span data-stu-id="be98a-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="be98a-123">Activation des vérifications d’accès pour une application</span><span class="sxs-lookup"><span data-stu-id="be98a-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="be98a-124">Activation des vérifications d’accès au niveau du composant</span><span class="sxs-lookup"><span data-stu-id="be98a-124">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="be98a-125">Définition d’un niveau de sécurité pour les vérifications d’accès</span><span class="sxs-lookup"><span data-stu-id="be98a-125">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



