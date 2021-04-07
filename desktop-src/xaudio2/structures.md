---
title: Structures XAudio2
description: Cette section contient des informations sur les structures fournies par l’API Microsoft XAudio2.
ms.assetid: 3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3b67e0312c5ac6b753881d895dff3972564f2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759477"
---
# <a name="xaudio2-structures"></a>Structures XAudio2

Cette section contient des informations sur les structures fournies par l’API Microsoft XAudio2.



| Structure                                                                                 | Description                                                                                                                                    |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer)                                                 | Représente une mémoire tampon de données audio.<br/>                                                                                                    |
| [**\_Mémoire tampon XAUDIO2 \_ WMA**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer_wma)                                        | Représente une mémoire tampon de données audio WMA.<br/>                                                                                                 |
| [**\_Configuration du débogage XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration)                      | Définit une nouvelle configuration de débogage globale pour XAudio2 quand elle est utilisée par la fonction SetDebugConfiguration.                                             |
| [**\_Chaîne d’effet XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_chain)                                    | Définit une chaîne d’effet.<br/>                                                                                                            |
| [**\_Descripteur d’effet XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_effect_descriptor)                          | Définit un effet.<br/>                                                                                                                  |
| [**\_Paramètres de filtre XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_filter_parameters)                          | Définit les paramètres de filtre pour une voix source.<br/>                                                                                       |
| [**\_Données de performances de XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_performance_data)                            | Récupère des informations sur les performances.<br/>                                                                                                  |
| [**\_Descripteur d’envoi XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_send_descriptor)                              | Décrit une destination d’envoi vocal.<br/>                                                                                                 |
| [**Détails de la \_ voix XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_details)                                  | Contient des informations sur les indicateurs de création, les canaux d’entrée et le taux d’échantillonnage d’une voix.<br/>                                          |
| [**Envoi de la \_ voix XAUDIO2 \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_sends)                                      | Définit un ensemble de voix pour recevoir des données à partir d’une seule voix de sortie.<br/>                                                                 |
| [**\_État vocal \_ XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_voice_state)                                      | Retourne les données sur l’état actuel et la position du curseur de la voix.<br/>                                                                         |
| [**Paramètres de I3DL2 de \_ réverbération XAUDIO2FX \_ \_**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_i3dl2_parameters)         | Décrit les paramètres de I3DL2 (Interactive 3D audio Rendering Guidelines Level 2,0) à utiliser dans la fonction ReverbConvertI3DL2ToNative.           |
| [**\_Paramètres de réverbération \_ XAUDIO2FX**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters)                      | Décrit les paramètres à utiliser dans le APO de réverbération.                                                                                                |
| [**\_Niveaux VOLUMEMETER \_ XAUDIO2FX**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_volumemeter_levels)                    | Décrit les paramètres à utiliser avec le APO de compteur de volume.                                                                                        |
| [**\_paramètres de \_ mémoire tampon XAPO LOCKFORPROCESS \_**](/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters) | Définit les paramètres de mémoire tampon qui restent constants lorsqu’un XAPO est verrouillé.<br/>                                                             |
| [**\_paramètres de \_ mémoire tampon du processus XAPO \_**](/windows/desktop/api/xapo/ns-xapo-xapo_process_buffer_parameters)               | Définit des paramètres de mémoire tampon qui peuvent changer d’un appel à l’autre.<br/>                                                                |
| [**\_propriétés d’inscription XAPO \_**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)                    | Décrit les caractéristiques générales d’un XAPO.<br/>                                                                                       |
| [**FXECHO \_ INITDATA**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_initdata)                                               | Paramètres d’initialisation à utiliser avec le XAPO FXECHO.<br/>                                                                             |
| [**\_paramètres FXECHO**](/windows/desktop/api/xapofx/ns-xapofx-fxecho_parameters)                                           | Paramètres à utiliser avec le XAPO FXECHO.<br/>                                                                                            |
| [**\_paramètres FXEQ**](/windows/desktop/api/xapofx/ns-xapofx-fxeq_parameters)                                               | Paramètres à utiliser avec le XAPO FXEQ.<br/>                                                                                              |
| [**\_paramètres FXMASTERINGLIMITER**](/windows/desktop/api/xapofx/ns-xapofx-fxmasteringlimiter_parameters)                   | Paramètres à utiliser avec le XAPO FXMasteringLimiter.<br/>                                                                                |
| [**\_paramètres FXREVERB**](/windows/desktop/api/xapofx/ns-xapofx-fxreverb_parameters)                                       | Paramètres à utiliser avec le XAPO FXReverb.<br/>                                                                                          |
| [**\_Cône X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)                                                   | Spécifie la direction d’un émetteur non-LFE à canal unique en mettant à l’échelle le comportement DSP en ce qui concerne l’orientation de l’émetteur.<br/>    |
| [**\_Courbe de distance X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve)                              | Définit une courbe par morceaux explicite composée de segments linéaires, en définissant directement le comportement DSP en ce qui concerne la distance normalisée.<br/> |
| [**\_Point de \_ courbe de distance X3DAUDIO \_**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_distance_curve_point)                 | Définit un paramètre DSP à une distance normalisée donnée.<br/>                                                                               |
| [**X3DAUDIO \_ DSP, \_ paramètres**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_dsp_settings)                                  | Reçoit les résultats d’un appel à X3DAudioCalculate.<br/>                                                                              |
| [**\_Émetteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_emitter)                                             | Définit une source audio 3D unique ou multipoint utilisée avec un nombre arbitraire de canaux audio.<br/>                                    |
| [**\_Écouteur X3DAUDIO**](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_listener)                                           | Définit un point de réception audio 3D.<br/>                                                                                              |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de référence de programmation](programming-reference.md)
</dt> </dl>

 

 




