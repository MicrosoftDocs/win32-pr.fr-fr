---
description: Gestion des événements de redessin dans la capture vidéo
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Gestion des événements de redessin dans la capture vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418ca42ebc80b338b077336fdac48a01dfb8509e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950314"
---
# <a name="handling-repaint-events-in-video-capture"></a><span data-ttu-id="b49b6-103">Gestion des événements de redessin dans la capture vidéo</span><span class="sxs-lookup"><span data-stu-id="b49b6-103">Handling Repaint Events in Video Capture</span></span>

<span data-ttu-id="b49b6-104">Si vous générez un graphique de capture vidéo sans utiliser l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) et que vous affichez un aperçu de la vidéo à l’aide de l’ancien filtre de convertisseur vidéo, vous devez remplacer la gestion par défaut des événements de [**\_ redessin ce**](ec-repaint.md) .</span><span class="sxs-lookup"><span data-stu-id="b49b6-104">If you build a video capture graph without using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, and you preview the video using the old Video Renderer filter, then you should override the default handling for [**EC\_REPAINT**](ec-repaint.md) events.</span></span> <span data-ttu-id="b49b6-105">Interrogez le gestionnaire du graphique de filtre pour l’interface [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) et appelez la méthode [**IMediaEvent :: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) avec la valeur EC \_ Repaint :</span><span class="sxs-lookup"><span data-stu-id="b49b6-105">Query the Filter Graph Manager for the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface and call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the value EC\_REPAINT:</span></span>


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



<span data-ttu-id="b49b6-106">Cela évite une erreur possible qui peut endommager votre fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="b49b6-106">This prevents a possible error that can corrupt your capture file.</span></span> <span data-ttu-id="b49b6-107">Si l’utilisateur couvre et Découvre la fenêtre d’aperçu, le filtre de convertisseur vidéo reçoit un message de \_ peinture WM.</span><span class="sxs-lookup"><span data-stu-id="b49b6-107">If the user covers and uncovers the preview window, the Video Renderer filter receives a WM\_PAINT message.</span></span> <span data-ttu-id="b49b6-108">Par défaut, le convertisseur vidéo demande un nouveau Frame, et le gestionnaire de graphique de filtre met en pause le graphique pour signaler une autre image vidéo.</span><span class="sxs-lookup"><span data-stu-id="b49b6-108">By default, the Video Renderer requests a new frame, and the Filter Graph Manager pauses the graph in order to cue another video frame.</span></span> <span data-ttu-id="b49b6-109">Si cela se produit pendant que le graphique écrit un fichier, le fichier est endommagé.</span><span class="sxs-lookup"><span data-stu-id="b49b6-109">If that happens while the graph is writing a file, it will corrupt the file.</span></span> <span data-ttu-id="b49b6-110">La substitution du comportement par défaut \_ de REDESSIN ce par défaut empêche le convertisseur de demander un nouveau Frame.</span><span class="sxs-lookup"><span data-stu-id="b49b6-110">Overriding the default EC\_REPAINT behavior prevents the renderer from requesting a new frame.</span></span>

<span data-ttu-id="b49b6-111">Vous n’avez pas à effectuer cette étape si vous utilisez l’interface **ICaptureGraphBuilder2** , car le générateur de graphiques de capture le fait automatiquement pour vous.</span><span class="sxs-lookup"><span data-stu-id="b49b6-111">You do not have to perform this step if you are using the **ICaptureGraphBuilder2** interface, because the Capture Graph Builder does it for you automatically.</span></span> <span data-ttu-id="b49b6-112">En outre, ce n’est pas obligatoire si vous utilisez le convertisseur de mixage vidéo (VMR) pour la version préliminaire.</span><span class="sxs-lookup"><span data-stu-id="b49b6-112">Also, it is not required if you are using the Video Mixing Renderer (VMR) for preview.</span></span> <span data-ttu-id="b49b6-113">VMR a toujours le frame le plus récent disponible. il n’envoie donc pas d' \_ événements de REDESSIN ce.</span><span class="sxs-lookup"><span data-stu-id="b49b6-113">The VMR always has the most recent frame available, so it does not send EC\_REPAINT events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b49b6-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b49b6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b49b6-115">Rubriques avancées sur la capture</span><span class="sxs-lookup"><span data-stu-id="b49b6-115">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="b49b6-116">Notification d’événement dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="b49b6-116">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



