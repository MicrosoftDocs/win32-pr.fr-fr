---
description: Capturer les attributs de l’appareil
ms.assetid: dd24671a-0689-4490-8d18-2a33ed461e9d
title: Capturer les attributs de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dd8dbcdf0a441ddb8a5ef2794526e961c22033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517428"
---
# <a name="capture-device-attributes"></a>Capturer les attributs de l’appareil

Les attributs suivants sont liés aux appareils de capture :



| Attribut                                                                                                                     | Description                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [\_ \_ \_ nom convivial de l’attribut DEVSOURCE MF \_](mf-devsource-attribute-friendly-name.md)                                          | Nom complet de l’appareil.                                                          |
| [\_type de \_ média d’attribut DEVSOURCE \_ MF \_](mf-devsource-attribute-media-type.md)                                                | Format de sortie de l’appareil.                                                         |
| [\_type de \_ source d’attribut MF DEVSOURCE \_ \_](mf-devsource-attribute-source-type.md)                                              | Type d’appareil, tel que la capture audio ou la capture vidéo.                         |
| [\_ID de \_ point \_ de \_ \_ terminaison AUDCAP \_ du type de source de \_ l’attribut DEVSOURCE MF](mf-devsource-attribute-source-type-audcap-endpoint-id.md)     | ID de point de terminaison pour un périphérique de capture audio.                                        |
| [TYPE de source de l' \_ attribut DEVSOURCE MF- \_ \_ \_ \_ \_ rôle AUDCAP](mf-devsource-attribute-source-type-audcap-role.md)                    | Le rôle d’appareil pour un périphérique de capture audio.                                        |
| [\_type de source d’attribut DEVSOURCE MF- \_ \_ \_ \_ \_ catégorie VIDCAP](mf-devsource-attribute-source-type-vidcap-category.md)            | Catégorie d’appareil pour un périphérique vidéo.                                             |
| [\_type de source d’attribut DEVSOURCE MF \_ \_ \_ \_ \_ source VIDCAP HW \_](mf-devsource-attribute-source-type-vidcap-hw-source.md)         | Spécifie si une source de capture vidéo est un périphérique matériel ou un périphérique logiciel. |
| [\_type de source d’attribut DEVSOURCE MF \_ \_ \_ \_ VIDCAP \_ Max \_ buffers](mf-devsource-attribute-source-type-vidcap-max-buffers.md)     | Spécifie le nombre maximal de trames que la source de capture vidéo va mettre en mémoire tampon.   |
| [\_ \_ \_ \_ \_ \_ lien symbolique VIDCAP du type de source de l’attribut \_ DEVSOURCE MF](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) | Lien symbolique pour un pilote de capture vidéo.                                       |
| [\_Horodateur de la MFT HW \_ avec l' \_ \_ \_ attribut QPC](mft-hw-timestamp-with-qpc-attribute.md)                                           | Spécifie si la source de l’appareil utilise l’heure système pour les horodatages.           |



 

Ces attributs sont utilisés avec les fonctions suivantes :

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Attributs Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



