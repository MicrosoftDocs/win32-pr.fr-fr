---
title: Pour implémenter des messages de lecture dans le rappel OnStatus
description: Pour implémenter des messages de lecture dans le rappel OnStatus
ms.assetid: f0535e02-a283-48bf-9242-ebcc17a6fb66
keywords:
- ASF (Advanced Systems Format), implémentation de messages de lecture
- ASF (format des systèmes avancés), implémentation des messages de lecture
- ASF (Advanced Systems Format), rappel OnStatus
- ASF (format avancé des systèmes), rappel OnStatus
- ASF (Advanced Systems Format), lecteurs asynchrones
- ASF (Advanced Systems Format), lecteurs asynchrones
- lecteurs asynchrones, implémentation des messages de lecture
- OnStatus méthode de rappel, implémentation des messages de lecture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384cf8df8628efa9bd2cc17920dc6b1303655691
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030792"
---
# <a name="to-implement-reader-messages-in-the-onstatus-callback"></a><span data-ttu-id="6b50b-111">Pour implémenter des messages de lecture dans le rappel OnStatus</span><span class="sxs-lookup"><span data-stu-id="6b50b-111">To Implement Reader Messages in the OnStatus Callback</span></span>

<span data-ttu-id="6b50b-112">Pour utiliser le lecteur asynchrone pour distribuer du contenu à partir d’un fichier ASF, vous devez implémenter au moins deux méthodes de rappel, [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) et [**IWMReaderCallback :: OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span><span class="sxs-lookup"><span data-stu-id="6b50b-112">To use the asynchronous reader to deliver content from an ASF file, you must implement a minimum of two callback methods, [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) and [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="6b50b-113">Cette section décrit comment implémenter **IWMStatusCallback :: OnStatus** pour recevoir les messages d’État envoyés par le lecteur et y répondre.</span><span class="sxs-lookup"><span data-stu-id="6b50b-113">This section describes how to implement **IWMStatusCallback::OnStatus** to receive and respond to status messages sent by the reader.</span></span> <span data-ttu-id="6b50b-114">**OnStatus** est utilisé par d’autres objets dans le kit de développement logiciel (SDK) Windows Media format.</span><span class="sxs-lookup"><span data-stu-id="6b50b-114">**OnStatus** is used by other objects in the Windows Media Format SDK.</span></span> <span data-ttu-id="6b50b-115">Pour obtenir des informations générales sur **OnStatus**, consultez [utilisation du rappel OnStatus](using-the-onstatus-callback.md).</span><span class="sxs-lookup"><span data-stu-id="6b50b-115">For general information about **OnStatus**, see [Using the OnStatus Callback](using-the-onstatus-callback.md).</span></span>

<span data-ttu-id="6b50b-116">Lorsque vous utilisez le lecteur asynchrone, vous devez intercepter les messages suivants dans **IWMStatusCallback :: OnStatus**.</span><span class="sxs-lookup"><span data-stu-id="6b50b-116">When using the asynchronous reader, you must trap the following messages in **IWMStatusCallback::OnStatus**.</span></span>



| <span data-ttu-id="6b50b-117">Message d’état</span><span class="sxs-lookup"><span data-stu-id="6b50b-117">Status message</span></span> | <span data-ttu-id="6b50b-118">Description</span><span class="sxs-lookup"><span data-stu-id="6b50b-118">Description</span></span>                                     |
|----------------|-------------------------------------------------|
| <span data-ttu-id="6b50b-119">WMT \_ ouvert</span><span class="sxs-lookup"><span data-stu-id="6b50b-119">WMT\_OPENED</span></span>    | <span data-ttu-id="6b50b-120">Envoyé lorsque les opérations d’ouverture de fichier sont terminées.</span><span class="sxs-lookup"><span data-stu-id="6b50b-120">Sent when file opening operations are complete.</span></span> |
| <span data-ttu-id="6b50b-121">WMT \_ fermé</span><span class="sxs-lookup"><span data-stu-id="6b50b-121">WMT\_CLOSED</span></span>    | <span data-ttu-id="6b50b-122">Envoyé lorsque les opérations de fermeture de fichier sont terminées.</span><span class="sxs-lookup"><span data-stu-id="6b50b-122">Sent when file closing operations are complete.</span></span> |



 

<span data-ttu-id="6b50b-123">Vous devez utiliser les messages d’État listés ci-dessus pour contrôler l’exécution de votre application de lecture.</span><span class="sxs-lookup"><span data-stu-id="6b50b-123">You should use the status messages listed above to control execution of your reading application.</span></span> <span data-ttu-id="6b50b-124">Par exemple, vous devez attendre la réception du message **WMT \_ ouvert** pour démarrer le lecteur ou appeler d’autres méthodes qui nécessitent que le lecteur dispose d’un fichier prêt.</span><span class="sxs-lookup"><span data-stu-id="6b50b-124">For example, you must wait until receiving the **WMT\_OPENED** message to start the reader or call other methods that require the reader to have a file ready.</span></span> <span data-ttu-id="6b50b-125">Souvent, les applications générées avec le lecteur asynchrone utilisent un événement pour signaler l’achèvement des appels asynchrones et poursuivre le traitement.</span><span class="sxs-lookup"><span data-stu-id="6b50b-125">Frequently, applications built with the asynchronous reader use an event to signal the completion of asynchronous calls and proceed with processing.</span></span> <span data-ttu-id="6b50b-126">Pour plus d’informations sur l’utilisation d’événements pour signaler l’achèvement des opérations, consultez [utilisation d’événements avec des appels asynchrones](using-events-with-asynchronous-calls.md).</span><span class="sxs-lookup"><span data-stu-id="6b50b-126">For more information about using events for signaling completion of operations, see [Using Events with Asynchronous Calls](using-events-with-asynchronous-calls.md).</span></span>

<span data-ttu-id="6b50b-127">De nombreux autres messages sont envoyés à **OnStatus** par l’objet lecteur pour permettre à l’application de répondre à l’état des opérations de lecture.</span><span class="sxs-lookup"><span data-stu-id="6b50b-127">Many other messages are sent to **OnStatus** by the reader object to enable the application to respond to the status of reading operations.</span></span> <span data-ttu-id="6b50b-128">Les valeurs de message d’État possibles sont définies dans le type d’énumération d' [**\_ État WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .</span><span class="sxs-lookup"><span data-stu-id="6b50b-128">The possible status message values are defined in the [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) enumeration type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b50b-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b50b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b50b-130">**IWMStatusCallback :: OnStatus**</span><span class="sxs-lookup"><span data-stu-id="6b50b-130">**IWMStatusCallback::OnStatus**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus)
</dt> <dt>

[<span data-ttu-id="6b50b-131">**Lecture des fichiers avec le lecteur asynchrone**</span><span class="sxs-lookup"><span data-stu-id="6b50b-131">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="6b50b-132">**Utilisation du rappel OnStatus**</span><span class="sxs-lookup"><span data-stu-id="6b50b-132">**Using the OnStatus Callback**</span></span>](using-the-onstatus-callback.md)
</dt> </dl>

 

 




