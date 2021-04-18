---
description: Broches de port vidéo dans la capture de fichiers
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Broches de port vidéo dans la capture de fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520420"
---
# <a name="video-port-pins-in-file-capture"></a><span data-ttu-id="a86af-103">Broches de port vidéo dans la capture de fichiers</span><span class="sxs-lookup"><span data-stu-id="a86af-103">Video Port Pins in File Capture</span></span>

<span data-ttu-id="a86af-104">Si le périphérique de capture a un port vidéo, le code pin du port vidéo doit être connecté à un convertisseur vidéo, même si vous souhaitez uniquement effectuer une capture dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="a86af-104">If the capture device has a video port, the video port pin must be connected to a video renderer, even if you only want to capture to a file.</span></span>

<span data-ttu-id="a86af-105">Si vous appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) avec la valeur **broche \_ catégorie \_ capturer** et que l’appareil a une broche de port vidéo, le générateur de graphiques de capture connecte automatiquement la broche de port vidéo au filtre de [mixage de superposition](overlay-mixer-filter.md) et connecte le mélangeur de superposition au convertisseur vidéo.</span><span class="sxs-lookup"><span data-stu-id="a86af-105">If you call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the value **PIN\_CATEGORY\_CAPTURE** and the device has a video port pin, the Capture Graph Builder automatically connects the video port pin to the [Overlay Mixer](overlay-mixer-filter.md) filter and connects the Overlay Mixer to the Video Renderer.</span></span> <span data-ttu-id="a86af-106">Le générateur de graphiques de capture masque la fenêtre vidéo en appelant [**IVideoWindow ::p ut \_ automatique**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) avec la valeur **OAFALSE**.</span><span class="sxs-lookup"><span data-stu-id="a86af-106">The Capture Graph Builder hides the video window by calling [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value **OAFALSE**.</span></span> <span data-ttu-id="a86af-107">Si l’application appelle ensuite **RenderStream** avec la version préliminaire de la **\_ catégorie \_ pin**, le générateur de graphiques de capture appelle la fonction d' **\_ affichage** automatique avec la valeur **OATRUE**, afin d’afficher la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="a86af-107">If the application later calls **RenderStream** with **PIN\_CATEGORY\_PREVIEW**, the Capture Graph Builder calls **put\_AutoShow** with the value **OATRUE**, in order to show the video window.</span></span>

<span data-ttu-id="a86af-108">Après avoir appelé **RenderStream** avec **la \_ \_ capture de catégorie pin**, vous pouvez vérifier s’il a ajouté le convertisseur vidéo en interrogeant le gestionnaire du graphique de filtre pour l’interface [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="a86af-108">After you call **RenderStream** with **PIN\_CATEGORY\_CAPTURE**, you can check whether it has added the Video Renderer by querying the Filter Graph Manager for the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a86af-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a86af-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a86af-110">Capture vidéo dans un fichier</span><span class="sxs-lookup"><span data-stu-id="a86af-110">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



