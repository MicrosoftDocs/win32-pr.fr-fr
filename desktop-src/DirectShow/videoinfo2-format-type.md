---
description: Type de format VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Type de format VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527781"
---
# <a name="videoinfo2-format-type"></a><span data-ttu-id="04655-103">Type de format VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="04655-103">VideoInfo2 Format Type</span></span>

<span data-ttu-id="04655-104">Le type de média préféré d’un pin d’aperçu peut être un type avec un format [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="04655-104">A preview pin's preferred media type might be a type with a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) format.</span></span> <span data-ttu-id="04655-105">Cette structure de format prend en charge des fonctionnalités spéciales telles que les proportions de vidéo et d’image entrelacées.</span><span class="sxs-lookup"><span data-stu-id="04655-105">This format structure supports special features such as interlaced video and picture aspect ratios.</span></span>

<span data-ttu-id="04655-106">VMR-7 et VMR-9 prennent en charge [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) directement.</span><span class="sxs-lookup"><span data-stu-id="04655-106">The VMR-7 and the VMR-9 both support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) directly.</span></span> <span data-ttu-id="04655-107">Quand vous connectez VMR au décodeur, il négocie le meilleur format.</span><span class="sxs-lookup"><span data-stu-id="04655-107">When you connect the VMR to the decoder, they will negotiate the best format.</span></span> <span data-ttu-id="04655-108">Toutefois, le filtre de convertisseur vidéo plus ancien ne prend pas en charge **VIDEOINFOHEADER2**.</span><span class="sxs-lookup"><span data-stu-id="04655-108">The older Video Renderer filter, however, does not support **VIDEOINFOHEADER2**.</span></span> <span data-ttu-id="04655-109">Pour utiliser les types de format **VIDEOINFOHEADER2** avec le filtre de convertisseur vidéo, vous devez insérer le filtre de [mixage de superposition](overlay-mixer-filter.md) dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="04655-109">To use **VIDEOINFOHEADER2** format types with the Video Renderer filter, you must insert the [Overlay Mixer](overlay-mixer-filter.md) filter into the graph.</span></span>

1.  <span data-ttu-id="04655-110">Énumérez les types de médias préférés sur la broche de sortie du filtre de décodeur, à l’aide de la méthode [**IPIN :: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="04655-110">Enumerate the preferred media types on the decoder filter's output pin, using the [**IPin::EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) method.</span></span>
2.  <span data-ttu-id="04655-111">Vérifiez le premier type de média dans la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="04655-111">Check the first media type in the enumeration sequence.</span></span>
3.  <span data-ttu-id="04655-112">Si le type de format **est \_ VideoInfo2 format**, connectez la broche de sortie au mélangeur de superposition.</span><span class="sxs-lookup"><span data-stu-id="04655-112">If the format type is **FORMAT\_VideoInfo2**, connect the output pin to the Overlay Mixer.</span></span> <span data-ttu-id="04655-113">Connectez ensuite le mixer de superposition au convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="04655-113">Then connect the Overlay Mixer to the video renderer.</span></span> <span data-ttu-id="04655-114">(Voir les [broches des ports vidéo](video-port-pins.md).)</span><span class="sxs-lookup"><span data-stu-id="04655-114">(See [Video Port Pins](video-port-pins.md).)</span></span>

<span data-ttu-id="04655-115">Si vous ne vous souciez pas de ces fonctionnalités, vous n’avez pas besoin d’utiliser le mélangeur de superposition.</span><span class="sxs-lookup"><span data-stu-id="04655-115">If you do not care about these features, you do not have to use the Overlay Mixer.</span></span> <span data-ttu-id="04655-116">Connectez le décodeur directement au convertisseur vidéo et il se connectera avec un format [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) à la place.</span><span class="sxs-lookup"><span data-stu-id="04655-116">Connect the decoder directly to the Video Renderer, and it will connect with a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format instead.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04655-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="04655-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="04655-118">Rubriques avancées sur la capture</span><span class="sxs-lookup"><span data-stu-id="04655-118">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="04655-119">Utilisation du mélangeur de superposition dans la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="04655-119">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



