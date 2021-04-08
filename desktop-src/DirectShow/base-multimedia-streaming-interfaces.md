---
description: Interfaces de base de diffusion multimédia
ms.assetid: a94dbb64-dfca-4c24-8c11-761835faf8a8
title: Interfaces de base de diffusion multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b715a68bd65a2fa3a3923edf10f0e2d1f6c22edb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953470"
---
# <a name="base-multimedia-streaming-interfaces"></a><span data-ttu-id="5865f-103">Interfaces de base de diffusion multimédia</span><span class="sxs-lookup"><span data-stu-id="5865f-103">Base Multimedia Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="5865f-104">Ces API sont déconseillées.</span><span class="sxs-lookup"><span data-stu-id="5865f-104">These APIs are deprecated.</span></span> <span data-ttu-id="5865f-105">Les applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="5865f-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="5865f-106">Les interfaces de base de diffusion multimédia en continu offrent un moyen d’accéder par programmation aux flux multimédias.</span><span class="sxs-lookup"><span data-stu-id="5865f-106">The base multimedia streaming interfaces provide a programmatic way to access multimedia streams.</span></span> <span data-ttu-id="5865f-107">Toutefois, l’utilisation d’une interface de base pour accéder à un type de données spécifique peut limiter la quantité de contrôle dont vous disposez sur les données, de sorte que les développeurs de médias doivent créer des versions dérivées de ces interfaces qui offrent un contrôle plus puissant sur les fonctionnalités uniques de leur type de média.</span><span class="sxs-lookup"><span data-stu-id="5865f-107">However, using a base interface to access a specific type of data can limit the amount of control you have over the data, so media developers should create derived versions of these interfaces that provide more powerful control over the unique capabilities of their media type.</span></span>



| <span data-ttu-id="5865f-108">Interface</span><span class="sxs-lookup"><span data-stu-id="5865f-108">Interface</span></span>                                      | <span data-ttu-id="5865f-109">Description</span><span class="sxs-lookup"><span data-stu-id="5865f-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5865f-110">**IMultiMediaStream**</span><span class="sxs-lookup"><span data-stu-id="5865f-110">**IMultiMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) | <span data-ttu-id="5865f-111">Définit comment accéder à l’objet de flux multimédia de plus haut niveau ; cet objet contient et permet d’accéder à d’autres objets de flux.</span><span class="sxs-lookup"><span data-stu-id="5865f-111">Defines how to access the highest-level multimedia stream object; this object contains and provides access to other stream objects.</span></span> <span data-ttu-id="5865f-112">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) possède des méthodes qui énumèrent ou récupèrent des flux spécifiques, ainsi que la vérification de la durée totale du flux et la recherche dans le flux.</span><span class="sxs-lookup"><span data-stu-id="5865f-112">[**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) has methods that enumerate or retrieve specific streams, as well as checking the stream's total time duration and seeking within the stream.</span></span>                                                                                                       |
| [<span data-ttu-id="5865f-113">**IMediaStream**</span><span class="sxs-lookup"><span data-stu-id="5865f-113">**IMediaStream**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)           | <span data-ttu-id="5865f-114">Définit un objet de flux générique.</span><span class="sxs-lookup"><span data-stu-id="5865f-114">Defines a generic stream object.</span></span> <span data-ttu-id="5865f-115">Utilisez ses méthodes pour récupérer un pointeur vers le flux, obtenir des informations sur le flux et créer des exemples à partir des données de flux.</span><span class="sxs-lookup"><span data-stu-id="5865f-115">Use its methods to retrieve a pointer to the stream, get information about the stream, and create samples from the stream data.</span></span> <span data-ttu-id="5865f-116">Vous pouvez également créer des exemples de flux partagés, auxquels plusieurs flux peuvent accéder sans dupliquer les données de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="5865f-116">You can also create shared stream samples, which multiple streams can access without duplicating the sample's data.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="5865f-117">**IStreamSample**</span><span class="sxs-lookup"><span data-stu-id="5865f-117">**IStreamSample**</span></span>](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)         | <span data-ttu-id="5865f-118">Contrôle le comportement d’un exemple de flux spécifique.</span><span class="sxs-lookup"><span data-stu-id="5865f-118">Controls the behavior of a specific stream sample.</span></span> <span data-ttu-id="5865f-119">Vous pouvez récupérer le flux qui a créé l’exemple, vérifier l’heure de début et de fin et l’état d’achèvement de l’exemple, et exécuter une fonction définie par l’utilisateur sur l’exemple lui-même (à l’aide de la méthode [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) ).</span><span class="sxs-lookup"><span data-stu-id="5865f-119">You can retrieve the stream that created the sample, check the sample's start and end times and completion status, and perform a user-defined function on the sample itself (through the [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) method).</span></span> <span data-ttu-id="5865f-120">En règle générale, la méthode de mise à jour traite les exemples de données de manière appropriée, comme le rendu des données vidéo ou la lecture de données audio.</span><span class="sxs-lookup"><span data-stu-id="5865f-120">Typically, the Update method processes the sample data in an appropriate manner, such as rendering video data or playing back audio data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5865f-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5865f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5865f-122">Liste des interfaces de diffusion multimédia</span><span class="sxs-lookup"><span data-stu-id="5865f-122">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



