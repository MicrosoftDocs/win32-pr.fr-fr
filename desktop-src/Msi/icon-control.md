---
description: Le contrôle Icon affiche une image statique d’une icône. L’arrière-plan de l’image est transparent.
ms.assetid: a2d19093-73d0-4e1f-bf82-21e7334a3f34
title: contrôle Icon (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce6d1dca9e6664018a0c7a36c9b44f3b5a0b6310bc8c6d18309b73649fa9240
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996709"
---
# <a name="icon-control"></a>Contrôle Icon

Le contrôle Icon affiche une image statique d’une icône. L’arrière-plan de l’image est transparent.

## <a name="control-attributes"></a>Attributs du contrôle

Vous pouvez utiliser les attributs suivants avec ce contrôle. Pour modifier la valeur d’un attribut à l’aide d’un événement, abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md) et répertoriez l’identificateur de l’attribut dans la colonne d’attribut. Entrez l’identificateur du ControlEvent, dans la colonne d’événement.



| Identificateur d’attribut                         | Bit hexadécimal                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)   |                                                                              | Position du contrôle dans la boîte de dialogue. Entrez la largeur, la hauteur et les coordonnées du contrôle dans la largeur, la hauteur, le X et les colonnes Y de la [table de contrôle](control-table.md). Utilisez les [unités d’installation](installer-units.md) pour la longueur et la distance.<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| [Text](text-control-attribute.md)           |                                                                              | Contient le nom d’une icône stockée dans la [table binaire](binary-table.md). Pour afficher une icône qui est stockée dans la table binaire, entrez le nom de l’enregistrement de l’image qui apparaît dans la table binaire dans la colonne de texte de l’enregistrement de la [table de contrôle](control-table.md) pour ce contrôle.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| [Visible](visible-control-attribute.md)     | 0x00000000 0x00000001<br/>                                             | Contrôle masqué. Contrôle visible.<br/> Incluez ce bit dans le mot de bits de la colonne d’attributs dans la [table de contrôle](control-table.md) pour rendre le contrôle visible ou masqué lors de sa création.<br/> Vous pouvez également masquer ou afficher un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/>                                                                                                                                                                                                                                                                                                                         |
| [Sunken](sunken-control-attribute.md)       | 0x00000000 0x00000004<br/>                                             | Affiche le style visuel par défaut. Affiche le contrôle avec une apparence 3D enfoncée.<br/> Incluez ces bits dans le mot de bits dans la colonne attributs de la [table de contrôle](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [FixedSize](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/>                                             | Étire l’image d’icône pour l’ajuster au contrôle. Rogne ou centre l’image d’icône dans le contrôle.<br/> Incluez ce bit dans le mot de bits de la colonne d’attributs de la [table de contrôle](control-table.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [Icône de](iconsize-control-attribute.md)   | 0x00000000 0x00200000<br/> 0x00400000<br/> 0x00600000<br/> | Charge la première image. Charge la première image de 16x16.<br/> Charge la première image 32 x 32.<br/> Charge la première image 48.<br/> Un fichier icône peut contenir différentes images de taille de la même icône. Incluez la valeur du mot de bits approprié dans la colonne attributs de la [table de contrôle](control-table.md) .<br/> Si ces bits ne sont pas définis, le programme d’installation ignore l’attribut FixedSize et l’image est étirée pour s’ajuster au rectangle de contrôle. Si les bits d’icône et les bits FixedSize sont tous les deux définis, une image plus petite que le contrôle est centrée et une image est plus grande que le contrôle qu’elle doit ajuster.<br/> |



 

## <a name="remarks"></a>Remarques

Ce contrôle peut être créé à partir de la classe statique à l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Il possède les styles d' **\_ icône SS**, **SS \_ CENTERIMAGE**, **WS \_ Child** et **WS \_ Group** .

 

 
