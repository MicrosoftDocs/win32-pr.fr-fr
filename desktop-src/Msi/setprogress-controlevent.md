---
description: Le programme d’installation utilise l’événement SetProgress pour publier des informations sur la progression de l’installation.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: SetProgress ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7523f03dd8fc8216991ae16b05a731e9f38f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952400"
---
# <a name="setprogress-controlevent"></a><span data-ttu-id="a37b7-103">SetProgress ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="a37b7-103">SetProgress ControlEvent</span></span>

<span data-ttu-id="a37b7-104">Le programme d’installation utilise l’événement SetProgress pour publier des informations sur la progression de l’installation.</span><span class="sxs-lookup"><span data-stu-id="a37b7-104">The installer uses the SetProgress event to publish information on the installation's progress.</span></span> <span data-ttu-id="a37b7-105">Un contrôle [ProgressBar](progressbar-control.md) ou un contrôle de tableau [blanc](billboard-control.md) doit s’abonner à l’événement via la [table EventMapping](eventmapping-table.md) en nommant l’action dont la progression est indiquée.</span><span class="sxs-lookup"><span data-stu-id="a37b7-105">A [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) should subscribe to the event via the [EventMapping table](eventmapping-table.md) by naming the Action whose progress is being indicated.</span></span> <span data-ttu-id="a37b7-106">Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="a37b7-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="a37b7-107">Ce ControlEvent, peut être géré par une interface utilisateur qui s’exécute au niveau de l’interface utilisateur de [*base*](b-gly.md), de l' [*interface utilisateur réduite*](r-gly.md)ou de l’interface utilisateur [*complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="a37b7-107">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="a37b7-108">Pour plus d’informations sur les niveaux d’interface utilisateur, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="a37b7-108">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="a37b7-109">Publié par</span><span class="sxs-lookup"><span data-stu-id="a37b7-109">Published By</span></span>

<span data-ttu-id="a37b7-110">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="a37b7-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="a37b7-111">Argument</span><span class="sxs-lookup"><span data-stu-id="a37b7-111">Argument</span></span>

<span data-ttu-id="a37b7-112">Aucun</span><span class="sxs-lookup"><span data-stu-id="a37b7-112">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="a37b7-113">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="a37b7-113">Action on Subscribers</span></span>

<span data-ttu-id="a37b7-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="a37b7-114">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="a37b7-115">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="a37b7-115">Typical Use</span></span>

<span data-ttu-id="a37b7-116">Un contrôle [ProgressBar](progressbar-control.md) sur une boîte de dialogue non modale s’abonne à cet événement à l’aide de l’attribut [Progress](progress-control-attribute.md) pour recevoir les informations de progression.</span><span class="sxs-lookup"><span data-stu-id="a37b7-116">A [ProgressBar](progressbar-control.md) control on a modeless dialog box subscribes to this event using the [Progress](progress-control-attribute.md) attribute to receive the progress information.</span></span>

 

 



