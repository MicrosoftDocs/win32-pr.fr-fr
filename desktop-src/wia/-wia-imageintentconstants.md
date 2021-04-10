---
description: Les constantes d’intention d’image spécifient le type de données que l’image doit représenter.
ms.assetid: 171228d9-a619-49aa-964e-f72a7f294a9d
title: Constantes d’intention d’image (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_INTENT_IMAGE_TYPE_COLOR
- WIA_INTENT_IMAGE_TYPE_GRAYSCALE
- WIA_INTENT_IMAGE_TYPE_TEXT
- WIA_INTENT_MINIMIZE_SIZE
- WIA_INTENT_MAXIMIZE_QUALITY
- WIA_INTENT_BEST_PREVIEW
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f35c1f7436c8cc5110215a6ccf0383960ec3fb87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951339"
---
# <a name="image-intent-constants"></a>Constantes d’intention d’image

Les constantes d’intention d’image spécifient le type de données que l’image doit représenter. La propriété de scanneur de l' [**\_ \_ \_ intention d’IPS d’WIA**](-wia-wiaitempropscanneritem.md) utilise ces indicateurs. Pour fournir une intention, associez un indicateur de type d’image prévu à un indicateur de taille/qualité prévu à l’aide de l’opérateur OR. \_L’intention WIA \_ None ne doit pas être combinée avec d’autres indicateurs. Notez qu’une image ne peut pas être à la fois des nuances de gris et des couleurs.

Les éléments suivants sont des constantes d’intention d’image valides :



| Indicateurs de type d’image prévu           | Description                                  |
|-------------------------------------|----------------------------------------------|
| \_intention WIA \_ aucune                   | Valeur par défaut. Ne pas définir de propriétés. |
| \_couleur du \_ type d’image d’intention WIA \_ \_     | Propriétés prédéfinies pour le contenu des couleurs.         |
| \_type d’image d’intention WIA nuances de \_ \_ \_ gris | Propriétés prédéfinies pour le contenu en nuances de gris.     |
| \_texte du \_ type d’image d’intention WIA \_ \_      | Propriétés prédéfinies pour le contenu de texte.          |
| \_masque de \_ type d’image d’intention WIA \_ \_      | Masque pour tous les indicateurs de type d’image.        |



 



| Indicateurs de qualité/taille d’image prévus | Description                                  |
|-----------------------------------|----------------------------------------------|
| \_ \_ taille limite de l’intention WIA \_       | Propriétés prédéfinies pour réduire la taille de l’image.    |
| optimiser la qualité de l' \_ intention WIA \_ \_    | Propriétés prédéfinies pour optimiser la qualité de l’image. |
| \_masque de \_ taille d’intention WIA \_           | Masque pour tous les indicateurs de taille/qualité.      |
| meilleure version préliminaire de l' \_ intention WIA \_ \_        | Spécifie la meilleure qualité d’aperçu.          |



 

La liste suivante affiche le nom de constante C/C++ suivi du nom correspondant entre parenthèses utilisé dans les scripts. Les noms de script proviennent du type énuméré WiaIntent. Notez que toutes les constantes ne sont pas disponibles par le biais d’un script.



| Constante/valeur                                                                                                                                                                                                                                                                         | Description                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------|
| <span id="WIA_INTENT_IMAGE_TYPE_COLOR"></span><span id="wia_intent_image_type_color"></span><dl> <dt>**WIA \_ TYPE d’image d’intention \_ \_ \_ couleur**</dt> <dt>0x00000001</dt> </dl>             | Propriétés prédéfinies pour le contenu des couleurs.<br/>         |
| <span id="WIA_INTENT_IMAGE_TYPE_GRAYSCALE"></span><span id="wia_intent_image_type_grayscale"></span><dl> <dt>**WIA \_ TYPE d’image d’intention \_ \_ nuances de \_ gris**</dt> <dt>0x00000002</dt> </dl> | Propriétés prédéfinies pour le contenu en nuances de gris.<br/>     |
| <span id="WIA_INTENT_IMAGE_TYPE_TEXT"></span><span id="wia_intent_image_type_text"></span><dl> <dt>**WIA \_ TYPE d’image d’intention \_ \_ \_ texte**</dt> <dt>0x00000004</dt> </dl>                | Propriétés prédéfinies pour le contenu de texte.<br/>          |
| <span id="WIA_INTENT_MINIMIZE_SIZE"></span><span id="wia_intent_minimize_size"></span><dl> <dt>**WIA \_ \_Limiter la \_ taille**</dt> des <dt>0x00010000</dt> </dl>                       | Propriétés prédéfinies pour réduire la taille de l’image.<br/>    |
| <span id="WIA_INTENT_MAXIMIZE_QUALITY"></span><span id="wia_intent_maximize_quality"></span><dl> <dt>**WIA \_ \_Optimiser la \_ qualité**</dt> <dt>0x00020000</dt> </dl>              | Propriétés prédéfinies pour optimiser la qualité de l’image.<br/> |
| <span id="WIA_INTENT_BEST_PREVIEW"></span><span id="wia_intent_best_preview"></span><dl> <dt>**WIA \_ INTENTION de la \_ meilleure version \_ préliminaire**</dt> <dt></dt> </dl>                          | Spécifie la meilleure qualité d’aperçu.<br/>          |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




