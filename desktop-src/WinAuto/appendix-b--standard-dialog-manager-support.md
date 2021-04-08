---
title: Annexe B prise en charge du gestionnaire de boîtes de dialogue standard
description: Microsoft Active Accessibility fournit une prise en charge complète des contrôles de boîte de dialogue du gestionnaire de boîtes de dialogue standard (SDM).
ms.assetid: cdec2dbd-943b-4160-ae22-c16198cc192a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a710b7f35a242badbff6295d1af0d08cada13fa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673445"
---
# <a name="appendix-b-standard-dialog-manager-support"></a><span data-ttu-id="fb5de-103">Annexe B : prise en charge du gestionnaire de boîtes de dialogue standard</span><span class="sxs-lookup"><span data-stu-id="fb5de-103">Appendix B: Standard Dialog Manager Support</span></span>

<span data-ttu-id="fb5de-104">Microsoft Active Accessibility fournit une prise en charge complète des contrôles de boîte de dialogue du gestionnaire de boîtes de dialogue standard (SDM).</span><span class="sxs-lookup"><span data-stu-id="fb5de-104">Microsoft Active Accessibility provides complete support for Standard Dialog Manager (SDM) dialog box controls.</span></span> <span data-ttu-id="fb5de-105">Le SDM est une bibliothèque de code interne Microsoft qui fournit aux applications Microsoft un degré d’indépendance par rapport aux différences entre les systèmes d’exploitation Macintosh et Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="fb5de-105">SDM is an internal Microsoft code library that provides Microsoft applications with a degree of independence from the differences between the Macintosh and Microsoft Windows operating systems.</span></span> <span data-ttu-id="fb5de-106">Le SDM est principalement utilisé pour les boîtes de dialogue dans Microsoft Excel et Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="fb5de-106">SDM is primarily used for dialog boxes in Microsoft Excel and Microsoft Word.</span></span>

<span data-ttu-id="fb5de-107">Le SDM présente des problèmes pour les aides à l’accessibilité, car il utilise des implémentations non standard de boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="fb5de-107">SDM presents problems for accessibility aids because it uses nonstandard implementations of dialog boxes.</span></span> <span data-ttu-id="fb5de-108">Par exemple, les boutons de la boîte de dialogue SDM n’utilisent pas les handles de fenêtre de la même façon que les éléments d’interface utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="fb5de-108">For example, SDM dialog box buttons do not use window handles the same way that the standard user interface elements do.</span></span> <span data-ttu-id="fb5de-109">Vous ne pouvez pas envoyer de messages à des boutons et les boutons ne sont pas contenus dans la liste des fenêtres.</span><span class="sxs-lookup"><span data-stu-id="fb5de-109">You cannot send messages to buttons and buttons are not contained in the window list.</span></span> <span data-ttu-id="fb5de-110">Une application utilisant le SDM communique avec le contrôle par le biais d’une interface privée.</span><span class="sxs-lookup"><span data-stu-id="fb5de-110">An application using SDM communicates with the control through a private interface.</span></span>

<span data-ttu-id="fb5de-111">L’illustration suivante montre un exemple de boîte de dialogue à partir de Word.</span><span class="sxs-lookup"><span data-stu-id="fb5de-111">The following illustration shows a sample dialog box from Word.</span></span> <span data-ttu-id="fb5de-112">Bien qu’il ressemble à une boîte de dialogue Windows normale qui utilise le contrôle onglet, il s’agit en réalité d’une boîte de dialogue SDM.</span><span class="sxs-lookup"><span data-stu-id="fb5de-112">Although it looks like a regular Windows dialog box that uses the tab control, it is really an SDM dialog box.</span></span>

![capture d’écran de la boîte de dialogue Options avec l’onglet Affichage sélectionné](images/dialog.gif)

 

 




