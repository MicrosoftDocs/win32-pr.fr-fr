---
description: Le décodeur MP3 Windows Media décode les fichiers audio qui ont été encodés dans les formats suivants.
ms.assetid: 817bbc2d-b3d5-49b4-84e4-bc8dc232a8ea
title: Décodeur MP3 Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de9bc49b3422e48f5de15678946845e21e868fe5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542736"
---
# <a name="windows-media-mp3-decoder"></a><span data-ttu-id="2d7b9-103">Décodeur MP3 Windows Media</span><span class="sxs-lookup"><span data-stu-id="2d7b9-103">Windows Media MP3 Decoder</span></span>

<span data-ttu-id="2d7b9-104">Le décodeur MP3 Windows Media décode les fichiers audio qui ont été encodés dans les formats suivants.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-104">The Windows Media MP3 decoder decodes audio files that have been encoded in the following formats.</span></span>

-   <span data-ttu-id="2d7b9-105">ISO/IEC 11172-3 (MPEG-1 audio) couche 3</span><span class="sxs-lookup"><span data-stu-id="2d7b9-105">ISO/IEC 11172-3 (MPEG-1 Audio) Layer 3</span></span>
-   <span data-ttu-id="2d7b9-106">ISO/IEC 13818-3 (MPEG-2 audio) couche 3, extension de fréquence d’échantillonnage faible</span><span class="sxs-lookup"><span data-stu-id="2d7b9-106">ISO/IEC 13818-3 (MPEG-2 Audio) Layer 3, low sampling frequency extension</span></span>

## <a name="class-identifier"></a><span data-ttu-id="2d7b9-107">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="2d7b9-107">Class Identifier</span></span>

<span data-ttu-id="2d7b9-108">L’identificateur de classe (CLSID) du décodeur MP3 Windows Media est représenté par la constante **CLSID \_ CMP3DecMediaObject**.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-108">The class identifier (CLSID) for the Windows Media MP3 decoder is represented by the constant **CLSID\_CMP3DecMediaObject**.</span></span> <span data-ttu-id="2d7b9-109">Vous pouvez créer une instance du décodeur MP3 en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-109">You can create an instance of the MP3 decoder by calling **CoCreateInstance**.</span></span>

## <a name="interfaces"></a><span data-ttu-id="2d7b9-110">Interfaces</span><span class="sxs-lookup"><span data-stu-id="2d7b9-110">Interfaces</span></span>

<span data-ttu-id="2d7b9-111">Un objet décodeur MP3 expose l’interface **IMediaObject** afin que l’objet puisse être utilisé en tant qu’objet de média DirectX (DMO) et expose l’interface **IMFTransform** afin que l’objet puisse être utilisé en tant que transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="2d7b9-111">An MP3 decoder object exposes the **IMediaObject** interface so that the object can be used as a DirectX Media Object (DMO), and it exposes the **IMFTransform** interface so that the object can be used as a Media Foundation Transform (MFT).</span></span>

<span data-ttu-id="2d7b9-112">Un décodeur MP3 Windows Media se comporte comme un DMO ou une table MFT en fonction des interfaces que vous obtenez et de la version de Windows en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-112">A Windows Media MP3 decoder behaves as a DMO or an MFT depending on which interfaces you obtain and which version of Windows is running.</span></span> <span data-ttu-id="2d7b9-113">Le tableau suivant indique les conditions sous lesquelles un décodeur MP3 Windows Media se comporte comme un DMO ou une table MFT.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-113">The following table shows the conditions under which a Windows Media MP3 decoder behaves as a DMO or an MFT.</span></span>



| <span data-ttu-id="2d7b9-114">Système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="2d7b9-114">Operating system</span></span> | <span data-ttu-id="2d7b9-115">Comportement du décodeur</span><span class="sxs-lookup"><span data-stu-id="2d7b9-115">Decoder behavior</span></span>                                                                                                                                                                               |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d7b9-116">Windows XP</span><span class="sxs-lookup"><span data-stu-id="2d7b9-116">Windows XP</span></span>       | <span data-ttu-id="2d7b9-117">Un décodeur MP3 Windows Media se comporte toujours comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-117">A Windows Media MP3 decoder always behaves as a DMO.</span></span>                                                                                                                                           |
| <span data-ttu-id="2d7b9-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d7b9-118">Windows Vista</span></span>    | <span data-ttu-id="2d7b9-119">Par défaut, un décodeur MP3 Windows Media se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-119">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="2d7b9-120">Si vous obtenez une interface **IMFTransform** ou une interface **IPropertyStore** sur un décodeur MP3 Windows Media, il se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-120">If you obtain an **IMFTransform** interface or an **IPropertyStore** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span> |
| <span data-ttu-id="2d7b9-121">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d7b9-121">Windows 7</span></span>        | <span data-ttu-id="2d7b9-122">Par défaut, un décodeur MP3 Windows Media se comporte comme un DMO.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-122">By default, a Windows Media MP3 decoder behaves as a DMO.</span></span> <span data-ttu-id="2d7b9-123">Si vous obtenez une interface **IMFTransform** sur un décodeur MP3 Windows Media, il se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-123">If you obtain an **IMFTransform** interface on a Windows Media MP3 decoder, it behaves as an MFT.</span></span>                                    |



 

## <a name="input-formats"></a><span data-ttu-id="2d7b9-124">Formats d’entrée</span><span class="sxs-lookup"><span data-stu-id="2d7b9-124">Input Formats</span></span>

<span data-ttu-id="2d7b9-125">Le tableau suivant montre la balise de format audio qui représente le type d’entrée pris en charge par le décodeur MP3 Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-125">The following table shows the audio format tag that represents the input type supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="2d7b9-126">Balise de format, constante</span><span class="sxs-lookup"><span data-stu-id="2d7b9-126">Format tag constant</span></span>      | <span data-ttu-id="2d7b9-127">Mettre en forme la valeur de balise</span><span class="sxs-lookup"><span data-stu-id="2d7b9-127">Format tag value</span></span> | <span data-ttu-id="2d7b9-128">Format audio</span><span class="sxs-lookup"><span data-stu-id="2d7b9-128">Audio format</span></span>     |
|--------------------------|------------------|------------------|
| <span data-ttu-id="2d7b9-129">\_MPEGLAYER3 format \_ Wave</span><span class="sxs-lookup"><span data-stu-id="2d7b9-129">WAVE\_FORMAT\_MPEGLAYER3</span></span> | <span data-ttu-id="2d7b9-130">0x55</span><span class="sxs-lookup"><span data-stu-id="2d7b9-130">0x55</span></span>             | <span data-ttu-id="2d7b9-131">Couche MPEG ISO 3</span><span class="sxs-lookup"><span data-stu-id="2d7b9-131">ISO MPEG Layer 3</span></span> |



 

## <a name="output-formats"></a><span data-ttu-id="2d7b9-132">Formats de sortie</span><span class="sxs-lookup"><span data-stu-id="2d7b9-132">Output Formats</span></span>

<span data-ttu-id="2d7b9-133">Le tableau suivant répertorie les balises de format audio qui représentent les types de sortie pris en charge par le décodeur MP3 Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-133">The following table shows the audio format tags that represent the output types supported by the Windows Media MP3 decoder.</span></span>



| <span data-ttu-id="2d7b9-134">Balise de format, constante</span><span class="sxs-lookup"><span data-stu-id="2d7b9-134">Format tag constant</span></span>       | <span data-ttu-id="2d7b9-135">Mettre en forme la valeur de balise</span><span class="sxs-lookup"><span data-stu-id="2d7b9-135">Format tag value</span></span> | <span data-ttu-id="2d7b9-136">Format audio</span><span class="sxs-lookup"><span data-stu-id="2d7b9-136">Audio format</span></span>                                                                |
|---------------------------|------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="2d7b9-137">\_PCM format \_ Wave</span><span class="sxs-lookup"><span data-stu-id="2d7b9-137">WAVE\_FORMAT\_PCM</span></span>         | <span data-ttu-id="2d7b9-138">0x0001</span><span class="sxs-lookup"><span data-stu-id="2d7b9-138">0x0001</span></span>           | <span data-ttu-id="2d7b9-139">Format PCM (en cas d’utilisation comme DMO ou MFT)</span><span class="sxs-lookup"><span data-stu-id="2d7b9-139">PCM format (when used as a DMO or an MFT)</span></span>                                   |
| <span data-ttu-id="2d7b9-140">\_format Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="2d7b9-140">WAVE\_FORMAT\_IEEE\_FLOAT</span></span> | <span data-ttu-id="2d7b9-141">0x0003</span><span class="sxs-lookup"><span data-stu-id="2d7b9-141">0x0003</span></span>           | <span data-ttu-id="2d7b9-142">Virgule flottante IEEE (en cas d’utilisation en tant que MFT)</span><span class="sxs-lookup"><span data-stu-id="2d7b9-142">IEEE floating point (when used as an MFT)</span></span>                                   |
| <span data-ttu-id="2d7b9-143">\_format Wave \_ extensible</span><span class="sxs-lookup"><span data-stu-id="2d7b9-143">WAVE\_FORMAT\_EXTENSIBLE</span></span>  | <span data-ttu-id="2d7b9-144">0xFFFE</span><span class="sxs-lookup"><span data-stu-id="2d7b9-144">0xFFFE</span></span>           | <span data-ttu-id="2d7b9-145">Format PCM/IEEE dans la structure **WAVEFORMATEXTENSIBLE** (en cas d’utilisation en tant que MFT)</span><span class="sxs-lookup"><span data-stu-id="2d7b9-145">PCM/IEEE format in **WAVEFORMATEXTENSIBLE** structure (when used as an MFT)</span></span> |



 

<span data-ttu-id="2d7b9-146">Le décodeur MP3 Windows Media prend en charge et énumère les types de médias de sortie suivants.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-146">The Windows Media MP3 decoder supports and enumerates the following output media types.</span></span>

-   <span data-ttu-id="2d7b9-147">Type de sortie qui a le même taux d’échantillonnage et le même nombre de canaux que le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-147">An output type that has the same sampling rate and number of channels as the input type.</span></span>
-   <span data-ttu-id="2d7b9-148">Sortie mono pour une entrée stéréo.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-148">Mono output for stereo input.</span></span>
-   <span data-ttu-id="2d7b9-149">Types de sortie avec des profondeur de bit de 8 et 16.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-149">Output types with bit depths of 8 and 16.</span></span>
-   <span data-ttu-id="2d7b9-150">Sortie à virgule flottante, si le décodeur se comporte comme une table MFT.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-150">Floating point output, if the decoder is behaving as an MFT.</span></span>

<span data-ttu-id="2d7b9-151">Le décodeur MP3 Windows Media prend en charge, mais n’énumère pas les types de médias de sortie suivants.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-151">The Windows Media MP3 decoder supports, but does not enumerate, the following output media types.</span></span>

-   <span data-ttu-id="2d7b9-152">Type de sortie qui a la moitié du taux d’échantillonnage du type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-152">An output type that has half the sampling rate of the input type.</span></span>
-   <span data-ttu-id="2d7b9-153">Type de sortie qui a un quatrième taux d’échantillonnage du type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="2d7b9-153">An output type that has one fourth the sampling rate of the input type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d7b9-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d7b9-154">Requirements</span></span>



| <span data-ttu-id="2d7b9-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d7b9-155">Requirement</span></span> | <span data-ttu-id="2d7b9-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d7b9-156">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d7b9-157">Client</span><span class="sxs-lookup"><span data-stu-id="2d7b9-157">Client</span></span><br/> | <span data-ttu-id="2d7b9-158">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d7b9-158">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="2d7b9-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d7b9-159">Header</span></span><br/> | <dl> <span data-ttu-id="2d7b9-160"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d7b9-160"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="2d7b9-161">DLL</span><span class="sxs-lookup"><span data-stu-id="2d7b9-161">DLL</span></span><br/>    | <dl> <span data-ttu-id="2d7b9-162"><dt>Mp3dmod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d7b9-162"><dt>Mp3dmod.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2d7b9-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d7b9-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d7b9-164">Objets codec</span><span class="sxs-lookup"><span data-stu-id="2d7b9-164">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="2d7b9-165">Implémentation du codec</span><span class="sxs-lookup"><span data-stu-id="2d7b9-165">Codec Implementation</span></span>](codecimplementation.md)
</dt> </dl>

 

 




