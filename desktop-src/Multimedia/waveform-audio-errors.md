---
title: Erreurs de Waveform-Audio
description: Erreurs de Waveform-Audio
ms.assetid: c898552a-a60a-4deb-ab4a-ed74b08a7d05
keywords:
- MCIERR les valeurs de retour, erreurs Waveform-Audio
- Référence multimédia, erreurs Waveform-Audio
- référence pour les erreurs multimédias, Waveform-Audio
- Erreurs MCI (Media Control Interface), Waveform-Audio
- MCI (interface de contrôle multimédia), erreurs Waveform-Audio
- référence pour les erreurs MCI, Waveform-Audio
- Référence MCI, erreurs Waveform-Audio
- MCI (Media Control Interface), Erreurs
- MCI (interface de contrôle multimédia), Erreurs
- informations de référence sur MCI, Erreurs
- Informations de référence sur MCI, Erreurs
- Erreurs Waveform-Audio
- Erreurs Waveform MCI-audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf64e8cd4ec6d061422bcf14d17dfb4c4317ee4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011706"
---
# <a name="waveform-audio-errors"></a>Erreurs de Waveform-Audio

Les valeurs de retour supplémentaires suivantes sont définies pour les périphériques MCI Waveform-Audio :



| Valeur                             | Signification                                                                                                                                                             |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ Wave \_ INPUTSINUSE         | Tous les périphériques Waveform qui peuvent enregistrer des fichiers dans le format actuel sont en cours d’utilisation. Attendez que l’un de ces appareils soit libre. Ensuite, réessayez.                              |
| MCIERR \_ Wave \_ INPUTSUNSUITABLE    | Aucun périphérique Waveform installé ne peut enregistrer des fichiers au format actuel. Utilisez l’option pilotes du panneau de configuration pour installer un périphérique d’enregistrement de la forme d’onde approprié. |
| MCIERR \_ Wave \_ INPUTUNSPECIFIED    | Vous pouvez spécifier n’importe quel appareil d’enregistrement de la forme d’onde compatible.                                                                                                           |
| MCIERR \_ Wave \_ OUTPUTSINUSE        | Tous les périphériques Waveform capables de lire des fichiers dans le format actuel sont en cours d’utilisation. Attendez que l’un de ces appareils soit libre. Ensuite, réessayez.                                |
| MCIERR \_ Wave \_ OUTPUTSUNSUITABLE   | Aucun périphérique Waveform installé ne peut lire des fichiers au format actuel. Utilisez l’option pilotes du panneau de configuration pour installer un périphérique de forme d’onde approprié.             |
| MCIERR \_ Wave \_ OUTPUTUNSPECIFIED   | Vous pouvez spécifier n’importe quel périphérique de lecture de la forme d’onde compatible.                                                                                                            |
| MCIERR \_ Wave \_ SETINPUTINUSE       | L’appareil Waveform actuel est en cours d’utilisation. Attendez que l’appareil soit libre. Ensuite, réessayez de configurer l’appareil pour l’enregistrement.                                              |
| MCIERR \_ Wave \_ SETINPUTUNSUITABLE  | L’appareil que vous utilisez pour enregistrer une forme d’onde ne peut pas reconnaître le format des données.                                                                                     |
| MCIERR \_ Wave \_ SETOUTPUTINUSE      | L’appareil Waveform actuel est en cours d’utilisation. Attendez que l’appareil soit libre. Ensuite, réessayez de configurer l’appareil pour la lecture.                                               |
| MCIERR \_ Wave \_ SETOUTPUTUNSUITABLE | L’appareil que vous utilisez pour lire une forme d’onde ne peut pas reconnaître le format des données.                                                                                   |



 

 

 




