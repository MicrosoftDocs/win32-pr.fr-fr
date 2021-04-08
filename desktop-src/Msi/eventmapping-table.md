---
description: Le tableau EventMapping répertorie les contrôles qui s’abonnent à certains événements de contrôle, et répertorie l’attribut à modifier lorsque l’événement est publié par un autre contrôle ou le Windows Installer.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: Table EventMapping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e9a7b5b4283b5d70102123dcb11e3e9e844221
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864238"
---
# <a name="eventmapping-table"></a><span data-ttu-id="a45ba-103">Table EventMapping</span><span class="sxs-lookup"><span data-stu-id="a45ba-103">EventMapping Table</span></span>

<span data-ttu-id="a45ba-104">Le tableau EventMapping répertorie les contrôles qui s’abonnent à certains événements de contrôle, et répertorie l’attribut à modifier lorsque l’événement est publié par un autre contrôle ou le Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a45ba-104">The EventMapping Table lists the controls that subscribe to some control events, and lists the attribute to be changed when the event is published by another control or the Windows Installer.</span></span>

<span data-ttu-id="a45ba-105">La table EventMapping contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a45ba-105">The EventMapping Table has the following columns.</span></span>



| <span data-ttu-id="a45ba-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="a45ba-106">Column</span></span>    | <span data-ttu-id="a45ba-107">Type</span><span class="sxs-lookup"><span data-stu-id="a45ba-107">Type</span></span>                         | <span data-ttu-id="a45ba-108">Clé</span><span class="sxs-lookup"><span data-stu-id="a45ba-108">Key</span></span> | <span data-ttu-id="a45ba-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="a45ba-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="a45ba-110">Dialogue\_</span><span class="sxs-lookup"><span data-stu-id="a45ba-110">Dialog\_</span></span>  | [<span data-ttu-id="a45ba-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a45ba-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="a45ba-112">O</span><span class="sxs-lookup"><span data-stu-id="a45ba-112">Y</span></span>   | <span data-ttu-id="a45ba-113">N</span><span class="sxs-lookup"><span data-stu-id="a45ba-113">N</span></span>        |
| <span data-ttu-id="a45ba-114">contrôle\_</span><span class="sxs-lookup"><span data-stu-id="a45ba-114">Control\_</span></span> | [<span data-ttu-id="a45ba-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a45ba-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="a45ba-116">O</span><span class="sxs-lookup"><span data-stu-id="a45ba-116">Y</span></span>   | <span data-ttu-id="a45ba-117">N</span><span class="sxs-lookup"><span data-stu-id="a45ba-117">N</span></span>        |
| <span data-ttu-id="a45ba-118">Événement</span><span class="sxs-lookup"><span data-stu-id="a45ba-118">Event</span></span>     | [<span data-ttu-id="a45ba-119">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a45ba-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="a45ba-120">O</span><span class="sxs-lookup"><span data-stu-id="a45ba-120">Y</span></span>   | <span data-ttu-id="a45ba-121">N</span><span class="sxs-lookup"><span data-stu-id="a45ba-121">N</span></span>        |
| <span data-ttu-id="a45ba-122">Attribut</span><span class="sxs-lookup"><span data-stu-id="a45ba-122">Attribute</span></span> | [<span data-ttu-id="a45ba-123">Identificateur</span><span class="sxs-lookup"><span data-stu-id="a45ba-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="a45ba-124">N</span><span class="sxs-lookup"><span data-stu-id="a45ba-124">N</span></span>   | <span data-ttu-id="a45ba-125">N</span><span class="sxs-lookup"><span data-stu-id="a45ba-125">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a45ba-126">Colonnes</span><span class="sxs-lookup"><span data-stu-id="a45ba-126">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a45ba-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogue\_</span><span class="sxs-lookup"><span data-stu-id="a45ba-127"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="a45ba-128">Clé externe de la première colonne de la [table de boîtes de dialogue](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="a45ba-128">An external key to the first column of the [Dialog Table](dialog-table.md).</span></span> <span data-ttu-id="a45ba-129">Ce champ et le champ de contrôle \_ identifient ensemble un contrôle.</span><span class="sxs-lookup"><span data-stu-id="a45ba-129">This field and the Control\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="a45ba-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Régulation\_</span><span class="sxs-lookup"><span data-stu-id="a45ba-130"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="a45ba-131">Clé externe de la deuxième colonne de la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="a45ba-131">An external key to the second column of the [Control Table](control-table.md).</span></span> <span data-ttu-id="a45ba-132">Ce champ et le champ de la boîte de dialogue \_ identifient un contrôle.</span><span class="sxs-lookup"><span data-stu-id="a45ba-132">This field and the Dialog\_ field together identify a control.</span></span>

</dd> <dt>

<span data-ttu-id="a45ba-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Événement</span><span class="sxs-lookup"><span data-stu-id="a45ba-133"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="a45ba-134">Ce champ est un identificateur qui spécifie le type d’événement auquel le contrôle s’abonne.</span><span class="sxs-lookup"><span data-stu-id="a45ba-134">This field is an identifier that specifies the type of event that is subscribed to by the control.</span></span> <span data-ttu-id="a45ba-135">Pour plus d’informations, consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a45ba-135">For more information, see [ControlEvent Overview](controlevent-overview.md).</span></span>

</dd> <dt>

<span data-ttu-id="a45ba-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribut</span><span class="sxs-lookup"><span data-stu-id="a45ba-136"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="a45ba-137">Nom de l’attribut de contrôle \_ défini lors de la réception de l’événement dans la colonne d’événement.</span><span class="sxs-lookup"><span data-stu-id="a45ba-137">The name of the Control\_ attribute that is set when the event in the Event column is received.</span></span> <span data-ttu-id="a45ba-138">L’argument de l’événement est passé comme argument de l’appel d’attribut pour modifier cet attribut du contrôle.</span><span class="sxs-lookup"><span data-stu-id="a45ba-138">The Argument of the event is passed as the argument of the attribute call to change this attribute of the control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a45ba-139">Notes</span><span class="sxs-lookup"><span data-stu-id="a45ba-139">Remarks</span></span>

<span data-ttu-id="a45ba-140">La [table ControlEvent,](controlevent-table.md) spécifie les événements de contrôle qui sont démarrés lorsqu’un utilisateur interagit avec un contrôle de [bouton](pushbutton-control.md)de commande, un [contrôle de case à cocher](checkbox-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="a45ba-140">The [ControlEvent Table](controlevent-table.md) specifies the control events that are started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="a45ba-141">Il s’agit des seuls contrôles qu’un utilisateur peut utiliser pour initier des événements de contrôle.</span><span class="sxs-lookup"><span data-stu-id="a45ba-141">These are the only controls that a user can use to initiate control events.</span></span>

<span data-ttu-id="a45ba-142">Plus d’un contrôle sur une boîte de dialogue peut s’abonner au même événement.</span><span class="sxs-lookup"><span data-stu-id="a45ba-142">More than one control on a dialog box can subscribe to the same event.</span></span>

<span data-ttu-id="a45ba-143">La liste suivante identifie les utilisations typiques de la table EventMapping :</span><span class="sxs-lookup"><span data-stu-id="a45ba-143">The following list identifies the typical uses for the EventMapping Table:</span></span>

-   <span data-ttu-id="a45ba-144">Pour abonner un [contrôle de texte](text-control.md) à un [ControlEvent, ActionText](actiontext-controlevent.md), [ActionData ControlEvent,](actiondata-controlevent.md), [ScriptInProgress controlevent,](scriptinprogress-controlevent.md) ou [TimeRemaining ControlEvent,](timeremaining-controlevent.md) publié par le Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a45ba-144">To subscribe a [Text Control](text-control.md) to an [ActionText ControlEvent](actiontext-controlevent.md), [ActionData ControlEvent](actiondata-controlevent.md), [ScriptInProgress ControlEvent](scriptinprogress-controlevent.md) or [TimeRemaining ControlEvent](timeremaining-controlevent.md) published by the Windows Installer.</span></span>
-   <span data-ttu-id="a45ba-145">Pour abonner un contrôle [ProgressBar](progressbar-control.md) ou un [contrôle Billboard](billboard-control.md) à un [ControlEvent, SetProgress](setprogress-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="a45ba-145">To subscribe a [ProgressBar Control](progressbar-control.md) or [Billboard Control](billboard-control.md) to a [SetProgress ControlEvent](setprogress-controlevent.md).</span></span>
-   <span data-ttu-id="a45ba-146">Pour abonner un [contrôle DirectoryCombo](directorycombo-control.md) à un [ControlEvent, IgnoreChange](ignorechange-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="a45ba-146">To subscribe a [DirectoryCombo Control](directorycombo-control.md) to an [IgnoreChange ControlEvent](ignorechange-controlevent.md).</span></span>
-   <span data-ttu-id="a45ba-147">Pour désactiver automatiquement un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue avec un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="a45ba-147">To automatically disable a [PushButton Control](pushbutton-control.md) located on the same dialog with a [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="a45ba-148">Pour désactiver le bouton de commande lorsque aucune fonctionnalité n’est répertoriée dans le [contrôle SelectionTree](selectiontree-control.md), utilisez la table EventMapping pour abonner le contrôle PUSHBUTTON à un [ControlEvent, SelectionNoItems](selectionnoitems-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="a45ba-148">To disable the push button when no features are listed in the [SelectionTree Control](selectiontree-control.md), use the EventMapping Table to subscribe the PushButton control to a [SelectionNoItems ControlEvent](selectionnoitems-controlevent.md).</span></span> <span data-ttu-id="a45ba-149">Entrez **Enable** dans le champ attributs de la table EventMapping.</span><span class="sxs-lookup"><span data-stu-id="a45ba-149">Enter **Enable** in the Attributes field of the EventMapping Table.</span></span>
-   <span data-ttu-id="a45ba-150">Pour afficher un [contrôle de texte](text-control.md) qui affiche le chemin d’accès à l’emplacement d’installation de la fonctionnalité sélectionnée dans un [contrôle SelectionTree](selectiontree-control.md) de la même boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="a45ba-150">To display a [Text Control](text-control.md) that shows the path to the installation location for the feature that is selected in a [SelectionTree Control](selectiontree-control.md) on the same dialog.</span></span> <span data-ttu-id="a45ba-151">Utilisez la table EventMapping pour abonner [le contrôle de texte](text-control.md) à une [SelectionPathOn ControlEvent,](selectionpathon-controlevent.md) et [SelectionPath ControlEvent,](selectionpath-controlevent.md) publiée par le [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="a45ba-151">Use the EventMapping Table to subscribe the [Text Control](text-control.md) to both a [SelectionPathOn ControlEvent](selectionpathon-controlevent.md) and [SelectionPath ControlEvent](selectionpath-controlevent.md) published by the [SelectionTree Control](selectiontree-control.md).</span></span>
-   <span data-ttu-id="a45ba-152">Pour afficher un [contrôle de texte](text-control.md) qui affiche une description de l’élément mis en surbrillance dans un [contrôle SelectionTree](selectiontree-control.md) situé dans la même boîte de dialogue, utilisez la table EventMapping pour abonner le [contrôle de texte](text-control.md) à un [SelectionDescription ControlEvent,](selectiondescription-controlevent.md), [Sélectionner ControlEvent,](selectionsize-controlevent.md) ou [SelectionAction ControlEvent,](selectionaction-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="a45ba-152">To display a [Text Control](text-control.md) that shows a description of the item highlighted in a [SelectionTree Control](selectiontree-control.md) located on the same dialog, use the EventMapping Table to subscribe the [Text Control](text-control.md) to a [SelectionDescription ControlEvent](selectiondescription-controlevent.md), [SelectionSize ControlEvent](selectionsize-controlevent.md) or [SelectionAction ControlEvent](selectionaction-controlevent.md).</span></span> <span data-ttu-id="a45ba-153">Entrez le **texte** dans le champ attribut de la table EventMapping.</span><span class="sxs-lookup"><span data-stu-id="a45ba-153">Enter **Text** in the Attribute field of the EventMapping Table.</span></span>

## <a name="validation"></a><span data-ttu-id="a45ba-154">Validation</span><span class="sxs-lookup"><span data-stu-id="a45ba-154">Validation</span></span>

<dl>

[<span data-ttu-id="a45ba-155">ICE03</span><span class="sxs-lookup"><span data-stu-id="a45ba-155">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a45ba-156">ICE06</span><span class="sxs-lookup"><span data-stu-id="a45ba-156">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a45ba-157">ICE32</span><span class="sxs-lookup"><span data-stu-id="a45ba-157">ICE32</span></span>](ice32.md)  
</dl>

 

 



