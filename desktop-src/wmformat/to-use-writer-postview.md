---
title: Pour utiliser l’enregistreur Postview
description: Pour utiliser l’enregistreur Postview
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- ASF (Advanced Systems Format), writer postview
- ASF (Advanced Systems Format), writer postview
- ASF (Advanced Systems Format), postviewing
- ASF (format avancé des systèmes), postviewing
- postview d’écriture
- postviewing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104507835"
---
# <a name="to-use-writer-postview"></a><span data-ttu-id="9bff4-109">Pour utiliser l’enregistreur Postview</span><span class="sxs-lookup"><span data-stu-id="9bff4-109">To Use Writer Postview</span></span>

<span data-ttu-id="9bff4-110">L’objet Writer fournit des fonctionnalités postviewing pour vous permettre de vérifier le contenu écrit sans avoir à configurer l’objet lecteur.</span><span class="sxs-lookup"><span data-stu-id="9bff4-110">The writer object provides postviewing capabilities so that you can verify written content without having to set up the reader object.</span></span> <span data-ttu-id="9bff4-111">L’objet Writer ne prend pas en charge postviewing pour le contenu audio.</span><span class="sxs-lookup"><span data-stu-id="9bff4-111">The writer object does not support postviewing for audio content.</span></span>

<span data-ttu-id="9bff4-112">Le postviewer du writer fonctionne à peu près de la même façon que l’objet lecteur asynchrone, uniquement avec moins de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="9bff4-112">The writer postviewer works in much the same way as the asynchronous reader object, only with fewer features.</span></span> <span data-ttu-id="9bff4-113">Pour plus d’informations sur la lecture des médias numériques, consultez [lecture des fichiers ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="9bff4-113">For detailed information about reading digital media, see [Reading ASF Files](reading-asf-files.md).</span></span>

<span data-ttu-id="9bff4-114">Pour implémenter postviewer, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="9bff4-114">To implement the postviewer, perform the following steps.</span></span>

1.  <span data-ttu-id="9bff4-115">Implémentez le rappel [**IWMWriterPostViewCallback :: OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) .</span><span class="sxs-lookup"><span data-stu-id="9bff4-115">Implement the [**IWMWriterPostViewCallback::OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) callback.</span></span> <span data-ttu-id="9bff4-116">Cette méthode est fondamentalement identique à [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , sauf qu’elle spécifie des numéros de flux au lieu de sorties.</span><span class="sxs-lookup"><span data-stu-id="9bff4-116">This method is essentially the same as [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it specifies stream numbers instead of outputs.</span></span>
2.  <span data-ttu-id="9bff4-117">Configuré pour l’écriture comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="9bff4-117">Set up for writing as usual.</span></span>
3.  <span data-ttu-id="9bff4-118">Obtenez un pointeur vers l’interface [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) de l’objet writer en appelant **IWMWriter :: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="9bff4-118">Obtain a pointer to the [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) interface of the writer object by calling **IWMWriter::QueryInterface**.</span></span>
4.  <span data-ttu-id="9bff4-119">Définissez le rappel pour le postviewer à utiliser en appelant [**IWMWriterPostView :: SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).</span><span class="sxs-lookup"><span data-stu-id="9bff4-119">Set the callback for the postviewer to use by calling [**IWMWriterPostView::SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).</span></span>
5.  <span data-ttu-id="9bff4-120">Pour chaque flux pour lequel vous souhaitez recevoir des exemples postview, appelez [**IWMWriterPostView :: SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span><span class="sxs-lookup"><span data-stu-id="9bff4-120">For each stream for which you want to receive postview samples, call [**IWMWriterPostView::SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span></span> <span data-ttu-id="9bff4-121">Vous pouvez vérifier si un flux est configuré pour recevoir des exemples postview en appelant [**IWMWriterPostView :: GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).</span><span class="sxs-lookup"><span data-stu-id="9bff4-121">You can check to see whether a stream is set to receive postview samples by calling [**IWMWriterPostView::GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).</span></span>
6.  <span data-ttu-id="9bff4-122">Vous pouvez manipuler les exemples de formats, comme vous le feriez avec les formats de sortie dans l’objet lecteur ou l’objet lecteur synchrone.</span><span class="sxs-lookup"><span data-stu-id="9bff4-122">You can manipulate the sample formats, just like you would the output formats in the reader object or synchronous reader object.</span></span>
7.  <span data-ttu-id="9bff4-123">Lorsque vous commencez à écrire le fichier, vous commencerez à recevoir des exemples dans votre implémentation de la méthode de rappel **OnPostViewSample** .</span><span class="sxs-lookup"><span data-stu-id="9bff4-123">When you start writing the file, you will begin to receive samples in your implementation of the **OnPostViewSample** callback method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bff4-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bff4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bff4-125">**Interface IWMWriterPostViewCallback**</span><span class="sxs-lookup"><span data-stu-id="9bff4-125">**IWMWriterPostViewCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[<span data-ttu-id="9bff4-126">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="9bff4-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




