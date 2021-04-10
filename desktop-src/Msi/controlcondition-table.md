---
description: La table ControlCondition permet à un auteur de spécifier des actions spéciales à appliquer aux contrôles en fonction du résultat d’une instruction conditionnelle. Par exemple, à l’aide de cette table, l’auteur peut choisir de masquer un contrôle en fonction de la propriété VersionNT.
ms.assetid: e36d20ec-cd7b-494f-b517-c07b40d2a338
title: Table ControlCondition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 671dcdee6e2ed1067c51a04084693c276b8db2d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952405"
---
# <a name="controlcondition-table"></a><span data-ttu-id="02ebd-104">Table ControlCondition</span><span class="sxs-lookup"><span data-stu-id="02ebd-104">ControlCondition Table</span></span>

<span data-ttu-id="02ebd-105">La table ControlCondition permet à un auteur de spécifier des actions spéciales à appliquer aux contrôles en fonction du résultat d’une instruction conditionnelle.</span><span class="sxs-lookup"><span data-stu-id="02ebd-105">The ControlCondition table enables an author to specify special actions to be applied to controls based on the result of a conditional statement.</span></span> <span data-ttu-id="02ebd-106">Par exemple, à l’aide de cette table, l’auteur peut choisir de masquer un contrôle en fonction de la propriété [**VersionNT**](versionnt.md) .</span><span class="sxs-lookup"><span data-stu-id="02ebd-106">For example, using this table the author could choose to hide a control based on the [**VersionNT**](versionnt.md) property.</span></span>

<span data-ttu-id="02ebd-107">La table ControlCondition contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="02ebd-107">The ControlCondition table has the following columns.</span></span>



| <span data-ttu-id="02ebd-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="02ebd-108">Column</span></span>    | <span data-ttu-id="02ebd-109">Type</span><span class="sxs-lookup"><span data-stu-id="02ebd-109">Type</span></span>                         | <span data-ttu-id="02ebd-110">Clé</span><span class="sxs-lookup"><span data-stu-id="02ebd-110">Key</span></span> | <span data-ttu-id="02ebd-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="02ebd-111">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="02ebd-112">Dialogue\_</span><span class="sxs-lookup"><span data-stu-id="02ebd-112">Dialog\_</span></span>  | [<span data-ttu-id="02ebd-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="02ebd-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="02ebd-114">O</span><span class="sxs-lookup"><span data-stu-id="02ebd-114">Y</span></span>   | <span data-ttu-id="02ebd-115">N</span><span class="sxs-lookup"><span data-stu-id="02ebd-115">N</span></span>        |
| <span data-ttu-id="02ebd-116">contrôle\_</span><span class="sxs-lookup"><span data-stu-id="02ebd-116">Control\_</span></span> | [<span data-ttu-id="02ebd-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="02ebd-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="02ebd-118">O</span><span class="sxs-lookup"><span data-stu-id="02ebd-118">Y</span></span>   | <span data-ttu-id="02ebd-119">N</span><span class="sxs-lookup"><span data-stu-id="02ebd-119">N</span></span>        |
| <span data-ttu-id="02ebd-120">Action</span><span class="sxs-lookup"><span data-stu-id="02ebd-120">Action</span></span>    | [<span data-ttu-id="02ebd-121">Text</span><span class="sxs-lookup"><span data-stu-id="02ebd-121">Text</span></span>](text.md)             | <span data-ttu-id="02ebd-122">O</span><span class="sxs-lookup"><span data-stu-id="02ebd-122">Y</span></span>   | <span data-ttu-id="02ebd-123">N</span><span class="sxs-lookup"><span data-stu-id="02ebd-123">N</span></span>        |
| <span data-ttu-id="02ebd-124">Condition</span><span class="sxs-lookup"><span data-stu-id="02ebd-124">Condition</span></span> | [<span data-ttu-id="02ebd-125">Condition</span><span class="sxs-lookup"><span data-stu-id="02ebd-125">Condition</span></span>](condition.md)   | <span data-ttu-id="02ebd-126">O</span><span class="sxs-lookup"><span data-stu-id="02ebd-126">Y</span></span>   | <span data-ttu-id="02ebd-127">N</span><span class="sxs-lookup"><span data-stu-id="02ebd-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="02ebd-128">Colonnes</span><span class="sxs-lookup"><span data-stu-id="02ebd-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="02ebd-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogue\_</span><span class="sxs-lookup"><span data-stu-id="02ebd-129"><span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialog\_</span></span>
</dt> <dd>

<span data-ttu-id="02ebd-130">Clé externe de la première colonne de la [table de boîtes de dialogue](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="02ebd-130">An external key to the first column of the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="02ebd-131">La combinaison de ce champ avec le champ de contrôle \_ identifie un contrôle unique.</span><span class="sxs-lookup"><span data-stu-id="02ebd-131">Combining this field with the Control\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="02ebd-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Régulation\_</span><span class="sxs-lookup"><span data-stu-id="02ebd-132"><span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Control\_</span></span>
</dt> <dd>

<span data-ttu-id="02ebd-133">Clé externe de la deuxième colonne de la [table de contrôle](control-table.md).</span><span class="sxs-lookup"><span data-stu-id="02ebd-133">An external key to the second column of the [Control table](control-table.md).</span></span> <span data-ttu-id="02ebd-134">Combinaison de ce champ le champ de la boîte de dialogue \_ identifie un contrôle unique.</span><span class="sxs-lookup"><span data-stu-id="02ebd-134">Combining this field the Dialog\_ field identifies a unique control.</span></span>

</dd> <dt>

<span data-ttu-id="02ebd-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel</span><span class="sxs-lookup"><span data-stu-id="02ebd-135"><span id="Action"></span><span id="action"></span><span id="ACTION"></span>Action</span></span>
</dt> <dd>

<span data-ttu-id="02ebd-136">Action qui doit être exécutée sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="02ebd-136">The action that is to be taken on the control.</span></span> <span data-ttu-id="02ebd-137">Les actions possibles sont présentées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="02ebd-137">The possible actions are shown in the following table.</span></span>



| <span data-ttu-id="02ebd-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="02ebd-138">Value</span></span>   | <span data-ttu-id="02ebd-139">Signification</span><span class="sxs-lookup"><span data-stu-id="02ebd-139">Meaning</span></span>                     |
|---------|-----------------------------|
| <span data-ttu-id="02ebd-140">Default</span><span class="sxs-lookup"><span data-stu-id="02ebd-140">Default</span></span> | <span data-ttu-id="02ebd-141">Définir le contrôle comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="02ebd-141">Set control as the default.</span></span> |
| <span data-ttu-id="02ebd-142">Désactiver</span><span class="sxs-lookup"><span data-stu-id="02ebd-142">Disable</span></span> | <span data-ttu-id="02ebd-143">Désactivez le contrôle.</span><span class="sxs-lookup"><span data-stu-id="02ebd-143">Disable the control.</span></span>        |
| <span data-ttu-id="02ebd-144">Activer</span><span class="sxs-lookup"><span data-stu-id="02ebd-144">Enable</span></span>  | <span data-ttu-id="02ebd-145">Activez le contrôle.</span><span class="sxs-lookup"><span data-stu-id="02ebd-145">Enable the control.</span></span>         |
| <span data-ttu-id="02ebd-146">Masquer</span><span class="sxs-lookup"><span data-stu-id="02ebd-146">Hide</span></span>    | <span data-ttu-id="02ebd-147">Masquez le contrôle.</span><span class="sxs-lookup"><span data-stu-id="02ebd-147">Hide the control.</span></span>           |
| <span data-ttu-id="02ebd-148">Afficher</span><span class="sxs-lookup"><span data-stu-id="02ebd-148">Show</span></span>    | <span data-ttu-id="02ebd-149">Affichez le contrôle.</span><span class="sxs-lookup"><span data-stu-id="02ebd-149">Display the control.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="02ebd-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat</span><span class="sxs-lookup"><span data-stu-id="02ebd-150"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="02ebd-151">Instruction conditionnelle qui spécifie les conditions dans lesquelles l’action doit être déclenchée.</span><span class="sxs-lookup"><span data-stu-id="02ebd-151">A conditional statement that specifies under which conditions the action should be triggered.</span></span> <span data-ttu-id="02ebd-152">Cette colonne ne peut pas être vide.</span><span class="sxs-lookup"><span data-stu-id="02ebd-152">This column may not be left blank.</span></span> <span data-ttu-id="02ebd-153">Si cette instruction ne prend pas la valeur TRUE, l’action n’a pas lieu.</span><span class="sxs-lookup"><span data-stu-id="02ebd-153">If this statement does not evaluate to TRUE, the action does not take place.</span></span> <span data-ttu-id="02ebd-154">S’il est défini sur 1, l’action est toujours appliquée.</span><span class="sxs-lookup"><span data-stu-id="02ebd-154">If it is set to 1, the action is always applied.</span></span> <span data-ttu-id="02ebd-155">Pour plus d’informations sur la syntaxe des instructions conditionnelles, consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="02ebd-155">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02ebd-156">Notes</span><span class="sxs-lookup"><span data-stu-id="02ebd-156">Remarks</span></span>

<span data-ttu-id="02ebd-157">Si vous souhaitez masquer et désactiver un contrôle de [bouton de commande](pushbutton-control.md) ou un contrôle de [case à cocher](checkbox-control.md) en fonction d’une instruction conditionnelle dans le champ condition de la table ControlCondition, vous devez utiliser quatre enregistrements pour chaque contrôle afin de désactiver et masquer le contrôle.</span><span class="sxs-lookup"><span data-stu-id="02ebd-157">If you want to hide and disable a [PushButton control](pushbutton-control.md) or [CheckBox control](checkbox-control.md) based on a conditional statement in the Condition field of the ControlCondition table, you should use four records for each control to disable as well as hide the control.</span></span> <span data-ttu-id="02ebd-158">Les contrôles de bouton de commande ou de case à cocher qui ont été masqués sont toujours accessibles par les touches de raccourci.</span><span class="sxs-lookup"><span data-stu-id="02ebd-158">PushButton or CheckBox controls that have only been hidden can still be accessed by shortcut keys.</span></span>

<span data-ttu-id="02ebd-159">Par exemple, les enregistrements suivants masquent et désactivent ControlA sur DIALOGA lorsque le produit est installé.</span><span class="sxs-lookup"><span data-stu-id="02ebd-159">For example, the following records hide and disable ControlA on DialogA when the product is installed.</span></span> <span data-ttu-id="02ebd-160">Le contrôle sera visible et activé lorsque le produit n’est pas installé.</span><span class="sxs-lookup"><span data-stu-id="02ebd-160">The control will be visible and enabled when the product is not installed.</span></span>



| <span data-ttu-id="02ebd-161">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="02ebd-161">Dialog</span></span>  | <span data-ttu-id="02ebd-162">Contrôler</span><span class="sxs-lookup"><span data-stu-id="02ebd-162">Control</span></span>  | <span data-ttu-id="02ebd-163">Action</span><span class="sxs-lookup"><span data-stu-id="02ebd-163">Action</span></span>  | <span data-ttu-id="02ebd-164">Condition</span><span class="sxs-lookup"><span data-stu-id="02ebd-164">Condition</span></span>                      |
|---------|----------|---------|--------------------------------|
| <span data-ttu-id="02ebd-165">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="02ebd-165">DialogA</span></span> | <span data-ttu-id="02ebd-166">ControlA</span><span class="sxs-lookup"><span data-stu-id="02ebd-166">ControlA</span></span> | <span data-ttu-id="02ebd-167">Masquer</span><span class="sxs-lookup"><span data-stu-id="02ebd-167">Hide</span></span>    | [<span data-ttu-id="02ebd-168">**Installé**</span><span class="sxs-lookup"><span data-stu-id="02ebd-168">**Installed**</span></span>](installed.md) |
| <span data-ttu-id="02ebd-169">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="02ebd-169">DialogA</span></span> | <span data-ttu-id="02ebd-170">ControlA</span><span class="sxs-lookup"><span data-stu-id="02ebd-170">ControlA</span></span> | <span data-ttu-id="02ebd-171">Désactiver</span><span class="sxs-lookup"><span data-stu-id="02ebd-171">Disable</span></span> | <span data-ttu-id="02ebd-172">Installé</span><span class="sxs-lookup"><span data-stu-id="02ebd-172">Installed</span></span>                      |
| <span data-ttu-id="02ebd-173">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="02ebd-173">DialogA</span></span> | <span data-ttu-id="02ebd-174">ControlA</span><span class="sxs-lookup"><span data-stu-id="02ebd-174">ControlA</span></span> | <span data-ttu-id="02ebd-175">Afficher</span><span class="sxs-lookup"><span data-stu-id="02ebd-175">Show</span></span>    | <span data-ttu-id="02ebd-176">NON installé</span><span class="sxs-lookup"><span data-stu-id="02ebd-176">NOT Installed</span></span>                  |
| <span data-ttu-id="02ebd-177">Boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="02ebd-177">DialogA</span></span> | <span data-ttu-id="02ebd-178">ControlA</span><span class="sxs-lookup"><span data-stu-id="02ebd-178">ControlA</span></span> | <span data-ttu-id="02ebd-179">Activer</span><span class="sxs-lookup"><span data-stu-id="02ebd-179">Enable</span></span>  | <span data-ttu-id="02ebd-180">NON installé</span><span class="sxs-lookup"><span data-stu-id="02ebd-180">NOT Installed</span></span>                  |



 

## <a name="validation"></a><span data-ttu-id="02ebd-181">Validation</span><span class="sxs-lookup"><span data-stu-id="02ebd-181">Validation</span></span>

<dl>

[<span data-ttu-id="02ebd-182">ICE03</span><span class="sxs-lookup"><span data-stu-id="02ebd-182">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="02ebd-183">ICE06</span><span class="sxs-lookup"><span data-stu-id="02ebd-183">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="02ebd-184">ICE17</span><span class="sxs-lookup"><span data-stu-id="02ebd-184">ICE17</span></span>](ice17.md)  
[<span data-ttu-id="02ebd-185">ICE32</span><span class="sxs-lookup"><span data-stu-id="02ebd-185">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="02ebd-186">ICE46</span><span class="sxs-lookup"><span data-stu-id="02ebd-186">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="02ebd-187">ICE79</span><span class="sxs-lookup"><span data-stu-id="02ebd-187">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="02ebd-188">ICE86</span><span class="sxs-lookup"><span data-stu-id="02ebd-188">ICE86</span></span>](ice86.md)  
</dl>

 

 



