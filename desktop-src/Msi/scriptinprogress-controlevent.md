---
description: Le programme d’installation utilise cet événement pour afficher une chaîne d’information pendant la compilation du script d’exécution de l’installation.
ms.assetid: 088e91e0-734a-4f18-8ceb-cfa4f904f75c
title: ScriptInProgress ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 788fdc9c0acec5979a835a6cd2a0ec09cc6f0c38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518486"
---
# <a name="scriptinprogress-controlevent"></a><span data-ttu-id="961ea-103">ScriptInProgress ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="961ea-103">ScriptInProgress ControlEvent</span></span>

<span data-ttu-id="961ea-104">Le programme d’installation utilise cet événement pour afficher une chaîne d’information pendant la compilation du script d’exécution de l’installation.</span><span class="sxs-lookup"><span data-stu-id="961ea-104">The installer uses this event to display an informational string while the installation's execution script is being compiled.</span></span> <span data-ttu-id="961ea-105">La chaîne d’information peut être affichée dans une boîte de dialogue par un [contrôle de texte](text-control.md) qui s’abonne à ce ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="961ea-105">The informational string can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="961ea-106">Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="961ea-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="961ea-107">Ce ControlEvent, peut être géré par une interface utilisateur qui s’exécute au niveau de l’interface utilisateur de [*base*](b-gly.md), de l' [*interface utilisateur réduite*](r-gly.md)ou de l’interface utilisateur [*complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="961ea-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="961ea-108">Pour plus d’informations sur les niveaux d’interface utilisateur, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="961ea-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="961ea-109">Publié par</span><span class="sxs-lookup"><span data-stu-id="961ea-109">Published By</span></span>

<span data-ttu-id="961ea-110">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="961ea-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="961ea-111">Argument</span><span class="sxs-lookup"><span data-stu-id="961ea-111">Argument</span></span>

<span data-ttu-id="961ea-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="961ea-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="961ea-113">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="961ea-113">Action on Subscribers</span></span>

<span data-ttu-id="961ea-114">Un [contrôle de texte](text-control.md) s’abonnant à ScriptInProgress affiche la chaîne de texte spécifiée dans la [table UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="961ea-114">A [Text control](text-control.md) subscribing to ScriptInProgress will display text string specified in [UIText table](uitext-table.md).</span></span>

## <a name="typical-use"></a><span data-ttu-id="961ea-115">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="961ea-115">Typical Use</span></span>

<span data-ttu-id="961ea-116">Pendant la compilation du script d’exécution, le programme d’installation affiche un ProgressBar indiquant l’heure restante avant le début de l’exécution du script.</span><span class="sxs-lookup"><span data-stu-id="961ea-116">While the execution script is being compiled, the installer displays a ProgressBar indicating the time remaining before the beginning of script execution.</span></span> <span data-ttu-id="961ea-117">L’auteur du package peut afficher un message préliminaire à ce stade, expliquant le ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="961ea-117">The package author can display a preliminary message at this time explaining the ProgressBar.</span></span> <span data-ttu-id="961ea-118">Pour afficher un message préliminaire, incluez un [contrôle de texte](text-control.md) dans la même boîte de dialogue non modale que le ProgressBar.</span><span class="sxs-lookup"><span data-stu-id="961ea-118">To display a preliminary message, include a [Text control](text-control.md) on the same modeless dialog box as the ProgressBar.</span></span> <span data-ttu-id="961ea-119">Spécifiez que ce contrôle de texte s’abonne au ControlEvent, ScriptInProgress via la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="961ea-119">Specify that this Text control subscribe to the ScriptInProgress ControlEvent via the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="961ea-120">Incluez une entrée dans la [table UIText](uitext-table.md) avec ScriptInProgress spécifié dans le champ clé.</span><span class="sxs-lookup"><span data-stu-id="961ea-120">Include an entry in the [UIText table](uitext-table.md) with ScriptInProgress specified in the Key field.</span></span> <span data-ttu-id="961ea-121">Spécifiez le message préliminaire sous la forme d’une chaîne de texte dans le champ de texte de la table UIText.</span><span class="sxs-lookup"><span data-stu-id="961ea-121">Specify the preliminary message as a text string in the Text field of the UIText table.</span></span> <span data-ttu-id="961ea-122">Ensuite, pendant la compilation du script, le programme d’installation affiche cette chaîne dans le contrôle de texte.</span><span class="sxs-lookup"><span data-stu-id="961ea-122">Then during script compilation, the installer will display this string within the text control.</span></span> <span data-ttu-id="961ea-123">Le texte affiché disparaît dès que la compilation du script est terminée.</span><span class="sxs-lookup"><span data-stu-id="961ea-123">The displayed text disappears as soon as the script compilation is finished.</span></span>

<span data-ttu-id="961ea-124">Le même contrôle de texte qui s’abonne au ControlEvent, ScriptInProgress peut également s’abonner au [ControlEvent, TimeRemaining](timeremaining-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="961ea-124">The same text control that subscribes to the ScriptInProgress ControlEvent can also subscribe to the [TimeRemaining ControlEvent](timeremaining-controlevent.md).</span></span> <span data-ttu-id="961ea-125">Dans ce cas, comme le texte de la chaîne ScriptInProgress préliminaire disparaît, il est remplacé par la chaîne « temps restant : XX minutes ».</span><span class="sxs-lookup"><span data-stu-id="961ea-125">In this case, as text of the preliminary ScriptInProgress string disappears, it is replaced by the "Time Remaining: xx minutes" string.</span></span>

 

 



