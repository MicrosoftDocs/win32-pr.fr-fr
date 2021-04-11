---
description: Utilisation de l’audio High-Definition
ms.assetid: 5e21943f-363c-4831-bc09-aadf6f4a0ad5
title: Utilisation de l’audio High-Definition (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05e7bd9311574c3d25f9069ea60c9d269d24390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755237"
---
# <a name="using-high-definition-audio-microsoft-media-foundation"></a><span data-ttu-id="1ca15-103">Utilisation de l’audio High-Definition (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="1ca15-103">Using High-Definition Audio (Microsoft Media Foundation)</span></span>

<span data-ttu-id="1ca15-104">L’audio haute définition, dans le contexte des codecs Windows Media Audio, est tout type audio avec plus de deux canaux ou plus de 16 bits par échantillon.</span><span class="sxs-lookup"><span data-stu-id="1ca15-104">High-definition audio, in the context of the Windows Media Audio codecs, is any audio type with more than two channels or more than 16 bits per sample.</span></span> <span data-ttu-id="1ca15-105">Le son haute définition est pris en charge par les catégories professionnel et sans perte de l' [Encodeur Windows Media Audio](windowsmediaaudioencoder.md).</span><span class="sxs-lookup"><span data-stu-id="1ca15-105">High-definition audio is supported by the Professional and Lossless categories of the [Windows Media Audio Encoder](windowsmediaaudioencoder.md).</span></span>

<span data-ttu-id="1ca15-106">Les types audio haute définition non compressés sont définis à l’aide de la structure [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1ca15-106">Uncompressed high-definition audio types are defined using the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure.</span></span> <span data-ttu-id="1ca15-107">**WAVEFORMATEXTENSIBLE** est une extension structurée de la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1ca15-107">**WAVEFORMATEXTENSIBLE** is a structured extension of the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="1ca15-108">Lorsque vous utilisez DMOs, le membre **formatType** de la structure [**de \_ \_ type de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) qui décrit un type audio haute définition doit être défini sur WMCFORMAT \_ WaveFormatEx, comme c’est le cas pour le son normal ; il n’existe aucun identificateur de format spécial pour **WAVEFORMATEXTENSIBLE**.</span><span class="sxs-lookup"><span data-stu-id="1ca15-108">When you are using DMOs, the **formattype** member of the [**DMO\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) structure that describes a high-definition audio type must be set to WMCFORMAT\_WaveFormatEx, just as it is for normal audio; there is no special format identifier for **WAVEFORMATEXTENSIBLE**.</span></span> <span data-ttu-id="1ca15-109">Si un format utilise **WAVEFORMATEXTENSIBLE** , vous devez définir le membre **cbSize** de la structure **WAVEFORMATEX** sur 22.</span><span class="sxs-lookup"><span data-stu-id="1ca15-109">If a format uses **WAVEFORMATEXTENSIBLE** , you must set the **cbSize** member of the **WAVEFORMATEX** structure to 22.</span></span>

<span data-ttu-id="1ca15-110">Lorsque vous utilisez Media Foundation, vous pouvez construire le type de média approprié à partir d’une structure [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) à l’aide de la fonction [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).</span><span class="sxs-lookup"><span data-stu-id="1ca15-110">When using Media Foundation, you can construct the correct media type from a [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)) structure by using the function [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex).</span></span>

<span data-ttu-id="1ca15-111">Les types de sortie à plusieurs canaux pris en charge par le codec Windows Media Audio 10 Professional n’utilisent pas [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), mais signalent le nombre correct de canaux et de bits par échantillon dans la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1ca15-111">The multi-channel output types supported by the Windows Media Audio 10 Professional codec do not use [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)), but report the correct number of channels and bits per sample in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="1ca15-112">Comme avec tous les types audio décrivant le contenu Windows Media Audio compressé, des informations supplémentaires sont ajoutées à la structure **WAVEFORMATEX** utilisée par le décodeur pour la décompression.</span><span class="sxs-lookup"><span data-stu-id="1ca15-112">As with all audio types describing compressed Windows Media Audio content, there is additional information appended to the **WAVEFORMATEX** structure that is used by the decoder for decompression.</span></span>

## <a name="decoding-high-definition-audio"></a><span data-ttu-id="1ca15-113">Décodage High-Definition audio</span><span class="sxs-lookup"><span data-stu-id="1ca15-113">Decoding High-Definition Audio</span></span>

<span data-ttu-id="1ca15-114">Pour décoder un son haute définition, vous devez définir la propriété [MFPKEY \_ WMADEC \_ HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) sur variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="1ca15-114">To decode high-definition audio, you must set the [MFPKEY\_WMADEC\_HIRESOUTPUT](mfpkey-wmadec-hiresoutputproperty.md) property to VARIANT\_TRUE.</span></span> <span data-ttu-id="1ca15-115">Si cette propriété n’est pas définie, le décodeur fournit du contenu stéréo avec un maximum de 16 bits par échantillon, quel que soit le format compressé.</span><span class="sxs-lookup"><span data-stu-id="1ca15-115">If this property is not set, the decoder will deliver stereo content with a maximum of 16 bits per sample, regardless of the compressed format.</span></span>

> [!Note]  
> <span data-ttu-id="1ca15-116">Le son haute définition est pris en charge uniquement pour Windows XP, Windows Vista et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1ca15-116">High-definition audio is supported only for Windows XP, Windows Vista and later.</span></span> <span data-ttu-id="1ca15-117">Dans les versions antérieures de Windows, Windows Media Audio le contenu encodé avec la haute définition est rendu sous la forme audio à deux canaux, avec un maximum de 16 bits par échantillon.</span><span class="sxs-lookup"><span data-stu-id="1ca15-117">On earlier versions of Windows, Windows Media Audio content encoded with high definition is rendered as two-channel audio with a maximum of 16 bits per sample.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1ca15-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1ca15-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ca15-119">Utilisation de l’audio</span><span class="sxs-lookup"><span data-stu-id="1ca15-119">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 
