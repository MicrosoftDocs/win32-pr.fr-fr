---
description: Per-Pixel la fusion alpha
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel la fusion alpha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7e67084ae19df4a1aab81474dc8a9b1a313b9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515901"
---
# <a name="per-pixel-alpha-blending"></a><span data-ttu-id="c87f2-103">Per-Pixel la fusion alpha</span><span class="sxs-lookup"><span data-stu-id="c87f2-103">Per-Pixel Alpha Blending</span></span>

<span data-ttu-id="c87f2-104">Quatre sous-types de média ont été définis pour la fusion alpha par pixel.</span><span class="sxs-lookup"><span data-stu-id="c87f2-104">Four media subtypes have been defined for per-pixel alpha blending.</span></span> <span data-ttu-id="c87f2-105">Ces sous-types sont pris en charge uniquement lorsque VMR est en mode de mixage.</span><span class="sxs-lookup"><span data-stu-id="c87f2-105">These subtypes are only supported when the VMR is in mixing mode.</span></span> <span data-ttu-id="c87f2-106">VMR rejette la connexion si elle n’est pas en mode de mixage lorsqu’un filtre en amont tente de se connecter à l’aide de l’un de ces sous-types.</span><span class="sxs-lookup"><span data-stu-id="c87f2-106">The VMR will reject the connection if it is not in mixing mode when an upstream filter attempts to connect using one of these subtypes.</span></span> <span data-ttu-id="c87f2-107">Ces sous-types sont définis dans UUID. h :</span><span class="sxs-lookup"><span data-stu-id="c87f2-107">These subtypes are defined in uuids.h:</span></span>

-   <span data-ttu-id="c87f2-108">MEDIASUBTYPE \_ ARGB1555</span><span class="sxs-lookup"><span data-stu-id="c87f2-108">MEDIASUBTYPE\_ARGB1555</span></span>
-   <span data-ttu-id="c87f2-109">MEDIASUBTYPE \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="c87f2-109">MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="c87f2-110">MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="c87f2-110">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="c87f2-111">MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="c87f2-111">MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="c87f2-112">Pour plus d’informations, consultez [sous-types de vidéo RVB non compressés](uncompressed-rgb-video-subtypes.md) et [**sous-types de vidéo YUV**](yuv-video-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="c87f2-112">For more information, see [Uncompressed RGB Video Subtypes](uncompressed-rgb-video-subtypes.md) and [**YUV Video Subtypes**](yuv-video-subtypes.md).</span></span>

 

 



