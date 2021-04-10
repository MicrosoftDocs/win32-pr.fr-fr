---
description: La table boîte de dialogue contient toutes les boîtes de dialogue qui s’affichent dans l’interface utilisateur (IU) dans les modes complet et réduit.
ms.assetid: 981386dd-4fee-4003-8c62-16933cc5bd14
title: Table de boîtes de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a210ad051eec950dcff8f8f940a1df11bf74c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866341"
---
# <a name="dialog-table"></a>Table de boîtes de dialogue

La table boîte de dialogue contient toutes les boîtes de dialogue qui s’affichent dans l’interface utilisateur (IU) dans les modes complet et réduit.

La table de boîte de dialogue contient les colonnes suivantes.



| Colonne           | Type                               | Clé | Nullable |
|------------------|------------------------------------|-----|----------|
| Boîte de dialogue           | [Identificateur](identifier.md)       | O   | N        |
| HCentering       | [Integer](integer.md)             | N   | N        |
| VCentering       | [Integer](integer.md)             | N   | N        |
| Largeur            | [Integer](integer.md)             | N   | N        |
| Hauteur           | [Integer](integer.md)             | N   | N        |
| Attributs       | [DoubleInteger](doubleinteger.md) | N   | O        |
| Intitulé            | [Correct](formatted.md)         | N   | O        |
| \_Premier contrôle   | [Identificateur](identifier.md)       | N   | N        |
| \_Valeur par défaut du contrôle | [Identificateur](identifier.md)       | N   | O        |
| Annuler le contrôle \_  | [Identificateur](identifier.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Dialog"></span><span id="dialog"></span><span id="DIALOG"></span>Dialogue
</dt> <dd>

La clé primaire et le nom de la boîte de dialogue.

</dd> <dt>

<span id="HCentering"></span><span id="hcentering"></span><span id="HCENTERING"></span>HCentering
</dt> <dd>

Position horizontale de la boîte de dialogue.

La plage est comprise entre 0 et 100, 0 sur le bord gauche de l’écran et 100 sur le bord droit.

</dd> <dt>

<span id="VCentering"></span><span id="vcentering"></span><span id="VCENTERING"></span>VCentering
</dt> <dd>

Position verticale de la boîte de dialogue.

La plage est comprise entre 0 et 100, 0 étant le bord supérieur de l’écran et 100 au bord inférieur.

</dd> <dt>

<span id="Width"></span><span id="width"></span><span id="WIDTH"></span>Largeur
</dt> <dd>

Largeur de la limite rectangulaire de la boîte de dialogue.

Ce nombre ne doit pas être négatif.

</dd> <dt>

<span id="Height"></span><span id="height"></span><span id="HEIGHT"></span>Celle
</dt> <dd>

Hauteur de la limite rectangulaire de la boîte de dialogue.

Ce nombre ne doit pas être négatif.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

Un mot 32 bits qui spécifie les indicateurs d’attribut à appliquer à cette boîte de dialogue.

Ce nombre ne doit pas être négatif. Pour plus d’informations, consultez [bits de style de boîte de dialogue](dialog-style-bits.md).

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Bonhomme
</dt> <dd>

Chaîne de texte localisable spécifiant le titre à afficher dans la barre de titre de la boîte de dialogue.

</dd> <dt>

<span id="Control_First"></span><span id="control_first"></span><span id="CONTROL_FIRST"></span>\_Premier contrôle
</dt> <dd>

Clé externe de la deuxième colonne de la [table de contrôle](control-table.md).

La combinaison de ce champ avec le champ de boîte de dialogue spécifie un contrôle unique dans la [table de contrôle](control-table.md) qui prend le focus lorsque la boîte de dialogue est ouverte. En règle générale, il peut s’agir d’un contrôle d' [édition](edit-control.md), d’un [contrôle SelectionTree](selectiontree-control.md)ou de tout autre contrôle qui peut prendre le focus. Si le [contrôle PUSHBUTTON](pushbutton-control.md) est le seul contrôle présent dans la boîte de dialogue qui peut prendre le focus, le bouton de commande entré dans le champ ControlDefault doit également être entré dans le premier champ Control. Cette colonne est ignorée dans une boîte de [dialogue d’erreur](error-dialog.md) .

Étant donné que le texte statique ne peut pas prendre le focus, un [contrôle de texte](text-control.md) décrivant un contrôle d' [édition](edit-control.md), un contrôle [PathEdit](pathedit-control.md), un contrôle [ListView](listview-control.md), un [contrôle ComboBox](combobox-control.md) ou un [contrôle VolumeSelectCombo](volumeselectcombo-control.md) doit être rendu en premier contrôle dans la boîte de dialogue pour garantir la compatibilité avec les lecteurs d’écran.

</dd> <dt>

<span id="Control_Default"></span><span id="control_default"></span><span id="CONTROL_DEFAULT"></span>\_Valeur par défaut du contrôle
</dt> <dd>

Clé externe de la deuxième colonne de la [table de contrôle](control-table.md).

La combinaison de ce champ avec le champ de boîte de dialogue spécifie le contrôle par défaut qui prend le focus lorsque la boîte de dialogue est ouverte. En règle générale, il peut s’agir d’un [contrôle PUSHBUTTON](pushbutton-control.md). Si aucun contrôle PushButton sur la boîte de dialogue n’a le focus, la touche Retour équivaut à cliquer sur le contrôle par défaut. Si cette colonne n’est pas renseignée, il n’y a pas de contrôle par défaut. Cette colonne est ignorée dans une boîte de [dialogue d’erreur](error-dialog.md) .

</dd> <dt>

<span id="Control_Cancel"></span><span id="control_cancel"></span><span id="CONTROL_CANCEL"></span>Annuler le contrôle \_
</dt> <dd>

Clé externe de la deuxième colonne de la [table de contrôle](control-table.md).

La combinaison de ce champ avec le champ de boîte de dialogue spécifie un contrôle qui annule l’installation. Ce contrôle est associé à des événements dans la [table ControlEvent,](controlevent-table.md) utilisée pour annuler l’installation. Le fait d’appuyer sur la touche Échap ou de cliquer sur le bouton Fermer équivaut à cliquer sur le contrôle annuler. Cette colonne est ignorée dans une [boîte de dialogue d’erreur](error-dialog.md)

.

Le contrôle Cancel est masqué lors de la restauration ou de la suppression des fichiers sauvegardés. Le gestionnaire d’interface utilisateur interne masque le contrôle lors de la réception d’un \_ message INSTALLMESSAGE COMMONDATA.

</dd> </dl>

## <a name="remarks"></a>Notes

Les valeurs entières pour la largeur et la hauteur se trouvent dans les [unités d’installation](installer-units.md), et non dans les unités de boîte de dialogue.

Les deux valeurs de centrage sont ignorées pour les boîtes de dialogue suivantes dans une séquence d’Assistant. Les positions de la boîte de dialogue sont définies par l’utilisateur ou comme pour la boîte de dialogue précédente. Ces séquences de boîte de dialogue sont créées par un [ControlEvent, NewDialog](newdialog-controlevent.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE13](ice13.md)  
[ICE20](ice20.md)  
[ICE23](ice23.md)  
[ICE27](ice27.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE45](ice45.md)  
[ICE46](ice46.md)  
</dl>

 

 



