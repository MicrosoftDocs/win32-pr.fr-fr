---
description: Exemple EVRPresenter
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Exemple EVRPresenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111774"
---
# <a name="evrpresenter-sample"></a><span data-ttu-id="07c35-103">Exemple EVRPresenter</span><span class="sxs-lookup"><span data-stu-id="07c35-103">EVRPresenter Sample</span></span>

<span data-ttu-id="07c35-104">Montre comment implémenter un présentateur personnalisé pour le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR).</span><span class="sxs-lookup"><span data-stu-id="07c35-104">Shows how to implement a custom presenter for the [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR).</span></span> <span data-ttu-id="07c35-105">Le présentateur personnalisé peut être utilisé avec le filtre DirectShow EVR ou le récepteur EVR Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="07c35-105">The custom presenter can be used with either the DirectShow EVR filter or the Microsoft Media Foundation EVR sink.</span></span>

## <a name="apis-demonstrated"></a><span data-ttu-id="07c35-106">API illustrées</span><span class="sxs-lookup"><span data-stu-id="07c35-106">APIs Demonstrated</span></span>

<span data-ttu-id="07c35-107">Cet exemple illustre les interfaces de Media Foundation suivantes :</span><span class="sxs-lookup"><span data-stu-id="07c35-107">This sample demonstrates the following Media Foundation interfaces:</span></span>

-   [<span data-ttu-id="07c35-108">**IMFClockStateSink**</span><span class="sxs-lookup"><span data-stu-id="07c35-108">**IMFClockStateSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [<span data-ttu-id="07c35-109">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="07c35-109">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="07c35-110">**IMFTopologyServiceLookupClient**</span><span class="sxs-lookup"><span data-stu-id="07c35-110">**IMFTopologyServiceLookupClient**</span></span>](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [<span data-ttu-id="07c35-111">**IMFVideoDeviceID**</span><span class="sxs-lookup"><span data-stu-id="07c35-111">**IMFVideoDeviceID**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [<span data-ttu-id="07c35-112">**IMFVideoDisplayControl**</span><span class="sxs-lookup"><span data-stu-id="07c35-112">**IMFVideoDisplayControl**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [<span data-ttu-id="07c35-113">**IMFVideoPresenter**</span><span class="sxs-lookup"><span data-stu-id="07c35-113">**IMFVideoPresenter**</span></span>](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a><span data-ttu-id="07c35-114">Utilisation</span><span class="sxs-lookup"><span data-stu-id="07c35-114">Usage</span></span>

<span data-ttu-id="07c35-115">L’exemple EVRPresenter génère une DLL qui est un serveur COM pour le présentateur.</span><span class="sxs-lookup"><span data-stu-id="07c35-115">The EVRPresenter sample builds a DLL that is a COM server for the presenter.</span></span> <span data-ttu-id="07c35-116">Avant d’utiliser le présentateur personnalisé, vous devez inscrire la DLL.</span><span class="sxs-lookup"><span data-stu-id="07c35-116">Before using the custom presenter, you must register the DLL.</span></span>

<span data-ttu-id="07c35-117">Pour utiliser cet exemple dans Media Foundation :</span><span class="sxs-lookup"><span data-stu-id="07c35-117">To use this sample in Media Foundation:</span></span>

1.  <span data-ttu-id="07c35-118">Générez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="07c35-118">Build the sample.</span></span>
2.  <span data-ttu-id="07c35-119">EvrPresenter.dll regsvr32.</span><span class="sxs-lookup"><span data-stu-id="07c35-119">Regsvr32 EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="07c35-120">Générez et exécutez l' [exemple MFPlayer](/previous-versions//bb970516(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="07c35-120">Build and run the [MFPlayer Sample](/previous-versions//bb970516(v=vs.85)).</span></span>
4.  <span data-ttu-id="07c35-121">Dans le menu **fichier** , sélectionnez **ouvrir** un fichier.</span><span class="sxs-lookup"><span data-stu-id="07c35-121">From the **File** menu, select **Open** File.</span></span>
5.  <span data-ttu-id="07c35-122">Dans la boîte de dialogue **ouvrir un fichier** , sélectionnez le **présentateur EVR personnalisé.**</span><span class="sxs-lookup"><span data-stu-id="07c35-122">In the **Open File** dialog box, select **Custom EVR Presenter.**</span></span>
6.  <span data-ttu-id="07c35-123">Sélectionnez un fichier pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="07c35-123">Select a file for playback.</span></span>

<span data-ttu-id="07c35-124">Pour utiliser cet exemple dans DirectShow :</span><span class="sxs-lookup"><span data-stu-id="07c35-124">To use this sample in DirectShow:</span></span>

1.  <span data-ttu-id="07c35-125">Générez l’exemple.</span><span class="sxs-lookup"><span data-stu-id="07c35-125">Build the sample.</span></span>
2.  <span data-ttu-id="07c35-126">Inscrire EvrPresenter.dll.</span><span class="sxs-lookup"><span data-stu-id="07c35-126">Register EvrPresenter.dll.</span></span>
3.  <span data-ttu-id="07c35-127">Générez et exécutez l’exemple EVRPlayer.</span><span class="sxs-lookup"><span data-stu-id="07c35-127">Build and run the EVRPlayer sample.</span></span> <span data-ttu-id="07c35-128">Cet exemple est fourni avec les exemples DirectShow dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="07c35-128">This sample is included with the DirectShow samples in the Windows SDK.</span></span>
4.  <span data-ttu-id="07c35-129">Dans le menu **fichier** , sélectionnez **EVR Presenter**.</span><span class="sxs-lookup"><span data-stu-id="07c35-129">From the **File** menu, select **EVR Presenter**.</span></span>
5.  <span data-ttu-id="07c35-130">Sélectionnez un fichier pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="07c35-130">Select a file for playback.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c35-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07c35-131">Requirements</span></span>



| <span data-ttu-id="07c35-132">Produit</span><span class="sxs-lookup"><span data-stu-id="07c35-132">Product</span></span>                                                        | <span data-ttu-id="07c35-133">Version</span><span class="sxs-lookup"><span data-stu-id="07c35-133">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="07c35-134">SDK Windows</span><span class="sxs-lookup"><span data-stu-id="07c35-134">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="07c35-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="07c35-135">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="07c35-136">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="07c35-136">Downloading the Sample</span></span>

<span data-ttu-id="07c35-137">Cet exemple est disponible dans le [référentiel GitHub des exemples classiques Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span><span class="sxs-lookup"><span data-stu-id="07c35-137">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).</span></span>

## <a name="related-topics"></a><span data-ttu-id="07c35-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07c35-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07c35-139">Convertisseur vidéo amélioré</span><span class="sxs-lookup"><span data-stu-id="07c35-139">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> <dt>

[<span data-ttu-id="07c35-140">Comment écrire un présentateur EVR</span><span class="sxs-lookup"><span data-stu-id="07c35-140">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> <dt>

[<span data-ttu-id="07c35-141">Exemples du kit de développement logiciel Media Foundation</span><span class="sxs-lookup"><span data-stu-id="07c35-141">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
