---
description: Le programme d’installation utilise cet événement pour publier des données sur la dernière action. Les données peuvent être affichées dans une boîte de dialogue par un contrôle de texte qui s’abonne à ce ControlEvent,. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ActionData ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521538"
---
# <a name="actiondata-controlevent"></a><span data-ttu-id="6e18a-105">ActionData ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="6e18a-105">ActionData ControlEvent</span></span>

<span data-ttu-id="6e18a-106">Le programme d’installation utilise cet événement pour publier des données sur la dernière action.</span><span class="sxs-lookup"><span data-stu-id="6e18a-106">The installer uses this event to publish data on the latest action.</span></span> <span data-ttu-id="6e18a-107">Les données peuvent être affichées dans une boîte de dialogue par un [contrôle de texte](text-control.md) qui s’abonne à ce ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="6e18a-107">The data can be displayed on a dialog box by a [Text Control](text-control.md) that subscribes to this ControlEvent.</span></span> <span data-ttu-id="6e18a-108">Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="6e18a-108">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="6e18a-109">Ce ControlEvent, peut être géré par une interface utilisateur qui s’exécute au niveau de l’interface utilisateur de [*base*](b-gly.md), de l' [*interface utilisateur réduite*](r-gly.md)ou de l’interface utilisateur [*complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="6e18a-109">This ControlEvent can be handled by a user interface run at the [*basic UI*](b-gly.md), [*reduced UI*](r-gly.md), or [*full UI*](f-gly.md) levels.</span></span> <span data-ttu-id="6e18a-110">Pour plus d’informations sur les niveaux d’interface utilisateur, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="6e18a-110">For information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="6e18a-111">Publié par</span><span class="sxs-lookup"><span data-stu-id="6e18a-111">Published By</span></span>

<span data-ttu-id="6e18a-112">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="6e18a-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="6e18a-113">Argument</span><span class="sxs-lookup"><span data-stu-id="6e18a-113">Argument</span></span>

<span data-ttu-id="6e18a-114">Ce ControlEvent, n’utilise pas d’argument.</span><span class="sxs-lookup"><span data-stu-id="6e18a-114">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="6e18a-115">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="6e18a-115">Action on Subscribers</span></span>

<span data-ttu-id="6e18a-116">Les abonnés sont masqués lorsqu’une nouvelle action démarre et s’affichent quand de nouvelles données d’action arrivent du programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="6e18a-116">The subscribers are hidden when a new action starts and shown when new action data arrives from the installer.</span></span>

## <a name="typical-use"></a><span data-ttu-id="6e18a-117">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="6e18a-117">Typical Use</span></span>

<span data-ttu-id="6e18a-118">Un [contrôle de texte](text-control.md) sur une boîte de dialogue non modale s’abonne à cet événement par le biais de la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="6e18a-118">A [Text Control](text-control.md) on a modeless dialog box subscribes to this event through the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="6e18a-119">L' [attribut de contrôle de texte](text-control-attribute.md) est listé dans le champ attributs de ce tableau pour recevoir les données d’action actuelles.</span><span class="sxs-lookup"><span data-stu-id="6e18a-119">The [Text Control Attribute](text-control-attribute.md) is listed in the Attributes field of this table to receive the current action data.</span></span> <span data-ttu-id="6e18a-120">Généralement utilisé pour afficher les noms des fichiers copiés lors de la copie de fichiers.</span><span class="sxs-lookup"><span data-stu-id="6e18a-120">Typically used to display the names of the files copied during file copy.</span></span>

 

 



