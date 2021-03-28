---
description: Un contexte de périphérique parent permet à une application de réduire le temps nécessaire pour configurer la zone de découpage pour une fenêtre.
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: Contextes de périphérique d’affichage parent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e423ceaa65790df35fa55c8dda597cb1bb45019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972594"
---
# <a name="parent-display-device-contexts"></a><span data-ttu-id="6a3c0-103">Contextes de périphérique d’affichage parent</span><span class="sxs-lookup"><span data-stu-id="6a3c0-103">Parent Display Device Contexts</span></span>

<span data-ttu-id="6a3c0-104">Un *contexte de périphérique parent* permet à une application de réduire le temps nécessaire pour configurer la zone de découpage pour une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6a3c0-104">A *parent device context* enables an application to minimize the time necessary to set up the clipping region for a window.</span></span> <span data-ttu-id="6a3c0-105">Une application utilise généralement des contextes d’appareil parent pour accélérer le dessin des fenêtres de contrôle sans nécessiter un contexte de périphérique ou de classe privé.</span><span class="sxs-lookup"><span data-stu-id="6a3c0-105">An application typically uses parent device contexts to speed up drawing for control windows without requiring a private or class device context.</span></span> <span data-ttu-id="6a3c0-106">Par exemple, le système utilise des contextes de périphérique parent pour le bouton de commande et les contrôles d’édition.</span><span class="sxs-lookup"><span data-stu-id="6a3c0-106">For example, the system uses parent device contexts for push button and edit controls.</span></span> <span data-ttu-id="6a3c0-107">Les contextes de périphérique parent sont destinés à être utilisés uniquement avec les fenêtres enfants, jamais avec des fenêtres contextuelles ou de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="6a3c0-107">Parent device contexts are intended for use with child windows only, never with top-level or pop-up windows.</span></span>

<span data-ttu-id="6a3c0-108">Une application peut spécifier le \_ style cs PARENTDC pour définir la zone de découpage de la fenêtre enfant sur celle de la fenêtre parente afin que l’enfant puisse dessiner dans le parent.</span><span class="sxs-lookup"><span data-stu-id="6a3c0-108">An application can specify the CS\_PARENTDC style to set the clipping region of the child window to that of the parent window so that the child can draw in the parent.</span></span> <span data-ttu-id="6a3c0-109">La spécification de CS \_ PARENTDC améliore les performances d’une application, car le système n’a pas besoin de recalculer la région visible pour chaque fenêtre enfant.</span><span class="sxs-lookup"><span data-stu-id="6a3c0-109">Specifying CS\_PARENTDC enhances an application's performance because the system doesn't need to keep recalculating the visible region for each child window.</span></span>

<span data-ttu-id="6a3c0-110">Les valeurs d’attribut définies par la fenêtre parente ne sont pas conservées pour la fenêtre enfant ; par exemple, la fenêtre parente ne peut pas définir le pinceau pour ses fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="6a3c0-110">Attribute values set by the parent window are not preserved for the child window; for example, the parent window cannot set the brush for its child windows.</span></span> <span data-ttu-id="6a3c0-111">La seule propriété conservée est la zone de découpage.</span><span class="sxs-lookup"><span data-stu-id="6a3c0-111">The only property preserved is the clipping region.</span></span> <span data-ttu-id="6a3c0-112">La fenêtre doit découper sa propre sortie vers les limites de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6a3c0-112">The window must clip its own output to the limits of the window.</span></span> <span data-ttu-id="6a3c0-113">Étant donné que la zone de découpage du contexte de périphérique parent est identique à la fenêtre parente, la fenêtre enfant peut potentiellement dessiner sur la totalité de la fenêtre parente, mais le contexte de périphérique parent ne doit pas être utilisé de cette façon.</span><span class="sxs-lookup"><span data-stu-id="6a3c0-113">Because the clipping region for the parent device context is identical to the parent window, the child window can potentially draw over the entire parent window, but the parent device context must not be used in this way.</span></span>

<span data-ttu-id="6a3c0-114">Le système ignore le \_ style cs PARENTDC si la fenêtre parente utilise un contexte de périphérique de classe ou privé, si la fenêtre parente découpe ses fenêtres enfants, ou si la fenêtre enfant découpe ses fenêtres enfants ou leurs fenêtres sœurs.</span><span class="sxs-lookup"><span data-stu-id="6a3c0-114">The system ignores the CS\_PARENTDC style if the parent window uses a private or class device context, if the parent window clips its child windows, or if the child window clips its child windows or sibling windows.</span></span>

 

 



