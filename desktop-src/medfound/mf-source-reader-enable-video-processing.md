---
description: Active le traitement vidéo par le lecteur source.
ms.assetid: b1ec1c0e-8042-4486-822f-eb106577c0b1
title: Attribut MF_SOURCE_READER_ENABLE_VIDEO_PROCESSING (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfcbb076d5f42e784277dbd78101b473ec33905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484808"
---
# <a name="mf_source_reader_enable_video_processing-attribute"></a>\_Lecteur source MF-activer l’attribut de \_ \_ \_ \_ traitement vidéo

Active le traitement vidéo par le [lecteur source](source-reader.md).

## <a name="data-type"></a>Type de données

**UINT32**



| Valeur                                                                                                                                                                | Signification                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="Nonzero"></span><span id="nonzero"></span><span id="NONZERO"></span><dl> <dt>**Différente**</dt> </dl> | Activez le traitement vidéo.<br/>            |
| <span id="Zero"></span><span id="zero"></span><span id="ZERO"></span><dl> <dt>**Nuls**</dt> </dl>             | Désactivez le traitement vidéo. (Par défaut)<br/> |



 

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Notes

Si cet attribut a la **valeur true** (différent de zéro), le lecteur source peut effectuer le traitement vidéo limité suivant sur des images vidéo non compressées :

-   Conversion de YUV en RGB-32.
-   Entrelac.

Ces opérations sont effectuées dans le logiciel et ne sont pas optimisées pour la lecture. Cette fonctionnalité est destinée aux applications qui traitent un petit nombre de frames, par exemple pour créer une miniature de vidéo, ou des applications qui ne décodent pas les trames en temps réel. L’opération de désentrelacement interpole les données d’un champ unique, de sorte qu’elles sont perdues.

Évitez ce paramètre si vous utilisez Direct3D pour afficher les images vidéo, car le GPU offre généralement de meilleures capacités de traitement vidéo.

Si cet attribut a la **valeur true**, les attributs suivants doivent avoir la **valeur false**:

-   [\_ \_ Gestionnaire D3D du lecteur source \_ MF \_](mf-source-reader-d3d-manager.md)
-   [\_ \_ convertisseurs de désactivation MF ReadWrite \_](mf-readwrite-disable-converters.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lecteur source](source-reader.md)
</dt> <dt>

[Attributs du lecteur source](source-reader-attributes.md)
</dt> </dl>

 

 




