---
description: Le ControlEvent, SpawnWaitDialog déclenche la boîte de dialogue spécifiée par la colonne argument de la table ControlEvent,, si l’expression dans la colonne condition prend la valeur FALSe.
ms.assetid: 38a5d896-2c11-4ce9-b829-104a882723b6
title: SpawnWaitDialog ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b20059c936a8534d00799c93dfbe3408a19c6dbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951282"
---
# <a name="spawnwaitdialog-controlevent"></a><span data-ttu-id="0a5c0-103">SpawnWaitDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="0a5c0-103">SpawnWaitDialog ControlEvent</span></span>

<span data-ttu-id="0a5c0-104">Le ControlEvent, SpawnWaitDialog déclenche la boîte de dialogue spécifiée par la colonne argument de la [table ControlEvent,](controlevent-table.md), si l’expression dans la colonne condition prend la valeur false.</span><span class="sxs-lookup"><span data-stu-id="0a5c0-104">The SpawnWaitDialog ControlEvent triggers the dialog box specified by the Argument column of the [ControlEvent table](controlevent-table.md), if the expression in the Condition column evaluates as FALSE.</span></span> <span data-ttu-id="0a5c0-105">La boîte de dialogue reste valable tant que l’expression conditionnelle conserve la valeur FALSe et est supprimée dès que la condition prend la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="0a5c0-105">The dialog box remains up for as long as the conditional expression remains FALSE and is removed as soon as the condition evaluates TRUE.</span></span>

<span data-ttu-id="0a5c0-106">Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="0a5c0-106">This event can be published by a [PushButton Control](pushbutton-control.md)or a [SelectionTree control](selectiontree-control.md).</span></span> <span data-ttu-id="0a5c0-107">Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="0a5c0-107">This event should be authored into the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="0a5c0-108">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="0a5c0-108">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="0a5c0-109">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0a5c0-109">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="0a5c0-110">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="0a5c0-110">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

## <a name="published-by"></a><span data-ttu-id="0a5c0-111">Publié par</span><span class="sxs-lookup"><span data-stu-id="0a5c0-111">Published By</span></span>

<span data-ttu-id="0a5c0-112">Ce ControlEvent, est publié par le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="0a5c0-112">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="0a5c0-113">Argument</span><span class="sxs-lookup"><span data-stu-id="0a5c0-113">Argument</span></span>

<span data-ttu-id="0a5c0-114">Boîte de dialogue de la [table de boîte de dialogue](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="0a5c0-114">A dialog box in the [Dialog table](dialog-table.md).</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="0a5c0-115">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="0a5c0-115">Action on Subscribers</span></span>

<span data-ttu-id="0a5c0-116">Aucun</span><span class="sxs-lookup"><span data-stu-id="0a5c0-116">None.</span></span>

## <a name="typical-use"></a><span data-ttu-id="0a5c0-117">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="0a5c0-117">Typical Use</span></span>

<span data-ttu-id="0a5c0-118">Le ControlEvent, SpawnWaitDialog peut être utilisé pour attendre toute tâche d’arrière-plan dont l’achèvement peut être testé à l’aide d’une expression conditionnelle telle que l’état d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="0a5c0-118">The SpawnWaitDialog ControlEvent can be used to wait for any background task the completion of which can be tested using a conditional expression such as the state of a property.</span></span> <span data-ttu-id="0a5c0-119">Pour obtenir un exemple d’utilisation de SpawnWaitDialog ControlEvent,, consultez la section [création d’un conditionnel « Veuillez patienter... » MessageBox.](authoring-a-conditional-please-wait-------message-box.md)</span><span class="sxs-lookup"><span data-stu-id="0a5c0-119">For an example of using the SpawnWaitDialog ControlEvent, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

 

 



