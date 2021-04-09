---
description: Le programme d’installation utilise cet événement pour publier le nom de l’action présente. Le nom peut être affiché sur une boîte de dialogue par un contrôle de texte qui s’abonne à ce ControlEvent,. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 2b4928fe-2d5c-46c1-8a31-cbebbc78d304
title: ActionText ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caf03829818ea7ce7732ca5f51f1710a11e8d07f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951799"
---
# <a name="actiontext-controlevent"></a><span data-ttu-id="523c4-105">ActionText ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="523c4-105">ActionText ControlEvent</span></span>

<span data-ttu-id="523c4-106">Le programme d’installation utilise cet événement pour publier le nom de l’action présente.</span><span class="sxs-lookup"><span data-stu-id="523c4-106">The installer uses this event to publish the name of the present action.</span></span> <span data-ttu-id="523c4-107">Le nom peut être affiché sur une boîte de dialogue par un [contrôle de texte](text-control.md) qui s’abonne à ce ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="523c4-107">The name can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="523c4-108">Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="523c4-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="523c4-109">Ce ControlEvent, peut être géré par une interface utilisateur qui s’exécute au niveau de l’interface utilisateur de [*base*](b-gly.md), de l' [*interface utilisateur réduite*](r-gly.md)ou de l’interface utilisateur [*complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="523c4-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="523c4-110">Pour plus d’informations sur les niveaux d’interface utilisateur, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="523c4-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="523c4-111">Publié par</span><span class="sxs-lookup"><span data-stu-id="523c4-111">Published By</span></span>

<span data-ttu-id="523c4-112">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="523c4-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="523c4-113">Argument</span><span class="sxs-lookup"><span data-stu-id="523c4-113">Argument</span></span>

<span data-ttu-id="523c4-114">Ce ControlEvent, n’utilise pas d’argument.</span><span class="sxs-lookup"><span data-stu-id="523c4-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="523c4-115">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="523c4-115">Action on Subscribers</span></span>

<span data-ttu-id="523c4-116">Les abonnés sont affichés lorsqu’une nouvelle donnée de progression arrive à partir du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="523c4-116">The subscribers are shown when a new progress data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="523c4-117">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="523c4-117">Typical Use</span></span>

<span data-ttu-id="523c4-118">Un [contrôle de texte](text-control.md) sur une boîte de dialogue non modale s’abonne à cet événement via la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="523c4-118">A [Text Control](text-control.md) on a modeless dialog subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="523c4-119">L' [attribut de contrôle de texte](text-control-attribute.md) doit figurer dans le champ attributs de ce tableau pour recevoir le nom de l’action actuelle.</span><span class="sxs-lookup"><span data-stu-id="523c4-119">The [Text Control Attribute](text-control-attribute.md) should be listed in the Attributes field of this table to receive the name of the current action.</span></span>

 

 



