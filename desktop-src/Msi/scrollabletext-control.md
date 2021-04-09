---
description: Ce contrôle affiche une longue chaîne de texte qui ne peut pas s’ajuster entièrement sur la page. Ce contrôle est couramment utilisé pour afficher le contrat de licence.
ms.assetid: a49209f3-043c-4360-b1e3-9fa9538c2c9b
title: Contrôle ScrollableText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ff807f2b0175eb411b3c45eb9d1e3b5eeaea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865193"
---
# <a name="scrollabletext-control"></a>Contrôle ScrollableText

Ce contrôle affiche une longue chaîne de texte qui ne peut pas s’ajuster entièrement sur la page. Ce contrôle est couramment utilisé pour afficher le contrat de licence.

Notez que la chaîne de texte utilisée avec ce contrôle ne peut pas contenir une propriété incorporée. Pour afficher du texte avec des propriétés incorporées, utilisez à la place le [contrôle de texte](text-control.md).

## <a name="control-attributes"></a>Attributs du contrôle

Vous pouvez utiliser les attributs suivants avec ce contrôle. Pour modifier la valeur d’un attribut à l’aide d’un événement, abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md) et répertoriez l’identificateur de l’attribut dans la colonne d’attribut. Entrez l’identificateur du ControlEvent, dans la colonne d’événement.



| Identificateur d’attribut                               | Bit hexadécimal                  | Description                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)         |                                  | Position du contrôle dans la boîte de dialogue. Entrez la largeur, la hauteur et les coordonnées du contrôle dans la largeur, la hauteur, le X et les colonnes Y de la table de [contrôle](control-table.md) ou de la [table BBControl](bbcontrol-table.md). Utilisez les [unités d’installation](installer-units.md) pour la longueur et la distance.<br/>                                            |
| [Text](text-control-attribute.md)                 |                                  | Texte affiché par le contrôle. Entrez la chaîne de texte RTF dans la colonne de texte de la [table de contrôle](control-table.md).                                                                                                                                                                                                                                                       |
| [Visible](visible-control-attribute.md)           | 0x00000000 0x00000001<br/> | Contrôle masqué. Contrôle visible.<br/> Pour rendre le contrôle visible ou masqué lors de sa création, incluez ce bit dans le mot de bits de la colonne attributs dans la table de [contrôle](control-table.md) ou la [table BBControl](bbcontrol-table.md).<br/> Vous pouvez également masquer ou afficher un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/> |
| [Enabled](enabled-control-attribute.md)           | 0x00000000 0x00000002<br/> | Contrôle dans un état désactivé. Contrôle dans un état activé.<br/> Incluez ce bit dans la colonne attributs des tables de [contrôle](control-table.md) ou de [BBControl](bbcontrol-table.md) pour activer le contrôle lors de la création.<br/> Vous pouvez également activer ou désactiver un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>             |
| [Sunken](sunken-control-attribute.md)             | 0x00000000 0x00000004<br/> | Affichez le style visuel par défaut. Affichez le contrôle avec des enfoncés, des 3D et un look.<br/> Incluez ces bits dans le mot de bits dans la colonne attributs de la [table de contrôle](control-table.md).<br/>                                                                                                                                                                    |
| [RTLRO](rtlro-control-attribute.md)               | 0x00000000 0x00000020<br/> | Le texte du contrôle est affiché dans un ordre de lecture de gauche à droite. Le texte du contrôle est affiché dans un ordre de lecture de droite à gauche.<br/>                                                                                                                                                                                                                               |
| [RightAligned](rightaligned-control-attribute.md) | 0x00000000 0x00000040<br/> | Le texte du contrôle est aligné sur la gauche. Le texte du contrôle est aligné à droite.<br/>                                                                                                                                                                                                                                                                            |
| [LeftScroll](leftscroll-control-attribute.md)     | 0x00000000 0x00000080<br/> | La barre de défilement se trouve sur le côté droit du contrôle. La barre de défilement se trouve sur le côté gauche du contrôle.<br/>                                                                                                                                                                                                                                              |
| [BiDi](bidi-control-attribute.md)                 | 0x000000E0                       | Définissez cette valeur pour une combinaison des attributs [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md)et [LeftScroll](leftscroll-control-attribute.md) .                                                                                                                                                                               |



 

## <a name="remarks"></a>Notes

Ce contrôle peut être créé à partir de la classe RICHEDIT à l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Il possède les **styles \_ Multiline**, **WS \_ VSCROLL**, **es \_ ReadOnly**, **WS \_ TABSTOP**, **es \_ AUTOVSCROLL**, **WS \_ Child**, **WS \_ Group** et **es \_ NOOLEDRAGDROP** .

 

 
