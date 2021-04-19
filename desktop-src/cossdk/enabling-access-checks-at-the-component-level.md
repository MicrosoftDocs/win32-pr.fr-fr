---
description: Activation des vérifications d’accès au niveau du composant
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: Activation des vérifications d’accès au niveau du composant
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5da2de5f9d2f4f2d39f43330c8320c0bb0218bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513922"
---
# <a name="enabling-access-checks-at-the-component-level"></a><span data-ttu-id="20df1-103">Activation des vérifications d’accès au niveau du composant</span><span class="sxs-lookup"><span data-stu-id="20df1-103">Enabling Access Checks at the Component Level</span></span>

<span data-ttu-id="20df1-104">Si votre application comprend un composant qui n’a pas besoin de vérifications de sécurité, vous pouvez décider de désactiver les vérifications de rôle pour ce composant afin d’améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="20df1-104">If your application includes a component that does not need security checks, you might decide to disable role checks for that component to improve performance.</span></span> <span data-ttu-id="20df1-105">Ou lors du débogage, il peut être utile de désactiver la sécurité afin que vous puissiez vous concentrer sur d’autres aspects de la fonctionnalité du programme.</span><span class="sxs-lookup"><span data-stu-id="20df1-105">Or when debugging, it might be helpful to disable security so that you can concentrate on other aspects of program functionality.</span></span>

<span data-ttu-id="20df1-106">Par défaut, lorsque vous installez un composant, les vérifications d’accès au niveau du composant sont activées.</span><span class="sxs-lookup"><span data-stu-id="20df1-106">By default, when you install a component, component-level access checks are enabled.</span></span> <span data-ttu-id="20df1-107">Toutefois, cela ne prend effet que lorsque les [contrôles d’accès au niveau](enabling-access-checks-for-an-application.md) de l’application sont activés et lorsque le [niveau de sécurité](setting-a-security-level-for-access-checks.md) est défini pour effectuer des **vérifications d’accès au niveau du processus et du composant**.</span><span class="sxs-lookup"><span data-stu-id="20df1-107">However, this takes effect only when [application-level access checks](enabling-access-checks-for-an-application.md) are enabled and when the [security level](setting-a-security-level-for-access-checks.md) is set to **Perform access checks at the process and component level**.</span></span>

<span data-ttu-id="20df1-108">**Pour activer ou désactiver les vérifications d’accès au niveau du composant**</span><span class="sxs-lookup"><span data-stu-id="20df1-108">**To enable or disable access checks at the component level**</span></span>

1.  <span data-ttu-id="20df1-109">Dans l’arborescence de la console de l’outil d’administration Services de composants, recherchez l’application COM+ qui contient le composant pour lequel vous souhaitez désactiver (ou activer) les vérifications de rôle.</span><span class="sxs-lookup"><span data-stu-id="20df1-109">In the console tree of the Component Services administrative tool, locate the COM+ application that contains the component for which you want to disable (or enable) role checks.</span></span> <span data-ttu-id="20df1-110">Développez la vue dans l’arborescence pour afficher les composants dans le dossier **composants** .</span><span class="sxs-lookup"><span data-stu-id="20df1-110">Expand the view in the tree to view the components in the **Components** folder.</span></span>

2.  <span data-ttu-id="20df1-111">Cliquez avec le bouton droit sur le composant pour lequel vous souhaitez activer les vérifications de rôle, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="20df1-111">Right-click the component for which you want to enable role checks, and then click **Properties**.</span></span>

3.  <span data-ttu-id="20df1-112">Dans la boîte de dialogue Propriétés du composant, cliquez sur l’onglet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="20df1-112">In the component properties dialog box, click the **Security** tab.</span></span>

4.  <span data-ttu-id="20df1-113">Sélectionnez **appliquer les vérifications d’accès au niveau du composant** pour appliquer les vérifications au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="20df1-113">Select **Enforce component level access checks** to enforce component-level checks.</span></span>

5.  <span data-ttu-id="20df1-114">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="20df1-114">Click **OK**.</span></span>

<span data-ttu-id="20df1-115">Le nouveau paramètre prendra effet lors du prochain démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="20df1-115">The new setting will take effect the next time the application is started.</span></span>

> [!Note]  
> <span data-ttu-id="20df1-116">À compter de Windows Server 2003, les contrôles d’accès au niveau du composant sont désactivés par défaut lors de la création d’une application COM+.</span><span class="sxs-lookup"><span data-stu-id="20df1-116">As of Windows Server 2003, component-level access checks are disabled by default when creating a COM+ application.</span></span> <span data-ttu-id="20df1-117">Les contrôles d’accès sont activés par défaut au niveau de l’application et sont désactivés par défaut au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="20df1-117">Access checks are enabled by default at the application level and disabled by default at the component level.</span></span> <span data-ttu-id="20df1-118">Auparavant, les contrôles d’accès étaient désactivés par défaut au niveau de l’application et activés par défaut au niveau du composant.</span><span class="sxs-lookup"><span data-stu-id="20df1-118">Previously, access checks were disabled by default at the application level and enabled by default at the component level.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="20df1-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20df1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20df1-120">Assignation de rôles à des composants, des interfaces ou des méthodes</span><span class="sxs-lookup"><span data-stu-id="20df1-120">Assigning Roles to Components, Interfaces, or Methods</span></span>](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[<span data-ttu-id="20df1-121">Configuration de la sécurité de Role-Based</span><span class="sxs-lookup"><span data-stu-id="20df1-121">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="20df1-122">Définition des rôles pour une application</span><span class="sxs-lookup"><span data-stu-id="20df1-122">Defining Roles for an Application</span></span>](defining-roles-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="20df1-123">Activation des vérifications d’accès pour une application</span><span class="sxs-lookup"><span data-stu-id="20df1-123">Enabling Access Checks for an Application</span></span>](enabling-access-checks-for-an-application.md)
</dt> <dt>

[<span data-ttu-id="20df1-124">Définition d’un niveau de sécurité pour les vérifications d’accès</span><span class="sxs-lookup"><span data-stu-id="20df1-124">Setting a Security Level for Access Checks</span></span>](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



