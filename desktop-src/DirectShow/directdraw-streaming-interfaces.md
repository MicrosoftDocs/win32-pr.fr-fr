---
description: Interfaces de streaming DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Interfaces de streaming DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033469"
---
# <a name="directdraw-streaming-interfaces"></a><span data-ttu-id="0b219-103">Interfaces de streaming DirectDraw</span><span class="sxs-lookup"><span data-stu-id="0b219-103">DirectDraw Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="0b219-104">Ces API sont déconseillées.</span><span class="sxs-lookup"><span data-stu-id="0b219-104">These APIs are deprecated.</span></span> <span data-ttu-id="0b219-105">Les applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="0b219-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="0b219-106">Si vous utilisez des formats vidéo pris en charge par DirectDraw dans vos flux, les interfaces suivantes vous offrent un contrôle plus puissant des données que les interfaces de base plus génériques.</span><span class="sxs-lookup"><span data-stu-id="0b219-106">If you use DirectDraw-supported video formats in your streams, the following interfaces give you more powerful control over the data than the more generic base interfaces.</span></span>



| <span data-ttu-id="0b219-107">Interface</span><span class="sxs-lookup"><span data-stu-id="0b219-107">Interface</span></span>                                                  | <span data-ttu-id="0b219-108">Description</span><span class="sxs-lookup"><span data-stu-id="0b219-108">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b219-109">**IDirectDrawMediaStream**</span><span class="sxs-lookup"><span data-stu-id="0b219-109">**IDirectDrawMediaStream**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | <span data-ttu-id="0b219-110">Définit et récupère le format de flux et l’objet DirectDraw associé au flux multimédia ; Cette interface est dérivée de [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream).</span><span class="sxs-lookup"><span data-stu-id="0b219-110">Sets and retrieves the stream format and the DirectDraw object associated with the media stream; this interface derives from [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream).</span></span> <span data-ttu-id="0b219-111">Vous pouvez également utiliser cette interface pour créer des exemples vidéo.</span><span class="sxs-lookup"><span data-stu-id="0b219-111">You can also use this interface to create video samples.</span></span> |
| [<span data-ttu-id="0b219-112">**IDirectDrawStreamSample**</span><span class="sxs-lookup"><span data-stu-id="0b219-112">**IDirectDrawStreamSample**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | <span data-ttu-id="0b219-113">Vous permet d’attacher des échantillons vidéo à des surfaces DirectDraw ; Cette interface est dérivée de l’interface [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) .</span><span class="sxs-lookup"><span data-stu-id="0b219-113">Enables you to attach video samples to DirectDraw surfaces; this interface derives from the [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) interface.</span></span> <span data-ttu-id="0b219-114">Chaque surface attachée comprend un rectangle de découpage pour faciliter le rendu.</span><span class="sxs-lookup"><span data-stu-id="0b219-114">Each attached surface includes a clipping rectangle to make rendering easier.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0b219-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b219-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b219-116">Liste des interfaces de diffusion multimédia</span><span class="sxs-lookup"><span data-stu-id="0b219-116">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



