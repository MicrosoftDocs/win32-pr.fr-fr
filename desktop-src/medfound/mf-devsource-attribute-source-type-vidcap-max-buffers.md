---
description: Spécifie le nombre maximal de trames que la source de capture vidéo va mettre en mémoire tampon.
ms.assetid: af30606b-f1a0-4fbf-a831-05ed891f5d53
title: Attribut MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_MAX_BUFFERS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa927d28b49da0eb0a0be40c3137f1cd9acf79b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519344"
---
# <a name="mf_devsource_attribute_source_type_vidcap_max_buffers-attribute"></a>\_Attribut MF DEVSOURCE \_ type de \_ source \_ \_ VIDCAP \_ Max \_ buffers

Spécifie le nombre maximal de trames que la source de capture vidéo va mettre en mémoire tampon.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Par défaut, la source de capture vidéo met en mémoire tampon un maximum d’une image à la fois. Vous pouvez augmenter la limite de la mémoire tampon en définissant cet attribut.

La méthode correcte pour définir cet attribut dépend de la fonction utilisée pour créer la source du média :

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource): définissez l’attribut par le biais du paramètre *pAttributes* de la fonction.
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate): définissez l’attribut par le biais du paramètre *pAttributes* de la fonction.
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources): définissez l’attribut sur le pointeur [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retourné par la fonction. Définissez l’attribut avant d’appeler [**IMFActivate :: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).

L’attribut s’applique uniquement aux périphériques de capture vidéo.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture audio/vidéo](audio-video-capture.md)
</dt> <dt>

[Capturer les attributs de l’appareil](capture-device-attributes.md)
</dt> </dl>

 

 




