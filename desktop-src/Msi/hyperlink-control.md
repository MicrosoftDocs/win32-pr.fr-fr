---
description: Le contrôle de lien hypertexte affiche un lien HTML vers une adresse, qui s’ouvre dans le navigateur par défaut de l’ordinateur.
ms.assetid: 06678b10-0915-4649-b917-ec90c40d5160
title: Contrôle HyperLink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d074efa00fcf51fec979d9df07f1854631279d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021657"
---
# <a name="hyperlink-control"></a>Contrôle HyperLink

Le contrôle de lien hypertexte affiche un lien HTML vers une adresse, qui s’ouvre dans le navigateur par défaut de l’ordinateur. Les liens ne sont pas pris en charge pour les protocoles autres que HTML.

**[Windows Installer 4,5 ou version antérieure](not-supported-in-windows-installer-4-5.md):** Non pris en charge. ce contrôle est disponible à partir de Windows Installer 5,0.

La valeur texte du contrôle HyperLink utilise la <a> balise d’ancrage et la valeur de l’attribut href pour spécifier l’URL et le texte affiché du lien.

``` syntax
[Blue Yonder Airlines](https://www.blueyonderairlines.com)
```

## <a name="control-attributes"></a>Attributs du contrôle

Vous pouvez utiliser les attributs suivants avec le contrôle HyperLink. Pour modifier la valeur d’un attribut à l’aide d’un événement, abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md) et répertoriez l’identificateur de l’attribut dans la colonne d’attribut. Entrez l’identificateur du ControlEvent, dans la colonne d’événement.



| Identificateur d’attribut                             | Bit hexadécimal                  | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)       |                                  | Position du contrôle dans la boîte de dialogue. Entrez la largeur, la hauteur et les coordonnées du contrôle dans la largeur, la hauteur, le X et les colonnes Y de la table de [contrôle](control-table.md) ou de la [table BBControl](bbcontrol-table.md). Utilisez les [unités d’installation](installer-units.md) pour la longueur et la distance.<br/>                                                                                                                                                                       |
| [Text](text-control-attribute.md)               |                                  | Texte affiché par le contrôle. Pour définir la police et le style de police d’une chaîne de texte, ajoutez le préfixe { \\ style} ou {&style} à la chaîne de caractères affichés. Où style est un identificateur figurant dans la colonne TextStyle de la [table TextStyle](textstyle-table.md). Si aucun de ces deux n’est présent, mais que la propriété [**DefaultUIFont**](defaultuifont.md) est définie comme un style de texte valide, cette police sera utilisée. La valeur Text résout également \[ \] la propriété en la propriété référencée. <br/> |
| [Visible](visible-control-attribute.md)         | 0x00000000 0x00000001<br/> | Contrôle masqué. Contrôle visible.<br/> Incluez ce bit dans le mot de bits de la colonne d’attributs dans la table de [contrôle](control-table.md) ou la [table BBControl](bbcontrol-table.md). pour rendre le contrôle visible ou masqué lors de sa création.<br/> Vous pouvez également masquer ou afficher un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>                                                                                                                           |
| [Activé](enabled-control-attribute.md)         | 0x00000000 0x00000002<br/> | Contrôle dans un état désactivé. Contrôle dans un état activé.<br/> Incluez ce bit dans le mot de bits de la colonne attributs des tables [Control](control-table.md) ou [BBControl](bbcontrol-table.md) pour activer le contrôle lors de la création.<br/> Vous pouvez également activer ou désactiver un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>                                                                                                                        |
| [Sunken](sunken-control-attribute.md)           | 0x00000000 0x00000004<br/> | Affiche le style visuel par défaut. Affiche le contrôle avec une apparence enfoncée, 3D et un look.<br/> Incluez ces bits dans le mot de bits dans la colonne attributs de la [table de contrôle](control-table.md).<br/>                                                                                                                                                                                                                                                                                            |
| [Transparente](transparent-control-attribute.md) | 0x00000000 0x00010000<br/> | Contrôle opaque. Arrière-plan montre le contrôle. Le contrôle a le \_ \_ style transparent WS.<br/> Incluez ce bit dans la colonne attributs des tables [Control](control-table.md) ou [BBControl](bbcontrol-table.md).<br/>                                                                                                                                                                                                                                                          |



 

## <a name="remarks"></a>Notes

Ce contrôle peut être créé à partir de la classe de lien WC à \_ l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Il possède les \_ styles WS Child, WS \_ TABSTOP et WS \_ Group.

Ne placez pas de [contrôles de texte](text-control.md) transparent par-dessus les bitmaps de couleur. Le texte peut ne pas être visible si l’utilisateur modifie le modèle de couleurs d’affichage. Par exemple, le texte peut devenir invisible si l’utilisateur définit le paramètre de contraste élevé pour des raisons d’accessibilité.

Si le texte du contrôle est plus long que la largeur du contrôle, le texte est renvoyé à la ligne ou tronqué, selon que la hauteur est suffisante pour s’ajuster au texte renvoyé à la ligne.

 

 
