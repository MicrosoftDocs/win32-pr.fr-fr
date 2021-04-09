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
# <a name="how-to-print-with-the-xps-print-api"></a>Comment : imprimer avec l’API d’impression XPS

Cette rubrique explique comment utiliser l' [API d’impression XPS](xpsprint-api.md) pour imprimer à partir d’une application Windows.

L' [API d’impression XPS](xpsprint-api.md) permet aux applications Windows natives d’imprimer des documents XPS. Une application peut créer un document XPS à l’aide de l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)). La rubrique d’aide sur les [tâches communes de programmation de documents XPS](/previous-versions/windows/desktop/dd316968(v=vs.85)) décrit la procédure à suivre. Une fois qu’un document XPS a été créé, l’application peut utiliser l’API d’impression XPS pour l’imprimer.

L’utilisation de l' [API d’impression XPS](xpsprint-api.md) pour imprimer un document à partir d’une application implique les étapes suivantes.

-   [Initialiser l’interface COM](#initialize-com-interface)
-   [Créer un événement d’achèvement](#create-a-completion-event)
-   [Démarrer un travail d’impression XPS](#start-an-xps-print-job)
-   [Créer une interface IXpsOMPackageWriter](#create-an-ixpsompackagewriter-interface)
-   [Fermer l’interface IXpsOMPackageWriter](#close-the-ixpsompackagewriter-interface)
-   [Fermer le flux du travail d’impression](#close-the-print-job-stream)
-   [Attendre l’événement d’achèvement](#wait-for-the-completion-event)
-   [Libérer des ressources](#release-resources)

L' [API d’impression XPS](xpsprint-api.md) requiert un document XPS à imprimer. Dans l’exemple suivant, le document XPS est créé, car il est envoyé à l’imprimante par l’API d’impression XPS. Il est également possible de créer un document XPS sans l’envoyer à une imprimante à l’aide de l' [API de document XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) et en le conservant en tant que modèle OM XPS ou en enregistrant le modèle d’objet XPS en tant que document XPS. Pour plus d’informations sur l’utilisation d’un modèle d’objet XPS, consultez l’API de document XPS.

### <a name="initialize-com-interface"></a>Initialiser l’interface COM

Initialiser l’interface COM, si l’application ne l’a pas déjà fait.


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



### <a name="create-a-completion-event"></a>Créer un événement d’achèvement

Créez un événement d’achèvement, que l' [API d’impression XPS](xpsprint-api.md) utilise pour notifier l’application lorsque le spouleur d’impression a reçu l’intégralité du document de l’application. L’API d’impression XPS prend également en charge un événement de progression afin qu’une application puisse connaître les autres activités de mise en file d’attente.


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



### <a name="start-an-xps-print-job"></a>Démarrer un travail d’impression XPS

Démarrez un travail d’impression XPS en appelant [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob). **StartXpsPrintJob** retourne un flux dans lequel l’application enverra le document à imprimer.


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



### <a name="create-an-ixpsompackagewriter-interface"></a>Créer une interface IXpsOMPackageWriter

Créez une interface [**IXpsOMPackageWriter**](/windows/win32/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter) en appelant [**IXpsOMObjectFactory :: CreatePackageWriterOnStream**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagewriteronstream) sur le flux retourné par [**StartXpsPrintJob**](/windows/desktop/api/XpsPrint/nf-xpsprint-startxpsprintjob).


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



Pour chaque document de ce travail d’impression, démarrez un nouveau document, puis ajoutez des pages à ce document.

### <a name="start-a-new-document"></a>Démarrer un nouveau document

Démarrez un nouveau document dans le writer de package en appelant [**IXpsOMPackageWriter :: StartNewDocument**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument). Si un document est ouvert lorsque cette méthode est appelée, il est fermé et un nouveau document est ouvert.


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



### <a name="add-a-page"></a>Ajouter une page

Appelez [**IXpsOMPackageWriter :: AddPage**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage) pour écrire chaque page du document à partir de l’application dans le nouveau document dans le writer de package.

> [!Note]  
> L’application est censée avoir créé la page avant cette étape. Pour plus d’informations sur la création de pages de document et l’ajout de contenu, consultez les [tâches de programmation de document XPS courantes](/previous-versions/windows/desktop/dd316968(v=vs.85)).

 


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



### <a name="close-the-ixpsompackagewriter-interface"></a>Fermer l’interface IXpsOMPackageWriter

Une fois que tous les documents ont été écrits pour ce travail d’impression, appelez [**IXpsOMPackageWriter :: Close**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-close) pour fermer le package.


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



### <a name="close-the-print-job-stream"></a>Fermer le flux du travail d’impression

Fermez le flux de travail d’impression en appelant [**Close**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjobstream-close), qui indique au spouleur d’impression que l’ensemble du travail d’impression a été envoyé par l’application.


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



### <a name="wait-for-the-completion-event"></a>Attendre l’événement d’achèvement

Attendez l’événement d’achèvement du travail d’impression.


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



Une fois l’événement d’achèvement signalé, appelez [**GetJobStatus**](/windows/desktop/api/XpsPrint/nf-xpsprint-ixpsprintjob-getjobstatus) pour connaître l’état du travail.


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



### <a name="release-resources"></a>Libérer des ressources

Une fois que l’état d’un travail indique la fin, libérez les interfaces et les ressources utilisées pour ce travail d’impression.


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



 

 
