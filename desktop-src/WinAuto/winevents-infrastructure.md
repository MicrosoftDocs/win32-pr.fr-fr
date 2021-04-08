---
title: Infrastructure WinEvents
description: Le système d’exploitation Microsoft Windows comprend une fonctionnalité, appelée WinEvents, qui permet aux processus et aux applications qui s’exécutent sur le bureau Windows d’échanger certains types d’informations.
ms.assetid: ba97b00b-4a4c-4889-ae9c-8e92eb742849
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8846582a6d18f304cc08e3cb13ddb444cb278d7
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/29/2020
ms.locfileid: "103679545"
---
# <a name="winevents"></a><span data-ttu-id="9d010-103">WinEvents</span><span class="sxs-lookup"><span data-stu-id="9d010-103">WinEvents</span></span>

<span data-ttu-id="9d010-104">Le système d’exploitation Microsoft Windows comprend une fonctionnalité, appelée *winEvents*, qui permet aux processus et aux applications qui s’exécutent sur le bureau Windows d’échanger certains types d’informations.</span><span class="sxs-lookup"><span data-stu-id="9d010-104">The Microsoft Windows operating system includes a feature, called *WinEvents*, that enables processes and applications running on the Windows desktop to exchange certain types of information.</span></span> <span data-ttu-id="9d010-105">Les outils d’accessibilité qui utilisent Microsoft UI Automation et Microsoft Active Accessibility font partie des principaux utilisateurs de WinEvents.</span><span class="sxs-lookup"><span data-stu-id="9d010-105">Accessibility tools that use Microsoft UI Automation and Microsoft Active Accessibility are among the primary users of the WinEvents.</span></span>

<span data-ttu-id="9d010-106">Dans le contexte de l’accessibilité, les fournisseurs UI Automation et les serveurs Microsoft Active Accessibility utilisent WinEvents pour informer les clients des modifications apportées à l’interface utilisateur d’une application, par exemple lorsqu’un élément d’interface utilisateur a été créé ou détruit, ou lorsqu’un nom d’élément, un État ou une valeur a changé.</span><span class="sxs-lookup"><span data-stu-id="9d010-106">In the context of accessibility, UI Automation providers and Microsoft Active Accessibility servers use WinEvents to notify clients of changes in an application UI, such as when a UI element has been created or destroyed, or when an element name, state, or value has changed.</span></span>

<span data-ttu-id="9d010-107">Cette section fournit des suggestions, des instructions et des exemples pour aider les clients à gérer les WinEvents et à aider les serveurs à déterminer quand déclencher le WinEvent approprié.</span><span class="sxs-lookup"><span data-stu-id="9d010-107">This section provides suggestions, guidelines, and examples to help clients handle WinEvents and to help servers determine when to trigger the appropriate WinEvent.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9d010-108">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="9d010-108">In this section</span></span>

-   [<span data-ttu-id="9d010-109">Qu’est-ce que WinEvents ?</span><span class="sxs-lookup"><span data-stu-id="9d010-109">What Are WinEvents?</span></span>](what-are-winevents.md)
-   [<span data-ttu-id="9d010-110">Inscription d’une fonction de raccordement</span><span class="sxs-lookup"><span data-stu-id="9d010-110">Registering a Hook Function</span></span>](registering-a-hook-function.md)
-   [<span data-ttu-id="9d010-111">Événements de niveau système et de Object-Level</span><span class="sxs-lookup"><span data-stu-id="9d010-111">System-Level and Object-Level Events</span></span>](system-level-and-object-level-events.md)
-   [<span data-ttu-id="9d010-112">Fonctions de raccordement dans le contexte et hors contexte</span><span class="sxs-lookup"><span data-stu-id="9d010-112">In-Context and Out-of-Context Hook Functions</span></span>](in-context-and-out-of-context-hook-functions.md)
-   [<span data-ttu-id="9d010-113">Protection contre la réentrance dans les fonctions de raccordement</span><span class="sxs-lookup"><span data-stu-id="9d010-113">Guarding Against Reentrancy in Hook Functions</span></span>](guarding-against-reentrancy-in-hook-functions.md)
-   [<span data-ttu-id="9d010-114">Allocation d’ID WinEvent</span><span class="sxs-lookup"><span data-stu-id="9d010-114">Allocation of WinEvent IDs</span></span>](allocation-of-winevent-ids.md)

<span data-ttu-id="9d010-115">Pour obtenir une vue d’ensemble du processus de notification d’événements dans Microsoft Active Accessibility, voir [winEvents](winevents-overview.md) dans la [vue d’ensemble technique](technical-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9d010-115">For an overview of the event notification process in Microsoft Active Accessibility, see [WinEvents](winevents-overview.md) in the [Technical Overview](technical-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d010-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d010-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d010-117">Infrastructure commune</span><span class="sxs-lookup"><span data-stu-id="9d010-117">Common Infrastructure</span></span>](common-infrastructure.md)
</dt> </dl>

 

 




