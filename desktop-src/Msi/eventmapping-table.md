---
description: le tableau EventMapping répertorie les contrôles qui s’abonnent à certains événements de contrôle, et répertorie l’attribut à modifier lorsque l’événement est publié par un autre contrôle ou le Windows Installer.
ms.assetid: 63c9ba3e-aa8a-475b-8360-4aec78ed19db
title: Table EventMapping
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f17380e3e91669926ef50532c36fec71f44d61eb2ed7273d053defe45fa874e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963109"
---
# <a name="eventmapping-table"></a>Table EventMapping

le tableau EventMapping répertorie les contrôles qui s’abonnent à certains événements de contrôle, et répertorie l’attribut à modifier lorsque l’événement est publié par un autre contrôle ou le Windows Installer.

La table EventMapping contient les colonnes suivantes.



| Colonne    | Type                         | Clé | Nullable |
|-----------|------------------------------|-----|----------|
| Boîte de dialogue\_  | [Identificateur](identifier.md) | O   | N        |
| contrôle\_ | [Identificateur](identifier.md) | O   | N        |
| Événement     | [Identificateur](identifier.md) | O   | N        |
| Attribut | [Identificateur](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Dialog_"></span><span id="dialog_"></span><span id="DIALOG_"></span>Dialogue\_
</dt> <dd>

Clé externe de la première colonne de la [table de boîtes de dialogue](dialog-table.md). Ce champ et le champ de contrôle \_ identifient ensemble un contrôle.

</dd> <dt>

<span id="Control_"></span><span id="control_"></span><span id="CONTROL_"></span>Régulation\_
</dt> <dd>

Clé externe de la deuxième colonne de la [table de contrôle](control-table.md). Ce champ et le champ de la boîte de dialogue \_ identifient un contrôle.

</dd> <dt>

<span id="Event"></span><span id="event"></span><span id="EVENT"></span>Événement
</dt> <dd>

Ce champ est un identificateur qui spécifie le type d’événement auquel le contrôle s’abonne. Pour plus d’informations, consultez [vue d’ensemble de ControlEvent,](controlevent-overview.md).

</dd> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribut
</dt> <dd>

Nom de l’attribut de contrôle \_ défini lors de la réception de l’événement dans la colonne d’événement. L’argument de l’événement est passé comme argument de l’appel d’attribut pour modifier cet attribut du contrôle.

</dd> </dl>

## <a name="remarks"></a>Remarques

La [table ControlEvent,](controlevent-table.md) spécifie les événements de contrôle qui sont démarrés lorsqu’un utilisateur interagit avec un contrôle de [bouton](pushbutton-control.md)de commande, un [contrôle de case à cocher](checkbox-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Il s’agit des seuls contrôles qu’un utilisateur peut utiliser pour initier des événements de contrôle.

Plus d’un contrôle sur une boîte de dialogue peut s’abonner au même événement.

La liste suivante identifie les utilisations typiques de la table EventMapping :

-   pour abonner un [contrôle de texte](text-control.md) à un [controlevent, ActionText](actiontext-controlevent.md), [ActionData controlevent,](actiondata-controlevent.md), [ScriptInProgress controlevent,](scriptinprogress-controlevent.md) ou [TimeRemaining controlevent,](timeremaining-controlevent.md) publié par le Windows Installer.
-   Pour abonner un contrôle [ProgressBar](progressbar-control.md) ou un [contrôle Billboard](billboard-control.md) à un [ControlEvent, SetProgress](setprogress-controlevent.md).
-   Pour abonner un [contrôle DirectoryCombo](directorycombo-control.md) à un [ControlEvent, IgnoreChange](ignorechange-controlevent.md).
-   Pour désactiver automatiquement un [contrôle PUSHBUTTON](pushbutton-control.md) situé dans la même boîte de dialogue avec un [contrôle SelectionTree](selectiontree-control.md). Pour désactiver le bouton de commande lorsque aucune fonctionnalité n’est répertoriée dans le [contrôle SelectionTree](selectiontree-control.md), utilisez la table EventMapping pour abonner le contrôle PUSHBUTTON à un [ControlEvent, SelectionNoItems](selectionnoitems-controlevent.md). Entrez **Enable** dans le champ attributs de la table EventMapping.
-   Pour afficher un [contrôle de texte](text-control.md) qui affiche le chemin d’accès à l’emplacement d’installation de la fonctionnalité sélectionnée dans un [contrôle SelectionTree](selectiontree-control.md) de la même boîte de dialogue. Utilisez la table EventMapping pour abonner [le contrôle de texte](text-control.md) à une [SelectionPathOn ControlEvent,](selectionpathon-controlevent.md) et [SelectionPath ControlEvent,](selectionpath-controlevent.md) publiée par le [contrôle SelectionTree](selectiontree-control.md).
-   Pour afficher un [contrôle de texte](text-control.md) qui affiche une description de l’élément mis en surbrillance dans un [contrôle SelectionTree](selectiontree-control.md) situé dans la même boîte de dialogue, utilisez la table EventMapping pour abonner le [contrôle de texte](text-control.md) à un [SelectionDescription ControlEvent,](selectiondescription-controlevent.md), [Sélectionner ControlEvent,](selectionsize-controlevent.md) ou [SelectionAction ControlEvent,](selectionaction-controlevent.md). Entrez le **texte** dans le champ attribut de la table EventMapping.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
</dl>

 

 



