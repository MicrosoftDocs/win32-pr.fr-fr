---
description: Objet de diffusion multimédia en continu et hiérarchie d’interface
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Objet de diffusion multimédia en continu et hiérarchie d’interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869610"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a><span data-ttu-id="beab8-103">Objet de diffusion multimédia en continu et hiérarchie d’interface</span><span class="sxs-lookup"><span data-stu-id="beab8-103">Multimedia Streaming Object and Interface Hierarchy</span></span>

> [!Note]  
> <span data-ttu-id="beab8-104">Ces API sont déconseillées.</span><span class="sxs-lookup"><span data-stu-id="beab8-104">These APIs are deprecated.</span></span> <span data-ttu-id="beab8-105">Les applications doivent utiliser le filtre d' [**accrochage d’exemple**](sample-grabber-filter.md) ou implémenter un filtre personnalisé pour obtenir des données à partir d’un graphique de filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="beab8-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="beab8-106">Le diagramme suivant illustre la hiérarchie d’objets utilisée dans la diffusion multimédia en continu.</span><span class="sxs-lookup"><span data-stu-id="beab8-106">The following diagram shows the object hierarchy used in multimedia streaming.</span></span>

![hiérarchie d’objets multimediastreaming](images/mmstream02.png)

<span data-ttu-id="beab8-108">L’architecture de diffusion multimédia en continu définit trois types généraux d’objets :</span><span class="sxs-lookup"><span data-stu-id="beab8-108">The multimedia streaming architecture defines three general type of object:</span></span>

-   <span data-ttu-id="beab8-109">L’objet **AMMultimediaStream** expose l’interface [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) .</span><span class="sxs-lookup"><span data-stu-id="beab8-109">The **AMMultimediaStream** object exposes the [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) interface.</span></span> <span data-ttu-id="beab8-110">En interne, cet objet encapsule le graphique de filtre DirectShow.</span><span class="sxs-lookup"><span data-stu-id="beab8-110">Internally, this object wraps the DirectShow filter graph.</span></span>
-   <span data-ttu-id="beab8-111">Les objets de *flux de média* exposent l’interface [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) et sont spécifiques aux données.</span><span class="sxs-lookup"><span data-stu-id="beab8-111">*Media stream* objects expose the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and are data specific.</span></span> <span data-ttu-id="beab8-112">L’objet AMMultimediaStream contient un ou plusieurs flux de média.</span><span class="sxs-lookup"><span data-stu-id="beab8-112">The AMMultimediaStream object contains one or more media streams.</span></span>
-   <span data-ttu-id="beab8-113">Les exemples d’objets *Stream* contiennent les données d’un flux particulier.</span><span class="sxs-lookup"><span data-stu-id="beab8-113">*Stream sample* objects contain the data for a particular stream.</span></span>

<span data-ttu-id="beab8-114">Les objets de flux multimédia suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="beab8-114">The following media stream objects are supported:</span></span>

-   <span data-ttu-id="beab8-115">Flux audio.</span><span class="sxs-lookup"><span data-stu-id="beab8-115">Audio stream.</span></span> <span data-ttu-id="beab8-116">Expose l’interface [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) .</span><span class="sxs-lookup"><span data-stu-id="beab8-116">Exposes the [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) interface.</span></span>
-   <span data-ttu-id="beab8-117">Flux DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="beab8-117">DirectDraw stream.</span></span> <span data-ttu-id="beab8-118">Représente un flux vidéo rendu sur une surface DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="beab8-118">Represents a video stream that is rendered to a DirectDraw surface.</span></span> <span data-ttu-id="beab8-119">Expose l’interface [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) .</span><span class="sxs-lookup"><span data-stu-id="beab8-119">Exposes the [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) interface.</span></span>
-   <span data-ttu-id="beab8-120">Flux de type de média.</span><span class="sxs-lookup"><span data-stu-id="beab8-120">Media type stream.</span></span> <span data-ttu-id="beab8-121">Représente des données arbitraires.</span><span class="sxs-lookup"><span data-stu-id="beab8-121">Represents arbitrary data.</span></span> <span data-ttu-id="beab8-122">Expose l’interface [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) .</span><span class="sxs-lookup"><span data-stu-id="beab8-122">Exposes the [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) interface.</span></span>

<span data-ttu-id="beab8-123">Chaque objet de flux de média crée son propre type d’objet de flux :</span><span class="sxs-lookup"><span data-stu-id="beab8-123">Each media stream object creates its own kind of stream sample object:</span></span>

-   <span data-ttu-id="beab8-124">Les flux audio créent des échantillons audio qui exposent l’interface [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .</span><span class="sxs-lookup"><span data-stu-id="beab8-124">Audio streams create audio samples, which expose the [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) interface.</span></span>
-   <span data-ttu-id="beab8-125">Les flux DirectDraw créent des exemples DirectDraw qui exposent l’interface [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="beab8-125">DirectDraw streams create DirectDraw samples, which expose the [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) interface.</span></span>
-   <span data-ttu-id="beab8-126">Les flux de type de média créent des exemples de type de média qui exposent l’interface [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) .</span><span class="sxs-lookup"><span data-stu-id="beab8-126">Media type streams create media type samples, which expose the [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) interface.</span></span>

<span data-ttu-id="beab8-127">Le diagramme suivant illustre la hiérarchie d’interface pour les interfaces listées précédemment :</span><span class="sxs-lookup"><span data-stu-id="beab8-127">The following diagram shows the interface hierarchy for the interfaces listed previously:</span></span>

![hiérarchie de l’interface multimediastreaming](images/mmstream01.png)

 

 



