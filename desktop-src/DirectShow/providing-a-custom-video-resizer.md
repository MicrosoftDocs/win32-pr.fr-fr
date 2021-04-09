---
description: Fournir un redimensionnement vidéo personnalisé
ms.assetid: 4009f93f-cd50-440f-b943-7e3700e0e2cb
title: Fournir un redimensionnement vidéo personnalisé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5247727cf16ef3c94a699db2907ff240b1d8a289
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108906"
---
# <a name="providing-a-custom-video-resizer"></a><span data-ttu-id="d5ec5-103">Fournir un redimensionnement vidéo personnalisé</span><span class="sxs-lookup"><span data-stu-id="d5ec5-103">Providing a Custom Video Resizer</span></span>

<span data-ttu-id="d5ec5-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="d5ec5-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

> [!Note]  
> <span data-ttu-id="d5ec5-105">Cette fonctionnalité nécessite DirectX 9,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-105">This feature requires DirectX 9.0 or later.</span></span>

 

<span data-ttu-id="d5ec5-106">Lorsque les [services d’édition DirectShow](directshow-editing-services.md) redimensionnent un clip source vidéo, le comportement par défaut est un *StretchBlt*, qui est rapide, mais pas avec anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-106">When [DirectShow Editing Services](directshow-editing-services.md) (DES) resizes a video source clip, the default behavior is a *StretchBlt*, which is fast but not anti-aliased.</span></span> <span data-ttu-id="d5ec5-107">Vous pouvez modifier le comportement de redimensionnement en implémentant un dimensionnement personnalisé en tant que filtre de transformation DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-107">You can change the resizing behavior by implementing a custom resizer as a DirectShow transform filter.</span></span> <span data-ttu-id="d5ec5-108">Le filtre doit exposer l’interface [**IResize**](iresize.md) , qui permet à des de spécifier la taille vidéo d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-108">The filter must expose the [**IResize**](iresize.md) interface, which enables DES to specify the input and output video size.</span></span> <span data-ttu-id="d5ec5-109">Pour plus d’informations sur l’écriture d’un filtre de transformation, consultez [écriture de filtres de transformation](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="d5ec5-109">For information about writing a transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span> <span data-ttu-id="d5ec5-110">La classe de base **CTransformFilter** est recommandée comme point de départ.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-110">The **CTransformFilter** base class is recommended as the starting point.</span></span> <span data-ttu-id="d5ec5-111">Lorsque vous implémentez le filtre, notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="d5ec5-111">When you implement the filter, note the following:</span></span>

-   <span data-ttu-id="d5ec5-112">Prend en charge l’interface **IResize** sur le filtre (pas les broches).</span><span class="sxs-lookup"><span data-stu-id="d5ec5-112">Support the **IResize** interface on the filter (not the pins).</span></span>
-   <span data-ttu-id="d5ec5-113">Le filtre doit accepter uniquement les formats [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) (format \_ videoinfo).</span><span class="sxs-lookup"><span data-stu-id="d5ec5-113">The filter should accept only [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) formats (FORMAT\_VideoInfo).</span></span> <span data-ttu-id="d5ec5-114">Refuser les autres types de format.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-114">Reject other format types.</span></span>
-   <span data-ttu-id="d5ec5-115">Le format vidéo à partir de peut être n’importe quel type RVB non compressé, y compris les RGB 32 bits avec alpha (MEDIASUBTYPE \_ ARGB32).</span><span class="sxs-lookup"><span data-stu-id="d5ec5-115">The video format from DES may be any uncompressed RGB type, including 32-bit RGB with alpha (MEDIASUBTYPE\_ARGB32).</span></span> <span data-ttu-id="d5ec5-116">Votre filtre peut rejeter en toute sécurité les formats avec la **bihauteur** < 0.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-116">Your filter can safely reject formats with **biHeight** < 0.</span></span>
-   <span data-ttu-id="d5ec5-117">Avant que le moteur de rendu connecte la broche de sortie du filtre, il appelle [**IResize ::p ut \_ MediaType**](iresize-put-mediatype.md) pour définir le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-117">Before the Render Engine connects the filter's output pin, it calls [**IResize::put\_MediaType**](iresize-put-mediatype.md) to set the output type.</span></span> <span data-ttu-id="d5ec5-118">Elle peut également appeler [**IResize ::p ut \_**](iresize-put-size.md) pour ajuster la taille de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-118">It may also call [**IResize::put\_Size**](iresize-put-size.md) to adjust the output size.</span></span> <span data-ttu-id="d5ec5-119">Il peut appeler ces deux méthodes dans n’importe quel ordre, le nombre de fois, avant de connecter la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-119">It can call these two methods in any order, any number of times, before it connects the output pin.</span></span>
-   <span data-ttu-id="d5ec5-120">Une fois que le moteur de rendu a connecté la broche de sortie, il peut appeler à nouveau **put \_ Size** .</span><span class="sxs-lookup"><span data-stu-id="d5ec5-120">After the Render Engine connects the output pin, it might call **put\_Size** again.</span></span> <span data-ttu-id="d5ec5-121">Le filtre de redimensionnement doit reconnecter sa broche de sortie avec la nouvelle taille.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-121">The resizer filter should reconnect its output pin with the new size.</span></span>
-   <span data-ttu-id="d5ec5-122">À l’intérieur de la méthode [**CTransformFilter :: Transform**](ctransformfilter-transform.md) du filtre, étendez la vidéo d’entrée à la taille de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-122">Inside the filter's [**CTransformFilter::Transform**](ctransformfilter-transform.md) method, stretch the input video to the output size.</span></span>
-   <span data-ttu-id="d5ec5-123">Votre filtre ne doit jamais définir l’indicateur de discontinuité sur l’exemple de sortie, ni attacher un type de média à l’exemple de sortie.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-123">Your filter should never set the discontinuity flag on the output sample, or attach a media type to the output sample.</span></span>
-   <span data-ttu-id="d5ec5-124">Pour enregistrer l’état du filtre dans un fichier GraphEdit (. GRF), implémentez l’interface **IPersistStream** .</span><span class="sxs-lookup"><span data-stu-id="d5ec5-124">To save the filter's state in a GraphEdit (.grf) file, implement the **IPersistStream** interface.</span></span> <span data-ttu-id="d5ec5-125">(Cette option est facultative, mais utile pour les tests.)</span><span class="sxs-lookup"><span data-stu-id="d5ec5-125">(This is optional, but useful for testing.)</span></span>

<span data-ttu-id="d5ec5-126">Pour utiliser le filtre de redimensionnement, le filtre doit être inscrit en tant qu’objet COM sur le système de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-126">To use the resizer filter, the filter must be registered as a COM object on the user's system.</span></span> <span data-ttu-id="d5ec5-127">Avant que l’application n’affiche le projet vidéo, interrogez le moteur de rendu de l’interface [**IRenderEngine2**](irenderengine2.md) et appelez [**IRenderEngine2 :: SETRESIZERGUID**](irenderengine2-setresizerguid.md) avec le CLSID du filtre de redimensionnement.</span><span class="sxs-lookup"><span data-stu-id="d5ec5-127">Before the application renders the video project, query the Render Engine for the [**IRenderEngine2**](irenderengine2.md) interface and call [**IRenderEngine2::SetResizerGUID**](irenderengine2-setresizerguid.md) with the CLSID of the resizer filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5ec5-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5ec5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5ec5-129">Rendu d’un projet</span><span class="sxs-lookup"><span data-stu-id="d5ec5-129">Rendering a Project</span></span>](rendering-a-project.md)
</dt> </dl>

 

 



