---
title: Structures clientes DRM Microsoft Windows Media
description: Structures clientes DRM Microsoft Windows Media
ms.assetid: 794de1b7-d60c-435e-9f77-c4df109b5372
keywords:
- Windows Media Format SDK, structures
- gestion des droits numériques (DRM), structures
- DRM (gestion des droits numériques), structures
- API étendues du client DRM, structures
- API étendues clientes, structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 145381cc6d702dd338176ffa89983de137285dcd7aef946d3ece956eb450880c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447839"
---
# <a name="microsoft-windows-media-drm-client-structures"></a>Structures clientes DRM Microsoft Windows Media

les structures suivantes sont prises en charge par le Windows les api étendues du Client DRM Media.



| Structure ou énumération                                                                    | Description                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ID de \_ protection de sortie audio \_ DRM \_**](drm-audio-output-protection-ids.md)              | Contient une liste d’identificateurs de protection de sortie audio.                                                                                                     |
| [**\_ID de \_ protection de sortie audio DRM \_ \_ \_ ex**](drm-audio-output-protection-ids-ex.md)       | Contient une liste d’identificateurs de protection de sortie audio. Cette structure étend **les \_ \_ ID de \_ protection \_ de sortie audio DRM** en ajoutant un numéro de version.          |
| [**\_OPL de copie DRM \_**](drmdrm-copy-opl.md)                                                   | Contient des informations sur les niveaux de protection de sortie spécifiés dans une licence pour les actions de copie.                                                               |
| [**données d’état de la \_ licence DRM \_ \_**](drmdrm-license-state-data.md)                              | Contient des informations sur les restrictions de licence pour un droit DRM.                                                                                        |
| [**\_niveaux de \_ protection de sortie DRM minimum \_ \_**](drmdrm-minimum-output-protection-levels.md) | Contient les niveaux de protection de sortie (OPLs) minimum pour la lecture de différents types de contenu.                                                                 |
| [**\_ID de \_ sortie DRM OPL \_**](drmdrm-opl-output-ids.md)                                      | Contient un certain nombre d’identificateurs de sortie OPL.                                                                                                                   |
| [**\_protection de sortie DRM \_**](drm-output-protection.md)                                    | Contient des informations sur une technologie de protection de sortie.                                                                                                    |
| [**PROTECTION de la sortie DRM par \_ \_ \_ exemple**](drm-output-protection-ex.md)                             | Contient des informations sur une technologie de protection de sortie. Cette structure étend **la \_ \_ protection de la sortie DRM** en ajoutant un numéro de version.                     |
| [**\_OPL de lecture DRM \_**](drmdrm-play-opl.md)                                                   | Contient des informations sur les OPLs spécifiés dans une licence pour les actions de lecture.                                                                                   |
| [**\_OPL de lecture DRM \_ \_ ex**](drm-play-opl-ex.md)                                               | Contient des informations étendues sur le OPLs spécifié dans une licence pour les actions de lecture.                                                                          |
| [**\_ID de \_ protection de sortie vidéo \_ DRM \_**](drmdrm-video-output-protection-ids.md)           | Contient un tableau de structures de **\_ \_ \_ protection de sortie vidéo DRM** .                                                                                            |
| [**\_ID de \_ protection de sortie vidéo DRM \_ \_ \_ ex**](drm-video-output-protection-ids-ex.md)       | Contient un tableau de structures de **\_ \_ \_ protection de sortie vidéo DRM** . Cette structure étend **les \_ \_ ID de \_ protection \_ de sortie vidéo DRM** en ajoutant un numéro de version. |
| [**État de restauration de la \_ sauvegarde WM \_ \_**](wm-backup-restore-status.md)                             | Contient des informations sur une opération de sauvegarde ou de restauration de licence en attente.                                                                                      |
| [**État de l' \_ individualisation WM \_**](drmwm-individualize-status.md)                             | Contient des informations sur un processus d’individualisation en attente.                                                                                                |
| [**RESTRICTIONS de la \_ vidéo analogique WMDRM \_ \_**](wmdrm-analog-video-restrictions.md)               | Contient des informations sur une restriction pour la diffusion de contenu en tant que vidéo analogique.                                                                             |
| [**RESTRICTIONS de la \_ vidéo analogique WMDRM \_ \_ \_ ex**](wmdrm-analog-video-restrictions-ex.md)        | Contient des informations étendues sur une restriction pour la diffusion de contenu en tant que vidéo analogique.                                                                    |
| [**\_bloc de diffusion de chiffrement WMDRM \_ \_**](wmdrm-encrypt-scatter-block.md)                       | Contient un bloc de données à chiffrer.                                                                                                                   |
| [**\_informations de diffusion de chiffrement WMDRM \_ \_**](wmdrm-encrypt-scatter-info.md)                         | Contient les informations nécessaires pour configurer l’interface [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md) en vue de son utilisation.                                        |
| [**\_filtre de licence WMDRM \_**](wmdrm-license-filter.md)                                      | Contient des informations de filtrage pour créer des énumérations de licence.                                                                                           |
| [**\_niveaux de \_ protection de sortie WMDRM \_**](wmdrm-output-protection-levels.md)                 | Contient les niveaux de protection de sortie requis par une licence pour effectuer diverses actions.                                                                    |
| [**WMDRMCryptoData**](wmdrmcryptodata.md)                                                  | Contient des informations sur l’algorithme de chiffrement utilisé pour chiffrer et déchiffrer le contenu.                                                                 |
| [**\_stratégie WMDRMNET**](wmdrmnet-policy.md)                                                 | contient la stratégie à utiliser pour le Windows Media DRM pour les opérations sur les périphériques réseau.                                                                        |
| [**\_ \_ exigences globales de la stratégie WMDRMNET \_**](wmdrmnet-policy-global-requirements.md)       | contient les exigences globales pour Windows DRM pour les périphériques réseau.                                                                                        |
| [**\_ \_ environnement minimal de la stratégie WMDRMNET \_**](wmdrmnet-policy-minimum-environment.md)       | contient les exigences de sécurité minimales pour Windows DRM de média pour les périphériques réseau.                                                                       |
| [**\_stratégie WMDRMNET \_ TRANSCRYPTPLAY**](wmdrmnet-policy-transcryptplay.md)                  | contient les informations de stratégie pour la diffusion de contenu à l’aide de Windows Media DRM pour les périphériques réseau.                                                               |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](drm-programming-reference.md)
</dt> </dl>

 

 




