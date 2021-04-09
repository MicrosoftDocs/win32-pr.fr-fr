---
description: La table ControlEvent, permet à l’auteur de spécifier les événements de contrôle démarrés lorsqu’un utilisateur interagit avec un contrôle de bouton de commande, un contrôle de case à cocher ou un contrôle SelectionTree.
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: Table ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 721dc7ac9a729b8df0623a2958a4d0fe32851307
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868462"
---
# <a name="controlevent-table"></a><span data-ttu-id="353c9-103">Table ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="353c9-103">ControlEvent Table</span></span>

<span data-ttu-id="353c9-104">La table ControlEvent, permet à l’auteur de spécifier [les événements de contrôle](control-events.md) démarrés lorsqu’un utilisateur interagit avec un contrôle de [bouton](pushbutton-control.md)de commande, un contrôle de [case à cocher](checkbox-control.md)ou un [contrôle SelectionTree](selectiontree-control.md).</span><span class="sxs-lookup"><span data-stu-id="353c9-104">The ControlEvent table allows the author to specify the [Control Events](control-events.md) started when a user interacts with a [PushButton Control](pushbutton-control.md), [CheckBox Control](checkbox-control.md), or [SelectionTree Control](selectiontree-control.md).</span></span> <span data-ttu-id="353c9-105">Il s’agit des seuls contrôles que les utilisateurs peuvent utiliser pour initier des événements de contrôle.</span><span class="sxs-lookup"><span data-stu-id="353c9-105">These are the only controls users can use to initiate control events.</span></span> <span data-ttu-id="353c9-106">Chaque contrôle peut publier plusieurs événements de contrôle.</span><span class="sxs-lookup"><span data-stu-id="353c9-106">Each control can publish multiple control events.</span></span> <span data-ttu-id="353c9-107">Le programme d’installation démarre chaque événement dans l’ordre spécifié dans la colonne classement.</span><span class="sxs-lookup"><span data-stu-id="353c9-107">The installer starts each event in the order specified in the Ordering column.</span></span> <span data-ttu-id="353c9-108">Par exemple, un contrôle de bouton de commande peut publier des événements pour lancer une transition vers une autre boîte de dialogue, quitter la séquence de la boîte de dialogue et commencer l’installation du fichier.</span><span class="sxs-lookup"><span data-stu-id="353c9-108">For example, a push button control can publish events to initiate a transition to another dialog box, exit the dialog box sequence, and begin file installation.</span></span>

<span data-ttu-id="353c9-109">La seule exception à noter est que chaque contrôle peut publier un [NewDialog](newdialog-controlevent.md) ou un événement [SpawnDialog](spawndialog-controlevent.md) .</span><span class="sxs-lookup"><span data-stu-id="353c9-109">The exception to note is that each control can publish a most one [NewDialog](newdialog-controlevent.md) or one [SpawnDialog](spawndialog-controlevent.md) event.</span></span> <span data-ttu-id="353c9-110">Si vous avez besoin de créer plusieurs événements de contrôle NewDialog et SpawnDialog dans ce tableau, incluez également des instructions conditionnelles dans les champs de condition qui garantissent qu’au plus un événement est publié.</span><span class="sxs-lookup"><span data-stu-id="353c9-110">If you need to author multiple NewDialog and SpawnDialog control events in this table, also include conditional statements in the Condition fields that ensure at most one event is published.</span></span> <span data-ttu-id="353c9-111">Si plusieurs événements de contrôle NewDialog et SpawnDialog sont sélectionnés pour le même contrôle, seul l’événement ayant la plus grande valeur dans la colonne Ordering est publié lorsque le contrôle est activé.</span><span class="sxs-lookup"><span data-stu-id="353c9-111">If multiple NewDialog and SpawnDialog control events are selected for the same control, only the event with the largest value in the Ordering column gets published when the control is activated.</span></span>

<span data-ttu-id="353c9-112">La table ControlEvent, contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="353c9-112">The ControlEvent table has the following columns.</span></span>



| <span data-ttu-id="353c9-113">Colonne</span><span class="sxs-lookup"><span data-stu-id="353c9-113">Column</span></span>    | <span data-ttu-id="353c9-114">Type</span><span class="sxs-lookup"><span data-stu-id="353c9-114">Type</span></span>                         | <span data-ttu-id="353c9-115">Clé</span><span class="sxs-lookup"><span data-stu-id="353c9-115">Key</span></span> | <span data-ttu-id="353c9-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="353c9-116">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="353c9-117">Dialogue\_</span><span class="sxs-lookup"><span data-stu-id="353c9-117">Dialog\_</span></span>  | [<span data-ttu-id="353c9-118">Identificateur</span><span class="sxs-lookup"><span data-stu-id="353c9-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="353c9-119">O</span><span class="sxs-lookup"><span data-stu-id="353c9-119">Y</span></span>   | <span data-ttu-id="353c9-120">N</span><span class="sxs-lookup"><span data-stu-id="353c9-120">N</span></span>        |
| <span data-ttu-id="353c9-121">contrôle\_</span><span class="sxs-lookup"><span data-stu-id="353c9-121">Control\_</span></span> | [<span data-ttu-id="353c9-122">Identificateur</span><span class="sxs-lookup"><span data-stu-id="353c9-122">Identifier</span></span>](identifier.md) | <span data-ttu-id="353c9-123">O</span><span class="sxs-lookup"><span data-stu-id="353c9-123">Y</span></span>   | <span data-ttu-id="353c9-124">N</span><span class="sxs-lookup"><span data-stu-id="353c9-124">N</span></span>        |
| <span data-ttu-id="353c9-125">Événement</span><span class="sxs-lookup"><span data-stu-id="353c9-125">Event</span></span>     | [<span data-ttu-id="353c9-126">Correct</span><span class="sxs-lookup"><span data-stu-id="353c9-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="353c9-127">O</span><span class="sxs-lookup"><span data-stu-id="353c9-127">Y</span></span>   | <span data-ttu-id="353c9-128">N</span><span class="sxs-lookup"><span data-stu-id="353c9-128">N</span></span>        |
| <span data-ttu-id="353c9-129">Argument</span><span class="sxs-lookup"><span data-stu-id="353c9-129">Argument</span></span>  | [<span data-ttu-id="353c9-130">Correct</span><span class="sxs-lookup"><span data-stu-id="353c9-130">Formatted</span></span>](formatted.md)   | <span data-ttu-id="353c9-131">O</span><span class="sxs-lookup"><span data-stu-id="353c9-131">Y</span></span>   | <span data-ttu-id="353c9-132">N</span><span class="sxs-lookup"><span data-stu-id="353c9-132">N</span></span>        |
| <span data-ttu-id="353c9-133">Condition</span><span class="sxs-lookup"><span data-stu-id="353c9-133">Condition</span></span> | [<span data-ttu-id="353c9-134">Condition</span><span class="sxs-lookup"><span data-stu-id="353c9-134">Condition</span></span>](condition.md)   | <span data-ttu-id="353c9-135">O</span><span class="sxs-lookup"><span data-stu-id="353c9-135">Y</span></span>   | <span data-ttu-id="353c9-136">O</span><span class="sxs-lookup"><span data-stu-id="353c9-136">Y</span></span>        |
| <span data-ttu-id="353c9-137">Classement</span><span class="sxs-lookup"><span data-stu-id="353c9-137">Ordering</span></span>  | [<span data-ttu-id="353c9-138">Integer</span><span class="sxs-lookup"><span data-stu-id="353c9-138">Integer</span></span>](integer.md)       | <span data-ttu-id="353c9-139">N</span><span class="sxs-lookup"><span data-stu-id="353c9-139">N</span></span>   | <span data-ttu-id="353c9-140">O</span><span class="sxs-lookup"><span data-stu-id="353c9-140">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="353c9-141">Colonnes</span><span class="sxs-lookup"><span data-stu-id="353c9-141">Columns</span></span>

<dl> <dt>

<span data-ttu-id="353c9-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogue\_</span><span class="sxs-lookup"><span data-stu-id="353c9-142"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="353c9-143">Clé externe de la première colonne de la [table de boîtes de dialogue](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="353c9-143">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="353c9-144">La combinaison de ce champ avec le champ de contrôle \_ identifie un contrôle unique.</span><span class="sxs-lookup"><span data-stu-id="353c9-144">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="353c9-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Régulation\_</span><span class="sxs-lookup"><span data-stu-id="353c9-145"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="353c9-146">Clé externe de la deuxième colonne de la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="353c9-146">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="353c9-147">La combinaison de ce champ avec le champ de boîte de dialogue \_ identifie un contrôle unique.</span><span class="sxs-lookup"><span data-stu-id="353c9-147">Combining this field with the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="353c9-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Événement</span><span class="sxs-lookup"><span data-stu-id="353c9-148"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="353c9-149">Identificateur qui spécifie le type d’événement qui doit avoir lieu lorsque l’utilisateur interagit avec le contrôle spécifié par la boîte de dialogue \_ et le contrôle \_ .</span><span class="sxs-lookup"><span data-stu-id="353c9-149">An identifier that specifies the type of event that should take place when the user interacts with the control specified by Dialog\_ and Control\_.</span></span> <span data-ttu-id="353c9-150">Pour obtenir la liste des valeurs possibles, consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="353c9-150">For a list of possible values see [ControlEvent Overview](controlevent-overview.md).</span></span>

<span data-ttu-id="353c9-151">Pour définir une propriété avec un contrôle, placez \[ \_ le nom \] de la propriété dans ce champ et la nouvelle valeur dans le champ argument.</span><span class="sxs-lookup"><span data-stu-id="353c9-151">To set a property with a control, put \[Property\_Name\] in this field and the new value in the argument field.</span></span> <span data-ttu-id="353c9-152">Placez {} dans le champ argument pour entrer la valeur null.</span><span class="sxs-lookup"><span data-stu-id="353c9-152">Put { } into the argument field to enter the null value.</span></span>

</dd> <dt>

<span data-ttu-id="353c9-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span><span class="sxs-lookup"><span data-stu-id="353c9-153"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="353c9-154">Valeur utilisée comme modificateur lors du déclenchement d’un événement particulier.</span><span class="sxs-lookup"><span data-stu-id="353c9-154">A value used as a modifier when triggering a particular event.</span></span>

<span data-ttu-id="353c9-155">Par exemple, l’argument de [NewDialog ControlEvent,](newdialog-controlevent.md) ou [SpawnDialog ControlEvent,](spawndialog-controlevent.md) est le nom de la boîte de dialogue et l’argument de l' [action d’installation](install-action.md) est un nombre définissant le niveau d’installation.</span><span class="sxs-lookup"><span data-stu-id="353c9-155">For example, the argument of the [NewDialog ControlEvent](newdialog-controlevent.md) or the [SpawnDialog ControlEvent](spawndialog-controlevent.md) is the name of the dialog box and the argument of the [Install action](install-action.md) is a number defining the install level.</span></span>

</dd> <dt>

<span data-ttu-id="353c9-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat</span><span class="sxs-lookup"><span data-stu-id="353c9-156"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="353c9-157">Instruction conditionnelle qui détermine si le programme d’installation active l’événement dans la colonne d’événement.</span><span class="sxs-lookup"><span data-stu-id="353c9-157">A conditional statement that determines whether the installer activates the event in the Event column.</span></span> <span data-ttu-id="353c9-158">Le programme d’installation déclenche l’événement si l’instruction conditionnelle dans le champ condition prend la valeur true.</span><span class="sxs-lookup"><span data-stu-id="353c9-158">The installer triggers the event if the conditional statement in the Condition field evaluates to True.</span></span> <span data-ttu-id="353c9-159">Par conséquent, placez un 1 dans cette colonne pour vous assurer que le programme d’installation déclenche l’événement.</span><span class="sxs-lookup"><span data-stu-id="353c9-159">Therefore put a 1 in this column to ensure that the installer triggers the event.</span></span> <span data-ttu-id="353c9-160">Le programme d’installation ne déclenche pas l’événement si le champ condition contient une instruction qui prend la valeur false.</span><span class="sxs-lookup"><span data-stu-id="353c9-160">The installer does not trigger the event if the Condition field contains a statement that evaluates to False.</span></span> <span data-ttu-id="353c9-161">Le programme d’installation ne déclenche pas d’événement avec un vide dans le champ condition, sauf si d’autres événements du contrôle ont la valeur true.</span><span class="sxs-lookup"><span data-stu-id="353c9-161">The installer does not trigger an event with a blank in the Condition field unless no other events of the control evaluate to True.</span></span> <span data-ttu-id="353c9-162">Si aucun des champs de condition pour le contrôle nommé dans le champ de contrôle \_ n’a la valeur true, le programme d’installation déclenche l’événement à l’aide d’un champ de condition vide et, si plusieurs champs de condition sont vides, il déclenche le seul événement avec la plus grande valeur dans le champ de tri.</span><span class="sxs-lookup"><span data-stu-id="353c9-162">If none of the Condition fields for the control named in the Control\_ field evaluate to True, the installer triggers the one event having a blank Condition field, and if more than one Condition field is blank it triggers the one event of these with the largest value in the Ordering field.</span></span> <span data-ttu-id="353c9-163">Consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="353c9-163">See [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="353c9-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Commandé</span><span class="sxs-lookup"><span data-stu-id="353c9-164"><span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Ordering</span></span>
</dt> <dd>

<span data-ttu-id="353c9-165">Entier utilisé pour classer plusieurs événements liés au même contrôle.</span><span class="sxs-lookup"><span data-stu-id="353c9-165">An integer used to order several events tied to the same control.</span></span> <span data-ttu-id="353c9-166">Il doit s’agir d’un nombre non négatif.</span><span class="sxs-lookup"><span data-stu-id="353c9-166">This must be a non-negative number.</span></span> <span data-ttu-id="353c9-167">Ce champ peut être laissé vide.</span><span class="sxs-lookup"><span data-stu-id="353c9-167">This field may be left blank.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="353c9-168">Notes</span><span class="sxs-lookup"><span data-stu-id="353c9-168">Remarks</span></span>

<span data-ttu-id="353c9-169">Le [tableau EventMapping](eventmapping-table.md) répertorie les contrôles qui s’abonnent à un événement de contrôle et répertorie l’attribut de contrôle à modifier lorsque cet événement est publié par un autre contrôle ou le programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="353c9-169">The [EventMapping table](eventmapping-table.md) lists the controls that subscribe to some control event and lists the control attribute to be changed when that event is published by the another control or the installer.</span></span>

<span data-ttu-id="353c9-170">Sur Windows XP ou les systèmes d’exploitation antérieurs, les utilisateurs peuvent publier un événement de contrôle uniquement en interagissant avec un contrôle [CheckBox](checkbox-control.md) ou un [contrôle PUSHBUTTON](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="353c9-170">On Windows XP or earlier operating systems, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md) or [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="353c9-171">Avec Windows Server 2003, les utilisateurs peuvent publier un événement de contrôle uniquement en interagissant avec un contrôle de [case à cocher](checkbox-control.md), un [contrôle SelectionTree](selectiontree-control.md)et un [contrôle PUSHBUTTON](pushbutton-control.md).</span><span class="sxs-lookup"><span data-stu-id="353c9-171">With Windows Server 2003, users can publish a control event only by interacting with a [Checkbox Control](checkbox-control.md), [SelectionTree Control](selectiontree-control.md), and [Pushbutton Control](pushbutton-control.md).</span></span> <span data-ttu-id="353c9-172">La liste d’autres contrôles dans le champ de contrôle n' \_ a aucun effet.</span><span class="sxs-lookup"><span data-stu-id="353c9-172">Listing other controls in the Control\_ field has no effect.</span></span>

## <a name="validation"></a><span data-ttu-id="353c9-173">Validation</span><span class="sxs-lookup"><span data-stu-id="353c9-173">Validation</span></span>

<dl>

[<span data-ttu-id="353c9-174">ICE03</span><span class="sxs-lookup"><span data-stu-id="353c9-174">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="353c9-175">ICE06</span><span class="sxs-lookup"><span data-stu-id="353c9-175">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="353c9-176">ICE17</span><span class="sxs-lookup"><span data-stu-id="353c9-176">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="353c9-177">ICE20</span><span class="sxs-lookup"><span data-stu-id="353c9-177">ICE20</span></span>](ice20.md)  
[<span data-ttu-id="353c9-178">ICE32</span><span class="sxs-lookup"><span data-stu-id="353c9-178">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="353c9-179">ICE44</span><span class="sxs-lookup"><span data-stu-id="353c9-179">ICE44</span></span>](ice44.md)  
[<span data-ttu-id="353c9-180">ICE46</span><span class="sxs-lookup"><span data-stu-id="353c9-180">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="353c9-181">ICE79</span><span class="sxs-lookup"><span data-stu-id="353c9-181">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="353c9-182">ICE86</span><span class="sxs-lookup"><span data-stu-id="353c9-182">ICE86</span></span>](ice86.md)  
</dl>

 

 



