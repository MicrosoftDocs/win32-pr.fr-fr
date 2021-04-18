---
description: 'Il existe trois types d’objets vocaux XAudio2 : les voix source, de mixage secondaire et de mastérisation.'
ms.assetid: 3a4acc03-e47a-ff33-dee8-a374051f85f6
title: Voix XAudio2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b11300cea770f59485e8a78b0d30110b5469befe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520157"
---
# <a name="xaudio2-voices"></a><span data-ttu-id="99f4b-103">Voix XAudio2</span><span class="sxs-lookup"><span data-stu-id="99f4b-103">XAudio2 Voices</span></span>

<span data-ttu-id="99f4b-104">Il existe trois types d’objets vocaux XAudio2 : les voix *source*, de *mixage secondaire* et de *mastérisation* .</span><span class="sxs-lookup"><span data-stu-id="99f4b-104">There are three types of XAudio2 voice objects: *source*, *submix*, and *mastering* voices.</span></span> <span data-ttu-id="99f4b-105">Les voix source opèrent sur les données audio fournies par le client.</span><span class="sxs-lookup"><span data-stu-id="99f4b-105">Source voices operate on audio data provided by the client.</span></span> <span data-ttu-id="99f4b-106">Les voix source et sous-mixées envoient leur sortie vers une ou plusieurs voix sous-mixées ou de matriçage.</span><span class="sxs-lookup"><span data-stu-id="99f4b-106">Source and submix voices send their output to one or more submix or mastering voices.</span></span> <span data-ttu-id="99f4b-107">Les voix sous-mixées et de matriçage mixent les signaux provenant de toutes les voix qui les alimentent et opèrent sur le résultat.</span><span class="sxs-lookup"><span data-stu-id="99f4b-107">Submix and mastering voices mix the audio from all voices feeding them, and operate on the result.</span></span> <span data-ttu-id="99f4b-108">Les voix de matriçage écrivent des données audio sur un périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="99f4b-108">Mastering voices write audio data to an audio device.</span></span>

## <a name="actions-performed-by-all-voices"></a><span data-ttu-id="99f4b-109">Actions effectuées par toutes les voix</span><span class="sxs-lookup"><span data-stu-id="99f4b-109">Actions Performed by All Voices</span></span>

<span data-ttu-id="99f4b-110">Toutes les voix effectuent les actions suivantes dans l’ordre audio qui les traverse.</span><span class="sxs-lookup"><span data-stu-id="99f4b-110">All voices perform the following actions in order on the audio that travels though them.</span></span>

1.  <span data-ttu-id="99f4b-111">Réglage global du volume, affectant tous les canaux audio.</span><span class="sxs-lookup"><span data-stu-id="99f4b-111">Overall volume adjustment, affecting all audio channels.</span></span> <span data-ttu-id="99f4b-112">Consultez [**IXAudio2Voice :: setVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span><span class="sxs-lookup"><span data-stu-id="99f4b-112">See [**IXAudio2Voice::SetVolume**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setvolume).</span></span>
2.  <span data-ttu-id="99f4b-113">Chaîne facultative spécifiée par le client d’un ou de plusieurs effets DSP, comme le verbe intégré ou l’effet utilisateur défini par l’interface [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) .</span><span class="sxs-lookup"><span data-stu-id="99f4b-113">An optional client-specified chain of one or more DSP effects, such as the built-in reverb or a user effect defined by the [**IXAPO**](/windows/desktop/api/XAPO/nn-xapo-ixapo) interface.</span></span> <span data-ttu-id="99f4b-114">Consultez [effets audio XAudio2](xaudio2-audio-effects.md).</span><span class="sxs-lookup"><span data-stu-id="99f4b-114">See [XAudio2 Audio Effects](xaudio2-audio-effects.md).</span></span>
3.  <span data-ttu-id="99f4b-115">Réglage du volume de sortie par canal.</span><span class="sxs-lookup"><span data-stu-id="99f4b-115">Per-channel output volume adjustment.</span></span> <span data-ttu-id="99f4b-116">Consultez [**IXAudio2Voice :: SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span><span class="sxs-lookup"><span data-stu-id="99f4b-116">See [**IXAudio2Voice::SetChannelVolumes**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setchannelvolumes).</span></span>
4.  <span data-ttu-id="99f4b-117">Mélange de matrices distincts à chacune des voix de destination ou à l’appareil de sortie audio pour la maîtrise des voix.</span><span class="sxs-lookup"><span data-stu-id="99f4b-117">Separate matrix mix to each of the destination voices or to the audio output device for mastering voices.</span></span> <span data-ttu-id="99f4b-118">Cette combinaison modifie le nombre de canaux dans l’audio, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="99f4b-118">This mix changes the number of channels in the audio, if necessary.</span></span>

## <a name="source-voices"></a><span data-ttu-id="99f4b-119">Voix source</span><span class="sxs-lookup"><span data-stu-id="99f4b-119">Source Voices</span></span>

<span data-ttu-id="99f4b-120">Utilisez les voix source pour envoyer des données audio dans le pipeline de traitement XAudio2.</span><span class="sxs-lookup"><span data-stu-id="99f4b-120">Use source voices to submit audio data into the XAudio2 processing pipeline.</span></span> <span data-ttu-id="99f4b-121">Il s’agit des points d’entrée dans le [graphique audio XAudio2](xaudio2-audio-graph.md).</span><span class="sxs-lookup"><span data-stu-id="99f4b-121">They are the entry points into the [XAudio2 Audio Graph](xaudio2-audio-graph.md).</span></span> <span data-ttu-id="99f4b-122">Vous devez envoyer des données vocales à une voix de mastérisation pour être entendues, soit directement, soit par le biais de voix de mixage secondaire intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="99f4b-122">You must send voice data to a mastering voice to be heard, either directly or through intermediate submix voices.</span></span>

<span data-ttu-id="99f4b-123">En plus des actions effectuées par toutes les voix, les voix source effectuent les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="99f4b-123">In addition to the actions performed by all voices, source voices perform the following actions.</span></span>

-   <span data-ttu-id="99f4b-124">Si nécessaire, un décodeur s’exécute en premier pour convertir les données sources encodées en PCM (Pulse Code Modulation).</span><span class="sxs-lookup"><span data-stu-id="99f4b-124">If necessary, a decoder runs first to convert encoded source data to Pulse Code Modulation (PCM).</span></span>
-   <span data-ttu-id="99f4b-125">Une conversion de taux d’échantillonnage à taux variable (SRC) convertit les données audio sources de la voix en taux d’échantillonnage attendu par ses voix de destination, si nécessaire, et prend également en charge les changements de pas dynamique.</span><span class="sxs-lookup"><span data-stu-id="99f4b-125">A variable-rate sample rate conversion (SRC) converts the voice's source audio data to the sample rate expected by its destination voices, if necessary, and also supports dynamic pitch changes.</span></span>
-   <span data-ttu-id="99f4b-126">Un filtre de variable d’État facultatif peut être utilisé pour colorer le son de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="99f4b-126">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="99f4b-127">Consultez [**IXAudio2Voice :: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="99f4b-127">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="99f4b-128">Un filtre facultatif peut être appliqué aux sorties de la voix.</span><span class="sxs-lookup"><span data-stu-id="99f4b-128">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="99f4b-129">Consultez [**IXAudio2Voice :: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="99f4b-129">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="submix-voices"></a><span data-ttu-id="99f4b-130">Voix de mixage secondaire</span><span class="sxs-lookup"><span data-stu-id="99f4b-130">Submix Voices</span></span>

<span data-ttu-id="99f4b-131">Une voix de mixage secondaire est principalement utilisée pour améliorer les performances et le traitement des effets.</span><span class="sxs-lookup"><span data-stu-id="99f4b-131">A submix voice is used primarily for performance improvements and effects processing.</span></span> <span data-ttu-id="99f4b-132">Vous ne pouvez pas envoyer directement des tampons de données à des voix de mixage secondaire.</span><span class="sxs-lookup"><span data-stu-id="99f4b-132">You cannot submit data buffers directly to submix voices.</span></span> <span data-ttu-id="99f4b-133">Il ne sera pas audible, sauf si vous le soumettez à une voix de mastérisation.</span><span class="sxs-lookup"><span data-stu-id="99f4b-133">It will not be audible unless you submit it to a mastering voice.</span></span> <span data-ttu-id="99f4b-134">Vous pouvez utiliser une voix de mixage secondaire pour vous assurer qu’un ensemble particulier de données vocales est converti au même format et qu’une chaîne d’effet particulière est traitée sur le résultat collectif.</span><span class="sxs-lookup"><span data-stu-id="99f4b-134">You can use a submix voice to ensure that a particular set of voice data is converted to the same format and to have a particular effect chain processed on the collective result.</span></span>

<span data-ttu-id="99f4b-135">En plus des actions effectuées par toutes les voix, les voix de mixage secondaire effectuent les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="99f4b-135">In addition to the actions performed by all voices, submix voices perform the following actions.</span></span>

-   <span data-ttu-id="99f4b-136">Un SRC à débit fixe s’exécute sur la sortie de la voix, si nécessaire, pour convertir l’audio en taux d’échantillonnage attendu par ses voix de destination.</span><span class="sxs-lookup"><span data-stu-id="99f4b-136">A fixed-rate SRC runs on the voice's output, if necessary, to convert the audio to the sample rate expected by its destination voices.</span></span>
-   <span data-ttu-id="99f4b-137">Un filtre de variable d’État facultatif peut être utilisé pour colorer le son de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="99f4b-137">An optional state-variable filter can be used to color the sound in various ways.</span></span> <span data-ttu-id="99f4b-138">Consultez [**IXAudio2Voice :: SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="99f4b-138">See [**IXAudio2Voice::SetFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setfilterparameters).</span></span>
-   <span data-ttu-id="99f4b-139">Un filtre facultatif peut être appliqué aux sorties de la voix.</span><span class="sxs-lookup"><span data-stu-id="99f4b-139">An optional filter can be applied to the voice's outputs.</span></span> <span data-ttu-id="99f4b-140">Consultez [**IXAudio2Voice :: SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span><span class="sxs-lookup"><span data-stu-id="99f4b-140">See [**IXAudio2Voice::SetOutputFilterParameters**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputfilterparameters).</span></span>

## <a name="mastering-voices"></a><span data-ttu-id="99f4b-141">Mastérisation des voix</span><span class="sxs-lookup"><span data-stu-id="99f4b-141">Mastering Voices</span></span>

<span data-ttu-id="99f4b-142">Utilisez une voix de mastérisation pour représenter l’appareil de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="99f4b-142">Use a mastering voice to represent the audio output device.</span></span> <span data-ttu-id="99f4b-143">Vous ne pouvez pas envoyer de tampons de données directement à des voix de mastérisation, mais les données soumises à d’autres types de voix doivent être envoyées à une voix de mastérisation.</span><span class="sxs-lookup"><span data-stu-id="99f4b-143">You cannot submit data buffers directly to mastering voices, but data submitted to other types of voices must go to a mastering voice to be heard.</span></span>

<span data-ttu-id="99f4b-144">En plus des actions effectuées par toutes les voix, les voix de mastérisation effectuent les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="99f4b-144">In addition to the actions performed by all voices, mastering voices perform the following actions.</span></span>

-   <span data-ttu-id="99f4b-145">Si vous créez la voix de mastérisation avec une valeur *InputSampleRate* explicite qui n’est pas prise en charge par le périphérique audio, un SRC à débit fixe est utilisé pour convertir le taux d’échantillonnage le plus proche pris en charge par l’appareil.</span><span class="sxs-lookup"><span data-stu-id="99f4b-145">If you create the mastering voice with an explicit *InputSampleRate* value that is not supported by the audio device, a fixed-rate SRC is used to convert to the closest sample rate supported by the device.</span></span>
-   <span data-ttu-id="99f4b-146">Découpez la sortie audio finale, si elle est requise par le périphérique de sortie.</span><span class="sxs-lookup"><span data-stu-id="99f4b-146">Clip the final output audio, if it is required by the output device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="99f4b-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99f4b-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99f4b-148">Voix</span><span class="sxs-lookup"><span data-stu-id="99f4b-148">Voices</span></span>](voices.md)
</dt> <dt>

[<span data-ttu-id="99f4b-149">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="99f4b-149">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="99f4b-150">**IXAudio2SourceVoice**</span><span class="sxs-lookup"><span data-stu-id="99f4b-150">**IXAudio2SourceVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)
</dt> <dt>

[<span data-ttu-id="99f4b-151">**IXAudio2SubmixVoice**</span><span class="sxs-lookup"><span data-stu-id="99f4b-151">**IXAudio2SubmixVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)
</dt> <dt>

[<span data-ttu-id="99f4b-152">**IXAudio2MasteringVoice**</span><span class="sxs-lookup"><span data-stu-id="99f4b-152">**IXAudio2MasteringVoice**</span></span>](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)
</dt> </dl>

 

 
