---
title: Active Accessibility et UI Automation
description: Microsoft Active Accessibility est conçu pour être utilisé avec Windows XP et les systèmes d’exploitation antérieurs.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510638"
---
# <a name="active-accessibility-and-ui-automation"></a><span data-ttu-id="5e330-103">Active Accessibility et UI Automation</span><span class="sxs-lookup"><span data-stu-id="5e330-103">Active Accessibility and UI Automation</span></span>

<span data-ttu-id="5e330-104">Microsoft Active Accessibility est conçu pour être utilisé avec Windows XP et les systèmes d’exploitation antérieurs.</span><span class="sxs-lookup"><span data-stu-id="5e330-104">Microsoft Active Accessibility is designed for use with Windows XP and earlier operating systems.</span></span> <span data-ttu-id="5e330-105">Les développeurs de contrôles personnalisés et d’applications clientes de technologie accessibles pour Windows XP et Windows Vista doivent envisager d’utiliser Microsoft [UI Automation](entry-uiauto-win32.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="5e330-105">Developers of custom controls and accessible technology client applications for Windows XP and Windows Vista should consider using Microsoft [UI Automation](entry-uiauto-win32.md) instead.</span></span>

<span data-ttu-id="5e330-106">Microsoft UI Automation est un système complet qui fournit des informations plus précises sur l’interface utilisateur et donne à l’utilisateur davantage de capacité d’interagir avec les contrôles.</span><span class="sxs-lookup"><span data-stu-id="5e330-106">Microsoft UI Automation is a full-featured system that provides more precise information about the user interface and gives the user more ability to interact with controls.</span></span> <span data-ttu-id="5e330-107">En particulier, il fournit une prise en charge beaucoup plus étendue du texte.</span><span class="sxs-lookup"><span data-stu-id="5e330-107">In particular, it provides greatly enhanced support for text.</span></span>

<span data-ttu-id="5e330-108">Un ensemble d’objets proxy assure la prise en charge d’UI Automation pour les contrôles Microsoft Win32 et Windows Forms standard.</span><span class="sxs-lookup"><span data-stu-id="5e330-108">A set of proxy objects provides UI Automation support for standard Microsoft Win32 and Windows Forms controls.</span></span> <span data-ttu-id="5e330-109">Une prise en charge plus riche est disponible pour les contrôles spécifiquement écrits avec UI Automation à l’esprit, y compris les éléments natifs Windows Presentation Foundation (WPF), qui ne prennent pas directement en charge les Active Accessibility Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5e330-109">Richer support is available for controls specifically written with UI Automation in mind, including native Windows Presentation Foundation (WPF) elements, which do not directly support Microsoft Active Accessibility.</span></span> <span data-ttu-id="5e330-110">Les contrôles personnalisés qui prennent en charge l’Automation d’interface utilisateur peuvent être écrits en code managé ou non managé.</span><span class="sxs-lookup"><span data-stu-id="5e330-110">Custom controls that support UI Automation can be written in either managed or unmanaged code.</span></span>

<span data-ttu-id="5e330-111">Les clients Microsoft Active Accessibility disposent d’un accès limité, via une couche de pontage, aux éléments d’interface utilisateur qui prennent en charge uniquement UI Automation.</span><span class="sxs-lookup"><span data-stu-id="5e330-111">Microsoft Active Accessibility clients have limited access, through a bridging layer, to UI elements that support only UI Automation.</span></span> <span data-ttu-id="5e330-112">Pour plus d’informations, consultez [l’annexe G : Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span><span class="sxs-lookup"><span data-stu-id="5e330-112">For more information, see [Appendix G: Active Accessibility Bridge to UI Automation](appendix-g--active-accessibility-bridge-to-ui-automation.md).</span></span>

<span data-ttu-id="5e330-113">Pour plus d’informations sur les similitudes et les différences entre Microsoft Active Accessibility et UI Automation, consultez [comparaison entre microsoft Active Accessibility et UI Automation](microsoft-active-accessibility-and-ui-automation-compared.md).</span><span class="sxs-lookup"><span data-stu-id="5e330-113">For more information about the similarities and differences between Microsoft Active Accessibility and UI Automation, see [Microsoft Active Accessibility and UI Automation Compared](microsoft-active-accessibility-and-ui-automation-compared.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e330-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5e330-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5e330-115">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5e330-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5e330-116">Prise en main</span><span class="sxs-lookup"><span data-stu-id="5e330-116">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="5e330-117">UI Automation</span><span class="sxs-lookup"><span data-stu-id="5e330-117">UI Automation</span></span>](entry-uiauto-win32.md)
</dt> </dl>

 

 




