---
title: Pour récupérer des exemples de médias avec le lecteur asynchrone
description: Pour récupérer des exemples de médias avec le lecteur asynchrone
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- ASF (Advanced Systems Format), récupération des exemples de supports
- ASF (format des systèmes avancés), récupération des exemples de média
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- lecteurs asynchrones, récupération d’exemples de médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030789"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a><span data-ttu-id="8691e-108">Pour récupérer des exemples de médias avec le lecteur asynchrone</span><span class="sxs-lookup"><span data-stu-id="8691e-108">To Retrieve Media Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="8691e-109">Une fois que vous avez reçu le \_ message d’état d’ouverture de WMT dans votre implémentation de [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), vous pouvez commencer à recevoir des exemples en appelant [**IWMReader :: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start).</span><span class="sxs-lookup"><span data-stu-id="8691e-109">After you have received the WMT\_OPENED status message in your implementation of [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), you can begin receiving samples by calling [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start).</span></span> <span data-ttu-id="8691e-110">Le lecteur asynchrone fournit des exemples à votre implémentation de [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span><span class="sxs-lookup"><span data-stu-id="8691e-110">The asynchronous reader delivers samples to your implementation of [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="8691e-111">Les exemples sont fournis dans l’ordre de la présentation.</span><span class="sxs-lookup"><span data-stu-id="8691e-111">Samples are delivered in presentation-time order.</span></span>

<span data-ttu-id="8691e-112">**Start** est un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="8691e-112">**Start** is an asynchronous call.</span></span> <span data-ttu-id="8691e-113">Elle retourne presque immédiatement et continue de s’exécuter sur des threads distincts.</span><span class="sxs-lookup"><span data-stu-id="8691e-113">It will return almost immediately and continue to run on separate threads.</span></span> <span data-ttu-id="8691e-114">Le lecteur asynchrone utilise plusieurs threads lors du décodage du contenu et de la diffusion des exemples.</span><span class="sxs-lookup"><span data-stu-id="8691e-114">The asynchronous reader uses multiple threads when decoding content and delivering samples.</span></span> <span data-ttu-id="8691e-115">Quand la fin du fichier est atteinte, le lecteur envoie un message d' \_ État d’un EOF WMT à votre implémentation du rappel **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="8691e-115">When the end of the file is reached, the reader sends a WMT\_EOF status message to your implementation of the **OnStatus** callback.</span></span> <span data-ttu-id="8691e-116">Lors de \_ l’envoi d’un EOF WMT, le lecteur arrête son propre traitement. vous n’avez pas besoin de répondre à la fin de la \_ demande WMT avec un appel à [**IWMReader :: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).</span><span class="sxs-lookup"><span data-stu-id="8691e-116">When WMT\_EOF is sent, the reader stops its own processing; you do not need to respond to WMT\_EOF with a call to [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8691e-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8691e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8691e-118">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="8691e-118">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="8691e-119">**Pour implémenter des messages de lecture dans le rappel OnStatus**</span><span class="sxs-lookup"><span data-stu-id="8691e-119">**To Implement Reader Messages in the OnStatus Callback**</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[<span data-ttu-id="8691e-120">**Pour implémenter le rappel OnSample**</span><span class="sxs-lookup"><span data-stu-id="8691e-120">**To Implement the OnSample Callback**</span></span>](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




