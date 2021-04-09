---
description: Les éléments suivants fournissent des instances courantes des instructions conditionnelles. Pour plus d’informations, consultez syntaxe d’instruction conditionnelle.
ms.assetid: 8b6bae7a-20ae-494c-bd96-66bd537c8630
title: Exemples de syntaxe d’instruction conditionnelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca91a2b3e89160fad19ad5d9b1c6a3d33929e5d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951686"
---
# <a name="examples-of-conditional-statement-syntax"></a><span data-ttu-id="71897-104">Exemples de syntaxe d’instruction conditionnelle</span><span class="sxs-lookup"><span data-stu-id="71897-104">Examples of Conditional Statement Syntax</span></span>

<span data-ttu-id="71897-105">Les éléments suivants fournissent des instances courantes des instructions conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="71897-105">The following provides some common instances of conditional statements.</span></span> <span data-ttu-id="71897-106">Pour plus d’informations, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="71897-106">For more information, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

## <a name="run-action-on-removal"></a><span data-ttu-id="71897-107">Exécuter l’action à la suppression.</span><span class="sxs-lookup"><span data-stu-id="71897-107">Run action on removal.</span></span>

<span data-ttu-id="71897-108">Pour plus d’informations, consultez [conditionnement des actions à exécuter pendant la suppression](conditioning-actions-to-run-during-removal.md).</span><span class="sxs-lookup"><span data-stu-id="71897-108">For information, see [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span>

## <a name="run-action-only-if-the-product-has-not-been-installed"></a><span data-ttu-id="71897-109">Exécuter l’action uniquement si le produit n’a pas été installé.</span><span class="sxs-lookup"><span data-stu-id="71897-109">Run action only if the product has not been installed.</span></span>

``` syntax
NOT Installed
```

## <a name="run-action-only-if-the-product-will-be-installed-local-do-not-run-action-on-a-reinstallation"></a><span data-ttu-id="71897-110">Exécuter l’action uniquement si le produit est installé en local.</span><span class="sxs-lookup"><span data-stu-id="71897-110">Run action only if the product will be installed local.</span></span> <span data-ttu-id="71897-111">Ne pas exécuter d’action sur une réinstallation.</span><span class="sxs-lookup"><span data-stu-id="71897-111">Do not run action on a reinstallation.</span></span>

``` syntax
(&FeatureName=3) AND NOT(!FeatureName=3)
```

<span data-ttu-id="71897-112">Le terme « &NomFonctionnalité = 3 » signifie que l’action consiste à installer la fonctionnalité locale.</span><span class="sxs-lookup"><span data-stu-id="71897-112">The term "&FeatureName=3" means the action is to install the feature local.</span></span> <span data-ttu-id="71897-113">Le terme «NOT ( ! NomFonctionnalité = 3)» signifie que la fonctionnalité n’est pas installée en local.</span><span class="sxs-lookup"><span data-stu-id="71897-113">The term "NOT(!FeatureName=3)" means the feature is not installed local.</span></span>

## <a name="run-action-only-if-the-feature-will-be-uninstalled"></a><span data-ttu-id="71897-114">Exécuter l’action uniquement si la fonctionnalité sera désinstallée.</span><span class="sxs-lookup"><span data-stu-id="71897-114">Run action only if the feature will be uninstalled.</span></span>

``` syntax
(&FeatureName=2) AND (!FeatureName=3)
```

<span data-ttu-id="71897-115">Cette condition vérifie uniquement la transition de la fonctionnalité d’un état installé de local à l’État absent.</span><span class="sxs-lookup"><span data-stu-id="71897-115">This condition only checks for a transition of the feature from an installed state of local to the absent state.</span></span>

## <a name="run-action-only-if-the-component-was-installed-local-but-is-transitioning-out-of-state"></a><span data-ttu-id="71897-116">Exécuter l’action uniquement si le composant a été installé en local, mais est en état de transition hors État.</span><span class="sxs-lookup"><span data-stu-id="71897-116">Run action only if the component was installed local, but is transitioning out of state.</span></span>

``` syntax
(?ComponentName=3) AND ($ComponentName=2 OR $ComponentName=4)
```

<span data-ttu-id="71897-117">Le terme « ? ComponetName = 3» signifie que le composant est installé en local.</span><span class="sxs-lookup"><span data-stu-id="71897-117">The term "?ComponetName=3" means the component is installed local.</span></span> <span data-ttu-id="71897-118">Le terme « $ComponentName = 2 » signifie que l’état de l’action sur le composant est absent.</span><span class="sxs-lookup"><span data-stu-id="71897-118">The term "$ComponentName=2" means that the action state on the component is Absent.</span></span> <span data-ttu-id="71897-119">Le terme « $ComponentName = 4 » signifie que l’état de l’action sur le composant est exécuté à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="71897-119">The term "$ComponentName=4" means that the action state on the component is run from source.</span></span> <span data-ttu-id="71897-120">Notez qu’un état d’action de publication n’est pas valide pour un composant.</span><span class="sxs-lookup"><span data-stu-id="71897-120">Note that an action state of advertise is not valid for a component.</span></span>

## <a name="run-action-only-on-the-reinstallation-of-a-component"></a><span data-ttu-id="71897-121">Exécuter l’action uniquement lors de la réinstallation d’un composant.</span><span class="sxs-lookup"><span data-stu-id="71897-121">Run action only on the reinstallation of a component.</span></span>

``` syntax
?ComponentName=$ComponentName
```

## <a name="run-action-only-when-a-particular-patch-is-applied"></a><span data-ttu-id="71897-122">Exécuter l’action uniquement lorsqu’un correctif est appliqué.</span><span class="sxs-lookup"><span data-stu-id="71897-122">Run action only when a particular patch is applied.</span></span>

``` syntax
PATCH AND PATCH >< MEDIASRCPROPNAME
```

<span data-ttu-id="71897-123">Pour plus d’informations, consultez la section Notes de la page de propriétés [**patch**](patch.md) .</span><span class="sxs-lookup"><span data-stu-id="71897-123">For more information, see the Remarks section on the [**PATCH**](patch.md) property page.</span></span>

 

 



