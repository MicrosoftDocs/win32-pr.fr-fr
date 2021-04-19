---
description: Les \_ GUID DEVINTERFACE xxx sont utilisés pour représenter les GUID pour les interfaces de périphérique.
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: GUID de DEVINTERFACE_XXX (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796f113d26ebc351a4d576ed76485d24d89fdb04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544463"
---
# <a name="devinterface_xxx-guids"></a><span data-ttu-id="413f2-103">\_GUID DEVINTERFACE xxx</span><span class="sxs-lookup"><span data-stu-id="413f2-103">DEVINTERFACE\_XXX GUIDs</span></span>

<span data-ttu-id="413f2-104">Les \_ GUID DEVINTERFACE xxx sont utilisés pour représenter les GUID pour les interfaces de périphérique.</span><span class="sxs-lookup"><span data-stu-id="413f2-104">The DEVINTERFACE\_XXX GUIDs are used to represent the GUIDs for device interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="413f2-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**\_capture audio \_ DEVINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="413f2-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**DEVINTERFACE\_AUDIO\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="413f2-106">Spécifie la chaîne de requête utilisée pour énumérer tous les périphériques de capture audio sur le système.</span><span class="sxs-lookup"><span data-stu-id="413f2-106">Specifies the query string used to enumerate all audio capture devices on the system.</span></span> <span data-ttu-id="413f2-107">Cette valeur est retournée par [**MediaDevice :: GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).</span><span class="sxs-lookup"><span data-stu-id="413f2-107">This value is returned by [**MediaDevice::GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).</span></span>

<span data-ttu-id="413f2-108">Le passage de cette valeur à [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) active l’interface demandée sur le périphérique de capture audio par défaut.</span><span class="sxs-lookup"><span data-stu-id="413f2-108">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio capture device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="413f2-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**\_rendu audio \_ DEVINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="413f2-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**DEVINTERFACE\_AUDIO\_RENDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="413f2-110">Spécifie la chaîne de requête utilisée pour énumérer tous les périphériques de rendu audio sur le système.</span><span class="sxs-lookup"><span data-stu-id="413f2-110">Specifies the query string used to enumerate all audio render devices on the system.</span></span> <span data-ttu-id="413f2-111">Cette valeur est retournée par [**MediaDevice :: GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).</span><span class="sxs-lookup"><span data-stu-id="413f2-111">This value is returned by [**MediaDevice::GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).</span></span>

<span data-ttu-id="413f2-112">Le passage de cette valeur à [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) active l’interface demandée sur le périphérique de rendu audio par défaut.</span><span class="sxs-lookup"><span data-stu-id="413f2-112">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio render device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="413f2-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**\_entrée MIDI \_ DEVINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="413f2-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**DEVINTERFACE\_MIDI\_INPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="413f2-114">Spécifie la chaîne de requête utilisée pour énumérer tous les objets [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) sur le système.</span><span class="sxs-lookup"><span data-stu-id="413f2-114">Specifies the query string used to enumerate all [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) objects on the system.</span></span> <span data-ttu-id="413f2-115">Cette valeur est retournée par [**MidiInPort :: GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).</span><span class="sxs-lookup"><span data-stu-id="413f2-115">This value is returned by [**MidiInPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="413f2-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**\_sortie MIDI \_ DEVINTERFACE**</span><span class="sxs-lookup"><span data-stu-id="413f2-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**DEVINTERFACE\_MIDI\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="413f2-117">Spécifie la chaîne de requête utilisée pour énumérer tous les objets [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) sur le système.</span><span class="sxs-lookup"><span data-stu-id="413f2-117">Specifies the query string used to enumerate all [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) objects on the system.</span></span> <span data-ttu-id="413f2-118">Cette valeur est retournée par [**MidiOutPort :: GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).</span><span class="sxs-lookup"><span data-stu-id="413f2-118">This value is returned by [**MidiOutPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="413f2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="413f2-119">Requirements</span></span>



| <span data-ttu-id="413f2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="413f2-120">Requirement</span></span> | <span data-ttu-id="413f2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="413f2-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="413f2-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="413f2-122">Header</span></span><br/> | <dl> <span data-ttu-id="413f2-123"><dt>MMDeviceAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="413f2-123"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



 

