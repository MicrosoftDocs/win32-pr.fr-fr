---
description: Utilisation du codec Windows Media Audio Voice
ms.assetid: 771acb04-33a4-4ea3-8f50-e5e3dbdf9495
title: Utilisation du codec Windows Media Audio Voice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d636bd97b76e23acc6b68da87c8a206b17dea60a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530466"
---
# <a name="using-the-windows-media-audio-voice-codec"></a><span data-ttu-id="14c50-103">Utilisation du codec Windows Media Audio Voice</span><span class="sxs-lookup"><span data-stu-id="14c50-103">Using the Windows Media Audio Voice Codec</span></span>

<span data-ttu-id="14c50-104">Le codec Windows Media Audio Voice offre une compression à vitesse de transmission faible et optimisée pour le son contenant de la parole.</span><span class="sxs-lookup"><span data-stu-id="14c50-104">The Windows Media Audio Voice codec provides low bit-rate compression optimized for audio containing speech.</span></span> <span data-ttu-id="14c50-105">La capacité du codec à produire de tels petits exemples est due à la plage de fréquences limitée des sons de la voix humaine.</span><span class="sxs-lookup"><span data-stu-id="14c50-105">The ability of the codec to produce such small samples is due to the limited frequency range of the sounds of the human voice.</span></span> <span data-ttu-id="14c50-106">Cette optimisation signifie qu’un encodeur vocal dédié crée une sortie de qualité médiocre pour le contenu qui contient des sons plus compliqués, tels que la musique.</span><span class="sxs-lookup"><span data-stu-id="14c50-106">This optimization means that a dedicated voice encoder creates poor-quality output for content that contains more complicated sounds, like music.</span></span> <span data-ttu-id="14c50-107">Toutefois, le codec Windows Media Audio Voice compense ce problème de qualité potentiel en fournissant des modes distincts pour la voix, la musique et le contenu mixte.</span><span class="sxs-lookup"><span data-stu-id="14c50-107">However, the Windows Media Audio Voice codec compensates for this potential quality issue by providing separate modes for voice, music, and mixed content.</span></span> <span data-ttu-id="14c50-108">Le codec analyse le contenu mixte pour déterminer le mode à utiliser pour chaque partie du fichier.</span><span class="sxs-lookup"><span data-stu-id="14c50-108">The codec analyzes mixed content to determine which mode to use for each portion of the file.</span></span>

<span data-ttu-id="14c50-109">Le codec Windows Media Audio Voice est implémenté dans l’objet encodeur identifié par l’identificateur de classe CLSID \_ CWMSPEncMediaObject2, et dans l’objet décodeur identifié par l’identificateur de classe CLSID \_ CWMSPDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="14c50-109">The Windows Media Audio Voice codec is implemented in the encoder object identified by the class identifier CLSID\_CWMSPEncMediaObject2, and in the decoder object identified by the class identifier CLSID\_CWMSPDecMediaObject.</span></span> <span data-ttu-id="14c50-110">La balise de format des types de média utilisant ce codec est 0x00A.</span><span class="sxs-lookup"><span data-stu-id="14c50-110">The format tag of media types using this codec is 0x00A.</span></span>

## <a name="configuring-the-encoder"></a><span data-ttu-id="14c50-111">Configuration de l’encodeur</span><span class="sxs-lookup"><span data-stu-id="14c50-111">Configuring the Encoder</span></span>

<span data-ttu-id="14c50-112">L’encodeur vocal prend en charge trois modes : la reconnaissance vocale, la musique et la combinaison.</span><span class="sxs-lookup"><span data-stu-id="14c50-112">The voice encoder supports three modes: speech, music, and mixed.</span></span> <span data-ttu-id="14c50-113">Chaque mode est optimisé pour obtenir les meilleurs résultats pour ce type de contenu.</span><span class="sxs-lookup"><span data-stu-id="14c50-113">Each mode is optimized to get the best results for that type of content.</span></span> <span data-ttu-id="14c50-114">Vous pouvez configurer le mode de l’encodeur vocal à l’aide des méthodes de **IPropertyStore** pour définir la propriété [MFPKEY \_ WMAVOICE \_ enc \_ MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="14c50-114">You can configure the mode of the voice encoder by using the methods of **IPropertyStore** to set the [MFPKEY\_WMAVOICE\_ENC\_MusicSpeechClassMode](mfpkey-wmavoice-enc-musicspeechclassmodeproperty.md) property.</span></span>

<span data-ttu-id="14c50-115">Lorsqu’il est configuré pour du contenu mixte, le codec Windows Media Audio Voice détecte automatiquement les passages de musique dans le contenu.</span><span class="sxs-lookup"><span data-stu-id="14c50-115">When configured for mixed content, the Windows Media Audio Voice codec will automatically detect passages of music in the content.</span></span> <span data-ttu-id="14c50-116">Si vous n’êtes pas satisfait des résultats, vous pouvez spécifier l’emplacement de musique dans le contenu à l’aide d’une liste de décisions de modification (EDL).</span><span class="sxs-lookup"><span data-stu-id="14c50-116">If you are not satisfied with the results, you can specify the location of music in the content using an editing decision list (EDL).</span></span> <span data-ttu-id="14c50-117">Pour plus d’informations, consultez [utilisation d’une liste de décisions de modification pour l’encodage vocal](usingavoiceeditingdecisionlist.md).</span><span class="sxs-lookup"><span data-stu-id="14c50-117">For more information, see [Using an Editing Decision List for Encoding Voice](usingavoiceeditingdecisionlist.md).</span></span>

<span data-ttu-id="14c50-118">Contrairement aux autres encodeurs audio, vous pouvez définir la valeur de la fenêtre de mémoire tampon pour le contenu vocal à l’aide de la propriété [MFPKEY \_ WMAVOICE \_ enc \_ BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="14c50-118">Unlike the other audio encoders, you can set the buffer window value for voice content by using the [MFPKEY\_WMAVOICE\_ENC\_BufferWindow](mfpkey-wmavoice-enc-bufferwindowproperty.md) property.</span></span> <span data-ttu-id="14c50-119">Toutefois, les valeurs par défaut devraient fonctionner correctement dans la plupart des cas.</span><span class="sxs-lookup"><span data-stu-id="14c50-119">However, the default values should work fine in most cases.</span></span>

> [!Note]  
>    <span data-ttu-id="14c50-120">Lors de la configuration de l’encodeur vocal, il est très important de définir le type de sortie avant de définir le type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="14c50-120">When configuring the voice encoder, it is very important that you set the output type before you set the input type.</span></span> <span data-ttu-id="14c50-121">Il s’agit de l’ordre d’opérations recommandé pour tous les codecs audio, mais l’encodeur vocal peut signaler des types de sortie erronés si une entrée est définie lorsque vous appelez **IMediaObject :: GetOutputType** ou **IMFTransform :: GetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="14c50-121">This is the recommended order of operations for all of the audio codecs, but the voice encoder can report erroneous output types if an input is set when you call **IMediaObject::GetOutputType** or **IMFTransform::GetOutputType**.</span></span>

 

## <a name="decoding"></a><span data-ttu-id="14c50-122">Décodage</span><span class="sxs-lookup"><span data-stu-id="14c50-122">Decoding</span></span>

<span data-ttu-id="14c50-123">Il n’existe aucune exigence particulière pour décoder l’audio vocal.</span><span class="sxs-lookup"><span data-stu-id="14c50-123">There are no special requirements for decoding voice audio.</span></span> <span data-ttu-id="14c50-124">Pour plus d’informations, consultez [configuration du décodage audio](configuringaudiodecoding.md).</span><span class="sxs-lookup"><span data-stu-id="14c50-124">Form more information, see [Configuring Audio Decoding](configuringaudiodecoding.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14c50-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="14c50-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14c50-126">Utilisation de l’audio</span><span class="sxs-lookup"><span data-stu-id="14c50-126">Working with Audio</span></span>](workingwithaudio.md)
</dt> </dl>

 

 



