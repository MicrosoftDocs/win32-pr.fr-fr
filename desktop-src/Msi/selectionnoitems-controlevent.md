---
description: Le contrôle SelectionTree utilise l’événement SelectionNoItems pour supprimer le texte de description de l’élément obsolète ou pour désactiver les boutons devenus inutiles. Cet événement doit être créé dans la table EventMapping.
ms.assetid: a79abd77-a6e5-4a1f-8a63-51644151404a
title: SelectionNoItems ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544dfcaad3d22b63d71703ea95d1aa4f09a1efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535689"
---
# <a name="selectionnoitems-controlevent"></a><span data-ttu-id="76c82-104">SelectionNoItems ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="76c82-104">SelectionNoItems ControlEvent</span></span>

<span data-ttu-id="76c82-105">Le [contrôle SelectionTree](selectiontree-control.md) utilise l’événement SelectionNoItems pour supprimer le texte de description de l’élément obsolète ou pour désactiver les boutons devenus inutiles.</span><span class="sxs-lookup"><span data-stu-id="76c82-105">The [SelectionTree control](selectiontree-control.md) uses the SelectionNoItems event to delete obsolete item description text or to disable buttons that have become useless.</span></span> <span data-ttu-id="76c82-106">Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="76c82-106">This event should be authored in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="76c82-107">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="76c82-107">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="76c82-108">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="76c82-108">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="76c82-109">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="76c82-109">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="76c82-110">Cet événement peut affecter uniquement les contrôles qui se trouvent dans la même boîte de dialogue que le contrôle SelectionTree.</span><span class="sxs-lookup"><span data-stu-id="76c82-110">This event can only affect controls that are located on the same dialog box as the SelectionTree control.</span></span>

## <a name="published-by"></a><span data-ttu-id="76c82-111">Publié par</span><span class="sxs-lookup"><span data-stu-id="76c82-111">Published By</span></span>

<span data-ttu-id="76c82-112">[Contrôle SelectionTree](selectiontree-control.md) si la sélection n’a aucun nœud.</span><span class="sxs-lookup"><span data-stu-id="76c82-112">[SelectionTree control](selectiontree-control.md) if the selection has no nodes.</span></span>

## <a name="argument"></a><span data-ttu-id="76c82-113">Argument</span><span class="sxs-lookup"><span data-stu-id="76c82-113">Argument</span></span>

<span data-ttu-id="76c82-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="76c82-114">None.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="76c82-115">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="76c82-115">Action on Subscribers</span></span>

<span data-ttu-id="76c82-116">Supprime le texte de description de l’élément obsolète ou désactive les boutons obsolètes.</span><span class="sxs-lookup"><span data-stu-id="76c82-116">Deletes obsolete item description text or disables obsolete buttons.</span></span>

## <a name="typical-use"></a><span data-ttu-id="76c82-117">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="76c82-117">Typical Use</span></span>

<span data-ttu-id="76c82-118">Peut être utilisé pour désactiver les boutons suivant, réinitialiser et DiskCost de la [boîte de dialogue de sélection](selection-dialog.md) lorsqu’une sélection n’a aucun nœud et que ces boutons deviennent inutiles.</span><span class="sxs-lookup"><span data-stu-id="76c82-118">May be used to disable the Next, Reset, and DiskCost buttons on the [Selection Dialog](selection-dialog.md) when a selection has no nodes and these buttons become useless.</span></span>

 

 



