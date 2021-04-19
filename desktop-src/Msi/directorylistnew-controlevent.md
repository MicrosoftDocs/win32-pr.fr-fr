---
description: Cet événement avertit le contrôle DirectoryList qu’un nouveau dossier doit être créé ; Il crée le nouveau dossier et sélectionne le champ nom du dossier pour le modifier.
ms.assetid: dc5859b9-f4b4-4ed7-93d5-369a3d2b9805
title: DirectoryListNew ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c99ce9398cb2780ab6042acb6ad6eaeeff83f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537139"
---
# <a name="directorylistnew-controlevent"></a><span data-ttu-id="19a9f-103">DirectoryListNew ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="19a9f-103">DirectoryListNew ControlEvent</span></span>

<span data-ttu-id="19a9f-104">Cet événement avertit le [contrôle DirectoryList](directorylist-control.md) qu’un nouveau dossier doit être créé ; Il crée le nouveau dossier et sélectionne le champ nom du dossier pour le modifier.</span><span class="sxs-lookup"><span data-stu-id="19a9f-104">This event notifies the [DirectoryList control](directorylist-control.md) that a new folder must be created; it creates the new folder, and selects the name field of the folder for editing.</span></span> <span data-ttu-id="19a9f-105">Le nom par défaut du nouveau dossier peut être créé dans la [table UIText](uitext-table.md).</span><span class="sxs-lookup"><span data-stu-id="19a9f-105">The default name of the new folder may be authored in the [UIText table](uitext-table.md).</span></span> <span data-ttu-id="19a9f-106">Entrez « NewFolder » dans la colonne clé.</span><span class="sxs-lookup"><span data-stu-id="19a9f-106">Enter "NewFolder" into the Key column.</span></span> <span data-ttu-id="19a9f-107">Entrez la valeur du nom par défaut du nouveau dossier dans la colonne de texte.</span><span class="sxs-lookup"><span data-stu-id="19a9f-107">Enter the value for the default name of the new folder into the Text column.</span></span> <span data-ttu-id="19a9f-108">Cette valeur doit se présenter sous la forme d’un type de données de colonne de [nom de fichier](filename.md) et utiliser la \| syntaxe SFN LFN.</span><span class="sxs-lookup"><span data-stu-id="19a9f-108">This value must be in the form of a [Filename](filename.md) column data type and use the SFN\|LFN syntax.</span></span> <span data-ttu-id="19a9f-109">Si cette valeur n’est pas présente dans la table UIText ou n’est pas une valeur valide, le programme d’installation utilise la valeur par défaut « FLDR \| New Folder ».</span><span class="sxs-lookup"><span data-stu-id="19a9f-109">If this value is not present in the UIText table or is an invalid value, the installer uses a default value of "Fldr\|New Folder."</span></span> <span data-ttu-id="19a9f-110">Pour obtenir des informations connexes, consultez [boîte de dialogue Parcourir](browse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="19a9f-110">For related information, see [Browse Dialog](browse-dialog.md).</span></span>

<span data-ttu-id="19a9f-111">Cet événement doit être publié par un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue que le contrôle qui s’abonne à cet événement.</span><span class="sxs-lookup"><span data-stu-id="19a9f-111">This event should be published by a [PushButton Control](pushbutton-control.md) located on the same dialog box as the control subscribing to this event.</span></span> <span data-ttu-id="19a9f-112">L’événement doit être créé dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="19a9f-112">The event should be authored in the [ControlEvent table](controlevent-table.md).</span></span>

<span data-ttu-id="19a9f-113">Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="19a9f-113">This ControlEvent requires the user interface to be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="19a9f-114">Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md).</span><span class="sxs-lookup"><span data-stu-id="19a9f-114">This event will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md).</span></span> <span data-ttu-id="19a9f-115">Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="19a9f-115">For information, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="19a9f-116">Notez que si ce ControlEvent, est rappelé lorsqu’un nouveau dossier existe déjà, un deuxième dossier ne sera pas créé.</span><span class="sxs-lookup"><span data-stu-id="19a9f-116">Note that if this ControlEvent is called again when a new folder already exists, a second new folder will not be created.</span></span> <span data-ttu-id="19a9f-117">Dans ce cas, l’appel de DirectoryListNew sélectionne le nom du nouveau dossier existant pour la modification.</span><span class="sxs-lookup"><span data-stu-id="19a9f-117">In this case, calling DirectoryListNew selects the existing new folder's name for editing.</span></span>

## <a name="published-by"></a><span data-ttu-id="19a9f-118">Publié par</span><span class="sxs-lookup"><span data-stu-id="19a9f-118">Published By</span></span>

[<span data-ttu-id="19a9f-119">DirectoryList</span><span class="sxs-lookup"><span data-stu-id="19a9f-119">DirectoryList</span></span>](directorylist-control.md)

## <a name="argument"></a><span data-ttu-id="19a9f-120">Argument</span><span class="sxs-lookup"><span data-stu-id="19a9f-120">Argument</span></span>

<span data-ttu-id="19a9f-121">Ce ControlEvent, n’utilise pas d’argument.</span><span class="sxs-lookup"><span data-stu-id="19a9f-121">This ControlEvent does not use an argument.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="19a9f-122">Action sur les abonnés</span><span class="sxs-lookup"><span data-stu-id="19a9f-122">Action on Subscribers</span></span>

<span data-ttu-id="19a9f-123">Ce ControlEvent, n’effectue pas d’action sur les abonnés.</span><span class="sxs-lookup"><span data-stu-id="19a9f-123">This ControlEvent does not perform an action on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="19a9f-124">Utilisation courante</span><span class="sxs-lookup"><span data-stu-id="19a9f-124">Typical Use</span></span>

<span data-ttu-id="19a9f-125">Un contrôle [PUSHBUTTON](pushbutton-control.md) sur la même boîte de dialogue modale que le DirectoryList est utilisé pour déclencher la création d’un nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="19a9f-125">A [PushButton](pushbutton-control.md) control on the same modal dialog box as the DirectoryList is used to trigger the creation of a new folder.</span></span>

 

 



