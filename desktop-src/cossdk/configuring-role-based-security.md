---
description: Si votre application COM+ utilise la sécurité basée sur les rôles, vous devez effectuer plusieurs tâches.
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: Configuration de la sécurité de Role-Based
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eafa71430dfa13f497b0e4f7f7cea45229a422e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317833"
---
# <a name="configuring-role-based-security"></a><span data-ttu-id="e97b9-103">Configuration de la sécurité de Role-Based</span><span class="sxs-lookup"><span data-stu-id="e97b9-103">Configuring Role-Based Security</span></span>

<span data-ttu-id="e97b9-104">Si votre application COM+ utilise la sécurité basée sur les rôles, vous devez effectuer plusieurs tâches.</span><span class="sxs-lookup"><span data-stu-id="e97b9-104">If your COM+ application uses role-based security, there are several tasks that need to be completed.</span></span> <span data-ttu-id="e97b9-105">Lors de la conception des composants de votre application, vous définissez les rôles nécessaires pour protéger l’accès à ces composants.</span><span class="sxs-lookup"><span data-stu-id="e97b9-105">When designing the components in your application, you define the roles that are necessary to help protect access to those components.</span></span> <span data-ttu-id="e97b9-106">Vous pouvez également choisir les rôles à assigner aux composants, interfaces et méthodes de l’application.</span><span class="sxs-lookup"><span data-stu-id="e97b9-106">You also decide which roles to assign to the application's components, interfaces, and methods.</span></span> <span data-ttu-id="e97b9-107">Pendant l’intégration de l’application, vous utilisez l’outil d’administration Services de composants pour ajouter les rôles définis à l’application et assigner chaque rôle aux composants, interfaces et méthodes appropriés.</span><span class="sxs-lookup"><span data-stu-id="e97b9-107">During application integration, you use the Component Services administrative tool to add the defined roles to the application and assign each role to the appropriate components, interfaces, and methods.</span></span>

<span data-ttu-id="e97b9-108">Dans Configuration de la sécurité basée sur les rôles, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="e97b9-108">In configuring role-based security, you perform the following steps:</span></span>

1.  <span data-ttu-id="e97b9-109">Activez les vérifications d’accès au niveau de l’application.</span><span class="sxs-lookup"><span data-stu-id="e97b9-109">Enable access checks at the application level.</span></span> <span data-ttu-id="e97b9-110">Pour activer la vérification de la sécurité pour une application.</span><span class="sxs-lookup"><span data-stu-id="e97b9-110">To turn on security checking for an application.</span></span> <span data-ttu-id="e97b9-111">Pour plus d’informations sur l’exécution de cette étape, consultez [activation des vérifications d’accès pour une application](enabling-access-checks-for-an-application.md) .</span><span class="sxs-lookup"><span data-stu-id="e97b9-111">See [Enabling Access Checks for an Application](enabling-access-checks-for-an-application.md) for details on how to perform this step.</span></span>
2.  <span data-ttu-id="e97b9-112">Définissez le niveau de sécurité pour les vérifications d’accès.</span><span class="sxs-lookup"><span data-stu-id="e97b9-112">Set security level for access checks.</span></span> <span data-ttu-id="e97b9-113">Pour définir la sécurité au niveau du processus ou au niveau du processus et du composant.</span><span class="sxs-lookup"><span data-stu-id="e97b9-113">To set security either at process or at process and component level.</span></span> <span data-ttu-id="e97b9-114">Pour plus d’informations sur l’exécution de cette étape, consultez [définition d’un niveau de sécurité pour les vérifications d’accès](setting-a-security-level-for-access-checks.md) .</span><span class="sxs-lookup"><span data-stu-id="e97b9-114">See [Setting a Security Level for Access Checks](setting-a-security-level-for-access-checks.md) for details on how to perform this step.</span></span>
3.  <span data-ttu-id="e97b9-115">Activez les vérifications d’accès au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="e97b9-115">Enable access checks at the component level.</span></span> <span data-ttu-id="e97b9-116">Pour activer la vérification de la sécurité au niveau du composant, de l’interface et de la méthode.</span><span class="sxs-lookup"><span data-stu-id="e97b9-116">To turn on security checking at the component, interface, and method levels.</span></span> <span data-ttu-id="e97b9-117">Pour plus d’informations sur l’exécution de cette étape, consultez [activation des vérifications d’accès au niveau du composant](enabling-access-checks-at-the-component-level.md) .</span><span class="sxs-lookup"><span data-stu-id="e97b9-117">See [Enabling Access Checks at the Component Level](enabling-access-checks-at-the-component-level.md) for details on how to perform this step.</span></span>
4.  <span data-ttu-id="e97b9-118">Définir des rôles pour une application.</span><span class="sxs-lookup"><span data-stu-id="e97b9-118">Define roles for an application.</span></span> <span data-ttu-id="e97b9-119">Pour créer des rôles pour une application.</span><span class="sxs-lookup"><span data-stu-id="e97b9-119">To create roles for an application.</span></span> <span data-ttu-id="e97b9-120">Pour plus d’informations sur l’exécution de cette étape, consultez [définition de rôles pour une application](defining-roles-for-an-application.md) .</span><span class="sxs-lookup"><span data-stu-id="e97b9-120">See [Defining Roles for an Application](defining-roles-for-an-application.md) for details on how to perform this step.</span></span>
5.  <span data-ttu-id="e97b9-121">Assignez des rôles à des composants, des interfaces ou des méthodes.</span><span class="sxs-lookup"><span data-stu-id="e97b9-121">Assign roles to components, interfaces, or methods.</span></span> <span data-ttu-id="e97b9-122">Pour assigner des rôles à des ressources spécifiques au sein d’une application.</span><span class="sxs-lookup"><span data-stu-id="e97b9-122">To assign roles to specific resources within an application.</span></span> <span data-ttu-id="e97b9-123">Pour plus d’informations sur l’exécution de cette étape [, consultez assignation de rôles à des composants, des interfaces ou des méthodes](assigning-roles-to-components--interfaces--or-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="e97b9-123">See [Assigning Roles to Components, Interfaces, or Methods](assigning-roles-to-components--interfaces--or-methods.md) for details on how to perform this step.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e97b9-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e97b9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e97b9-125">Configuration de la stratégie de restriction logicielle</span><span class="sxs-lookup"><span data-stu-id="e97b9-125">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="e97b9-126">Définition d’un niveau d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="e97b9-126">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 



