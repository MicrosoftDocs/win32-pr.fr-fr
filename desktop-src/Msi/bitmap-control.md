---
description: Le contrôle bitmap affiche un fichier image statique JPEG ou bitmap. Le Windows Installer détermine automatiquement le format des données binaires et affiche l’image. Le contrôle ne prend pas en charge l’animation.
ms.assetid: 4b511d8a-1819-4a9b-a942-dc32fade75c6
title: Contrôle bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058b67d52266906735719976bf7311b4f562b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518207"
---
# <a name="bitmap-control"></a>Contrôle bitmap

Le contrôle bitmap affiche un fichier image statique JPEG ou bitmap. Le Windows Installer détermine automatiquement le format des données binaires et affiche l’image. Le contrôle ne prend pas en charge l’animation.

**Windows 8 et Windows Server 2012 :** Le fichier image peut être dans n’importe quel format standard pris en charge par le composant WIC (Windows Imaging Component), notamment TIFF, JPEG, PNG, GIF, BMP et HDPhoto. Le contrôle ne prend pas en charge l’animation.

## <a name="control-attributes"></a>Attributs du contrôle

Vous pouvez utiliser les attributs suivants avec ce contrôle. Pour modifier la valeur d’un attribut à l’aide d’un événement, abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md) et répertoriez l’identificateur de l’attribut dans la colonne d’attribut. Entrez l’identificateur du ControlEvent, dans la colonne d’événement.



| Identificateur d’attribut                                 | Bit hexadécimal                  | Description                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Position](position-control-attribute.md)           |                                  | Position du contrôle dans la boîte de dialogue. Entrez la largeur, la hauteur et les coordonnées du contrôle dans la largeur, la hauteur, le X et les colonnes Y de la table de [contrôle](control-table.md) ou de la [table BBControl](bbcontrol-table.md). Utilisez les [unités d’installation](installer-units.md) pour la longueur et la distance.<br/>                                         |
| [Text](text-control-attribute.md)                   |                                  | Contient le nom d’une image bitmap stockée dans la [table binaire](binary-table.md). Pour afficher un fichier bitmap stocké dans la table binaire, procédez comme suit. Entrez le nom de l’image bitmap qui apparaît dans la colonne nom de la table binaire dans la colonne de texte de l’enregistrement de la [table de contrôle](control-table.md) pour ce contrôle. <br/>                                         |
| [Visible](visible-control-attribute.md)             | 0x00000000 0x00000001<br/> | Contrôle masqué. Contrôle visible.<br/> Incluez ce bit dans le mot de bits de la colonne d’attributs dans la table de [contrôle](control-table.md) ou la [table BBControl](bbcontrol-table.md). pour rendre le contrôle visible ou masqué lors de sa création.<br/> Vous pouvez également masquer ou afficher un contrôle à l’aide de la [table ControlCondition](controlcondition-table.md).<br/> |
| [Sunken](sunken-control-attribute.md)               | 0x00000000 0x00000004<br/> | Affiche le style visuel par défaut. Affiche le contrôle avec une apparence 3D enfoncée.<br/> Incluez ces bits dans le mot de bits dans la colonne attributs de la [table de contrôle](control-table.md).<br/>                                                                                                                                                                   |
| [Contrôle FixedSize](fixedsize-control-attribute.md) | 0x00000000 0x00100000<br/> | Étire l’image bitmap en fonction du contrôle. Rogne ou centre l’image bitmap dans le contrôle.<br/> Incluez ce bit dans le mot de bits de la colonne Attributes de la [table BBControl](bbcontrol-table.md) ou de la [table de contrôle](control-table.md).<br/>                                                                                                       |



 

## <a name="remarks"></a>Notes

Ce contrôle peut être créé à partir de la classe statique à l’aide de la fonction [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . Il possède les **styles \_ SS bitmap**, **SS \_ CENTERIMAGE**, **WS \_ Child** et **WS \_ Group** .

 

