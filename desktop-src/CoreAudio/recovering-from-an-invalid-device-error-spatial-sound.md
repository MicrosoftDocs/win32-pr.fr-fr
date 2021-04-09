---
description: Récupération à partir d’une erreur de Invalid-Device (son spatial)
title: Récupération à partir d’une erreur de Invalid-Device (son spatial)
ms.topic: article
ms.date: 10/29/2020
ms.openlocfilehash: 1ec4f040aff10f2d118b20c489e74d792c907113
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111307"
---
# <a name="recovering-from-an-invalid-device-error-spatial-sound"></a><span data-ttu-id="9b217-103">Récupération à partir d’une erreur de Invalid-Device (son spatial)</span><span class="sxs-lookup"><span data-stu-id="9b217-103">Recovering from an Invalid-Device Error (Spatial Sound)</span></span>

<span data-ttu-id="9b217-104">La plupart des méthodes de l’API Microsoft spatiale audio, telles que [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)et [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), renvoient des codes d’erreur si l’appareil de point de terminaison audio utilisé par l’application cliente n’est pas valide ou si le format de rendu audio spatial est modifié sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="9b217-104">Many of the methods of the Microsoft Spatial Audio API, such as [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream), and [ISpatialAudioObject](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject), return error codes if the audio endpoint device that the client application is using becomes invalid or the spatial audio rendering format is changed on the endpoint.</span></span> <span data-ttu-id="9b217-105">Ces codes d’erreur indiquent que l’appareil de point de terminaison a été débranché, ou que le matériel audio ou les ressources matérielles associées ont été reconfigurés, désactivés, supprimés, que le mode audio spatial est modifié ou qu’il n’est pas possible de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="9b217-105">These error codes indicates that the endpoint device has been unplugged, or that the audio hardware or associated hardware resources have been reconfigured, disabled, removed, spatial audio mode is changed or otherwise made unavailable for use.</span></span> <span data-ttu-id="9b217-106">Souvent, l’application peut récupérer à partir de cette erreur.</span><span class="sxs-lookup"><span data-stu-id="9b217-106">Frequently, the application can recover from this error.</span></span>

<span data-ttu-id="9b217-107">Les codes d’erreur qui indiquent une erreur de périphérique non valide sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="9b217-107">Error codes that indicate an invalid-device error include the following:</span></span>

- <span data-ttu-id="9b217-108">SPTLAUDCLNT_E_DESTROYED</span><span class="sxs-lookup"><span data-stu-id="9b217-108">SPTLAUDCLNT_E_DESTROYED</span></span>
- <span data-ttu-id="9b217-109">AUDCLNT_E_DEVICE_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="9b217-109">AUDCLNT_E_DEVICE_INVALIDATED</span></span>
- <span data-ttu-id="9b217-110">AUDCLNT_E_RESOURCES_INVALIDATED</span><span class="sxs-lookup"><span data-stu-id="9b217-110">AUDCLNT_E_RESOURCES_INVALIDATED</span></span>
- <span data-ttu-id="9b217-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span><span class="sxs-lookup"><span data-stu-id="9b217-111">AUDCLNT_E_UNSUPPORTED_FORMAT</span></span>
- <span data-ttu-id="9b217-112">SPTLAUDCLNT_E_INTERNAL</span><span class="sxs-lookup"><span data-stu-id="9b217-112">SPTLAUDCLNT_E_INTERNAL</span></span>

## <a name="strategies-for-handling-invalid-device-errors"></a><span data-ttu-id="9b217-113">Stratégies de gestion des erreurs de périphérique non valide</span><span class="sxs-lookup"><span data-stu-id="9b217-113">Strategies for handling invalid-device errors</span></span>

<span data-ttu-id="9b217-114">La stratégie recommandée pour la récupération à partir d’une erreur d’appareil non valide varie selon que l’application sélectionne automatiquement un appareil spécifique en fonction des exigences internes ou qu’il permet à l’utilisateur de sélectionner explicitement un appareil dans une liste d’appareils disponibles.</span><span class="sxs-lookup"><span data-stu-id="9b217-114">The recommended strategy for recovering from an invalid-device error depends on whether the application automatically selects a specific device based on internal requirements or it allows the user to explicitly select a device from a list of available devices.</span></span> 

### <a name="default-audio-device"></a><span data-ttu-id="9b217-115">Périphérique audio par défaut</span><span class="sxs-lookup"><span data-stu-id="9b217-115">Default audio device</span></span>

<span data-ttu-id="9b217-116">Si l’application sélectionne automatiquement l’appareil par défaut, procédez comme suit pour effectuer la récupération.</span><span class="sxs-lookup"><span data-stu-id="9b217-116">If the application automatically selects the default device, use the following steps to recover.</span></span>

1. <span data-ttu-id="9b217-117">Libérez l’interface [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) et [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) et toutes les autres interfaces audio spatiales utilisées pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="9b217-117">Release the [ISpatialAudioObjectRenderStream](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream) and [ISpatialAudioClient](/windows/win32/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) interface and any other spatial audio interfaces that are used for rendering.</span></span> 
1. <span data-ttu-id="9b217-118">Appelez [IMMDeviceEnumerator :: GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) pour récupérer le périphérique audio par défaut actuel.</span><span class="sxs-lookup"><span data-stu-id="9b217-118">Call [IMMDeviceEnumerator::GetDefaultAudioEndpoint](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) to get the current default audio device.</span></span>
1. <span data-ttu-id="9b217-119">Essayez d’activer **ISpatialAudioClient** sur le périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="9b217-119">Attempt to activate **ISpatialAudioClient** on the audio device.</span></span>
1. <span data-ttu-id="9b217-120">Activez **ISpatialAudioObjectRenderStream**.</span><span class="sxs-lookup"><span data-stu-id="9b217-120">Activate **ISpatialAudioObjectRenderStream**.</span></span> 

### <a name="specifically-selected-audio-device"></a><span data-ttu-id="9b217-121">Périphérique audio spécifiquement sélectionné</span><span class="sxs-lookup"><span data-stu-id="9b217-121">Specifically selected audio device</span></span>

<span data-ttu-id="9b217-122">Si l’application sélectionne un périphérique audio spécifique, procédez comme suit pour effectuer la récupération.</span><span class="sxs-lookup"><span data-stu-id="9b217-122">If the application selects a specific audio device, use the following steps to recover.</span></span>

1. <span data-ttu-id="9b217-123">Libérez l’interface ISpatialAudioObjectRenderStream et toutes les autres interfaces audio spatiales utilisées pour le rendu, mais ne libérez pas **ISpatialAudioClient**.</span><span class="sxs-lookup"><span data-stu-id="9b217-123">Release the ISpatialAudioObjectRenderStream interface and any other spatial audio interfaces that are used for rendering, but don't release **ISpatialAudioClient**.</span></span>
1. <span data-ttu-id="9b217-124">Utilisez l’instance **ISpatialAudioClient** actuelle pour activer **ISpatialAudioObjectRenderStream**.</span><span class="sxs-lookup"><span data-stu-id="9b217-124">Use the current **ISpatialAudioClient** instance to activate **ISpatialAudioObjectRenderStream**.</span></span>

<span data-ttu-id="9b217-125">Notez que pour les deux stratégies mentionnées ci-dessus, les mêmes étapes peuvent être appliquées aux applications qui utilisent les interfaces [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) ou [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) .</span><span class="sxs-lookup"><span data-stu-id="9b217-125">Note that for both strategies listed above, the same steps can be applied to applications that use the [ISpatialAudioObjectRenderStreamForMetadata](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudioobjectrenderstreamformetadata) or [ISpatialAudioObjectRenderStreamForHrtf](/windows/win32/api/spatialaudiohrtf/nn-spatialaudiohrtf-ispatialaudioobjectrenderstreamforhrtf) interfaces.</span></span> <span data-ttu-id="9b217-126">Remplacez simplement **ISpatialAudioObjectRenderStream** dans les étapes ci-dessus par les interfaces de métadonnées ou HRTF.</span><span class="sxs-lookup"><span data-stu-id="9b217-126">Simply replace **ISpatialAudioObjectRenderStream** in the above steps with the metadata or Hrtf interfaces.</span></span>


## <a name="related-topics"></a><span data-ttu-id="9b217-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9b217-127">Related topics</span></span>

<dl> <span data-ttu-id="9b217-128"><dt>
[Récupération à partir d’une erreur Invalid-Device](recovering-from-an-invalid-device-error.md) 
 [Gestion de flux](stream-management.md)
</dt> </span><span class="sxs-lookup"><span data-stu-id="9b217-128"><dt>
[Recovering from an Invalid-Device Error](recovering-from-an-invalid-device-error.md)
[Stream Management](stream-management.md)
</dt> </span></span></dl>

 

 



