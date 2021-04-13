---
title: Pour implémenter le rappel OnSample
description: Pour implémenter le rappel OnSample
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- ASF (Advanced Systems Format), implémentation du rappel OnStatus
- ASF (format avancé des systèmes), implémentation du rappel OnStatus
- ASF (Advanced Systems Format), rappel OnStatus
- ASF (format avancé des systèmes), rappel OnStatus
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- lecteurs asynchrones, implémenter le rappel OnStatus
- OnStatus, méthode de rappel, implémentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f19e81df5ee4769e1353c299a14626cb1a9aed
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314515"
---
# <a name="to-implement-the-onsample-callback"></a><span data-ttu-id="83085-111">Pour implémenter le rappel OnSample</span><span class="sxs-lookup"><span data-stu-id="83085-111">To Implement the OnSample Callback</span></span>

<span data-ttu-id="83085-112">Le lecteur asynchrone fournit des exemples à l’application de contrôle dans l’ordre de la présentation en effectuant des appels à la méthode de rappel [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .</span><span class="sxs-lookup"><span data-stu-id="83085-112">The asynchronous reader delivers samples to the controlling application in presentation-time order by making calls to the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) callback method.</span></span> <span data-ttu-id="83085-113">Quand vous créez une application à l’aide du lecteur asynchrone, vous devez implémenter **OnSample** pour gérer les exemples non compressés.</span><span class="sxs-lookup"><span data-stu-id="83085-113">When you create an application using the asynchronous reader, you must implement **OnSample** to deal with uncompressed samples.</span></span> <span data-ttu-id="83085-114">En règle générale, les fonctions ou les méthodes créées pour afficher le contenu sont appelées à partir de **OnSample**.</span><span class="sxs-lookup"><span data-stu-id="83085-114">Typically, functions or methods created to render content will be called from within **OnSample**.</span></span>

<span data-ttu-id="83085-115">L’implémentation classique du rappel **OnSample** comprend les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="83085-115">Typical implementation of the **OnSample** callback includes the following steps.</span></span>

1.  <span data-ttu-id="83085-116">Récupérez l’emplacement et la taille de la mémoire tampon contenant l’exemple en appelant [**INSSBuffer :: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) sur la mémoire tampon transmise en tant que *pSample*.</span><span class="sxs-lookup"><span data-stu-id="83085-116">Retrieve the location and size of the buffer containing the sample by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) on the buffer passed as *pSample*.</span></span>
2.  <span data-ttu-id="83085-117">Créer une branche de votre logique en fonction du numéro de sortie.</span><span class="sxs-lookup"><span data-stu-id="83085-117">Branch your logic depending upon the output number.</span></span> <span data-ttu-id="83085-118">Le numéro de sortie est passé à **OnSample** en tant que *dwOutputNumber*.</span><span class="sxs-lookup"><span data-stu-id="83085-118">The output number is passed to **OnSample** as *dwOutputNumber*.</span></span>
3.  <span data-ttu-id="83085-119">Incluez la logique de rendu pour chaque numéro de sortie que vous souhaitez prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="83085-119">Include rendering logic for each output number you want to support.</span></span> <span data-ttu-id="83085-120">Si vous affichez des exemples à partir de plusieurs sorties, vous devrez peut-être synchroniser votre rendu.</span><span class="sxs-lookup"><span data-stu-id="83085-120">If you are rendering samples from multiple outputs, you may need to synchronize your rendering.</span></span>

<span data-ttu-id="83085-121">Les applications qui fournissent des échantillons compressés à partir de fichiers ASF doivent implémenter la méthode de rappel [**IWMReaderCallbackAdvanced :: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="83085-121">Applications that deliver compressed samples from ASF files need to implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span> <span data-ttu-id="83085-122">**OnStreamSample** fonctionne presque de la même façon que **OnSample**, à ceci près qu’il reçoit des échantillons compressés par numéro de flux au lieu d’exemples non compressés par numéro de sortie.</span><span class="sxs-lookup"><span data-stu-id="83085-122">**OnStreamSample** functions almost identically to **OnSample**, except that it receives compressed samples by stream number instead of uncompressed samples by output number.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83085-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83085-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83085-124">**Interface IWMReaderCallback**</span><span class="sxs-lookup"><span data-stu-id="83085-124">**IWMReaderCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[<span data-ttu-id="83085-125">**Interface IWMReaderCallbackAdvanced**</span><span class="sxs-lookup"><span data-stu-id="83085-125">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="83085-126">**Lecture des fichiers avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="83085-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="83085-127">**Utilisation des méthodes de rappel**</span><span class="sxs-lookup"><span data-stu-id="83085-127">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




