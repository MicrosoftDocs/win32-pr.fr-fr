---
description: Attributs du descripteur de flux
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Attributs du descripteur de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5db29ef0076415ff07e9ed25f7e6ca3e0588ec25257802fe0c7829ab3178c935
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953229"
---
# <a name="stream-descriptor-attributes"></a>Attributs du descripteur de flux

## <a name="common-stream-descriptor-attributes"></a>Attributs courants du descripteur de flux

Les attributs suivants s’appliquent aux descripteurs de flux.



| Attribut                                                   | Description                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**\_langage SD \_ MF**](mf-sd-language-attribute.md)        | Spécifie la langue d’un flux.                                                  |
| [MF SD s’excluant \_ \_ mutuellement \_](mf-sd-mutually-exclusive.md) | Spécifie si un flux s’exclut mutuellement avec d’autres flux du même type. |
| [**\_protégé SD \_ sécurisé**](mf-sd-protected-attribute.md)      | Spécifie si un flux de données contient du contenu protégé.                                |
| [\_nom du \_ flux \_ SD MF](mf-sd-stream-name.md)               | Contient le nom d’un flux.                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a>Attributs du descripteur de flux ASF-Specific

Les attributs suivants s’appliquent aux descripteurs de flux pour les fichiers ASF (Advanced Systems Format).



| Attribut                                                                                                                | Description                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**\_bufferSize SD \_ ASF \_ EXTSTRMPROP \_ Moy \_ .**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | Spécifie la taille moyenne de la mémoire tampon nécessaire pour un flux dans un fichier ASF, en octets.            |
| [**\_vitesse de \_ \_ \_ transmission moyenne des \_ données EXTSTRMPROP \_ MF SD ASF**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | Spécifie la vitesse moyenne de transmission de données d’un flux dans un fichier ASF, en bits par seconde.        |
| [**\_ID de \_ \_ langue EXTSTRMPROP \_ \_ MF \_ SD ASF**](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | Spécifie la langue utilisée par un flux dans un fichier ASF.                                    |
| [**\_bufferSize SD \_ \_ EXTSTRMPROP ASF \_ Max \_ .**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | Spécifie la taille maximale de la mémoire tampon nécessaire pour un flux dans un fichier ASF, en octets.            |
| [**\_vitesse de \_ \_ transmission de \_ \_ données Max \_ . ASF EXTSTRMPROP ASF**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | Spécifie la vitesse de transmission maximale de données d’un flux dans un fichier ASF, en bits par seconde.         |
| [**\_modèle de \_ \_ conformité des appareils de métadonnées ASF SD ASF \_ \_ \_**](mf-sd-asf-metadata-device-conformance-template-attribute.md) | Spécifie le modèle de conformité de périphérique pour un flux de données dans un fichier ASF, en bits par seconde. |
| [**\_vitesse de \_ \_ transmission de STREAMBITRATES MF SD ASF \_**](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | Spécifie la vitesse de transmission moyenne d’un flux dans un fichier ASF, en bits par seconde.             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a>Attributs du descripteur du flux de source du média SAMI

L’attribut suivant s’applique au descripteur de flux pour la source du média SAMI.



| Attribut                                                       | Description                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**PP \_ SD \_ ( \_ langage sami)**](mf-sd-sami-language-attribute.md) | Contient le nom du langage SAMI (Synchronized Accessible Media Interchange) qui est défini pour le flux. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



