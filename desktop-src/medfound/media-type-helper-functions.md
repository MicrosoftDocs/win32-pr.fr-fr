---
description: Les fonctions suivantes se rapportent aux objets de type de média.
ms.assetid: 7d4f3581-8cb9-4d31-b2f7-c8fbde24cf2a
title: Fonctions d’assistance du type de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7e5edb9748bad8ee16903eb9ff1ada50c1c043b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530531"
---
# <a name="media-type-helper-functions"></a><span data-ttu-id="b3ae2-103">Fonctions d’assistance du type de média</span><span class="sxs-lookup"><span data-stu-id="b3ae2-103">Media Type Helper Functions</span></span>

<span data-ttu-id="b3ae2-104">Les fonctions suivantes se rapportent aux objets de type de média.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-104">The following functions pertain to media type objects.</span></span>



| <span data-ttu-id="b3ae2-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="b3ae2-105">Function</span></span>                                                                     | <span data-ttu-id="b3ae2-106">Description</span><span class="sxs-lookup"><span data-stu-id="b3ae2-106">Description</span></span>                                                           |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="b3ae2-107">**MFAverageTimePerFrameToFrameRate**</span><span class="sxs-lookup"><span data-stu-id="b3ae2-107">**MFAverageTimePerFrameToFrameRate**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) | <span data-ttu-id="b3ae2-108">Calcule la fréquence d’images à partir de la durée moyenne d’une image vidéo.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-108">Calculates the frame rate from the average duration of a video frame.</span></span> |
| [<span data-ttu-id="b3ae2-109">**MFCalculateImageSize**</span><span class="sxs-lookup"><span data-stu-id="b3ae2-109">**MFCalculateImageSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcalculateimagesize)                         | <span data-ttu-id="b3ae2-110">Récupère la taille de l’image pour un format vidéo non compressé.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-110">Retrieves the image size for an uncompressed video format.</span></span>            |
| [<span data-ttu-id="b3ae2-111">**MFCompareFullToPartialMediaType**</span><span class="sxs-lookup"><span data-stu-id="b3ae2-111">**MFCompareFullToPartialMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcomparefulltopartialmediatype)   | <span data-ttu-id="b3ae2-112">Compare un type de média complet à un type de média partiel.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-112">Compares a full media type to a partial media type.</span></span>                   |
| [<span data-ttu-id="b3ae2-113">**MFCreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="b3ae2-113">**MFCreateMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemediatype)                               | <span data-ttu-id="b3ae2-114">Crée un type de média vide.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-114">Creates an empty media type.</span></span>                                          |
| [<span data-ttu-id="b3ae2-115">**MFFrameRateToAverageTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="b3ae2-115">**MFFrameRateToAverageTimePerFrame**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) | <span data-ttu-id="b3ae2-116">Convertit une fréquence d’images vidéo en une durée de trame.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-116">Converts a video frame rate into a frame duration.</span></span>                    |
| [<span data-ttu-id="b3ae2-117">**MFGetStrideForBitmapInfoHeader**</span><span class="sxs-lookup"><span data-stu-id="b3ae2-117">**MFGetStrideForBitmapInfoHeader**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfgetstrideforbitmapinfoheader)     | <span data-ttu-id="b3ae2-118">Récupère le Stride de surface minimal pour un format vidéo.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-118">Retrieves the minimum surface stride for a video format.</span></span>              |
| [<span data-ttu-id="b3ae2-119">**MFIsFormatYUV**</span><span class="sxs-lookup"><span data-stu-id="b3ae2-119">**MFIsFormatYUV**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfisformatyuv)                                       | <span data-ttu-id="b3ae2-120">Interroge si un code FOURCC ou une valeur **D3DFORMAT** est un format YUV.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-120">Queries whether a FOURCC code or **D3DFORMAT** value is a YUV format.</span></span> |
| [<span data-ttu-id="b3ae2-121">**MFValidateMediaTypeSize**</span><span class="sxs-lookup"><span data-stu-id="b3ae2-121">**MFValidateMediaTypeSize**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfvalidatemediatypesize)                   | <span data-ttu-id="b3ae2-122">Valide la taille d’une mémoire tampon pour un bloc de format vidéo.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-122">Validates the size of a buffer for a video format block.</span></span>              |
| [<span data-ttu-id="b3ae2-123">**MFWrapMediaType**</span><span class="sxs-lookup"><span data-stu-id="b3ae2-123">**MFWrapMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfwrapmediatype)                                   | <span data-ttu-id="b3ae2-124">Crée un type de média qui encapsule un autre type de média.</span><span class="sxs-lookup"><span data-stu-id="b3ae2-124">Creates a media type that wraps another media type.</span></span>                   |



 

## <a name="related-topics"></a><span data-ttu-id="b3ae2-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3ae2-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3ae2-126">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b3ae2-126">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="b3ae2-127">Conversions de type de média</span><span class="sxs-lookup"><span data-stu-id="b3ae2-127">Media Type Conversions</span></span>](media-type-conversions.md)
</dt> <dt>

[<span data-ttu-id="b3ae2-128">Types de médias</span><span class="sxs-lookup"><span data-stu-id="b3ae2-128">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



