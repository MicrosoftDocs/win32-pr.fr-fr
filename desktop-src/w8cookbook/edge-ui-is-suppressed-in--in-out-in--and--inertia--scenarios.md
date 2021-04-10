---
title: L’interface utilisateur Edge est supprimée dans les scénarios « in-out-in » et « inertie »
description: L’interface utilisateur Edge est supprimée dans les scénarios « in-out-in » et « inertie »
ms.assetid: 005B6D03-52A6-4780-8D3E-4A5CDA5EED8C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef08eab653349beab0710d59d45bedc2874ced44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197330"
---
# <a name="edge-ui-is-suppressed-in-in-out-in-and-inertia-scenarios"></a><span data-ttu-id="51902-103">L’interface utilisateur Edge est supprimée dans les scénarios « in-out-in » et « inertie »</span><span class="sxs-lookup"><span data-stu-id="51902-103">Edge UI is suppressed in “in-out-in” and “inertia” scenarios</span></span>

## <a name="platform"></a><span data-ttu-id="51902-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="51902-104">Platform</span></span>

<dl> <span data-ttu-id="51902-105">Clients-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="51902-105">Clients - Windows 8.1</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="51902-106">Description</span><span class="sxs-lookup"><span data-stu-id="51902-106">Description</span></span>

<span data-ttu-id="51902-107">Dans certains cas, les utilisateurs peuvent involontairement appeler l’interface utilisateur Edge (icônes, barre d’application, changement d’application).</span><span class="sxs-lookup"><span data-stu-id="51902-107">There are some cases where users may unintentionally invoke Edge UI (Charms, App Bar, app switching).</span></span> <span data-ttu-id="51902-108">Nous avons introduit une fonctionnalité qui permet aux développeurs de concevoir leur interface utilisateur pour la totalité de l’écran sans faire de intuitivité (par exemple, des bordures) pour empêcher l’utilisateur d’atteindre accidentellement les bords.</span><span class="sxs-lookup"><span data-stu-id="51902-108">We have introduced a feature to allow developers to design their UI for the whole screen without making affordances (for example, borders) to prevent the user from accidentally hitting the edges.</span></span>

<span data-ttu-id="51902-109">Il existe deux cas qui peuvent mener le plus souvent à des balayages d’arête involontaires :</span><span class="sxs-lookup"><span data-stu-id="51902-109">There are two cases that might lead most often to inadvertent edge swipes:</span></span>

-   <span data-ttu-id="51902-110">Dans la panoramisation rapide, la vitesse et la imprécision de l’interaction peuvent parfois provoquer l’apparition de ces dernières à partir du bord de l’écran</span><span class="sxs-lookup"><span data-stu-id="51902-110">In fast panning, the speed and imprecision of the interaction can occasionally cause them to come in from the edge of the screen</span></span>
-   <span data-ttu-id="51902-111">Si les utilisateurs quittent et resaisient rapidement la zone d’écran lors de l’écriture manuscrite avec leur doigt, par exemple dans une application de peinture, ce comportement de sortie peut déclencher par erreur l’interface utilisateur du bord et interrompre l’expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="51902-111">If users rapidly leave and re-enter the screen area while inking with their finger, for example, in a painting app, this in-out-in behavior can mistakenly trigger the Edge UI and interrupt the user experience</span></span>

<span data-ttu-id="51902-112">Pour améliorer l’expérience des utilisateurs et des développeurs, l’interface utilisateur Edge sera désormais supprimée dans deux instances spécifiques :</span><span class="sxs-lookup"><span data-stu-id="51902-112">To improve the user and developer experience, the Edge UI will now be suppressed in two specific instances:</span></span>

-   <span data-ttu-id="51902-113">Lorsqu’un utilisateur effectue une panoramisation dans une application qui prend en charge l’inertie de DManip et effectue un balayage en dehors de l’écran pendant l’inertie, l’interface utilisateur du bord n’est pas appelée dans une fenêtre de délai d’attente</span><span class="sxs-lookup"><span data-stu-id="51902-113">When a user is panning in an application that supports DManip Inertia and swipes outside of the screen while inertia is occurring, the Edge UI will not be invoked within a timeout window</span></span>
-   <span data-ttu-id="51902-114">Sur les appareils certifiés, lorsqu’un utilisateur passe rapidement de l’écran à l’extérieur de l’écran, et vice versa, à l’intérieur de certains paramètres, l’interface utilisateur du bord n’est pas appelée</span><span class="sxs-lookup"><span data-stu-id="51902-114">On certified devices, when a user quickly swipes from within the screen to outside the screen and back inside (in-out-in motion) within certain parameters, the Edge UI will not be invoked</span></span>

## <a name="manifestations"></a><span data-ttu-id="51902-115">Manifestations</span><span class="sxs-lookup"><span data-stu-id="51902-115">Manifestations</span></span>

<span data-ttu-id="51902-116">Les utilisateurs qui défilent rapidement par rapport à la périphérie lors de l’utilisation d’une application voient une baisse de l’inadvertance de bord involontaire.</span><span class="sxs-lookup"><span data-stu-id="51902-116">Users quickly swiping against the edge while using an app will see a decrease in unintentional edge invocation.</span></span>

## <a name="solution"></a><span data-ttu-id="51902-117">Solution</span><span class="sxs-lookup"><span data-stu-id="51902-117">Solution</span></span>

<span data-ttu-id="51902-118">Les développeurs doivent garder à l’esprit ces atténuations et doivent être en mesure d’utiliser le plein écran sans craindre que les utilisateurs déclenchent accidentellement l’interface utilisateur Edge tout en interagissant avec l’application le long du bord.</span><span class="sxs-lookup"><span data-stu-id="51902-118">Developers should keep these mitigations in mind and should be able to use the full screen without fear that users will accidentally trigger the Edge UI while interacting with the application along the edge.</span></span>

 

 




