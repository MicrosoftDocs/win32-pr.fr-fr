---
description: Structures audio principales
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Structures audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078f49ac7abce8fc2773549df26431b780550c1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513301"
---
# <a name="core-audio-structures"></a><span data-ttu-id="15138-103">Structures audio principales</span><span class="sxs-lookup"><span data-stu-id="15138-103">Core Audio Structures</span></span>

<span data-ttu-id="15138-104">Cette section décrit les structures utilisées par les API audio principales dans Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="15138-104">This section describes the structures that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="15138-105">Structure</span><span class="sxs-lookup"><span data-stu-id="15138-105">Structure</span></span>                                                                     | <span data-ttu-id="15138-106">Description</span><span class="sxs-lookup"><span data-stu-id="15138-106">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15138-107">**\_données de \_ notification du volume audio \_**</span><span class="sxs-lookup"><span data-stu-id="15138-107">**AUDIO\_VOLUME\_NOTIFICATION\_DATA**</span></span>](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | <span data-ttu-id="15138-108">Décrit une modification du niveau de volume ou de l’État muet d’un périphérique de point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="15138-108">Describes a change in the volume level or muting state of an audio endpoint device.</span></span>                                                                                 |
| [<span data-ttu-id="15138-109">**paramètres d’activation de DIRECTX \_ audio \_ \_**</span><span class="sxs-lookup"><span data-stu-id="15138-109">**DIRECTX\_AUDIO\_ACTIVATION\_PARAMS**</span></span>](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | <span data-ttu-id="15138-110">Spécifie les paramètres d’initialisation d’un flux DirectSound.</span><span class="sxs-lookup"><span data-stu-id="15138-110">Specifies the initialization parameters for a DirectSound stream.</span></span>                                                                                                   |
| [<span data-ttu-id="15138-111">**Description de KSJACK \_**</span><span class="sxs-lookup"><span data-stu-id="15138-111">**KSJACK\_DESCRIPTION**</span></span>](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | <span data-ttu-id="15138-112">Récupéré par le biais de [**IKsJackDescription :: GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); décrit une prise jack audio.</span><span class="sxs-lookup"><span data-stu-id="15138-112">Retrieved through [**IKsJackDescription::GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); describes an audio jack.</span></span>                                 |
| [<span data-ttu-id="15138-113">**KSJACK \_ Description2**</span><span class="sxs-lookup"><span data-stu-id="15138-113">**KSJACK\_DESCRIPTION2**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | <span data-ttu-id="15138-114">Récupéré par le biais de [**IKsJackDescription2 :: GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); décrit une prise jack audio.</span><span class="sxs-lookup"><span data-stu-id="15138-114">Retrieved through [**IKsJackDescription2::GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); describes an audio jack.</span></span> <br/>                 |
| [<span data-ttu-id="15138-115">**\_informations sur le récepteur KSJACK \_**</span><span class="sxs-lookup"><span data-stu-id="15138-115">**KSJACK\_SINK\_INFORMATION**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | <span data-ttu-id="15138-116">Récupéré par le biais de [**IKsJackSinkInformation :: GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); décrit un récepteur Jack audio.</span><span class="sxs-lookup"><span data-stu-id="15138-116">Retrieved through [**IKsJackSinkInformation::GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); describes an audio jack sink.</span></span><br/> |
| [<span data-ttu-id="15138-117">**LUID**</span><span class="sxs-lookup"><span data-stu-id="15138-117">**LUID**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | <span data-ttu-id="15138-118">Stocke l’identificateur de port vidéo.</span><span class="sxs-lookup"><span data-stu-id="15138-118">Stores the video port identifier.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="15138-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15138-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15138-120">Guide de référence de programmation</span><span class="sxs-lookup"><span data-stu-id="15138-120">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




