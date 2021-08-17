---
description: Les GUID de classe de terminal identifient un terminal particulier par fonctionnalités.
ms.assetid: 2a16d33c-2d87-4172-a5ff-33ff62e96615
title: Classe de terminal (Tapi3if. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd20d3e540529b343d1fb848b9e8cb2579a621b40146e0d170fdb175c4c9a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975449"
---
# <a name="terminal-class"></a>Classe de terminal

Les GUID de classe de terminal identifient un terminal particulier par fonctionnalités.

<dl> <dt>

<span id="CLSID_FilePlaybackTerminal"></span><span id="clsid_fileplaybackterminal"></span><span id="CLSID_FILEPLAYBACKTERMINAL"></span>**CLSID \_ FilePlaybackTerminal**
</dt> <dd> <dl> <dt>



Terminal de lecture de fichier.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTerminal"></span><span id="clsid_filerecordingterminal"></span><span id="CLSID_FILERECORDINGTERMINAL"></span>**CLSID \_ FileRecordingTerminal**
</dt> <dd> <dl> <dt>



Terminal d’enregistrement de fichier.


</dt> </dl> </dd> <dt>

<span id="CLSID_FileRecordingTrack"></span><span id="clsid_filerecordingtrack"></span><span id="CLSID_FILERECORDINGTRACK"></span>**CLSID \_ FileRecordingTrack**
</dt> <dd> <dl> <dt>



Piste d’enregistrement du fichier.


</dt> </dl> </dd> <dt>

<span id="CLSID_HandsetTerminal"></span><span id="clsid_handsetterminal"></span><span id="CLSID_HANDSETTERMINAL"></span>**CLSID \_ HandsetTerminal**
</dt> <dd> <dl> <dt>



Téléphone.


</dt> </dl> </dd> <dt>

<span id="CLSID_HeadsetTerminal"></span><span id="clsid_headsetterminal"></span><span id="CLSID_HEADSETTERMINAL"></span>**CLSID \_ HeadsetTerminal**
</dt> <dd> <dl> <dt>



Ensemble de têtes.


</dt> </dl> </dd> <dt>

<span id="CLSID_MediaStreamTerminal"></span><span id="clsid_mediastreamterminal"></span><span id="CLSID_MEDIASTREAMTERMINAL"></span>**CLSID \_ MediaStreamTerminal**
</dt> <dd> <dl> <dt>



Terminal de diffusion multimédia en continu, créé dynamiquement.


</dt> </dl> </dd> <dt>

<span id="CLSID_MicrophoneTerminal"></span><span id="clsid_microphoneterminal"></span><span id="CLSID_MICROPHONETERMINAL"></span>**CLSID \_ MicrophoneTerminal**
</dt> <dd> <dl> <dt>



Cravate.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakerphoneTerminal"></span><span id="clsid_speakerphoneterminal"></span><span id="CLSID_SPEAKERPHONETERMINAL"></span>**CLSID \_ SpeakerphoneTerminal**
</dt> <dd> <dl> <dt>



Téléphone de l’orateur.


</dt> </dl> </dd> <dt>

<span id="CLSID_SpeakersTerminal"></span><span id="clsid_speakersterminal"></span><span id="CLSID_SPEAKERSTERMINAL"></span>**CLSID \_ SpeakersTerminal**
</dt> <dd> <dl> <dt>



Intervenants.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoInputTerminal"></span><span id="clsid_videoinputterminal"></span><span id="CLSID_VIDEOINPUTTERMINAL"></span>**CLSID \_ VideoInputTerminal**
</dt> <dd> <dl> <dt>



Terminal d’entrée vidéo.


</dt> </dl> </dd> <dt>

<span id="CLSID_VideoWindowTerm"></span><span id="clsid_videowindowterm"></span><span id="CLSID_VIDEOWINDOWTERM"></span>**CLSID \_ VideoWindowTerm**
</dt> <dd> <dl> <dt>



Fenêtre d’affichage vidéo, créée dynamiquement.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

la version **BSTR** des classes de terminal est principalement désignée pour l’utilisation d’applications Visual Basic. (Par exemple, ils sont retournés en tant qu’éléments de la collection obtenue avec l' [**obtention de \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses).)

-   Chaîne CLSID de BSTR \_ \_ HandsetTerminal
-   Chaîne CLSID de BSTR \_ \_ HeadsetTerminal
-   Chaîne CLSID de BSTR \_ \_ MediaStreamTerminal
-   Chaîne CLSID de BSTR \_ \_ MicrophoneTerminal
-   Chaîne CLSID de BSTR \_ \_ SpeakerphoneTerminal
-   Chaîne CLSID de BSTR \_ \_ SpeakersTerminal
-   Chaîne CLSID de BSTR \_ \_ VideoInputTerminal
-   Chaîne CLSID de BSTR \_ \_ VideoWindowTerm

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|--------------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 3,0 ou une version ultérieure<br/>                                                |
| En-tête<br/>       | <dl> <dt>Tapi3if. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal)
</dt> <dt>

[**ITTerminal :: obtient \_ TerminalClass**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_terminalclass)
</dt> <dt>

[**ITTerminalManager::CreateDynamicTerminal**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-createdynamicterminal)
</dt> <dt>

[**ITTerminalManager::GetDynamicTerminalClasses**](/windows/desktop/api/Termmgr/nf-termmgr-itterminalmanager-getdynamicterminalclasses)
</dt> <dt>

[**ITTerminalSupport::EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses)
</dt> </dl>

 

