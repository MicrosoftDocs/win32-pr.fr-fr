---
description: Active le traitement vidéo avancé par le lecteur source, notamment la conversion de l’espace colorimétrique, le désentrelacement, le redimensionnement vidéo et la conversion de la fréquence d’images.
ms.assetid: 1055CD55-4B25-4EEC-AF1B-C84C52287F8F
title: Attribut MF_SOURCE_READER_ENABLE_ADVANCED_VIDEO_PROCESSING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6978239c5c1c466c78a310b38b5d10bd41f9e004
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525996"
---
# <a name="mf_source_reader_enable_advanced_video_processing-attribute"></a>\_Lecteur source MF-activer l’attribut de \_ \_ \_ \_ traitement vidéo avancé \_

Active le traitement vidéo avancé par le [lecteur source](source-reader.md), notamment la conversion de l’espace colorimétrique, le désentrelacement, le redimensionnement vidéo et la conversion de la fréquence d’images.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Si cet attribut a la **valeur true**, le lecteur source peut insérer un processeur vidéo dans le pipeline de traitement, ce qui permet les types de conversion de format suivants :

-   Conversion de l’espace colorimétrique (YUV en RVB-32)
-   Entrelac
-   Redimensionnement vidéo
-   Conversion de la fréquence des images

Si cet attribut a la **valeur true**, l’attribut de [ \_ \_ \_ convertisseurs de désactivation MF ReadWrite](mf-readwrite-disable-converters.md) doit avoir la **valeur false**.

Le lecteur source recherche les processeurs vidéo inscrits dans la catégorie **du \_ \_ \_ processeur vidéo de catégorie MFT** , y compris les MFTS enregistrés pour le processus local. (Pour plus d’informations sur l’inscription locale de MFTs, consultez [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) .) Le lecteur source utilise le processeur vidéo de transcodage (XVP) si aucun autre processeur vidéo approprié n’est trouvé.

L’application spécifie le type de sortie souhaité en appelant [**IMFSourceReader :: SetCurrentMediaType**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-setcurrentmediatype). Lorsque le lecteur source configure le processeur vidéo, il tente de faire correspondre les attributs suivants du type de sortie :

-   Fréquence d’images[( \_ \_ \_ fréquence d’images MF MT](mf-mt-frame-rate-attribute.md))
-   Taille de trame ([ \_ \_ \_ taille de trame MF MT](mf-mt-frame-size-attribute.md))
-   Mode entrelacé ([ \_ \_ \_ mode entrelacé MF MT](mf-mt-interlace-mode-attribute.md))
-   Proportions en pixels (proportions de[ \_ pixels MF MT \_ \_ \_ ](mf-mt-pixel-aspect-ratio-attribute.md))
-   SubType (sous-type[MF \_ MT \_ ](mf-mt-subtype-attribute.md))

Cet attribut est similaire à l' [attribut \_ lecteur source MF activer l’attribut de \_ \_ \_ \_ traitement vidéo](mf-source-reader-enable-video-processing.md) , mais offre les avantages suivants :

-   Une plus grande plage de conversions de format est prise en charge.
-   Les applications peuvent inscrire leurs propres convertisseurs.
-   Certaines conversions peuvent être effectuées dans le matériel à l’aide du GPU.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                              |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lecteur source](source-reader.md)
</dt> <dt>

[Attributs du lecteur source](source-reader-attributes.md)
</dt> </dl>

 

 




