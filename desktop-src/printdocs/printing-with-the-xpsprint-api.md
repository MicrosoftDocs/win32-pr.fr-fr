---
description: Cette rubrique explique comment utiliser l’API d’impression XPS pour imprimer à partir d’une application Windows.
ms.assetid: 3d7ab169-412c-434f-a865-4da4af370eaf
title: 'Comment : imprimer avec l’API d’impression XPS'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b4be5f083fb31eccaf2dc4b555435bd15a7fb45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867537"
---
# <a name="how-to-print-with-the-xps-print-api"></a><span data-ttu-id="d290f-103">Comment : imprimer avec l’API d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="d290f-103">How To: Print with the XPS Print API</span></span>

<span data-ttu-id="d290f-104">Cette rubrique explique comment utiliser l' [API d’impression XPS](xpsprint-api.md) pour imprimer à partir d’une application Windows.</span><span class="sxs-lookup"><span data-stu-id="d290f-104">This topic describes how to use the [XPS Print API](xpsprint-api.md) to print from a Windows application.</span></span>

<span data-ttu-id="d290f-105">L' [API d’impression XPS](xpsprint-api.md) permet aux applications Windows natives d’imprimer des documents XPS.</span><span class="sxs-lookup"><span data-stu-id="d290f-105">The [XPS Print API](xpsprint-api.md) enables native Windows applications to print XPS documents.</span></span> <span data-ttu-id="d290f-106">Une application peut créer un document XPS à l’aide de l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d290f-106">An application can create an XPS document by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span> <span data-ttu-id="d290f-107">La rubrique d’aide sur les [tâches communes de programmation de documents XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)) décrit la procédure à suivre.</span><span class="sxs-lookup"><span data-stu-id="d290f-107">The [Common XPS Document Programming Tasks](/previous-versions/windows/desktop/dd316968(v=vs.85)) help topic describes how to do this.</span></span> <span data-ttu-id="d290f-108">Une fois qu’un document XPS a été créé, l’application peut utiliser l’API d’impression XPS pour l’imprimer.</span><span class="sxs-lookup"><span data-stu-id="d290f-108">Once an XPS document has been created, the application can use the XPS Print API to print it.</span></span>

<span data-ttu-id="d290f-109">L’utilisation de l' [API d’impression XPS](xpsprint-api.md) pour imprimer un document à partir d’une application implique les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="d290f-109">Using the [XPS Print API](xpsprint-api.md) to print a document from an application involves the following steps.</span></span>

-   [<span data-ttu-id="d290f-110">Initialiser l’interface COM</span><span class="sxs-lookup"><span data-stu-id="d290f-110">Initialize COM Interface</span></span>](#initialize-com-interface)
-   [<span data-ttu-id="d290f-111">Créer un événement d’achèvement</span><span class="sxs-lookup"><span data-stu-id="d290f-111">Create a Completion Event</span></span>](#create-a-completion-event)
-   [<span data-ttu-id="d290f-112">Démarrer un travail d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="d290f-112">Start an XPS Print Job</span></span>](#start-an-xps-print-job)
-   [<span data-ttu-id="d290f-113">Créer une interface IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="d290f-113">Create an IXpsOMPackageWriter Interface</span></span>](#create-an-ixpsompackagewriter-interface)
-   [<span data-ttu-id="d290f-114">Fermer l’interface IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="d290f-114">Close the IXpsOMPackageWriter Interface</span></span>](#close-the-ixpsompackagewriter-interface)
-   [<span data-ttu-id="d290f-115">Fermer le flux du travail d’impression</span><span class="sxs-lookup"><span data-stu-id="d290f-115">Close the Print Job Stream</span></span>](#close-the-print-job-stream)
-   [<span data-ttu-id="d290f-116">Attendre l’événement d’achèvement</span><span class="sxs-lookup"><span data-stu-id="d290f-116">Wait for the Completion Event</span></span>](#wait-for-the-completion-event)
-   [<span data-ttu-id="d290f-117">Libérer des ressources</span><span class="sxs-lookup"><span data-stu-id="d290f-117">Release Resources</span></span>](#release-resources)

<span data-ttu-id="d290f-118">L' [API d’impression XPS](xpsprint-api.md) requiert un document XPS à imprimer.</span><span class="sxs-lookup"><span data-stu-id="d290f-118">The [XPS Print API](xpsprint-api.md) requires an XPS document to print.</span></span> <span data-ttu-id="d290f-119">Dans l’exemple suivant, le document XPS est créé, car il est envoyé à l’imprimante par l’API d’impression XPS.</span><span class="sxs-lookup"><span data-stu-id="d290f-119">In the following example, the XPS document is created as it is sent to the printer by the XPS Print API.</span></span> <span data-ttu-id="d290f-120">Il est également possible de créer un document XPS sans l’envoyer à une imprimante à l’aide de l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) et en le conservant en tant que modèle OM XPS ou en enregistrant le modèle d’objet XPS en tant que document XPS.</span><span class="sxs-lookup"><span data-stu-id="d290f-120">It is also possible to create an XPS document without sending it to a printer by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) and maintaining it as an XPS OM or by saving the XPS OM as an XPS document.</span></span> <span data-ttu-id="d290f-121">Pour plus d’informations sur l’utilisation d’un modèle d’objet XPS, consultez l’API de document XPS.</span><span class="sxs-lookup"><span data-stu-id="d290f-121">For more information about using an XPS OM, see the XPS Document API.</span></span>

### <a name="initialize-com-interface"></a><span data-ttu-id="d290f-122">Initialiser l’interface COM</span><span class="sxs-lookup"><span data-stu-id="d290f-122">Initialize COM Interface</span></span>

<span data-ttu-id="d290f-123">Initialiser l’interface COM, si l’application ne l’a pas déjà fait.</span><span class="sxs-lookup"><span data-stu-id="d290f-123">Initialize the COM interface, if the application has not already done so.</span></span>


```C++
    // Initialize the COM interface, if the application has not 
    //  already done so.
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        fwprintf(stderr, 
            L"ERROR: CoInitializeEx failed with HRESULT 0x%X\n", hr);
        return 1;
    }
```



### <a name="create-a-completion-event"></a><span data-ttu-id="d290f-124">Créer un événement d’achèvement</span><span class="sxs-lookup"><span data-stu-id="d290f-124">Create a Completion Event</span></span>

<span data-ttu-id="d290f-125">Créez un événement d’achèvement, que l' [API d’impression XPS](xpsprint-api.md) utilise pour notifier l’application lorsque le spouleur d’impression a reçu l’intégralité du document de l’application.</span><span class="sxs-lookup"><span data-stu-id="d290f-125">Create a completion event, which the [XPS Print API](xpsprint-api.md) uses to notify the application when the print spooler has received the entire document from the application.</span></span> <span data-ttu-id="d290f-126">L’API d’impression XPS prend également en charge un événement de progression afin qu’une application puisse connaître les autres activités de mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="d290f-126">The XPS Print API also supports a progress event so an application can know about other spooling activity.</span></span>


```C++
        // Create the completion event
        completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
        if (!completionEvent)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(stderr, 
                L"ERROR: Could not create completion event: %08X\n", hr);
        }
```



### <a name="start-an-xps-print-job"></a><span data-ttu-id="d290f-127">Démarrer un travail d’impression XPS</span><span class="sxs-lookup"><span data-stu-id="d290f-127">Start an XPS Print Job</span></span>

<span data-ttu-id="d290f-128">Démarrez un travail d’impression XPS en appelant [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="d290f-128">Start an XPS print job by calling [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span></span> <span data-ttu-id="d290f-129">**StartXpsPrintJob** retourne un flux dans lequel l’application enverra le document à imprimer.</span><span class="sxs-lookup"><span data-stu-id="d290f-129">**StartXpsPrintJob** returns a stream into which the application will send the document to be printed.</span></span>


```C++
        // Start an XPS Print Job
        if (FAILED(hr = StartXpsPrintJob(
                    printerName,
                    NULL,
                    NULL,
                    NULL,
                    completionEvent,
                    NULL,
                    0,
                    &job,
                    &jobStream,
                    NULL
                    )))
        {
            fwprintf(stderr, 
                L"ERROR: Could not start XPS print job: %08X\n", hr);
        }
```



### <a name="create-an-ixpsompackagewriter-interface"></a><span data-ttu-id="d290f-130">Créer une interface IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="d290f-130">Create an IXpsOMPackageWriter Interface</span></span>

<span data-ttu-id="d290f-131">Créez une interface [**IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) en appelant [**IXpsOMObjectFactory :: CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) sur le flux retourné par [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="d290f-131">Create an [**IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) interface by calling [**IXpsOMObjectFactory::CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) on the stream returned by [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).</span></span>


```C++
    // Create an XPS OM Object Factory. If one has already been 
    //  created by the application, a new one is not necessary.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory), 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&xpsFactory))))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create XPS OM Object Factory: %08X\n", 
                hr);
        }
    }
    // Create the Part URI for the Fixed Document Sequence. The
    //  Fixed Document Sequence is the top-level element in the
    //  package hierarchy of objects. There is one Fixed Document
    //  Sequence in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name used in this example is the part name
    //  used by convention.
    //
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/FixedDocumentSequence.fdseq", 
                    &partUri)))
        {
            fwprintf(stderr, 
                L"ERROR: Could not create part URI: %08X\n", hr);
        }
    }

    // Create the package writer on the print job stream.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePackageWriterOnStream(
                    jobStream,
                    TRUE,
                    XPS_INTERLEAVING_ON,
                    partUri,
                    NULL,
                    NULL,
                    NULL,
                    NULL,
                    &packageWriter
                    )
                )
           )
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create package writer: 0x%X\n", 
                hr);
        }
    }

    // Release the part URI interface.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



<span data-ttu-id="d290f-132">Pour chaque document de ce travail d’impression, démarrez un nouveau document, puis ajoutez des pages à ce document.</span><span class="sxs-lookup"><span data-stu-id="d290f-132">For each document in this print job, start a new document and then add pages to that document.</span></span>

### <a name="start-a-new-document"></a><span data-ttu-id="d290f-133">Démarrer un nouveau document</span><span class="sxs-lookup"><span data-stu-id="d290f-133">Start a New Document</span></span>

<span data-ttu-id="d290f-134">Démarrez un nouveau document dans le writer de package en appelant [**IXpsOMPackageWriter :: StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).</span><span class="sxs-lookup"><span data-stu-id="d290f-134">Start a new document in the package writer by calling [**IXpsOMPackageWriter::StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument).</span></span> <span data-ttu-id="d290f-135">Si un document est ouvert lorsque cette méthode est appelée, il est fermé et un nouveau document est ouvert.</span><span class="sxs-lookup"><span data-stu-id="d290f-135">If a document is open when this method is called, it is closed and a new document is opened.</span></span>


```C++
    // Create the Part URI for the Fixed Document. The
    //  Fixed Document part contains the pages of the document. 
    //  There can be one or more Fixed Documents in an XPS document.
    //
    // The part name is not specified by the XML Paper Specification,
    //  however, the name format used in this example is the format 
    //  used by convention. The number "1" in this example must be 
    //  changed for each document in the package. For example, 1 
    //  for the first document, 2 for the second, and so on.
    //

    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = xpsFactory->CreatePartUri(
                    L"/Documents/1/FixedDocument.fdoc", 
                    &partUri)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not create part URI: %08X\n", 
                hr);
        }
    }

    // Start the new document.
    //
    //  If there was already a document started in this page,
    //  this call will close it and start a new one.
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->StartNewDocument(
                    partUri, 
                    NULL, 
                    NULL, 
                    NULL,
                    NULL)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not start new document: 0x%X\n", 
                hr);
        }
    }
    
    // Release the part URI interface
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }
```



### <a name="add-a-page"></a><span data-ttu-id="d290f-136">Ajouter une page</span><span class="sxs-lookup"><span data-stu-id="d290f-136">Add a Page</span></span>

<span data-ttu-id="d290f-137">Appelez [**IXpsOMPackageWriter :: AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) pour écrire chaque page du document à partir de l’application dans le nouveau document dans le writer de package.</span><span class="sxs-lookup"><span data-stu-id="d290f-137">Call [**IXpsOMPackageWriter::AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) to write each of the document's pages from the application to the new document in the package writer.</span></span>

> [!Note]  
> <span data-ttu-id="d290f-138">L’application est censée avoir créé la page avant cette étape.</span><span class="sxs-lookup"><span data-stu-id="d290f-138">The application is assumed to have created the page prior to this step.</span></span> <span data-ttu-id="d290f-139">Pour plus d’informations sur la création de pages de document et l’ajout de contenu, consultez les [tâches de programmation de document XPS courantes](/previous-versions/windows/desktop/dd316968(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d290f-139">For more information about creating document pages and adding content to them, see the [Common XPS Document Programming Tasks](/previous-versions/windows/desktop/dd316968(v=vs.85)).</span></span>

 


```C++
    if (SUCCEEDED(hr))
    {
        // Add the current page to the document.
        if (FAILED(hr = packageWriter->AddPage(
                    xpsPage,
                    &pageSize,
                    NULL,
                    NULL,
                    NULL,
                    NULL
                    )))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not add page to document: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-ixpsompackagewriter-interface"></a><span data-ttu-id="d290f-140">Fermer l’interface IXpsOMPackageWriter</span><span class="sxs-lookup"><span data-stu-id="d290f-140">Close the IXpsOMPackageWriter Interface</span></span>

<span data-ttu-id="d290f-141">Une fois que tous les documents ont été écrits pour ce travail d’impression, appelez [**IXpsOMPackageWriter :: Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) pour fermer le package.</span><span class="sxs-lookup"><span data-stu-id="d290f-141">After all the documents have been written for this print job, call [**IXpsOMPackageWriter::Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) to close the package.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = packageWriter->Close()))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not close package writer: %08X\n", 
                hr);
        }
    }
```



### <a name="close-the-print-job-stream"></a><span data-ttu-id="d290f-142">Fermer le flux du travail d’impression</span><span class="sxs-lookup"><span data-stu-id="d290f-142">Close the Print Job Stream</span></span>

<span data-ttu-id="d290f-143">Fermez le flux de travail d’impression en appelant [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), qui indique au spouleur d’impression que l’ensemble du travail d’impression a été envoyé par l’application.</span><span class="sxs-lookup"><span data-stu-id="d290f-143">Close the print job stream by calling [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), which tells the print spooler that the entire print job has been sent by the application.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = jobStream->Close()))
        {
            fwprintf(
                stderr,
                L"ERROR: Could not close job stream: %08X\n",
                hr);
        }
    }
    else
    {
        // Only cancel the job if we succeeded in creating a job.
        if (job)
        {
            // Tell the XPS Print API that we're giving up.  
            //  Don't overwrite hr with the return from this function.
            job->Cancel();
        }
    }
```



### <a name="wait-for-the-completion-event"></a><span data-ttu-id="d290f-144">Attendre l’événement d’achèvement</span><span class="sxs-lookup"><span data-stu-id="d290f-144">Wait for the Completion Event</span></span>

<span data-ttu-id="d290f-145">Attendez l’événement d’achèvement du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d290f-145">Wait for the print job's completion event.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        wprintf(L"Waiting for job completion...\n");

        if (WaitForSingleObject(completionEvent, INFINITE) != 
                                                    WAIT_OBJECT_0)
        {
            hr = HRESULT_FROM_WIN32(GetLastError());
            fwprintf(
                stderr, 
                L"ERROR: Wait for completion event failed: %08X\n", 
                hr);
        }
    }
```



<span data-ttu-id="d290f-146">Une fois l’événement d’achèvement signalé, appelez [**GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) pour connaître l’état du travail.</span><span class="sxs-lookup"><span data-stu-id="d290f-146">After the completion event is signaled, call [**GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) to get the job status.</span></span>


```C++
    if (SUCCEEDED(hr))
    {
        if (FAILED(hr = job->GetJobStatus(&jobStatus)))
        {
            fwprintf(
                stderr, 
                L"ERROR: Could not get job status: %08X\n", 
                hr);
        }
    }

    if (SUCCEEDED(hr))
    {
        switch (jobStatus.completion)
        {
            case XPS_JOB_COMPLETED:
                break;
            case XPS_JOB_CANCELLED:
                fwprintf(stderr, L"ERROR: job was cancelled\n");
                hr = E_FAIL;
                break;
            case XPS_JOB_FAILED:
                fwprintf(
                    stderr, 
                    L"ERROR: Print job failed: %08X\n", 
                    jobStatus.jobStatus);
                hr = E_FAIL;
                break;
            default:
                fwprintf(stderr, L"ERROR: unexpected failure\n");
                hr = E_UNEXPECTED;
                break;
        }
    }
```



### <a name="release-resources"></a><span data-ttu-id="d290f-147">Libérer des ressources</span><span class="sxs-lookup"><span data-stu-id="d290f-147">Release Resources</span></span>

<span data-ttu-id="d290f-148">Une fois que l’état d’un travail indique la fin, libérez les interfaces et les ressources utilisées pour ce travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d290f-148">After a job status indicates completion, release the interfaces and resources used for this print job.</span></span>


```C++
    if (packageWriter)
    {
        packageWriter->Release();
        packageWriter = NULL;
    }

    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    if (xpsFactory)
    {
        xpsFactory->Release();
        xpsFactory = NULL;
    }

    if (jobStream)
    {
        jobStream->Release();
        jobStream = NULL;
    }

    if (job)
    {
        job->Release();
        job = NULL;
    }

    if (completionEvent)
    {
        CloseHandle(completionEvent);
        completionEvent = NULL;
    }
```



 

 
