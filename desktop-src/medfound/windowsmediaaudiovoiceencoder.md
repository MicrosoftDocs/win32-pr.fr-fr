---
description: L’encodeur vocal Windows Media Audio est optimisé pour l’encodage de la voix humaine à des taux de compression élevés. Il s’agit de l’encodeur par défaut pour les flux composés principalement de mots prononcés.
ms.assetid: b3cfa845-4fe1-405f-88e5-4555398639ef
title: Encodeur vocal Windows Media Audio (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef79f2c3d0c48fee8ec33e08bfb9fdf21c3656b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533440"
---
# <a name="windows-media-audio-voice-encoder"></a><span data-ttu-id="1294b-104">Encodeur vocal Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="1294b-104">Windows Media Audio Voice Encoder</span></span>

<span data-ttu-id="1294b-105">L’encodeur vocal Windows Media Audio est optimisé pour l’encodage de la voix humaine à des taux de compression élevés.</span><span class="sxs-lookup"><span data-stu-id="1294b-105">The Windows Media Audio Voice encoder is optimized for encoding the human voice at high compression ratios.</span></span> <span data-ttu-id="1294b-106">Il s’agit de l’encodeur par défaut pour les flux composés principalement de mots prononcés.</span><span class="sxs-lookup"><span data-stu-id="1294b-106">This is the preferred encoder for streams consisting mostly of spoken words.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="1294b-107">Identificateur de classe</span><span class="sxs-lookup"><span data-stu-id="1294b-107">Class Identifier</span></span>

<span data-ttu-id="1294b-108">L’identificateur de classe (CLSID) de l’encodeur vocal Windows Media Audio est représenté par la constante **CLSID \_ CWMSPEncMediaObject2**.</span><span class="sxs-lookup"><span data-stu-id="1294b-108">The class identifier (CLSID) for the Windows Media Audio Voice encoder is represented by the constant **CLSID\_CWMSPEncMediaObject2**.</span></span> <span data-ttu-id="1294b-109">Vous pouvez créer une instance de l’encodeur vocal en appelant **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="1294b-109">You can create an instance of the voice encoder by calling **CoCreateInstance**.</span></span>

## <a name="output-formats"></a><span data-ttu-id="1294b-110">Formats de sortie</span><span class="sxs-lookup"><span data-stu-id="1294b-110">Output Formats</span></span>

<span data-ttu-id="1294b-111">Windows Media Audio contenu encodé en voix est identifié par la balise de format 0x00A.</span><span class="sxs-lookup"><span data-stu-id="1294b-111">Windows Media Audio Voice encoded content is identified by the format tag 0x00A.</span></span>

## <a name="encoder-properties"></a><span data-ttu-id="1294b-112">Propriétés de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="1294b-112">Encoder Properties</span></span>

<span data-ttu-id="1294b-113">L’encodeur vocal Windows Media Audio prend en charge les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="1294b-113">The Windows Media Audio Voice encoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="1294b-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="1294b-114">Property</span></span></th>
<th><span data-ttu-id="1294b-115">Description</span><span class="sxs-lookup"><span data-stu-id="1294b-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1294b-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span><span class="sxs-lookup"><span data-stu-id="1294b-116"><a href="mfpkey-wmavoice-enc-bufferwindowproperty.md">MFPKEY_WMAVOICE_ENC_BufferWindow</a></span></span></td>
<td><span data-ttu-id="1294b-117">Spécifie la fenêtre de mémoire tampon, en millisecondes, utilisée pour le codec vocal.</span><span class="sxs-lookup"><span data-stu-id="1294b-117">Specifies the buffer window, in milliseconds, used for the voice codec.</span></span><br/> <dl> <span data-ttu-id="1294b-118">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1294b-118">Windows XP and later.</span></span><br />
<span data-ttu-id="1294b-119">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="1294b-119">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1294b-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span><span class="sxs-lookup"><span data-stu-id="1294b-120"><a href="mfpkey-wmavoice-enc-decoderdelayproperty.md">MFPKEY_WMAVOICE_ENC_DecoderDelay</a></span></span></td>
<td><span data-ttu-id="1294b-121">Spécifie la latence de l’encodeur dans les unités de paquets.</span><span class="sxs-lookup"><span data-stu-id="1294b-121">Specifies encoder latency in packet units.</span></span><br/> <dl> <span data-ttu-id="1294b-122">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1294b-122">Windows XP and later.</span></span><br />
<span data-ttu-id="1294b-123">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="1294b-123">Write-only.</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1294b-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span><span class="sxs-lookup"><span data-stu-id="1294b-124"><a href="mfpkey-wmavoice-enc-edlproperty.md">MFPKEY_WMAVOICE_ENC_EDL</a></span></span></td>
<td><span data-ttu-id="1294b-125">Spécifie les portions de contenu à encoder en musique par le codec vocal.</span><span class="sxs-lookup"><span data-stu-id="1294b-125">Specifies the portions of content to be encoded as music by the voice codec.</span></span><br/> <dl> <span data-ttu-id="1294b-126">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1294b-126">Windows XP and later.</span></span><br />
<span data-ttu-id="1294b-127">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1294b-127">Read/write.</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1294b-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span><span class="sxs-lookup"><span data-stu-id="1294b-128"><a href="mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md">MFPKEY_WMAVOICE_ENC_MusicSpeechClassMode</a></span></span></td>
<td><span data-ttu-id="1294b-129">Spécifie le mode du codec vocal.</span><span class="sxs-lookup"><span data-stu-id="1294b-129">Specifies the mode of the voice codec.</span></span><br/> <dl> <span data-ttu-id="1294b-130">Windows XP et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="1294b-130">Windows XP and later.</span></span><br />
<span data-ttu-id="1294b-131">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1294b-131">Read/write.</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="1294b-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1294b-132">Requirements</span></span>



| <span data-ttu-id="1294b-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1294b-133">Requirement</span></span> | <span data-ttu-id="1294b-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="1294b-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1294b-135">Client</span><span class="sxs-lookup"><span data-stu-id="1294b-135">Client</span></span><br/> | <span data-ttu-id="1294b-136">Windows XP, Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="1294b-136">Windows XP, Windows Vista or Windows 7</span></span><br/>                                       |
| <span data-ttu-id="1294b-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="1294b-137">Header</span></span><br/> | <dl> <span data-ttu-id="1294b-138"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1294b-138"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="1294b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1294b-139">DLL</span></span><br/>    | <dl> <span data-ttu-id="1294b-140"><dt>Wmspdmoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1294b-140"><dt>Wmspdmoe.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1294b-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1294b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1294b-142">Objets codec</span><span class="sxs-lookup"><span data-stu-id="1294b-142">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="1294b-143">Utilisation du codec Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="1294b-143">Using the Windows Media Audio Voice Codec</span></span>](usingthewindowsmediaaudio9voicecodec.md)
</dt> </dl>

 

 




