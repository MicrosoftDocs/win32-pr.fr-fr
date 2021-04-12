---
description: Attributs de flux
ms.assetid: 83b64ad8-2552-41d1-bc61-20361831020b
title: Attributs de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a25de9ae6cf769268b3868d36bac2e293cfd8d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527825"
---
# <a name="stream-attributes"></a><span data-ttu-id="fc7db-103">Attributs de flux</span><span class="sxs-lookup"><span data-stu-id="fc7db-103">Stream Attributes</span></span>

<span data-ttu-id="fc7db-104">Les attributs suivants s’appliquent aux flux multimédias.</span><span class="sxs-lookup"><span data-stu-id="fc7db-104">The following attributes apply to media streams.</span></span> <span data-ttu-id="fc7db-105">Pour obtenir les attributs d’un exemple de média, utilisez la méthode [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) .</span><span class="sxs-lookup"><span data-stu-id="fc7db-105">To get the attributes from a media sample, use the [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) method.</span></span>



| <span data-ttu-id="fc7db-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="fc7db-106">Attribute</span></span>                                                                                   | <span data-ttu-id="fc7db-107">Description</span><span class="sxs-lookup"><span data-stu-id="fc7db-107">Description</span></span>                                   |
|---------------------------------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="fc7db-108">MFStreamExtension \_ CameraExtrinsics</span><span class="sxs-lookup"><span data-stu-id="fc7db-108">MFStreamExtension\_CameraExtrinsics</span></span>](mfstreamextension-cameraextrinsics.md)               | <span data-ttu-id="fc7db-109">Extrinsics de l’appareil photo pour le flux.</span><span class="sxs-lookup"><span data-stu-id="fc7db-109">The camera extrinsics for the stream.</span></span>         |
| [<span data-ttu-id="fc7db-110">MFStreamExtension \_ PinholeCameraIntrinsics</span><span class="sxs-lookup"><span data-stu-id="fc7db-110">MFStreamExtension\_PinholeCameraIntrinsics</span></span>](mfstreamextension-pinholecameraintrinsics.md) | <span data-ttu-id="fc7db-111">L’appareil photo Pinhole est intrinsèque pour le flux.</span><span class="sxs-lookup"><span data-stu-id="fc7db-111">The pinhole camera intrinsics for the stream.</span></span> |



 

<span data-ttu-id="fc7db-112">Tous les flux de médias ne contiennent pas tous les attributs répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="fc7db-112">Not every media stream contains every attribute listed here.</span></span> <span data-ttu-id="fc7db-113">Dans certains cas, un attribut s’applique uniquement à certains genres de données.</span><span class="sxs-lookup"><span data-stu-id="fc7db-113">In some cases, an attribute applies only to certain kinds of data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc7db-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc7db-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc7db-115">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="fc7db-115">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
</dt> <dt>

[<span data-ttu-id="fc7db-116">Attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="fc7db-116">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fc7db-117">Exemples de supports</span><span class="sxs-lookup"><span data-stu-id="fc7db-117">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 



