---
description: Le contrôle d’affichage des panneaux affiche les contrôles couramment utilisés qui sont ajoutés et supprimés de la boîte de dialogue par ControlEvents.
ms.assetid: c4c0ed5a-2518-499f-805f-dcbe0b0f9393
title: Contrôle de tableau blanc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5671cd9f345bb4a93efb0a103017fe733bf35beaf58d271c1c2e9906daa9ddf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105399"
---
# <a name="billboard-control"></a>Contrôle de tableau blanc

Le contrôle d’affichage des panneaux affiche les contrôles couramment utilisés qui sont ajoutés et supprimés de la boîte de dialogue par ControlEvents. Seuls les contrôles qui ne sont pas associés à une propriété, tels que [Text](text-control.md), [bitmap](bitmap-control.md)ou [Icon](icon-control.md), ou des contrôles personnalisés peuvent être placés sur un panneau. Les contrôles de tableau blanc affichent généralement des messages de progression.

## <a name="control-attributes"></a>Attributs du contrôle

Vous pouvez utiliser les attributs suivants avec le contrôle de tableau blanc. Pour modifier la valeur d’un attribut à l’aide d’un événement, abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md) et répertoriez l’identificateur de l’attribut dans la colonne d’attribut. Entrez l’identificateur du ControlEvent, dans la colonne d’événement.



| Identificateur d’attribut                                 | Bit hexadécimal                  | Description                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BillboardName](billboardname-control-attribute.md) |                                  | Nom du panneau de l’en-cours. Entrez l’identificateur du panneau des panneaux dans la colonne de tableau de la [table BBControl](bbcontrol-table.md).<br/>                                                                                                                                                                            |
| [Position](position-control-attribute.md)           |                                  | Position du contrôle dans la boîte de dialogue. Entrez la largeur, la hauteur et les coordonnées du contrôle dans la largeur, la hauteur, le X et les colonnes Y de la [table BBControl](bbcontrol-table.md). Utilisez les [unités d’installation](installer-units.md) pour la longueur et la distance.<br/>                                |
| [Visible](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | Contrôle masqué. Contrôle visible.<br/> Incluez ce bit dans le mot de bits de la colonne d’attributs dans la [table BBControl](bbcontrol-table.md) pour rendre le contrôle visible ou masqué lors de sa création.<br/> Masquer ou afficher un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | Affiche le style visuel par défaut. Affiche le contrôle avec une apparence enfoncée, 3D et un look.<br/> Incluez ces bits dans le mot de bits dans la colonne attributs de la [table de contrôle](control-table.md).<br/>                                                                                                               |



 

## <a name="remarks"></a>Remarques

Ce contrôle n’a pas de fenêtre propre.

Les contrôles de tableau blanc qui s’affichent dans l’interface utilisateur complète sont répertoriés dans le [tableau des panneaux](billboard-table.md).

Les contrôles qui se trouvent dans un tableau blanc doivent être répertoriés dans la [table BBControl](bbcontrol-table.md) et non dans la [table de contrôle](control-table.md).

 

 




