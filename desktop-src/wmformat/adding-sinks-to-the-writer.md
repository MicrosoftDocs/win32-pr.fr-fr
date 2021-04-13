---
title: Ajout de récepteurs à l’enregistreur
description: Ajout de récepteurs à l’enregistreur
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- ASF (Advanced Systems Format), ajout de récepteurs à l’enregistreur
- ASF (format de systèmes avancés), ajout de récepteurs à l’enregistreur
- ASF (Advanced Systems Format), récepteurs
- ASF (format des systèmes avancés), récepteurs
- ASF (Advanced Systems Format), récepteurs d’écriture
- ASF (format de systèmes avancés), récepteurs d’écriture
- récepteurs, ajout au writer
- récepteurs d’écriture, ajout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886a6630a02d1fea56ce387077484f173ddf4dd3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104381517"
---
# <a name="adding-sinks-to-the-writer"></a><span data-ttu-id="69423-111">Ajout de récepteurs à l’enregistreur</span><span class="sxs-lookup"><span data-stu-id="69423-111">Adding Sinks to the Writer</span></span>

<span data-ttu-id="69423-112">Les récepteurs d’écriture sont des objets distincts du writer et doivent être ajoutés au Writer pour être utilisés.</span><span class="sxs-lookup"><span data-stu-id="69423-112">Writer sinks are separate objects from the writer and must be added to the writer to be used.</span></span> <span data-ttu-id="69423-113">Si vous écrivez dans un fichier, vous pouvez simplement appeler [**IWMWriter :: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), ce qui permet de configurer automatiquement le récepteur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="69423-113">If you are writing to a file, you can simply call [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), which will set up the file sink automatically.</span></span> <span data-ttu-id="69423-114">Sinon, pour ajouter un récepteur au writer, appelez la méthode [**IWMWriterAdvanced :: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) .</span><span class="sxs-lookup"><span data-stu-id="69423-114">Otherwise, to add a sink to the writer, call the [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) method.</span></span> <span data-ttu-id="69423-115">**AddSink** requiert un pointeur vers l’interface [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) du récepteur.</span><span class="sxs-lookup"><span data-stu-id="69423-115">**AddSink** requires a pointer to the [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) interface of the sink.</span></span>

<span data-ttu-id="69423-116">Lorsque vous avez terminé d’utiliser un récepteur, vous devez le fermer en appelant la méthode appropriée, en fonction du type de récepteur, puis le supprimer du writer en appelant [**IWMWriterAdvanced :: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).</span><span class="sxs-lookup"><span data-stu-id="69423-116">When you are finished using a sink, you should close it by calling the appropriate method, depending on the type of sink, and then remove it from the writer by calling [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).</span></span>

<span data-ttu-id="69423-117">L’exemple de code suivant montre comment créer un récepteur de fichiers d’écriture et l’ajouter au writer.</span><span class="sxs-lookup"><span data-stu-id="69423-117">The following example code shows how to create a writer file sink and add it to the writer.</span></span> <span data-ttu-id="69423-118">Pour plus d’informations sur l’utilisation de ce code, consultez [utilisation des exemples de code](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="69423-118">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT AddFileSink(IWMWriterFileSink** ppFileSink, IWMWriter* pWriter)
{
    HRESULT hr = S_OK;
    IWMWriterSink*     pSinkBase       = NULL;
    IWMWriterAdvanced* pWriterAdvanced = NULL;

    hr = CreateWriterFileSink(ppFileSink);
    GOTO_EXIT_IF_FAILED(hr);

    hr = *ppFileSink->QueryInterface(IID_IWMWriterSink, 
                                     (void**) &pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced,
                                 (void**) &pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriterAdvanced->AddSink(pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

Exit:
    SAFE_RELEASE(pSinkBase);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="69423-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69423-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69423-120">**Obtention de messages d’erreur à partir d’un récepteur**</span><span class="sxs-lookup"><span data-stu-id="69423-120">**Getting Error Messages from a Sink**</span></span>](getting-error-messages-from-a-sink.md)
</dt> <dt>

[<span data-ttu-id="69423-121">**Interface IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="69423-121">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="69423-122">**Utilisation des récepteurs d’écriture**</span><span class="sxs-lookup"><span data-stu-id="69423-122">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




