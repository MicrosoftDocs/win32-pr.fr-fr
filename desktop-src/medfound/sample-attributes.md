---
description: Exemples d’attributs
ms.assetid: 64aead5a-61c4-4e83-a556-af33e0aa82be
title: Exemples d’attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1329946c36b1b7454deb76a25247985d9dcfdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527843"
---
# <a name="sample-attributes"></a>Exemples d’attributs

Les attributs suivants s’appliquent aux [exemples de supports](media-samples.md). Pour obtenir les attributs d’un exemple de média, utilisez l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .



| Attribut                                                                                                      | Description                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MFSampleExtension \_ 3DVideo](mfsampleextension-3dvideo.md)                                                    | Spécifie si un exemple de média contient une image vidéo 3D.                                                                                                                                                                                        |
| [MFSampleExtension \_ 3DVideo \_ SampleFormat](mfsampleextension-3dvideo-sampleformat.md)                         | Spécifie la manière dont une image vidéo 3D est stockée dans un échantillon de média.                                                                                                                                                                                        |
| [**MFSampleExtension \_ BottomFieldFirst**](mfsampleextension-bottomfieldfirst-attribute.md)                    | Spécifie la dominante de champ pour une image vidéo entrelacée.                                                                                                                                                                                       |
| [MFSampleExtension \_ CameraExtrinsics](mfsampleextension-cameraextrinsics.md)                                  | Extrinsics de l’appareil photo pour l’exemple.                                                                                                                                                                                                              |
| [MFSampleExtension \_ CaptureMetadata](mfsampleextension-capturemetadata.md)                                    | Magasin [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pour toutes les métadonnées associées au pipeline de capture.                                                                                                                                             |
| [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md)                                | Indique si un exemple de vidéo est une image clé.                                                                                                                                                                                                   |
| [MFSampleExtension de \_ contenu \_ KeyId](mfsampleextension-content-keyid.md)                                       | Définit l’ID de clé de l’exemple.                                                                                                                                                                                                                    |
| [**MFSampleExtension \_ DerivedFromTopField**](mfsampleextension-derivedfromtopfield-attribute.md)              | Spécifie si une image vidéo désentrelacée a été dérivée du champ supérieur ou du champ inférieur.                                                                                                                                                  |
| [MFSampleExtension \_ DeviceTimestamp](mfsampleextension-devicetimestamp.md)                                    | Horodatage du pilote de périphérique.                                                                                                                                                                                                             |
| [**MFSampleExtension \_ discontinuité**](mfsampleextension-discontinuity-attribute.md)                          | Spécifie si un échantillon de média est le premier échantillon après un intervalle dans le flux.                                                                                                                                                                    |
| [MFSampleExtension de \_ chiffrement \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md)               | Spécifie la taille de bloc d’octets chiffrés pour le chiffrement de modèle basé sur l’exemple.                                                                                                                                                                       |
| [MFSampleExtension de \_ chiffrement \_ ProtectionScheme](mfsampleextension-encryption-protectionscheme.md)           | Spécifie le schéma de protection pour les exemples chiffrés.                                                                                                                                                                                             |
| [MFSampleExtension de \_ chiffrement \_ SampleID](mfsampleextension-encryption-sampleid.md)                           | Spécifie l’ID d’un échantillon chiffré.                                                                                                                                                                                                           |
| [MFSampleExtension de \_ chiffrement \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md)                 | Spécifie la taille de bloc d’octets Clear (non chiffrée) pour le chiffrement de modèle basé sur un échantillon.                                                                                                                                                           |
| [MFSampleExtension de \_ chiffrement \_ SubSampleMappingSplit](mfsampleextension-encryption-subsamplemappingsplit.md) | Définit le mappage de sous-échantillon pour l’exemple indiquant les octets clairs et chiffrés dans les exemples de données.                                                                                                                                            |
| [MFSampleExtension \_ FrameCorruption](mfsampleextension-framecorruption.md)                                    | Spécifie si une image vidéo est endommagée.                                                                                                                                                                                                      |
| [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md)                          | Obtient un objet de type [**IMFCollection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) contenant des objets [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) qui contiennent des unités de couche d’abstraction de réseau (NALUs) et des unités SEI (Supplémental addition information) transmises par un décodeur. |
| [MFSampleExtension \_ ForwardedDecodeUnitType](mfsampleextension-forwardeddecodeunittype.md)                    | Spécifie le type, NALU ou SEI, d’une unité attachée à un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) dans une collection [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) .                                                    |
| [**MFSampleExtension \_ entrelacé**](mfsampleextension-interlaced-attribute.md)                                | Indique si une image vidéo est entrelacée ou progressive.                                                                                                                                                                                      |
| [MFSampleExtension \_ LongTermReferenceFrameInfo](mfsampleextension-longtermreferenceframeinfo.md)              | Spécifie les informations de trame de référence à long terme et est retourné sur l’exemple de sortie.                                                                                                                                                               |
| [MFSampleExtension \_ MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md)                      | Cet attribut retourne la différence absolue moyenne (MAD) sur tous les blocs de macro dans le plan Y.                                                                                                                                                  |
| [**MFSampleExtension \_ PacketCrossOffsets**](mfsampleextension-packetcrossoffsets-attribute.md)                | Spécifie les limites de charge utile pour un frame. Cela s’applique aux exemples chiffrés.                                                                                                                                                                   |
| [Miniature de MFSampleExtension \_](mfsampleextension-photothumbnail.md)                                      | Contient la miniature de photo d’un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample).                                                                                                                                                                                  |
| [MFSampleExtension \_ PhotoThumbnailMediaType](mfsampleextension-photothumbnailmediatype.md)                    | Contient le [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) qui décrit le type de format d’image contenu dans l’attribut de [ \_ photominiature MFSampleExtension](mfsampleextension-photothumbnail.md) .                                                      |
| [MFSampleExtension \_ PinholeCameraIntrinsics](mfsampleextension-pinholecameraintrinsics.md)                    | L’appareil photo Pinhole est intrinsèque pour l’exemple.                                                                                                                                                                                                      |
| [**MFSampleExtension \_ RepeatFirstField**](mfsampleextension-repeatfirstfield-attribute.md)                    | Spécifie s’il faut répéter le premier champ dans un frame entrelacé.                                                                                                                                                                                |
| [MFSampleExtension \_ ROIRectangle](mfsampleextension-roirectangle.md)                                          | Spécifie les limites de la zone d’intérêt qui indique la région du cadre qui requiert une qualité différente.                                                                                                                            |
| [**MFSampleExtension \_ SingleField**](mfsampleextension-singlefield-attribute.md)                              | Spécifie si un exemple de vidéo contient un champ unique ou deux champs entrelacés                                                                                                                                                                 |
| [MFSampleExtension \_ TargetGlobalLuminance](mfsampleextension-targetgloballuminance.md)                        | Valeur de nits qui spécifie la luminance de rétroéclairage globale ciblée pour l’image vidéo associée.                                                                                                                                           |
| [**\_Jeton MFSampleExtension**](mfsampleextension-token-attribute.md)                                          | Contient un pointeur vers le jeton qui a été fourni à la méthode [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .                                                                                                             |
| [MFSampleExtension \_ VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)                      | Spécifie les limites de la zone d’intérêt qui indique la région du cadre qui requiert une qualité différente.                                                                                                                            |
| [MFSampleExtension \_ VideoEncodeQP](mfsampleextension-videoencodeqp.md)                                        | Spécifie le paramètre de quantification (QP) utilisé pour encoder un échantillon vidéo.                                                                                                                                                                  |



 

Chaque échantillon de média ne contient pas tous les attributs répertoriés ici. Dans certains cas, un attribut s’applique uniquement à certains genres de données. Par exemple, certains attributs s’appliquent uniquement aux exemples de vidéos et ne doivent pas apparaître sur les échantillons audio. Dans d’autres cas, l’attribut a une valeur par défaut qui s’applique si l’attribut n’est pas défini.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Exemples de supports](media-samples.md)
</dt> </dl>

 

 



