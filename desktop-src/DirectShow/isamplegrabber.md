---
description: L’interface ISampleGrabber est exposée par l’exemple de filtre d’accrochage. Il permet à une application de récupérer des exemples de médias individuels lorsqu’ils se déplacent dans le graphique de filtre.
ms.assetid: 97cf1127-d5d7-4e6a-a371-19f24e497a7f
title: Interface ISampleGrabber (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f6e923032e74f88dceb1c2465e27dab9423bae1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523472"
---
# <a name="isamplegrabber-interface"></a><span data-ttu-id="e6730-104">Interface ISampleGrabber</span><span class="sxs-lookup"><span data-stu-id="e6730-104">ISampleGrabber interface</span></span>

> [!Note]  
> <span data-ttu-id="e6730-105">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e6730-105">\[Deprecated.</span></span> <span data-ttu-id="e6730-106">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e6730-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e6730-107">L’interface **ISampleGrabber** est exposée par l’exemple de filtre d' [**accrochage**](sample-grabber-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="e6730-107">The **ISampleGrabber** interface is exposed by the [**Sample Grabber**](sample-grabber-filter.md) filter.</span></span> <span data-ttu-id="e6730-108">Il permet à une application de récupérer des exemples de médias individuels lorsqu’ils se déplacent dans le graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="e6730-108">It enables an application to retrieve individual media samples as they move through the filter graph.</span></span>

## <a name="members"></a><span data-ttu-id="e6730-109">Membres</span><span class="sxs-lookup"><span data-stu-id="e6730-109">Members</span></span>

<span data-ttu-id="e6730-110">L’interface **ISampleGrabber** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e6730-110">The **ISampleGrabber** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e6730-111">**ISampleGrabber** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e6730-111">**ISampleGrabber** also has these types of members:</span></span>

-   [<span data-ttu-id="e6730-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e6730-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e6730-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e6730-113">Methods</span></span>

<span data-ttu-id="e6730-114">L’interface **ISampleGrabber** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e6730-114">The **ISampleGrabber** interface has these methods.</span></span>



| <span data-ttu-id="e6730-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="e6730-115">Method</span></span>                                                                | <span data-ttu-id="e6730-116">Description</span><span class="sxs-lookup"><span data-stu-id="e6730-116">Description</span></span>                                                                                                                       |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6730-117">**GetConnectedMediaType**</span><span class="sxs-lookup"><span data-stu-id="e6730-117">**GetConnectedMediaType**</span></span>](isamplegrabber-getconnectedmediatype.md) | <span data-ttu-id="e6730-118">Récupère le type de média pour la connexion sur la broche d’entrée de la accroche d’échantillon.</span><span class="sxs-lookup"><span data-stu-id="e6730-118">Retrieves the media type for the connection on the input pin of Sample Grabber.</span></span><br/>                                        |
| [<span data-ttu-id="e6730-119">**GetCurrentBuffer**</span><span class="sxs-lookup"><span data-stu-id="e6730-119">**GetCurrentBuffer**</span></span>](isamplegrabber-getcurrentbuffer.md)           | <span data-ttu-id="e6730-120">Récupère une copie de l’exemple que le filtre a reçu le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="e6730-120">Retrieves a copy of the sample that the filter received most recently.</span></span><br/>                                                 |
| [<span data-ttu-id="e6730-121">**GetCurrentSample**</span><span class="sxs-lookup"><span data-stu-id="e6730-121">**GetCurrentSample**</span></span>](isamplegrabber-getcurrentsample.md)           | <span data-ttu-id="e6730-122">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="e6730-122">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="e6730-123">**SetBufferSamples**</span><span class="sxs-lookup"><span data-stu-id="e6730-123">**SetBufferSamples**</span></span>](isamplegrabber-setbuffersamples.md)           | <span data-ttu-id="e6730-124">Spécifie s’il faut copier les exemples de données dans une mémoire tampon à mesure qu’elle passe par le filtre.</span><span class="sxs-lookup"><span data-stu-id="e6730-124">Specifies whether to copy sample data into a buffer as it goes through the filter.</span></span><br/>                                     |
| [<span data-ttu-id="e6730-125">**SetCallback**</span><span class="sxs-lookup"><span data-stu-id="e6730-125">**SetCallback**</span></span>](isamplegrabber-setcallback.md)                     | <span data-ttu-id="e6730-126">Spécifie une méthode de rappel à appeler sur les exemples entrants.</span><span class="sxs-lookup"><span data-stu-id="e6730-126">Specifies a callback method to call on incoming samples.</span></span><br/>                                                               |
| [<span data-ttu-id="e6730-127">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="e6730-127">**SetMediaType**</span></span>](isamplegrabber-setmediatype.md)                   | <span data-ttu-id="e6730-128">Spécifie le type de média pour la connexion sur la broche d’entrée de la accroche d’échantillon.</span><span class="sxs-lookup"><span data-stu-id="e6730-128">Specifies the media type for the connection on the input pin of the Sample Grabber.</span></span><br/>                                    |
| [<span data-ttu-id="e6730-129">**SetOneShot**</span><span class="sxs-lookup"><span data-stu-id="e6730-129">**SetOneShot**</span></span>](isamplegrabber-setoneshot.md)                       | <span data-ttu-id="e6730-130">Spécifie si le filtre d' [**accrochage**](sample-grabber-filter.md) de l’exemple s’arrête une fois que le filtre a reçu un exemple.</span><span class="sxs-lookup"><span data-stu-id="e6730-130">Specifies whether the [**Sample Grabber**](sample-grabber-filter.md) filter halts after the filter receives a sample.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e6730-131">Notes</span><span class="sxs-lookup"><span data-stu-id="e6730-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e6730-132">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="e6730-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e6730-133">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e6730-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e6730-134">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e6730-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e6730-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6730-135">Requirements</span></span>



| <span data-ttu-id="e6730-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6730-136">Requirement</span></span> | <span data-ttu-id="e6730-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6730-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6730-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6730-138">Header</span></span><br/>  | <dl> <span data-ttu-id="e6730-139"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6730-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e6730-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6730-140">Library</span></span><br/> | <dl> <span data-ttu-id="e6730-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6730-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6730-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6730-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6730-143">Utilisation de l’exemple d’accrochage</span><span class="sxs-lookup"><span data-stu-id="e6730-143">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> </dl>

 

 
