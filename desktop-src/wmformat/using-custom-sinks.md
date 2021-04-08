---
title: Utilisation de récepteurs personnalisés
description: Utilisation de récepteurs personnalisés
ms.assetid: 7151583a-c7ab-40b0-a7bf-ddd56f93b7aa
keywords:
- ASF (Advanced Systems Format), récepteurs personnalisés
- ASF (format des systèmes avancés), récepteurs personnalisés
- ASF (Advanced Systems Format), récepteurs
- ASF (format des systèmes avancés), récepteurs
- récepteurs, récepteurs personnalisés
- récepteurs personnalisés, à propos de
- récepteurs d’écriture, récepteurs personnalisés
- récepteurs personnalisés, interface IWMWriterSink
- IWMWriterSink
- récepteurs d’écriture, interface IWMWriterSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e324d654fa8c85d6145b0f4bf8f20de1f06e125f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723482"
---
# <a name="using-custom-sinks"></a><span data-ttu-id="896e8-113">Utilisation de récepteurs personnalisés</span><span class="sxs-lookup"><span data-stu-id="896e8-113">Using Custom Sinks</span></span>

<span data-ttu-id="896e8-114">Si vous avez besoin d’écriture spéciale, vous pouvez créer vos propres récepteurs de writer.</span><span class="sxs-lookup"><span data-stu-id="896e8-114">If you have a special writing need, you can create your own writer sinks.</span></span> <span data-ttu-id="896e8-115">L’enregistreur maintient une communication unidirectionnelle avec un récepteur en effectuant des appels aux méthodes de [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink).</span><span class="sxs-lookup"><span data-stu-id="896e8-115">The writer maintains one-way communication with a sink by making calls to the methods of [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink).</span></span> <span data-ttu-id="896e8-116">Pour créer votre propre récepteur, implémentez l’interface **IWMWriterSink** dans une classe de votre application.</span><span class="sxs-lookup"><span data-stu-id="896e8-116">To create your own sink, implement the **IWMWriterSink** interface in a class in your application.</span></span> <span data-ttu-id="896e8-117">Ce processus est très similaire à l’implémentation d’une autre interface de rappel utilisée par les objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="896e8-117">This process is very similar to implementing any other callback interface used by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="896e8-118">Pour plus d’informations sur les rappels, consultez [utilisation des méthodes de rappel](using-the-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="896e8-118">For more information about callbacks, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>

<span data-ttu-id="896e8-119">La mémoire tampon reçue dans [**IWMWriterSink :: OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) doit être écrite au début du fichier, et toutes les mémoires tampons reçues dans [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) doivent être écrites de manière séquentielle.</span><span class="sxs-lookup"><span data-stu-id="896e8-119">The buffer received in [**IWMWriterSink::OnHeader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-onheader) should be written to the beginning of the file, and all buffers received in [**OnDataUnit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwritersink-ondataunit) should be written out sequentially.</span></span> <span data-ttu-id="896e8-120">**OnHeader** sera appelé au début, mais peut également être appelé à d’autres moments, et si c’est le cas, vous devriez, si possible, remplacer l’en-tête d’origine.</span><span class="sxs-lookup"><span data-stu-id="896e8-120">**OnHeader** will be called at the beginning but might be called at other times, too, and if it is, you should, if possible, overwrite the original header.</span></span> <span data-ttu-id="896e8-121">Si votre application n’est pas en mesure de le faire pour une raison quelconque, ignorez simplement les appels **OnHeader** suivants.</span><span class="sxs-lookup"><span data-stu-id="896e8-121">If your application is not able to do this for some reason, then simply ignore the subsequent **OnHeader** calls.</span></span>

<span data-ttu-id="896e8-122">Votre récepteur personnalisé doit communiquer son état à votre application d’écriture en effectuant des appels à la méthode de rappel [**IWMStatusCallback :: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="896e8-122">Your custom sink should communicate its status to your writing application by making calls to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="896e8-123">Si vous implémentez votre récepteur en tant qu’objet COM, vous souhaiterez peut-être exposer l’interface [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="896e8-123">If you implement your sink as a COM object, you may want to expose the [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) interface.</span></span> <span data-ttu-id="896e8-124">Toutefois, vous pouvez transmettre l’adresse du rappel **OnStatus** à votre récepteur et définir un contexte comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="896e8-124">However, you can pass the address of the **OnStatus** callback to your sink and set a context in any way you like.</span></span>

## <a name="related-topics"></a><span data-ttu-id="896e8-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="896e8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="896e8-126">**Utilisation des récepteurs d’écriture**</span><span class="sxs-lookup"><span data-stu-id="896e8-126">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




