---
description: Pour déterminer une stratégie de sécurité pour une application, vous devez définir les privilèges de sécurité requis.
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: Définition des rôles pour une application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e46eb2cb857a2b2dee2aabe41cb571e12ed98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513127"
---
# <a name="defining-roles-for-an-application"></a><span data-ttu-id="b5a1a-103">Définition des rôles pour une application</span><span class="sxs-lookup"><span data-stu-id="b5a1a-103">Defining Roles for an Application</span></span>

<span data-ttu-id="b5a1a-104">Pour déterminer une stratégie de sécurité pour une application, vous devez définir les privilèges de sécurité requis.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-104">You determine a security policy for an application by defining the security privileges that it requires.</span></span> <span data-ttu-id="b5a1a-105">Pour ce faire, vous devez déclarer un niveau de privilège symbolique en tant que rôle, c’est-à-dire définir le rôle de l’application, puis [attribuer le rôle](assigning-roles-to-components--interfaces--or-methods.md) à des ressources spécifiques au sein de l’application.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-105">To do this you declare a symbolic level of privilege as a role—that is, define the role for the application—and then [assign the role](assigning-roles-to-components--interfaces--or-methods.md) to specific resources within the application.</span></span> <span data-ttu-id="b5a1a-106">Cette conception est remplie lorsque l’application est déployée et que les administrateurs système remplissent le rôle avec des utilisateurs et des groupes d’utilisateurs réels.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-106">This design is fulfilled when the application is deployed and system administrators populate the role with actual users and user groups.</span></span> <span data-ttu-id="b5a1a-107">Pour plus d’informations, consultez administration de la [sécurité basée sur les rôles](role-based-security-administration.md).</span><span class="sxs-lookup"><span data-stu-id="b5a1a-107">For greater detail, see [Role-Based Security Administration](role-based-security-administration.md).</span></span>

<span data-ttu-id="b5a1a-108">**Pour ajouter un rôle à une application**</span><span class="sxs-lookup"><span data-stu-id="b5a1a-108">**To add a role to an application**</span></span>

1.  <span data-ttu-id="b5a1a-109">Dans l’arborescence de la console de l’outil d’administration Services de composants, localisez l’application COM+ à laquelle vous souhaitez ajouter le rôle.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-109">In the console tree of the Component Services administrative tool, locate the COM+ application to which you want to add the role.</span></span> <span data-ttu-id="b5a1a-110">Développez l’arborescence pour afficher les dossiers de l’application.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-110">Expand the tree to view the folders for the application.</span></span>

2.  <span data-ttu-id="b5a1a-111">Cliquez avec le bouton droit sur le dossier **rôles** pour l’application, pointez sur **nouveau**, puis cliquez sur **rôle**.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-111">Right-click the **Roles** folder for the application, point to **New**, and then click **Role**.</span></span>

3.  <span data-ttu-id="b5a1a-112">Dans la boîte de dialogue **rôle**, tapez le nom du nouveau rôle dans la zone prévue à cet effet.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-112">In the **Role** dialog box, type the name of the new role in the box provided.</span></span>

4.  <span data-ttu-id="b5a1a-113">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-113">Click **OK**.</span></span>

> [!Note]  
> <span data-ttu-id="b5a1a-114">Après avoir ajouté des rôles à l’application, vous devez vous assurer d’affecter les rôles aux composants, interfaces et méthodes appropriés.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-114">After adding roles to the application, you must be sure to assign the roles to the appropriate components, interfaces, and methods.</span></span> <span data-ttu-id="b5a1a-115">Dans le cas contraire, si la sécurité basée sur les rôles a été choisie et activée et si des rôles ont été ajoutés mais non affectés, tous les appels à l’application échouent.</span><span class="sxs-lookup"><span data-stu-id="b5a1a-115">Otherwise, if role-based security has been chosen and enabled and if roles have been added but not assigned, all calls to the application will fail.</span></span> <span data-ttu-id="b5a1a-116">Pour plus d’informations, consultez [assignation de rôles à des composants, des interfaces ou des méthodes](assigning-roles-to-components--interfaces--or-methods.md).</span><span class="sxs-lookup"><span data-stu-id="b5a1a-116">For more information, see [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b5a1a-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5a1a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5a1a-118">Assignation de rôles à des composants, des interfaces ou des méthodes</span><span class="sxs-lookup"><span data-stu-id="b5a1a-118">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="b5a1a-119">Configuration de la sécurité de Role-Based</span><span class="sxs-lookup"><span data-stu-id="b5a1a-119">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="b5a1a-120">Activation des vérifications d’accès pour une application</span><span class="sxs-lookup"><span data-stu-id="b5a1a-120">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="b5a1a-121">Activation des vérifications d’accès au niveau du composant</span><span class="sxs-lookup"><span data-stu-id="b5a1a-121">Enabling Access Checks at the Component Level</span></span>](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[<span data-ttu-id="b5a1a-122">Définition d’un niveau de sécurité pour les vérifications d’accès</span><span class="sxs-lookup"><span data-stu-id="b5a1a-122">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



