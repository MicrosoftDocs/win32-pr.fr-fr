---
description: Mémoires tampons de média
ms.assetid: 3ee073ea-7bac-4971-9167-93a4e541ab77
title: Mémoires tampons de média
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87316ea64e24173dfa73f2cc2ff280a1281d50f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106532365"
---
# <a name="media-buffers"></a><span data-ttu-id="b952d-103">Mémoires tampons de média</span><span class="sxs-lookup"><span data-stu-id="b952d-103">Media Buffers</span></span>

<span data-ttu-id="b952d-104">Une mémoire tampon de média est un objet COM qui gère un bloc de mémoire, généralement pour contenir des données multimédias.</span><span class="sxs-lookup"><span data-stu-id="b952d-104">A media buffer is a COM object that manages a block of memory, typically to hold media data.</span></span> <span data-ttu-id="b952d-105">Les mémoires tampons de média sont utilisées pour déplacer des données d’un composant de pipeline à l’autre.</span><span class="sxs-lookup"><span data-stu-id="b952d-105">Media buffers are used to move data from one pipeline component to the next.</span></span> <span data-ttu-id="b952d-106">La plupart des applications n’utilisent pas directement les mémoires tampons de média, car la session de média gère l’ensemble du flot de données entre les objets de pipeline.</span><span class="sxs-lookup"><span data-stu-id="b952d-106">Most applications do not use media buffers directly, because the Media Session handles all of the data flow between pipeline objects.</span></span> <span data-ttu-id="b952d-107">Vous devez utiliser des mémoires tampons de média si vous écrivez votre propre composant de pipeline, ou si vous utilisez un composant de pipeline directement sans la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="b952d-107">You must use media buffers if you are writing your own pipeline component, or if you are using a pipeline component directly without the Media Session.</span></span>

<span data-ttu-id="b952d-108">Les mémoires tampons de média exposent l’interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) .</span><span class="sxs-lookup"><span data-stu-id="b952d-108">Media buffers exposes the [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) interface.</span></span> <span data-ttu-id="b952d-109">Cette interface est conçue pour lire ou écrire n’importe quel type de données.</span><span class="sxs-lookup"><span data-stu-id="b952d-109">This interface is designed for reading or writing any type of data.</span></span> <span data-ttu-id="b952d-110">Les images vidéo non compressées nécessitent un traitement spécial, car elles peuvent être stockées dans des surfaces Direct3D situées dans la mémoire vidéo.</span><span class="sxs-lookup"><span data-stu-id="b952d-110">Uncompressed video frames require special handling, because they might be stored in Direct3D surfaces located in video memory.</span></span>

<span data-ttu-id="b952d-111">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b952d-111">This section contains the following topics.</span></span>



| <span data-ttu-id="b952d-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="b952d-112">Topic</span></span>                                                        | <span data-ttu-id="b952d-113">Description</span><span class="sxs-lookup"><span data-stu-id="b952d-113">Description</span></span>                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="b952d-114">Utilisation des mémoires tampons de média</span><span class="sxs-lookup"><span data-stu-id="b952d-114">Working with Media Buffers</span></span>](working-with-media-buffers.md) | <span data-ttu-id="b952d-115">Décrit le comportement général des mémoires tampons de média pour tous les types de média.</span><span class="sxs-lookup"><span data-stu-id="b952d-115">Describes the general behavior of media buffers for all media types.</span></span> |
| [<span data-ttu-id="b952d-116">Mémoires tampons vidéo non compressées</span><span class="sxs-lookup"><span data-stu-id="b952d-116">Uncompressed Video Buffers</span></span>](uncompressed-video-buffers.md) | <span data-ttu-id="b952d-117">Utilisation des mémoires tampons de média qui contiennent des images vidéo non compressées.</span><span class="sxs-lookup"><span data-stu-id="b952d-117">How work with media buffers that contain uncompressed video frames.</span></span>  |
| [<span data-ttu-id="b952d-118">Mémoire tampon de surface DirectX</span><span class="sxs-lookup"><span data-stu-id="b952d-118">DirectX Surface Buffer</span></span>](directx-surface-buffer.md)         | <span data-ttu-id="b952d-119">Décrit comment stocker une surface Direct3D dans une mémoire tampon de média.</span><span class="sxs-lookup"><span data-stu-id="b952d-119">Describes how to store a Direct3D surface in a media buffer.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="b952d-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b952d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b952d-121">Primitives de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b952d-121">Media Foundation Primitives</span></span>](media-foundation-primitives.md)
</dt> </dl>

 

 



