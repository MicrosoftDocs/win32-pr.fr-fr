---
description: Les \_ GUID DEVINTERFACE xxx sont utilisés pour représenter les GUID pour les interfaces de périphérique.
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: GUID de DEVINTERFACE_XXX (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796f113d26ebc351a4d576ed76485d24d89fdb04
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114978"
---
# <a name="devinterface_xxx-guids"></a>\_GUID DEVINTERFACE xxx

Les \_ GUID DEVINTERFACE xxx sont utilisés pour représenter les GUID pour les interfaces de périphérique.

<dl> <dt>

<span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**\_capture audio \_ DEVINTERFACE**
</dt> <dd> <dl> <dt>



Spécifie la chaîne de requête utilisée pour énumérer tous les périphériques de capture audio sur le système. Cette valeur est retournée par [**MediaDevice :: GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).

Le passage de cette valeur à [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) active l’interface demandée sur le périphérique de capture audio par défaut.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**\_rendu audio \_ DEVINTERFACE**
</dt> <dd> <dl> <dt>



Spécifie la chaîne de requête utilisée pour énumérer tous les périphériques de rendu audio sur le système. Cette valeur est retournée par [**MediaDevice :: GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).

Le passage de cette valeur à [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) active l’interface demandée sur le périphérique de rendu audio par défaut.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**\_entrée MIDI \_ DEVINTERFACE**
</dt> <dd> <dl> <dt>



Spécifie la chaîne de requête utilisée pour énumérer tous les objets [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) sur le système. Cette valeur est retournée par [**MidiInPort :: GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**\_sortie MIDI \_ DEVINTERFACE**
</dt> <dd> <dl> <dt>



Spécifie la chaîne de requête utilisée pour énumérer tous les objets [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) sur le système. Cette valeur est retournée par [**MidiOutPort :: GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



 

