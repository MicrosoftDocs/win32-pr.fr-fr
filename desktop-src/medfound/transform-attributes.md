---
description: Attributs de transformation
ms.assetid: 9beb1306-1378-499c-b9e1-c768a7b4c8bc
title: Attributs de transformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e68240f5341319db2b06ad6160cf8153f107eca9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235835"
---
# <a name="transform-attributes"></a>Attributs de transformation

Les attributs suivants s’appliquent à [Media Foundation transformations](media-foundation-transforms.md) (MFTS) ou aux [objets d’activation](activation-objects.md) pour MFTS, ou les deux.



| Attribut                                                                                                     | Description                                                                                                                                                                                   | S'applique à                  |
|---------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| [**MF \_ activer \_ MFT \_ verrouillé**](mf-activate-mft-locked-attribute.md)                                         | Spécifie si le chargeur de topologie doit modifier les types de média sur une table MFT.                                                                                                                  | MFTs                        |
| [**Compatible avec la prise en \_ \_ charge Direct3D MF \_**](mf-sa-d3d-aware-attribute.md)                                                       | Spécifie si une Media Foundation transformation (MFT) prend en charge l’accélération vidéo DirectX.                                                                                                     | MFTs                        |
| [\_transformation MF \_ asynchrone](mf-transform-async.md)                                                                | Spécifie si une table MFT effectue un traitement asynchrone.                                                                                                                                    | MFTs                        |
| [mode \_ de \_ déverrouillage asynchrone de la transformation MF \_](mf-transform-async-unlock.md)                                                 | Active l’utilisation d’une table MFT asynchrone.                                                                                                                                                       | MFTs                        |
| [\_Attribut de \_ catégorie de transformation MF \_](mf-transform-category-attribute.md)                                     | Spécifie la catégorie pour une table MFT.                                                                                                                                                            | Objets d’activation MFT      |
| [\_Attribut des \_ indicateurs de transformation MF \_](mf-transform-flags-attribute.md)                                           | Contient des indicateurs pour un objet d’activation MFT.                                                                                                                                                  | Objets d’activation MFT      |
| [\_Attribut de \_ mérite du codec MFT \_](mft-codec-merit-attribute.md)                                                 | Contient la valeur mérite d’un codec matériel.                                                                                                                                                 | Objets d’activation MFT      |
| [\_attribut de \_ flux \_ connecté MFT](mft-connected-stream-attribute.md)                                       | Contient un pointeur vers les attributs de flux du flux connecté sur une table MFT basée sur le matériel.                                                                                                  | MFTs                        |
| [MFT \_ connecté \_ au \_ flux de matériel \_](mft-connected-to-hw-stream.md)                                              | Spécifie si une table MFT basée sur le matériel est connectée à une autre table MFT basée sur le matériel.                                                                                                            | MFTs                        |
| [le \_ DÉcodeur MFT \_ expose les \_ \_ types \_ de sortie dans l' \_ \_ ordre natif](mft-decoder-expose-output-types-in-native-order.md) | Spécifie si un décodeur expose des types de sortie IYUV/I420 (convenant au transcodage) avant d’autres formats.                                                                                   | MFTs                        |
| [\_ \_ indicateur de \_ résolution vidéo final \_ du décodeur MFT \_](mft-decoder-final-video-resolution-hint.md)                   | Spécifie la résolution de sortie finale de l’image décodée, après le traitement vidéo.                                                                                                           | MFTs                        |
| [l' \_ encodeur MFT \_ prend en charge l' \_ événement de configuration \_](mft-encoder-supports-config-event.md)                                | Spécifie que l’encodeur MFT prend en charge la réception des événements [MEEncodingParameter](meencodingparameters.md) lors de la diffusion en continu.                                                                     | MFTs                        |
| [\_LUID d’adaptateur d’énumération MFT \_ \_](mft-enum-adapter-luid.md)                                                         | Spécifie un identificateur unique pour une carte vidéo. Utilisez cet attribut lors de l’appel de MFTEnum2 pour énumérer les MFTs associés à un adaptateur spécifique.                                             | MFTs                        |
| [Attribut de l' \_ \_ URL matérielle de l’ÉNUMÉRation MFT \_ \_](mft-enum-hardware-url-attribute.md)                                    | Contient le lien symbolique pour une table MFT basée sur le matériel.                                                                                                                                          | Objets d’activation MFTs/MFT |
| [\_Attribut d' \_ \_ ID de fournisseur de matériel d’énumération MFT \_ \_](mft-enum-hardware-vendor-id-attribute.md)                       | Spécifie l’ID de fournisseur pour une transformation de Media Foundation matérielle                                                                                                                       | MFTs                        |
| [\_attribut de transcodage d’énumération MFT \_ \_ uniquement \_](mft-enum-transcode-only-attribute.md)                                | Spécifie si un décodeur est optimisé pour le transcodage plutôt que pour la lecture.                                                                                                            | MFTs                        |
| [\_Attribut de \_ déverrouillage MFT FIELDOFUSE \_](mft-fieldofuse-unlock-attribute.md)                                     | Contient un pointeur [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , qui peut être utilisé pour déverrouiller la table MFT.                                                                            | Objets d’activation MFT      |
| [\_Attribut de \_ nom \_ convivial de la MFT](mft-friendly-name-attribute.md)                                             | Contient le nom complet d’une table MFT basée sur le matériel.                                                                                                                                           | Objets d’activation MFT      |
| [\_Attributs des \_ types d’entrée MFT \_](mft-input-types-attributes.md)                                               | Contient les types d’entrée inscrits pour une table MFT.                                                                                                                                               | Objets d’activation MFT      |
| [\_Attributs des \_ types de sortie MFT \_](mft-output-types-attributes.md)                                             | Contient les types de sortie inscrits pour une table MFT.                                                                                                                                              | Objets d’activation MFT      |
| [\_profil d' \_ encodeur préféré MFT \_](mft-preferred-encoder-profile.md)                                         | Contient les propriétés de configuration d’un encodeur.                                                                                                                                             | Objets d’activation MFT      |
| [\_ \_ Attribut OUTPUTTYPE préféré de MFT \_](mft-preferred-outputtype-attribute.md)                               | Spécifie le format de sortie préféré pour un encodeur.                                                                                                                                         | Objets d’activation MFT      |
| [\_ \_ Attribut OUTPUTTYPE préféré de MFT \_](mft-preferred-outputtype-attribute.md)                               | Spécifie le format de sortie préféré pour un encodeur.                                                                                                                                         | Objets d’activation MFT      |
| [\_ \_ Attribut local de processus MFT \_](mft-process-local-attribute.md)                                             | Spécifie si une table MFT est inscrite uniquement dans le processus de l’application.                                                                                                                     | Objets d’activation MFT      |
| [\_ \_ image de la marque REMUX MFT \_ \_ \_ comme \_ point de nettoyage \_](mft-remux-mark-i-picture-as-clean-point.md)                 | Spécifie si la table MFT REMUX vidéo H. 264 doit marquer I images comme point de nettoyage pour améliorer la capacité de recherche. Cela risque d’endommager les recherches dans des fichiers MP4 finaux non conformes. | Objets d’activation MFT      |
| [\_Prise en charge de MFT \_ 3DVIDEO](mft-support-3dvideo.md)                                                              | Spécifie si une Media Foundation transformation (MFT) prend en charge la vidéo stéréoscopique 3D.                                                                                                          | Objets d’activation MFT      |
| [**\_modification du \_ format dynamique de la prise en charge de \_ MFT \_**](mft-support-dynamic-format-change-attribute.md)                  | Spécifie si une Media Foundation transformation (MFT) prend en charge les modifications de format dynamiques.                                                                                                         | MFTs                        |
| [\_Attribut de \_ CLSID de transformation MFT \_](mft-transform-clsid-attribute.md)                                         | Contient l’identificateur de classe (CLSID) d’une table MFT.                                                                                                                                              | Objets d’activation MFT      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Transformations de Media Foundation](media-foundation-transforms.md)
</dt> </dl>

 

 



