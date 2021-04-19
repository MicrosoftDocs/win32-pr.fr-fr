---
description: Les identificateurs globaux uniques (GUID) suivants définissent les types de nœud pour les filtres en mode noyau. Pour rechercher le type de nœud, interrogez le filtre de l’interface IKsTopologyInfo.
ms.assetid: 0e133ce3-8815-47d1-a5c3-577a98963912
title: Types de nœuds KS (Ksmedia. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSNODETYPE_DEV_SPECIFIC
- KSNODETYPE_VIDEO_CAMERA_TERMINAL
- KSNODETYPE_VIDEO_INPUT_MTT
- KSNODETYPE_VIDEO_INPUT_TERMINAL
- KSNODETYPE_VIDEO_OUTPUT_MTT
- KSNODETYPE_VIDEO_OUTPUT_TERMINAL
- KSNODETYPE_VIDEO_PROCESSING
- KSNODETYPE_VIDEO_SELECTOR
- KSNODETYPE_VIDEO_STREAMING
api_type:
- HeaderDef
api_location:
- Ksmedia.h
ms.openlocfilehash: eadae4fdd70fd80115ea4e8902ba1bb2aa7bf53b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543595"
---
# <a name="ks-node-types"></a>Types de nœuds KS

Les identificateurs globaux uniques (GUID) suivants définissent les types de nœud pour les filtres en mode noyau. Pour rechercher le type de nœud, interrogez le filtre de l’interface [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) .



| GUID                                                                                                                                                                                                                     | Description                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KSNODETYPE_DEV_SPECIFIC"></span><span id="ksnodetype_dev_specific"></span><dl> <dt>**\_spécifique au dev KSNODETYPE \_**</dt> </dl>                             | Représente une ou plusieurs fonctions de traitement spécifiques à l’appareil. Le nœud possède une connexion d’entrée et une connexion de sortie.<br/> Le nœud peut exposer une interface COM personnalisée via un plug-in KsProxy, s’il est fourni par le fabricant de l’appareil.<br/>                                            |
| <span id="KSNODETYPE_VIDEO_CAMERA_TERMINAL"></span><span id="ksnodetype_video_camera_terminal"></span><dl> <dt>**\_terminal de \_ caméra \_ vidéo KSNODETYPE**</dt> </dl> | Représente les données qui se déplacent dans l’appareil à partir d’un capteur d’appareil photo, indépendant du bus USB. Le nœud possède une connexion de sortie.<br/> Le nœud expose les interfaces [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) et [**ICameraControl**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-icameracontrol) pour le contrôle de l’appareil photo.<br/> |
| <span id="KSNODETYPE_VIDEO_INPUT_MTT"></span><span id="ksnodetype_video_input_mtt"></span><dl> <dt>**KSNODETYPE \_ vidéo \_ d’entrée \_ MTT**</dt> </dl>                   | Représente les données qui se déplacent dans l’appareil à partir d’un transport multimédia séquentiel, tel qu’une bande VTR, indépendante du bus USB. Le nœud possède une connexion de sortie.<br/> Le nœud expose l’interface [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) pour le contrôle du mécanisme de transport.<br/>   |
| <span id="KSNODETYPE_VIDEO_INPUT_TERMINAL"></span><span id="ksnodetype_video_input_terminal"></span><dl> <dt>**\_ \_ terminal d’entrée vidéo KSNODETYPE \_**</dt> </dl>    | Représente les données qui se déplacent dans l’appareil, indépendamment du bus USB. Par exemple, ce nœud peut représenter une prise jack audio analogique ou un Jack S/PDIF. Le nœud possède une connexion de sortie.<br/>                                                                                                             |
| <span id="KSNODETYPE_VIDEO_OUTPUT_MTT"></span><span id="ksnodetype_video_output_mtt"></span><dl> <dt>**\_sortie vidéo \_ KSNODETYPE \_ MTT**</dt> </dl>                | Représente les données qui se déplacent de l’appareil vers un transport multimédia séquentiel, tel qu’une bande VTR, indépendante du bus USB. Le nœud possède une connexion d’entrée.<br/> Le nœud expose l’interface [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) pour le contrôle du mécanisme de transport.<br/>      |
| <span id="KSNODETYPE_VIDEO_OUTPUT_TERMINAL"></span><span id="ksnodetype_video_output_terminal"></span><dl> <dt>**\_terminal de \_ sortie \_ vidéo KSNODETYPE**</dt> </dl> | Représente les données qui se déplacent de l’appareil, indépendamment du bus USB. Par exemple, ce nœud peut représenter une prise jack audio analogique ou un Jack S/PDIF. Le nœud possède une connexion d’entrée.<br/>                                                                                                              |
| <span id="KSNODETYPE_VIDEO_PROCESSING"></span><span id="ksnodetype_video_processing"></span><dl> <dt>**\_traitement vidéo \_ KSNODETYPE**</dt> </dl>                 | Représente une ou plusieurs fonctions de traitement vidéo. Le nœud possède une connexion d’entrée et une connexion de sortie.<br/> Le nœud expose les interfaces [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) et [**IVideoProcAmp**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ivideoprocamp) pour ajuster les qualités du signal vidéo.<br/> |
| <span id="KSNODETYPE_VIDEO_SELECTOR"></span><span id="ksnodetype_video_selector"></span><dl> <dt>**\_sélecteur vidéo \_ KSNODETYPE**</dt> </dl>                       | Représente un mécanisme permettant de sélectionner le chemin d’entrée à partir de plusieurs sources possibles. Le nœud possède au moins deux connexions d’entrée et une connexion de sortie.<br/> Le nœud expose l’interface [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) pour la sélection entre les entrées.<br/>                               |
| <span id="KSNODETYPE_VIDEO_STREAMING"></span><span id="ksnodetype_video_streaming"></span><dl> <dt>**\_diffusion vidéo \_ KSNODETYPE**</dt> </dl>                    | Représente les données qui se déplacent entre l’hôte et l’appareil. Pour les appareils UVC, ce nœud représente un point de terminaison USB. Les points de terminaison d’entrée ont une connexion d’entrée ; les points de terminaison de sortie ont une connexion de sortie.<br/>                                                                                         |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Ksmedia. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes et GUID](constants-and-guids.md)
</dt> </dl>

 

 




