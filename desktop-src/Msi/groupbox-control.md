---
description: Le contrôle GroupBox affiche un rectangle, éventuellement avec du texte de légende, qui sert à regrouper d’autres contrôles dans la boîte de dialogue.
ms.assetid: e1cdcf71-876f-4115-96a4-95d8a0f61a9b
title: GroupBox, contrôle (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a3b0ce04006096f97ac28d0a3415e0246d3fbf8489e812e121097cfa25ff995
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649389"
---
# <a name="groupbox-control"></a>GroupBox, contrôle

Le contrôle GroupBox affiche un rectangle, éventuellement avec du texte de légende, qui sert à regrouper d’autres contrôles dans la boîte de dialogue.

## <a name="control-attributes"></a>Attributs du contrôle

Vous pouvez utiliser les attributs suivants avec le contrôle GroupBox. Pour modifier la valeur d’un attribut à l’aide d’un événement, abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md) et répertoriez l’identificateur de l’attribut dans la colonne d’attribut. Entrez l’identificateur du ControlEvent, dans la colonne d’événement.



| Identificateur d’attribut                               | Bit hexadécimal                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)         |                                  | Position du contrôle dans la boîte de dialogue. Entrez la largeur, la hauteur et les coordonnées du contrôle dans la largeur, la hauteur, le X et les colonnes Y de la table de [contrôle](control-table.md) ou de la [table BBControl](bbcontrol-table.md). Utilisez les [unités d’installation](installer-units.md) pour la longueur et la distance.<br/>                                                                                                                         |
| [Text](text-control-attribute.md)                 |                                  | Affiche une légende dans le coin supérieur gauche du contrôle. Pour définir la police et le style de police d’une chaîne de texte, ajoutez le préfixe { \\ style} ou {&style} à la chaîne de caractères affichés. Où style est un identificateur figurant dans la colonne TextStyle de la [table TextStyle](textstyle-table.md). Si aucun de ces deux n’est présent, mais que la propriété [**DefaultUIFont**](defaultuifont.md) est définie comme un style de texte valide, cette police sera utilisée.<br/> |
| [Visible](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Contrôle masqué. Contrôle visible.<br/> Incluez ce bit dans le mot de bits de la colonne d’attributs dans la table de [contrôle](control-table.md) ou la [table BBControl](bbcontrol-table.md) pour rendre le contrôle visible ou masqué lors de sa création.<br/> Vous pouvez également masquer ou afficher un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>                                                                             |
| [Sunken](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Affiche le style visuel par défaut. Affiche le contrôle avec une apparence 3D enfoncée.<br/> Incluez ces bits dans le mot de bits dans la colonne attributs de la [table de contrôle](control-table.md).<br/>                                                                                                                                                                                                                                               |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | Le texte du contrôle est affiché dans l’ordre de lecture de gauche à droite. Le texte du contrôle est affiché dans l’ordre de lecture de droite à gauche.<br/>                                                                                                                                                                                                                                                                                                                |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | Le texte du contrôle est aligné à gauche. Le texte du contrôle est aligné à droite.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="remarks"></a>Remarques

Ce contrôle peut être créé à partir de la classe BUTTON à l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Il possède les styles de groupe de la zone de **\_ groupe** de la catégorie **BS \_**, **WS \_ Child** et WS.

Il y a toujours un intervalle entre le haut de la fenêtre du contrôle et le cadre visible, même en l’absence de légende.

 

 
