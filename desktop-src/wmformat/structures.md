---
title: Windows Structures du SDK Media format
description: Windows Structures du SDK Media format
ms.assetid: 118ef278-ca4f-4c30-9633-a2d851f5c758
keywords:
- Windows Media Format SDK, structures
- ASF (Advanced Systems Format), structures
- ASF (format des systèmes avancés), structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 319be2d061132f59c1c75ebb295c8ceb8ae87ffbcce48e8259a1faedcf18d666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006609"
---
# <a name="windows-media-format-sdk-structures"></a>Windows Structures du SDK Media format

le kit de développement logiciel (SDK) Windows Media Format implémente les structures suivantes.



| Structure                                                                                | Description                                                                                                                                                               |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_OPL de copie DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_copy_opl)                                                   | Contient les informations de niveau de protection de sortie qui s’appliquent à l’action de copie dans une licence DRM.                                                                               |
| [**données d’état de la \_ licence DRM \_ \_**](drm-license-state-data.md)                              | Contient des informations de [*licence*](wmformat-glossary.md) sur un droit [*DRM*](wmformat-glossary.md) spécifié. |
| [**\_niveaux de \_ protection de sortie DRM minimum \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_minimum_output_protection_levels) | Contient les niveaux de protection de sortie minimum requis par une licence DRM pour lire du contenu dans différents formats.                                                                      |
| [**\_ID de \_ sortie DRM OPL \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_opl_output_ids)                                      | Contient un tableau d’identificateurs de la technologie DRM. Cette structure est utilisée pour définir des groupes de technologies dans d’autres structures DRM.                                            |
| [**\_OPL de lecture DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_play_opl)                                                   | Contient les informations de niveau de protection de sortie qui s’appliquent à l’action de lecture dans une licence DRM.                                                                               |
| [**ID de contenu de la \_ sélection DRM \_ \_**](drm-playlist-content-id.md)                            | Contient des informations sur le contenu qui doit être copié sur CD dans le cadre d’une gravure de sélection.                                                                                 |
| [**\_VAL16 DRM**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-drm_val16)                                                          | Stocke une valeur 128 bits utilisée comme identificateur d’appareil.                                                                                                                       |
| [**PROTECTION de sortie de la \_ vidéo DRM \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_output_protection)                    | Contient l’identificateur d’une technologie de protection vidéo et les données de configuration requises par cette technologie.                                                             |
| [**\_ID de \_ protection de sortie vidéo \_ DRM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_video_output_protection_ids)           | Contient un tableau de structures de **\_ \_ \_ protection de sortie vidéo DRM** .                                                                                                          |
| [**WAVEFORMATEX**](/previous-versions/windows/desktop/legacy/dd757720(v=vs.85))                                                | Définit le format des données Waveform-Audio.                                                                                                                                |
| [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85))                                | Définit le format des données Waveform-Audio pour les formats comportant plus de deux canaux.                                                                                      |
| [**ACCESSENTRY de l' \_ adresse WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_address_accessentry)                               | Spécifie une entrée dans une liste d’accès à une adresse IP.                                                                                                                          |
| [**\_Propriétés du client WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties)                                   | Enregistre des informations sur le client.                                                                                                                                     |
| [**Propriétés du client WM par \_ \_ \_ exemple**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_client_properties_ex)                            | Enregistre des informations étendues sur le client.                                                                                                                            |
| [**données de licence de l' \_ offre WM \_ \_**](wm-get-license-data.md)                                    | Contient des informations sur une licence DRM.                                                                                                                                 |
| [**État de l' \_ individualisation WM \_**](wm-individualize-status.md)                             | Enregistre l’état du processus d' [*individualisation*](wmformat-glossary.md) .                                                                |
| [**\_ \_ paire de compartiments de fuite WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair)                                  | Décrit les exigences en matière de mise en mémoire tampon pour un fichier VBR (variable-bit-rate).                                                                                                  |
| [**\_données d' \_ État de licence WM \_**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85))                                | Encapsule une structure de [**\_ données d' \_ état \_ de licence DRM**](drm-license-state-data.md) qui décrit les données d’état de licence DRM.                                              |
| [**\_type de média WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)                                                 | Décrit un exemple de média.                                                                                                                                                 |
| [**WMMPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmmpeg2videoinfo)                                             | Décrit un flux vidéo MPEG-2.                                                                                                                                         |
| [**\_image WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)                                                        | Contient les données de l’attribut de métadonnées complexes [**WM/Picture**](wmpicture.md) .                                                                                     |
| [**\_plage de \_ numéros de port WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_port_number_range)                                  | Décrit la plage des numéros de port utilisés par l’interface **IWMReaderNetworkConfig** .                                                                                     |
| [**\_CLIENTINFO de lecteur WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_clientinfo)                                   | Décrit le lecteur client (lecteur) qui accède au flux multimédia.                                                                                                          |
| [**\_statistiques du lecteur WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics)                                   | Décrit les performances d’une opération de lecture.                                                                                                                         |
| [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat)                                                 | Définit le format d’un flux de script.                                                                                                                                    |
| [**\_enregistrement de \_ priorité de flux WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_priority_record)                        | Contient un numéro de flux et spécifie si la remise de ce flux est obligatoire.                                                                                      |
| [**\_ \_ informations sur le type de flux WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info)                                    | Contient les données pour l’attribut de métadonnées complexes [**WM/StreamTypeInfo**](wm-streamtypeinfo.md) .                                                                      |
| [**\_paroles synchronisées \_ WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_synchronised_lyrics)                               | Contient les données de l’attribut de métadonnées complexes [**\_ synchronisées WM/paroles**](wm-lyrics-synchronised.md) .                                                           |
| [**texte de l' \_ utilisateur WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_text)                                                   | Contient les données pour l’attribut de métadonnées complexes [**WM/Text**](wm-text.md) .                                                                                          |
| [**\_ \_ URL Web de l’utilisateur WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_user_web_url)                                            | Contient les données pour l’attribut de métadonnées complexes [**WM/UserWebURL**](wm-userweburl.md) .                                                                              |
| [**\_statistiques du rédacteur WM \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics)                                   | Décrit les performances d’une opération d’écriture.                                                                                                                         |
| [**\_statistiques du rédacteur WM \_ \_ ex**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex)                            | Contient les statistiques de l’enregistreur étendu.                                                                                                                                      |
| [**\_clé de \_ contenu d’importation WMDRM \_**](wmdrm-import-content-key.md)                          | Contient la clé de contenu utilisée pour l’importation de contenu protégé.                                                                                                                |
| [**\_struct import \_ init \_ struct**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)                          | Contient la clé de session chiffrée et la clé de contenu utilisées pour l’importation de contenu protégé.                                                                                      |
| [**\_clé de \_ session d’importation WMDRM \_**](wmdrm-import-session-key.md)                          | Contient la clé de session pour l’importation de contenu protégé.                                                                                                                    |
| [**\_segment de mémoire tampon WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_buffer_segment)                                       | Contient les informations nécessaires pour spécifier un segment dans un paquet.                                                                                                      |
| [**\_données d' \_ extension \_ COLORSPACEINFO WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data)        | Contient les données pour l' \_ extension d’unité de données WM SampleExtensionGUID \_ ColorSpaceInfo.                                                                                    |
| [**\_unité de \_ données \_ FILESINK WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_filesink_data_unit)                              | Contient des informations sur un paquet.                                                                                                                                      |
| [**\_fragment de charge utile WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_payload_fragment)                                   | Contient les informations nécessaires pour extraire un fragment de charge utile d’un paquet.                                                                                           |
| [**\_données d’extension du code temporel WMT \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)                    | Contient un code temporel SMPTE unique et les informations associées.                                                                                                                |
| [**\_exemple d’VIDEOIMAGE WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample)                                 | Contient des informations sur un exemple d’image vidéo.                                                                                                                          |
| [**\_entrée de filigrane WMT \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_watermark_entry)                                     | Contient des informations sur un système de filigrane.                                                                                                                         |
| [**\_format WEBSTREAM \_ WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format)                                   | Contient des informations sur un flux de données Web.                                                                                                                                  |
| [**\_ \_ exemple d' \_ en-tête d’exemple webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header)                    | Contient des informations d’en-tête pour les exemples de flux Web.                                                                                                                       |
| [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)                                           | Décrit les informations de bitmap et de couleur pour une image vidéo.                                                                                                             |
| [**WMVIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader2)                                         | Décrit les informations de bitmap et de couleur pour une image vidéo, y compris l' [*entrelacement*](wmformat-glossary.md), la protection contre la copie et les proportions.       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 
