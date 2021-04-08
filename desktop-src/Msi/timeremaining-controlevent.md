---
description: Le programme d’installation utilise l’événement TimeRemaining pour publier le temps approximatif restant, en secondes, pour la séquence de progression actuelle.
ms.assetid: ec5fc2b3-13a9-4681-89f0-fd39bab1de5f
title: TimeRemaining ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8978dfb7ed3be855921ad66af8554ea50972a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035164"
---
# <a name="timeremaining-controlevent"></a><span data-ttu-id="ec590-103">TimeRemaining ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="ec590-103">TimeRemaining ControlEvent</span></span>

<span data-ttu-id="ec590-104">Le programme d’installation utilise l’événement TimeRemaining pour publier le temps approximatif restant, en secondes, pour la séquence de progression actuelle.</span><span class="sxs-lookup"><span data-stu-id="ec590-104">The installer uses the TimeRemaining event to publish the approximate time remaining, in seconds, for the current progress sequence.</span></span> <span data-ttu-id="ec590-105">Le temps restant peut être affiché sur une boîte de dialogue par un [contrôle de texte](text-control.md) qui s’abonne à ce ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="ec590-105">The time remaining can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="ec590-106">Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="ec590-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="ec590-107">Ce ControlEvent, peut être géré par une interface utilisateur qui s’exécute au niveau de l’interface utilisateur de [*base*](b-gly.md), de l' [*interface utilisateur réduite*](r-gly.md)ou de l’interface utilisateur [*complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ec590-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="ec590-108">Pour plus d’informations sur les niveaux d’interface utilisateur, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="ec590-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="ec590-109">Publié par</span><span class="sxs-lookup"><span data-stu-id="ec590-109">Published By</span></span>

<span data-ttu-id="ec590-110">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="ec590-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="ec590-111">Argument</span><span class="sxs-lookup"><span data-stu-id="ec590-111">Argument</span></span>

<span data-ttu-id="ec590-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="ec590-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="ec590-113">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="ec590-113">Action on Subscribers</span></span>

<span data-ttu-id="ec590-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="ec590-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="ec590-115">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="ec590-115">Typical Use</span></span>

<span data-ttu-id="ec590-116">Un [contrôle de texte](text-control.md) sur une boîte de dialogue non modale s’abonne à cet événement via la [table EventMapping](eventmapping-table.md) et utilise l' [attribut TimeRemaining](timeremaining-control-attribute.md) pour afficher le temps restant.</span><span class="sxs-lookup"><span data-stu-id="ec590-116">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md) and uses the [TimeRemaining attribute](timeremaining-control-attribute.md) to display the time remaining.</span></span>

<span data-ttu-id="ec590-117">Le même contrôle de texte qui s’abonne au ControlEvent, TimeRemaining peut également s’abonner au [ControlEvent, ScriptInProgress](scriptinprogress-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="ec590-117">The same text control that subscribes to the TimeRemaining ControlEvent can also subscribe to the [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md).</span></span> <span data-ttu-id="ec590-118">Dans ce cas, en tant que chaîne de message ScriptInProgress préliminaire, il est remplacé par la chaîne « temps restant : XX minutes ».</span><span class="sxs-lookup"><span data-stu-id="ec590-118">In this case, as the preliminary ScriptInProgress message string, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



