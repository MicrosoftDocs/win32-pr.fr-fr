---
title: Structures WMDM
description: Structures
ms.assetid: 3068359f-5ac0-41e0-a09b-283b439527a0
keywords:
- Gestionnaire de périphériques Windows Media, structures
- Gestionnaire de périphériques, structures
- Référence de programmation, structures
- informations de référence sur les Gestionnaire de périphériques Windows Media, structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903aa07bbe3d01029eb2020b521523b545843f2a
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104381259"
---
# <a name="wmdm-structures"></a>Structures WMDM

Windows Media Gestionnaire de périphériques définit les structures suivantes.



| Structure                                                   | Description                                                                                                                                                                                                                                              |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)             | Définit le format de l’image vidéo.                                                                                                                                                                                                                       |
| [**\_ \_ données de commande MTP \_ dans**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_in)       | Contient des commandes personnalisées MTP (Media Transport Protocol) qui sont envoyées à l’appareil à l’aide de la méthode [**IWMDMDevice3 ::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) .                                                                           |
| [**\_ \_ sortie des données de commande MTP \_**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_out)     | Contient les réponses MTP (Media Transport Protocol) qui sont remplies par le pilote de périphérique.                                                                                                                                                                  |
| [**OPAQUECOMMAND**](opaquecommand.md)                      | Contient des données pour les commandes qui sont transmises par le biais de Windows Media Gestionnaire de périphériques à un appareil, mais qui ne sont pas destinées à être traitées par Windows Media Gestionnaire de périphériques.                                                                                       |
| [**\_VIDEOINFOHEADER**](-videoinfoheader.md)               | Définit le format d’un flux vidéo.                                                                                                                                                                                                                    |
| [**\_WAVEFORMATEX**](-waveformatex.md)                     | Définit le format des données Waveform-Audio.                                                                                                                                                                                                               |
| [**\_fonction de format WMDM \_**](wmdm-format-capability.md)  | Décrit les fonctionnalités d’un appareil pour un format particulier. Cette structure contient un ensemble de configurations de propriétés dans un tableau de structures de configuration [**WMDM \_ prop \_**](wmdm-prop-config.md) .                                                       |
| [**configuration de WMDM \_ prop \_**](wmdm-prop-config.md)              | Décrit un ensemble de valeurs de propriété compatibles sur toutes les propriétés prises en charge par l’appareil pour un format particulier. Cette structure contient un certain nombre de descriptions de propriété dans un tableau de structures [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) . |
| [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md)                  | Décrit les valeurs valides d’une propriété dans une configuration de propriété particulière.                                                                                                                                                                             |
| [**\_ \_ énumération des valeurs prop WMDM \_**](wmdm-prop-values-enum.md)   | Contient un ensemble énuméré de valeurs valides pour une propriété particulière dans une configuration de propriété particulière.                                                                                                                                             |
| [**plage de valeurs de WMDM \_ prop \_ \_**](wmdm-prop-values-range.md) | Décrit la plage de valeurs valides pour une propriété particulière dans une configuration de propriété particulière.                                                                                                                                                        |
| [**WMDMDATETIME**](wmdmdatetime.md)                        | Contient une date et une heure.                                                                                                                                                                                                                                |
| [**WMDMID**](wmdmid.md)                                    | Décrit les numéros de série et les ID de groupe.                                                                                                                                                                                                                  |
| [**WMDMMetadataView**](wmdmmetadataview.md)                | Définit la vue de métadonnées.                                                                                                                                                                                                                               |
| [**WMDMRIGHTS**](wmdmrights.md)                            | Décrit les droits d’utilisation de contenu.                                                                                                                                                                                                                            |
| [**WMFILECAPABILITIES**](wmfilecapabilities.md)            | Décrit un type MIME.                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](programming-reference.md)
</dt> </dl>

 

 




