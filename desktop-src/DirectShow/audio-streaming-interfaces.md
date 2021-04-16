---
description: Interfaces de streaming audio
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Interfaces de streaming audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68210beef0b05fcfc89ae5005c485fbc4b74d40f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522484"
---
# <a name="audio-streaming-interfaces"></a><span data-ttu-id="ba61f-103">Interfaces de streaming audio</span><span class="sxs-lookup"><span data-stu-id="ba61f-103">Audio Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="ba61f-104">Ces API sont déconseillées.</span><span class="sxs-lookup"><span data-stu-id="ba61f-104">These APIs are deprecated.</span></span> <span data-ttu-id="ba61f-105">Les applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="ba61f-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 



| <span data-ttu-id="ba61f-106">Interface</span><span class="sxs-lookup"><span data-stu-id="ba61f-106">Interface</span></span>                                        | <span data-ttu-id="ba61f-107">Description</span><span class="sxs-lookup"><span data-stu-id="ba61f-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba61f-108">**IAudioMediaStream**</span><span class="sxs-lookup"><span data-stu-id="ba61f-108">**IAudioMediaStream**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | <span data-ttu-id="ba61f-109">Contrôle les flux de média audio.</span><span class="sxs-lookup"><span data-stu-id="ba61f-109">Controls audio media streams.</span></span> <span data-ttu-id="ba61f-110">Cette interface hérite de l’interface [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) et est utilisée pour créer un ou plusieurs objets [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .</span><span class="sxs-lookup"><span data-stu-id="ba61f-110">This interface inherits from the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and is used to create one or more [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) objects.</span></span> <span data-ttu-id="ba61f-111">Il est également utilisé pour définir et récupérer le format actuel des données de flux.</span><span class="sxs-lookup"><span data-stu-id="ba61f-111">It is also used to set and retrieve the current format of the stream data.</span></span>                                                                                                            |
| [<span data-ttu-id="ba61f-112">**IAudioStreamSample**</span><span class="sxs-lookup"><span data-stu-id="ba61f-112">**IAudioStreamSample**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | <span data-ttu-id="ba61f-113">Récupère des informations à partir des objets de données [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) sous-jacents.</span><span class="sxs-lookup"><span data-stu-id="ba61f-113">Retrieves information from the underlying [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) data objects.</span></span>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="ba61f-114">**IMemoryData**</span><span class="sxs-lookup"><span data-stu-id="ba61f-114">**IMemoryData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | <span data-ttu-id="ba61f-115">Contient des méthodes qui définissent et récupèrent les données de mémoire sur les objets de données audio.</span><span class="sxs-lookup"><span data-stu-id="ba61f-115">Contains methods that set and retrieve memory data on audio data objects.</span></span> <span data-ttu-id="ba61f-116">Les objets de données audio fournissent les données sous-jacentes auxquelles les exemples de flux accèdent.</span><span class="sxs-lookup"><span data-stu-id="ba61f-116">Audio data objects provide the underlying data that stream samples access.</span></span> <span data-ttu-id="ba61f-117">Cette interface fournit un moyen d’initialiser les mémoires tampons de mémoire et de définir les quantités réelles de données audio dans les objets.</span><span class="sxs-lookup"><span data-stu-id="ba61f-117">This interface provides a way to initialize memory buffers and to set actual amounts of audio data in the objects.</span></span> <span data-ttu-id="ba61f-118">En outre, la méthode [**IMemoryData :: GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) peut être utilisée pour récupérer des données de mémoire audio.</span><span class="sxs-lookup"><span data-stu-id="ba61f-118">Additionally, the [**IMemoryData::GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) method can be used to retrieve audio memory data.</span></span> |
| [<span data-ttu-id="ba61f-119">**IAudioData**</span><span class="sxs-lookup"><span data-stu-id="ba61f-119">**IAudioData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | <span data-ttu-id="ba61f-120">Fournit des méthodes qui permettent aux applications de définir et d’extraire les données audio sous-jacentes auxquelles les flux audio feront référence.</span><span class="sxs-lookup"><span data-stu-id="ba61f-120">Provides methods that enable applications to set and get the underlying audio data that audio streams will reference.</span></span> <span data-ttu-id="ba61f-121">Le format de données audio est défini dans la structure [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ba61f-121">The audio data format is set in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="ba61f-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ba61f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba61f-123">Liste des interfaces de diffusion multimédia</span><span class="sxs-lookup"><span data-stu-id="ba61f-123">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
