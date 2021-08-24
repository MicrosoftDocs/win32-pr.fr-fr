---
description: La table ControlEvent, permet à l’auteur de spécifier les événements de contrôle démarrés lorsqu’un utilisateur interagit avec un contrôle de bouton de commande, un contrôle de case à cocher ou un contrôle SelectionTree.
ms.assetid: e34d17e9-cd6b-4a21-9abc-9562ee648c59
title: Table ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fec4837fa7d98289495bbb0773ae7260f957485cd87214dabf1999b1e1a876c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692999"
---
# <a name="controlevent-table"></a>Table ControlEvent,

La table ControlEvent, permet à l’auteur de spécifier [les événements de contrôle](control-events.md) démarrés lorsqu’un utilisateur interagit avec un contrôle de [bouton](pushbutton-control.md)de commande, un contrôle de [case à cocher](checkbox-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Il s’agit des seuls contrôles que les utilisateurs peuvent utiliser pour initier des événements de contrôle. Chaque contrôle peut publier plusieurs événements de contrôle. Le programme d’installation démarre chaque événement dans l’ordre spécifié dans la colonne classement. Par exemple, un contrôle de bouton de commande peut publier des événements pour lancer une transition vers une autre boîte de dialogue, quitter la séquence de la boîte de dialogue et commencer l’installation du fichier.

La seule exception à noter est que chaque contrôle peut publier un [NewDialog](newdialog-controlevent.md) ou un événement [SpawnDialog](spawndialog-controlevent.md) . Si vous avez besoin de créer plusieurs événements de contrôle NewDialog et SpawnDialog dans ce tableau, incluez également des instructions conditionnelles dans les champs de condition qui garantissent qu’au plus un événement est publié. Si plusieurs événements de contrôle NewDialog et SpawnDialog sont sélectionnés pour le même contrôle, seul l’événement ayant la plus grande valeur dans la colonne Ordering est publié lorsque le contrôle est activé.

La table ControlEvent, contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| Boîte de dialogue\_  | [Identificateur](identifier.md) | O   | N        |
| contrôle\_ | [Identificateur](identifier.md) | O   | N        |
| Événement     | [Correct](formatted.md)   | O   | N        |
| Argument  | [Correct](formatted.md)   | O   | N        |
| Condition | [Condition](condition.md)   | O   | O        |
| Organisation  | [Integer](integer.md)       | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogue\_
</dt> <dd>

Clé externe de la première colonne de la [table de boîtes de dialogue](dialog-table.md). La combinaison de ce champ avec le champ de contrôle \_ identifie un contrôle unique.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Régulation\_
</dt> <dd>

Clé externe de la deuxième colonne de la [table de contrôle](control-table.md). La combinaison de ce champ avec le champ de boîte de dialogue \_ identifie un contrôle unique.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Événement
</dt> <dd>

Identificateur qui spécifie le type d’événement qui doit avoir lieu lorsque l’utilisateur interagit avec le contrôle spécifié par la boîte de dialogue \_ et le contrôle \_ . Pour obtenir la liste des valeurs possibles, consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md).

Pour définir une propriété avec un contrôle, placez \[ \_ le nom \] de la propriété dans ce champ et la nouvelle valeur dans le champ argument. Placez {} dans le champ argument pour entrer la valeur null.

</dd> <dt>

<span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument
</dt> <dd>

Valeur utilisée comme modificateur lors du déclenchement d’un événement particulier.

Par exemple, l’argument de [NewDialog ControlEvent,](newdialog-controlevent.md) ou [SpawnDialog ControlEvent,](spawndialog-controlevent.md) est le nom de la boîte de dialogue et l’argument de l' [action d’installation](install-action.md) est un nombre définissant le niveau d’installation.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Etat
</dt> <dd>

Instruction conditionnelle qui détermine si le programme d’installation active l’événement dans la colonne d’événement. Le programme d’installation déclenche l’événement si l’instruction conditionnelle dans le champ condition prend la valeur true. Par conséquent, placez un 1 dans cette colonne pour vous assurer que le programme d’installation déclenche l’événement. Le programme d’installation ne déclenche pas l’événement si le champ condition contient une instruction qui prend la valeur false. Le programme d’installation ne déclenche pas d’événement avec un vide dans le champ condition, sauf si d’autres événements du contrôle ont la valeur true. Si aucun des champs de condition pour le contrôle nommé dans le champ de contrôle \_ n’a la valeur true, le programme d’installation déclenche l’événement à l’aide d’un champ de condition vide et, si plusieurs champs de condition sont vides, il déclenche le seul événement avec la plus grande valeur dans le champ de tri. Consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).

</dd> <dt>

<span id="Ordering"></span><span id="ordering"></span><span id="ORDERING"></span>Commandé
</dt> <dd>

Entier utilisé pour classer plusieurs événements liés au même contrôle. Il doit s’agir d’un nombre non négatif. Ce champ peut être laissé vide.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le [tableau EventMapping](eventmapping-table.md) répertorie les contrôles qui s’abonnent à un événement de contrôle et répertorie l’attribut de contrôle à modifier lorsque cet événement est publié par un autre contrôle ou le programme d’installation.

sur Windows XP ou les systèmes d’exploitation antérieurs, les utilisateurs peuvent publier un événement de contrôle uniquement en interagissant avec un contrôle [Checkbox](checkbox-control.md) ou un [contrôle Pushbutton](pushbutton-control.md). avec Windows Server 2003, les utilisateurs peuvent publier un événement de contrôle uniquement en interagissant avec un contrôle de [case à cocher](checkbox-control.md), un [contrôle SelectionTree](selectiontree-control.md)et un [contrôle Pushbutton](pushbutton-control.md). La liste d’autres contrôles dans le champ de contrôle n' \_ a aucun effet.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE17](ice17.md)  
[ICE20](ice20.md)  
[ICE32](ice32.md)  
[ICE44](ice44.md)  
[ICE46](ice46.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
</dl>

 

 



