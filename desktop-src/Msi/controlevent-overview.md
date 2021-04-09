---
description: ControlEvents est analogue aux messages Microsoft Windows dans les applications Win32.
ms.assetid: ac62bb94-0605-4145-996a-e91fb1a42a77
title: Présentation de ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b92f8662a87bf9040b6a811fc170c25a5cf62ad7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868465"
---
# <a name="controlevent-overview"></a><span data-ttu-id="b22c1-103">Présentation de ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-103">ControlEvent Overview</span></span>

<span data-ttu-id="b22c1-104">ControlEvents est analogue aux messages Microsoft Windows dans les applications Win32.</span><span class="sxs-lookup"><span data-stu-id="b22c1-104">ControlEvents are analogous to Microsoft Windows messages in Win32-based applications.</span></span> <span data-ttu-id="b22c1-105">Toutefois, au lieu de créer une fonction de rappel pour recevoir des messages Windows et envoyer des messages Windows avec la fonction [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) , le programme d’installation de l’interface utilisateur et les contrôles publient [ControlEvents](control-events.md).</span><span class="sxs-lookup"><span data-stu-id="b22c1-105">However, rather than creating a callback function to receive Windows messages and sending Windows messages with the [SendMessage](/windows/win32/api/winuser/nf-winuser-sendmessage) function, the user interface (UI) installer and controls publish [ControlEvents](control-events.md).</span></span> <span data-ttu-id="b22c1-106">D’autres contrôles et le programme d’installation peuvent être spécifiés pour s’abonner à un ControlEvents particulier qui modifie ensuite les attributs du contrôle d’abonnement.</span><span class="sxs-lookup"><span data-stu-id="b22c1-106">Other controls and the installer can be specified to subscribe to particular ControlEvents that will then change attributes of the subscribing control.</span></span> <span data-ttu-id="b22c1-107">Pour ajouter des contrôles de travail aux boîtes de dialogue, l’auteur de l’interface utilisateur spécifie la publication de ControlEvents dans la [table ControlEvent,](controlevent-table.md) et abonne les contrôles à ControlEvents dans la [table EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="b22c1-107">To add working controls to dialog boxes, the author of the UI specifies the publication of ControlEvents in the [ControlEvent table](controlevent-table.md) and subscribes controls to ControlEvents in the [EventMapping table](eventmapping-table.md).</span></span>

<span data-ttu-id="b22c1-108">Le programme d’installation publiera les événements suivants sur les contrôles d’abonnement listés dans le [tableau EventMapping](eventmapping-table.md).</span><span class="sxs-lookup"><span data-stu-id="b22c1-108">The installer will publish the following events to subscribing controls listed in the [EventMapping table](eventmapping-table.md).</span></span> <span data-ttu-id="b22c1-109">Un contrôle [ProgressBar](progressbar-control.md) ou un contrôle de tableau [blanc](billboard-control.md) s’abonne généralement à SetProgress, le reste est abonné aux [contrôles de texte](text-control.md).</span><span class="sxs-lookup"><span data-stu-id="b22c1-109">A [ProgressBar control](progressbar-control.md) or [Billboard control](billboard-control.md) typically subscribes to SetProgress, the rest are subscribed to by [Text controls](text-control.md).</span></span>

[<span data-ttu-id="b22c1-110">ActionData ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-110">ActionData ControlEvent</span></span>](actiondata-controlevent.md)

[<span data-ttu-id="b22c1-111">ActionText ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-111">ActionText ControlEvent</span></span>](actiontext-controlevent.md)

[<span data-ttu-id="b22c1-112">SetProgress ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-112">SetProgress ControlEvent</span></span>](setprogress-controlevent.md)

[<span data-ttu-id="b22c1-113">TimeRemaining ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-113">TimeRemaining ControlEvent</span></span>](timeremaining-controlevent.md)

[<span data-ttu-id="b22c1-114">ScriptInProgress ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-114">ScriptInProgress ControlEvent</span></span>](scriptinprogress-controlevent.md)

<span data-ttu-id="b22c1-115">Les événements suivants sont publiés par le contrôle lorsque la sélection de l’élément est déplacée dans un contrôle [SelectionTree](selectiontree-control.md) ou un [contrôle DirectoryList](directorylist-control.md).</span><span class="sxs-lookup"><span data-stu-id="b22c1-115">The following events are published by the control when the item selection is moved in a [SelectionTree control](selectiontree-control.md) or [DirectoryList Control](directorylist-control.md).</span></span> <span data-ttu-id="b22c1-116">Les contrôles d’abonnement doivent se trouver dans la même boîte de dialogue et être listés dans le tableau EventMapping.</span><span class="sxs-lookup"><span data-stu-id="b22c1-116">Subscribing controls must be located on the same dialog box and listed in the EventMapping table.</span></span>

[<span data-ttu-id="b22c1-117">IgnoreChange ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-117">IgnoreChange ControlEvent</span></span>](ignorechange-controlevent.md)

[<span data-ttu-id="b22c1-118">SelectionDescription ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-118">SelectionDescription ControlEvent</span></span>](selectiondescription-controlevent.md)

[<span data-ttu-id="b22c1-119">Sélection de ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-119">SelectionSize ControlEvent</span></span>](selectionsize-controlevent.md)

[<span data-ttu-id="b22c1-120">SelectionPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-120">SelectionPath ControlEvent</span></span>](selectionpath-controlevent.md)

[<span data-ttu-id="b22c1-121">SelectionAction ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-121">SelectionAction ControlEvent</span></span>](selectionaction-controlevent.md)

[<span data-ttu-id="b22c1-122">SelectionNoItems ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-122">SelectionNoItems ControlEvent</span></span>](selectionnoitems-controlevent.md)

<span data-ttu-id="b22c1-123">Le ControlEvents suivant peut être publié à la discrétion d’un utilisateur en interagissant avec un contrôle de [bouton de commande](pushbutton-control.md) ou un contrôle de [case à cocher](checkbox-control.md) sur une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b22c1-123">The following ControlEvents can be published at the discretion of a user by interacting with a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) on a dialog box.</span></span> <span data-ttu-id="b22c1-124">Le contrôle CheckBox peut uniquement publier les événements AddLocal, AddSource, Remove, inaction et SetProperty.</span><span class="sxs-lookup"><span data-stu-id="b22c1-124">The Checkbox control can only publish the AddLocal, AddSource, Remove, DoAction, and SetProperty events.</span></span> <span data-ttu-id="b22c1-125">Avec les versions de Windows Installer fournies avec Windows Server 2003 et versions ultérieures, le [contrôle SelectionTree](selectiontree-control.md) peut publier les actions action, ControlEvent, et SetProperty ControlEvents.</span><span class="sxs-lookup"><span data-stu-id="b22c1-125">With Windows Installer versions that shipped with Windows Server 2003 and later, the [SelectionTree control](selectiontree-control.md) can publish the DoAction, ControlEvent and SetProperty ControlEvents.</span></span> <span data-ttu-id="b22c1-126">L’auteur de l’interface utilisateur doit répertorier le ControlEvent, dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="b22c1-126">The author of the UI should list the ControlEvent in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="b22c1-127">Le gestionnaire d’interface utilisateur du programme d’installation est l’abonné à ces événements.</span><span class="sxs-lookup"><span data-stu-id="b22c1-127">The UI handler of the installer is the subscriber to these events.</span></span>

[<span data-ttu-id="b22c1-128">AddLocal ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-128">AddLocal ControlEvent</span></span>](addlocal-controlevent.md)

[<span data-ttu-id="b22c1-129">AddSource ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-129">AddSource ControlEvent</span></span>](addsource-controlevent.md)

[<span data-ttu-id="b22c1-130">CheckExistingTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-130">CheckExistingTargetPath ControlEvent</span></span>](checkexistingtargetpath-controlevent.md)

[<span data-ttu-id="b22c1-131">CheckTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-131">CheckTargetPath ControlEvent</span></span>](checktargetpath-controlevent.md)

[<span data-ttu-id="b22c1-132">Action ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-132">DoAction ControlEvent</span></span>](doaction-controlevent.md)

[<span data-ttu-id="b22c1-133">EnableRollback ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-133">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)

[<span data-ttu-id="b22c1-134">ControlEvent, EndDialog</span><span class="sxs-lookup"><span data-stu-id="b22c1-134">EndDialog ControlEvent</span></span>](enddialog-controlevent.md)

[<span data-ttu-id="b22c1-135">NewDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-135">NewDialog ControlEvent</span></span>](newdialog-controlevent.md)

[<span data-ttu-id="b22c1-136">Réinstaller ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-136">Reinstall ControlEvent</span></span>](reinstall-controlevent.md)

[<span data-ttu-id="b22c1-137">ReinstallMode ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-137">ReinstallMode ControlEvent</span></span>](reinstallmode-controlevent.md)

[<span data-ttu-id="b22c1-138">Supprimer ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-138">Remove ControlEvent</span></span>](remove-controlevent.md)

[<span data-ttu-id="b22c1-139">Réinitialiser ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-139">Reset ControlEvent</span></span>](reset-controlevent.md)

[<span data-ttu-id="b22c1-140">SetInstallLevel ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-140">SetInstallLevel ControlEvent</span></span>](setinstalllevel-controlevent.md)

[<span data-ttu-id="b22c1-141">ControlEvent, SetProperty</span><span class="sxs-lookup"><span data-stu-id="b22c1-141">SetProperty ControlEvent</span></span>](setproperty-controlevent.md)

[<span data-ttu-id="b22c1-142">SetTargetPath ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-142">SetTargetPath ControlEvent</span></span>](settargetpath-controlevent.md)

[<span data-ttu-id="b22c1-143">SpawnDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-143">SpawnDialog ControlEvent</span></span>](spawndialog-controlevent.md)

[<span data-ttu-id="b22c1-144">SpawnWaitDialog ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-144">SpawnWaitDialog ControlEvent</span></span>](spawnwaitdialog-controlevent.md)

[<span data-ttu-id="b22c1-145">ValidateProductID ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-145">ValidateProductID ControlEvent</span></span>](validateproductid-controlevent.md)

<span data-ttu-id="b22c1-146">Un [contrôle PUSHBUTTON](pushbutton-control.md) peut publier les événements suivants dans un contrôle [SelectionTree](selectiontree-control.md) d’abonnement ou un [contrôle DirectoryList](directorylist-control.md) situé dans la même boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b22c1-146">A [PushButton control](pushbutton-control.md) can publish the following events to a subscribing [SelectionTree control](selectiontree-control.md) or [DirectoryList control](directorylist-control.md) located in the same dialog box.</span></span> <span data-ttu-id="b22c1-147">Le contrôle PushButton doit être listé dans la table ControlEvent, et les contrôles d’abonnement doivent être listés dans la table EventMapping.</span><span class="sxs-lookup"><span data-stu-id="b22c1-147">The PushButton Control should be listed in the ControlEvent table and the subscribing controls should be listed in the EventMapping table.</span></span>

[<span data-ttu-id="b22c1-148">SelectionBrowse ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-148">SelectionBrowse ControlEvent</span></span>](selectionbrowse-controlevent.md)

[<span data-ttu-id="b22c1-149">DirectoryListUp ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-149">DirectoryListUp ControlEvent</span></span>](directorylistup-controlevent.md)

[<span data-ttu-id="b22c1-150">DirectoryListNew ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-150">DirectoryListNew ControlEvent</span></span>](directorylistnew-controlevent.md)

[<span data-ttu-id="b22c1-151">DirectoryListOpen ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="b22c1-151">DirectoryListOpen ControlEvent</span></span>](directorylistopen-controlevent.md)

<span data-ttu-id="b22c1-152">Les événements de contrôle requièrent généralement que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="b22c1-152">Control events generally require that the UI be run at the [*full UI*](f-gly.md) level.</span></span> <span data-ttu-id="b22c1-153">La plupart des ControlEvents ne fonctionneront pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md) , car ces niveaux affichent uniquement des boîtes de dialogue non modales.</span><span class="sxs-lookup"><span data-stu-id="b22c1-153">Most ControlEvents will not work with a [*reduced UI*](r-gly.md) or [*basic UI*](b-gly.md) because these levels only display modeless dialog boxes.</span></span> <span data-ttu-id="b22c1-154">Les événements ActionText, AddSource, SetProgress, TimeRemaining et ScriptInProgress sont des exceptions et fonctionnent dans une interface utilisateur réduite ou de base.</span><span class="sxs-lookup"><span data-stu-id="b22c1-154">The ActionText, AddSource, SetProgress, TimeRemaining, and ScriptInProgress events are exceptions and will work in reduced or basic UI.</span></span> <span data-ttu-id="b22c1-155">Pour plus d’informations sur les niveaux d’interface utilisateur, consultez [niveaux d’interface utilisateur](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="b22c1-155">For more information about UI levels, see [User Interface Levels](user-interface-levels.md).</span></span>

<span data-ttu-id="b22c1-156">Vous pouvez exécuter des [actions personnalisées](custom-actions.md) en publiant un ControlEvent, à partir d’un contrôle de [bouton de commande](pushbutton-control.md) ou d’un [contrôle CheckBox](checkbox-control.md).</span><span class="sxs-lookup"><span data-stu-id="b22c1-156">You can run [custom actions](custom-actions.md) by publishing a ControlEvent from a [PushButton control](pushbutton-control.md) or [Checkbox control](checkbox-control.md).</span></span> <span data-ttu-id="b22c1-157">Ajoutez un enregistrement à la [table ControlEvent,](controlevent-table.md) avec les noms de la boîte de dialogue et le contrôle qui publie ControlEvent,.</span><span class="sxs-lookup"><span data-stu-id="b22c1-157">Add a record to the [ControlEvent table](controlevent-table.md) with the names of the dialog and the control publishing the ControlEvent.</span></span> <span data-ttu-id="b22c1-158">Ce contrôle doit publier un [ControlEvent,](doaction-controlevent.md) de script qui notifie le programme d’installation de l’exécution de l’action personnalisée.</span><span class="sxs-lookup"><span data-stu-id="b22c1-158">This control should publish a [DoAction ControlEvent](doaction-controlevent.md) notifying the installer to run the custom action.</span></span> <span data-ttu-id="b22c1-159">Sur les systèmes Windows XP ou versions antérieures, vous ne pouvez pas exécuter une action personnalisée en publiant un ControlEvent, à partir d’un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="b22c1-159">On Windows XP or earlier systems, you cannot run a custom action by publishing a ControlEvent from a [SelectionTree control](selectiontree-control.md).</span></span>

<span data-ttu-id="b22c1-160">Pour plus d’informations sur le ControlEvents particulier, consultez la liste des données de [référence de l’interface utilisateur](user-interface-reference.md)standard [ControlEvents](control-events.md) .</span><span class="sxs-lookup"><span data-stu-id="b22c1-160">For a more information about particular ControlEvents, see the list of standard [ControlEvents](control-events.md) in [User Interface Reference](user-interface-reference.md).</span></span>

 

 
