---
description: Spécifie les caractéristiques qu’un client peut assigner à un flux audio pendant l’initialisation du flux.
ms.assetid: 7b2267c3-79f5-4ada-a7ce-78dd514f8487
title: Constantes AUDCLNT_STREAMFLAGS_XXX (Audiosessiontypes. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65faf887c35b4ce1110cecb7d7509eb3dfda1d57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115106"
---
# <a name="audclnt_streamflags_xxx-constants"></a>AUDCLNT \_ STREAMFLAGS \_ xxx, constantes

Spécifie les caractéristiques qu’un client peut assigner à un flux audio pendant l’initialisation du flux.



| Constante/valeur                                                                                                                                                                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AUDCLNT_STREAMFLAGS_CROSSPROCESS"></span><span id="audclnt_streamflags_crossprocess"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ CROSSPROCESS**</dt> <dt>0x00010000</dt> </dl>                                       | Le flux audio sera membre d’une session audio interprocessus. Pour plus d'informations, consultez la section Notes.<br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_LOOPBACK"></span><span id="audclnt_streamflags_loopback"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS de \_ bouclage**</dt> <dt>0x00020000</dt> </dl>                                                   | Le flux audio fonctionne en mode de bouclage. Pour plus d'informations, consultez la section Notes.<br/>                                                                                                                                                                                                                                                      |
| <span id="AUDCLNT_STREAMFLAGS_EVENTCALLBACK"></span><span id="audclnt_streamflags_eventcallback"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ EventCallback suivante**</dt> <dt>0x00040000</dt> </dl>                                    | Le traitement de la mémoire tampon audio par le client est piloté par les événements. Pour plus d'informations, consultez la section Notes. <br/>                                                                                                                                                                                                                                  |
| <span id="AUDCLNT_STREAMFLAGS_NOPERSIST"></span><span id="audclnt_streamflags_nopersist"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ NoPersist**</dt> <dt>0x00080000</dt> </dl>                                                | Les paramètres de volume et de sourdine pour une session audio ne sont pas conservés au cours des redémarrages de l’application. Pour plus d'informations, consultez la section Notes.<br/>                                                                                                                                                                                                           |
| <span id="AUDCLNT_STREAMFLAGS_RATEADJUST"></span><span id="audclnt_streamflags_rateadjust"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ RATEADJUST**</dt> <dt>0x00100000</dt> </dl>                                             | cette constante est une nouveauté de Windows 7. Le taux d’échantillonnage du flux est ajusté à la fréquence spécifiée par une application. Pour plus d'informations, consultez la section Notes. <br/>                                                                                                                                                                                 |
| <span id="AUDCLNT_STREAMFLAGS_AUTOCONVERTPCM"></span><span id="audclnt_streamflags_autoconvertpcm"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM**</dt> <dt>0x80000000</dt> </dl>                                 | Une matrice de canaux et un exemple de convertisseur de taux sont insérés si nécessaire pour effectuer une conversion entre le format non compressé fourni à [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) et le format de combinaison de moteurs audio.<br/>                                                                                                            |
| <span id="AUDCLNT_STREAMFLAGS_SRC_DEFAULT_QUALITY"></span><span id="audclnt_streamflags_src_default_quality"></span><dl> <dt>**AUDCLNT \_ STREAMFLAGS \_ src \_ default \_ Quality**</dt> <dt>0x08000000</dt> </dl>                | Lorsqu’il est utilisé avec **AUDCLNT \_ STREAMFLAGS \_ AUTOCONVERTPCM**, un convertisseur de taux d’échantillonnage avec une meilleure qualité que la conversion par défaut, mais avec un coût de performances supérieur, est utilisé. Cette valeur doit être utilisée si l’audio est finalement destiné à être entendu par des humains, par opposition à d’autres scénarios tels que le silence de pompage ou le remplissage d’un compteur.<br/> |



## <a name="remarks"></a>Notes

La méthode [**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) et la structure [**des \_ \_ \_ paramètres d’activation audio DirectX**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) utilisent les \_ constantes AUDCLNT STREAMFLAGS \_ xxx.

L' \_ indicateur AUDCLNT STREAMFLAGS \_ CROSSPROCESS indique que la session audio du flux est une session inter-processus. Une session inter-processus peut accepter des flux issus de plusieurs processus. Si deux applications de deux processus distincts appellent **IAudioClient :: Initialize** avec des GUID de session identiques, et que les deux applications définissent l' \_ indicateur AUDCLNT SHAREMODE \_ CROSSPROCESS, le moteur audio affecte leurs flux à la même session inter-processus. Cet indicateur remplace le comportement par défaut, qui consiste à assigner le flux à une session spécifique au processus plutôt qu’à une session inter-processus. Le \_ \_ bit d’indicateur CROSSPROCESS AUDCLNT STREAMFLAGS est incompatible avec le mode exclusif. Pour plus d’informations sur les sessions inter-processus, consultez [sessions audio](audio-sessions.md).

L' \_ indicateur de bouclage AUDCLNT STREAMFLAGS active l’enregistrement de \_ bouclage. Dans l’enregistrement de bouclage, le moteur audio copie le flux audio qui est lu par un périphérique de point de terminaison de rendu dans une mémoire tampon de point de terminaison audio afin qu’un client [WASAPI](wasapi.md) puisse capturer le flux. Si cet indicateur est défini, la méthode **IAudioClient :: Initialize** tente d’ouvrir une mémoire tampon de capture sur le périphérique de rendu. Cet indicateur est valide uniquement pour un périphérique de rendu et uniquement si l’appel **Initialize** définit le paramètre *ShareMode* sur AUDCLNT \_ ShareMode \_ Shared. Dans le cas contraire, l’appel **Initialize** échoue. Si l’appel a échoué, le client peut appeler la méthode [**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) pour obtenir une interface [**IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient) sur le périphérique de rendu. Pour plus d’informations, consultez [enregistrement en boucle](loopback-recording.md).

L' \_ indicateur AUDCLNT STREAMFLAGS \_ EventCallback suivante active la mise en mémoire tampon pilotée par les événements. Si un client définit cet indicateur dans l’appel à **IAudioClient :: Initialize** qui initialise un flux, le client doit ensuite appeler la méthode [**IAudioClient :: SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle) pour fournir un handle d’événement pour le flux. Après le démarrage du flux, le moteur audio indique au handle d’événement qu’il doit notifier le client chaque fois qu’une mémoire tampon est prête à être traitée par le client. WASAPI prend en charge la mise en mémoire tampon pilotée par les événements pour les mémoires tampons de rendu et de capture. Les flux en mode partagé et en mode exclusif peuvent utiliser la mise en mémoire tampon pilotée par les événements. Pour obtenir un exemple de code qui utilise \_ l' \_ indicateur AUDCLNT STREAMFLAGS EventCallback suivante, consultez [flux en mode exclusif](exclusive-mode-streams.md).

L' \_ indicateur AUDCLNT STREAMFLAGS \_ nopersiste désactive la persistance des paramètres de volume et de sourdine pour une session qui contient des flux de rendu. Par défaut, le niveau de volume et l’état d’activation d’une session de rendu sont persistants entre les redémarrages d’application. Le niveau de volume et l’État muet d’une session de capture ne sont jamais persistants. Pour plus d’informations sur la persistance des paramètres de volume de session et de sourdine, consultez [sessions audio](audio-sessions.md).

L' \_ indicateur AUDCLNT STREAMFLAGS \_ RATEADJUST permet à une application d’obtenir une référence à l’interface [**IAudioClockAdjustment**](/windows/desktop/api/audioclient/nn-audioclient-iaudioclockadjustment) utilisée pour définir le taux d’échantillonnage du flux. Pour obtenir un pointeur vers ce interface, une application doit initialiser le client audio avec cet indicateur, puis appeler [**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice) en spécifiant l' **IID \_ IAudioClockAdjustment** identifier. Pour définir le nouveau taux d’échantillonnage, appelez [**IAudioClockAdjustment :: SetSampleRate**](/windows/desktop/api/audioclient/nf-audioclient-iaudioclockadjustment-setsamplerate). Cet indicateur n’est valide que pour un périphérique de rendu. Dans le cas contraire, l’appel de **GetService** échoue avec le code d’erreur AUDCLNT \_ E \_ type de point de terminaison incorrect \_ \_ . L’application doit également définir le paramètre *ShareMode* sur AUDCLNT \_ ShareMode \_ Shared pendant l’appel [**Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize) . **SetSampleRate** échoue si le client audio n’est pas en mode partagé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Audiosessiontypes. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes audio principales](core-audio-constants.md)
</dt> <dt>

[**Interface IAudioCaptureClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudiocaptureclient)
</dt> <dt>

[**IAudioClient :: GetService**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-getservice)
</dt> <dt>

[**IAudioClient :: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize)
</dt> <dt>

[**IAudioClient::SetEventHandle**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-seteventhandle)
</dt> </dl>

 

 




