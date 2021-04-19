---
description: Paramètres du décodeur pour Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Paramètres du décodeur pour Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f66b5107fa0316f6ce2547e1f5f066165ed598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106527041"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a><span data-ttu-id="063fe-103">Paramètres du décodeur pour Windows Media Center Edition</span><span class="sxs-lookup"><span data-stu-id="063fe-103">Decoder Settings for Windows Media Center Edition</span></span>

<span data-ttu-id="063fe-104">Windows XP Media Center Edition 2005 et versions ultérieures utilise l’interface [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) pour configurer le filtre de décodeur audio pour la télévision et la lecture de DVD.</span><span class="sxs-lookup"><span data-stu-id="063fe-104">Windows XP Media Center Edition 2005 and later uses the [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) interface to configure the audio decoder filter for television and DVD playback.</span></span> <span data-ttu-id="063fe-105">Les propriétés suivantes sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="063fe-105">The following properties are supported.</span></span>



| <span data-ttu-id="063fe-106">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="063fe-106">Property GUID</span></span>                   | <span data-ttu-id="063fe-107">Description</span><span class="sxs-lookup"><span data-stu-id="063fe-107">Description</span></span>                                      |
|---------------------------------|--------------------------------------------------|
| <span data-ttu-id="063fe-108">\_format de \_ sortie \_ audio CODECAPI</span><span class="sxs-lookup"><span data-stu-id="063fe-108">CODECAPI\_AUDIO\_OUTPUT\_FORMAT</span></span> | <span data-ttu-id="063fe-109">Configure le format de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="063fe-109">Configures the audio output format.</span></span> <span data-ttu-id="063fe-110">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="063fe-110">See Remarks.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="063fe-111">Notes</span><span class="sxs-lookup"><span data-stu-id="063fe-111">Remarks</span></span>

<span data-ttu-id="063fe-112">La valeur de la \_ \_ propriété format de sortie audio CODECAPI \_ est une représentation sous forme de chaîne d’un GUID, stockée en tant que valeur **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="063fe-112">The value of the CODECAPI\_AUDIO\_OUTPUT\_FORMAT property is a string representation of a GUID, stored as a **BSTR** value.</span></span> <span data-ttu-id="063fe-113">Les GUID suivants sont définis.</span><span class="sxs-lookup"><span data-stu-id="063fe-113">The following GUIDs are defined.</span></span>



| <span data-ttu-id="063fe-114">GUID</span><span class="sxs-lookup"><span data-stu-id="063fe-114">GUID</span></span>                                                        | <span data-ttu-id="063fe-115">Description</span><span class="sxs-lookup"><span data-stu-id="063fe-115">Description</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="063fe-116">\_format de \_ sortie audio CODECAPI \_ \_ PCM \_ stéréo \_ MATRIXENCODED</span><span class="sxs-lookup"><span data-stu-id="063fe-116">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO\_MATRIXENCODED</span></span> | <span data-ttu-id="063fe-117">Le filtre audio logiciel doit effectuer le décodage logiciel et générer un flux audio stéréo, avec la matrice audio multicanal encodée sur les deux canaux.</span><span class="sxs-lookup"><span data-stu-id="063fe-117">The software audio filter should perform software decoding and output a stereo audio stream, with the multichannel audio matrix encoded to the two channels.</span></span>                                                   |
| <span data-ttu-id="063fe-118">\_format de \_ sortie audio CODECAPI \_ \_ PCM \_ stéréo</span><span class="sxs-lookup"><span data-stu-id="063fe-118">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_STEREO</span></span>                | <span data-ttu-id="063fe-119">Le filtre audio logiciel doit effectuer le décodage logiciel et générer un flux audio stéréo.</span><span class="sxs-lookup"><span data-stu-id="063fe-119">The software audio filter should perform software decoding and output a stereo audio stream.</span></span>                                                                                                                   |
| <span data-ttu-id="063fe-120">\_PCM CODECAPI \_ format de sortie audio \_ \_ SPDIF \_</span><span class="sxs-lookup"><span data-stu-id="063fe-120">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_PCM</span></span>                 | <span data-ttu-id="063fe-121">Le filtre audio logiciel doit effectuer le décodage logiciel audio, même si la sortie physique du PC peut être une interface numérique, telle que S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="063fe-121">The software audio filter should perform software audio decoding, even though the physical output from the PC may be a digital interface, such as S/PDIF.</span></span>                                                      |
| <span data-ttu-id="063fe-122">\_ \_ \_ \_ flux binaire SPDIF de format de sortie audio CODECAPI \_</span><span class="sxs-lookup"><span data-stu-id="063fe-122">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_SPDIF\_BITSTREAM</span></span>           | <span data-ttu-id="063fe-123">Le filtre audio logiciel ne doit pas effectuer de décodage audio logiciel, mais il doit transmettre le flux de données audio numérique brut pour le traitement externe par un appareil connecté avec une liaison audio numérique, comme S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="063fe-123">The software audio filter should not perform software audio decoding, but should pass the raw digital audio bitstream for external processing by a device connected with a digital audio link, such as S/PDIF.</span></span> |
| <span data-ttu-id="063fe-124">\_ \_ \_ \_ casque PCM format de sortie audio CODECAPI \_</span><span class="sxs-lookup"><span data-stu-id="063fe-124">CODECAPI\_AUDIO\_OUTPUT\_FORMAT\_PCM\_HEADPHONES</span></span>            | <span data-ttu-id="063fe-125">Le filtre audio logiciel doit effectuer le décodage logiciel audio et doit appliquer un traitement propriétaire pour optimiser le casque.</span><span class="sxs-lookup"><span data-stu-id="063fe-125">The software audio filter should perform software audio decoding and should apply proprietary processing to optimize for headphones.</span></span> <span data-ttu-id="063fe-126">La prise en charge de ce paramètre est facultative.</span><span class="sxs-lookup"><span data-stu-id="063fe-126">Support for this setting is optional.</span></span>                                     |



 

> [!Note]  
> <span data-ttu-id="063fe-127">L’interface **ICodecAPI** stocke les propriétés de codec sous forme de paires clé/valeur, où la clé est un GUID et la valeur est un type **Variant** .</span><span class="sxs-lookup"><span data-stu-id="063fe-127">The **ICodecAPI** interface stores codec properties as key/value pairs, where the key is a GUID and the value is a **VARIANT** type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="063fe-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="063fe-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="063fe-129">Développement d’encodeur et de décodeur</span><span class="sxs-lookup"><span data-stu-id="063fe-129">Encoder and Decoder Development</span></span>](encoder-and-decoder-development.md)
</dt> </dl>

 

 



