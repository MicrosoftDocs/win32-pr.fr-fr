---
description: Windows Les périphériques matériels d’acquisition d’images (WIA) sont représentés sous forme d’arborescences hiérarchiques d’objets Item. L’élément racine de cette arborescence représente le périphérique lui-même, tandis que les éléments enfants représentent des images, des dossiers ou des lits d’analyse.
ms.assetid: 240557d6-665e-4879-8c6e-f564ca61e031
title: Item (objet)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 6af0642a47db9d3a7a1c30aea76be22ea5ce1d07
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219961"
---
# <a name="item-object"></a>Item (objet)

Windows Les périphériques matériels d’acquisition d’images (WIA) sont représentés sous forme d’arborescences hiérarchiques d’objets **Item** . L’élément racine de cette arborescence représente le périphérique lui-même, tandis que les éléments enfants représentent des images, des dossiers ou des lits d’analyse.

Utilisez l’objet **Item** pour transférer des données vers un fichier, pour naviguer dans l’arborescence d’éléments pour un périphérique particulier ou pour récupérer des informations sur une image ou un appareil.

## <a name="members"></a>Membres

L’objet **Item** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **Item** possède ces méthodes.



| Méthode                                                         | Description                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) | La méthode [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) de l’objet **Item** affiche une boîte de dialogue qui permet à un utilisateur de sélectionner des images et de l’audio à transférer à partir d’un appareil.<br/>                                                                     |
| [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md)       | La méthode [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md) de l’objet **Item** utilise l’ID d’une propriété Item pour retourner sa valeur.<br/>                                                                                                                     |
| [**TakePicture**](-wia-iwiadispatchitem-takepicture.md)       | La méthode [**TakePicture**](-wia-iwiadispatchitem-takepicture.md) de l’objet **Item** fait qu’un appareil photo numérique prend une image et retourne un objet **Item** qui représente l’image résultante. Cette méthode s’applique uniquement aux appareils photo numériques.<br/> |
| [**Transférer**](-wia-iwiadispatchitem-transfer.md)             | La méthode de [**transfert**](-wia-iwiadispatchitem-transfer.md) de l’objet **Item** transfère les données d’un appareil vers un fichier. Cette méthode s’applique uniquement aux éléments de type périphérique.<br/>                                                                                         |



 

### <a name="properties"></a>Propriétés

L’objet **Item** possède ces propriétés.



| Propriété                                                                    | Type d’accès          | Description                                                                                                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Children**](-wia-iwiadispatchitem-children.md)<br/>               | Lecture seule<br/> | La propriété [**Children**](-wia-iwiadispatchitem-children.md) de l’objet **Item** récupère une collection d’objets **Item** . Les éléments de cette collection représentent des éléments qui sont des enfants directs de cet élément dans l’arborescence hiérarchique. <br/> |
| [**ConnectStatus**](-wia-iwiadispatchitem-connectstatus.md)<br/>     | Lecture seule<br/> | Récupère l’état de la connexion de l’appareil. Cette propriété s’applique uniquement aux éléments de type périphérique (éléments racines). Les valeurs possibles sont « connected », « Disconnected » ou **null** (si cette propriété ne s’applique pas à l’élément). <br/>                     |
| [**FirmwareVersion**](-wia-iwiadispatchitem-firmwareversion.md)<br/> | Lecture seule<br/> | Récupère la version du microprogramme de l’appareil. Cette propriété s’applique uniquement aux éléments de type périphérique (éléments racines). <br/>                                                                                                                                  |
| [**FullName**](-wia-iwiadispatchitem-fullname.md)<br/>               | Lecture seule<br/> | Récupère le nom complet de l’élément tel qu’il apparaît dans l’interface utilisateur. <br/>                                                                                                                                                                                    |
| [**Hauteur**](-wia-iwiadispatchitem-height.md)<br/>                   | Lecture seule<br/> | Hauteur, en pixels, de l’élément. <br/>                                                                                                                                                                                                             |
| [**ItemType**](-wia-iwiadispatchitem-itemtype.md)<br/>               | Lecture seule<br/> | Type de cet élément. <br/>                                                                                                                                                                                                                          |
| [**Nom**](-wia-iwiadispatchitem-name.md)<br/>                       | Lecture seule<br/> | Nom de l’élément tel qu’il apparaît dans l’interface utilisateur. <br/>                                                                                                                                                                                                   |
| [**PictureHeight**](-wia-iwiadispatchitem-pictureheight.md)<br/>     | Lecture seule<br/> | Hauteur, en pixels, des images produites par cet appareil photo numérique. S’applique uniquement aux appareils photo numériques. <br/>                                                                                                                                              |
| [**PictureWidth**](-wia-iwiadispatchitem-picturewidth.md)<br/>       | Lecture seule<br/> | Largeur, en pixels, des images produites par cet appareil photo numérique. S’applique uniquement aux appareils photo numériques. <br/>                                                                                                                                               |
| [**ThumbHeight**](-wia-iwiadispatchitem-thumbheight.md)<br/>         | Lecture seule<br/> | Hauteur, en pixels, de l’image miniature. Cette propriété retourne-1 si cet élément ne prend pas en charge les miniatures. <br/>                                                                                                                               |
| [**Fer**](-wia-iwiadispatchitem-thumbnail.md)<br/>             | Lecture seule<br/> | Chemin d’accès et nom de fichier de l’image miniature. Cette propriété a la **valeur null** si l’élément ne prend pas en charge les miniatures, ou si un chemin d’accès ne peut pas être généré. <br/>                                                                                                  |
| [**ThumbWidth**](-wia-iwiadispatchitem-thumbwidth.md)<br/>           | Lecture seule<br/> | Largeur, en pixels, de l’image miniature. Cette propriété retourne-1 si cet élément ne prend pas en charge les miniatures. <br/>                                                                                                                                |
| [**Simultanément**](-wia-iwiadispatchitem-time.md)<br/>                       | Lecture seule<br/> | L’heure actuelle. S’applique uniquement aux appareils. <br/>                                                                                                                                                                                                      |
| [**Largeur**](-wia-iwiadispatchitem-width.md)<br/>                     | Lecture seule<br/> | Largeur, en pixels, de l’élément. <br/>                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Notes

### <a name="creationaccess-functions"></a>Fonctions d’accès de création \\

Utilisez l’une des méthodes suivantes pour récupérer une référence à l’objet :



[**TakePicture**](-wia-iwiadispatchitem-takepicture.md)

[**Créer**](-wia-iwiadeviceinfo-create.md)

[**Créer**](-wia-iwia-create.md)



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |



 

 




