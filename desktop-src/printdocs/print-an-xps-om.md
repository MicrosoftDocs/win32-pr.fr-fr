---
description: Décrit comment envoyer un modèle OM XPS à une imprimante sous la forme d’un document XPS.
ms.assetid: eb1068c4-6a6a-4ef2-8ed6-033a6a2c273b
title: Imprimer un modèle OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01ae1081c4f0c58c66efedc30406e310dd8dd9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034690"
---
# <a name="print-an-xps-om"></a><span data-ttu-id="4c97b-103">Imprimer un modèle OM XPS</span><span class="sxs-lookup"><span data-stu-id="4c97b-103">Print an XPS OM</span></span>

<span data-ttu-id="4c97b-104">Décrit comment envoyer un modèle OM XPS à une imprimante sous la forme d’un document XPS.</span><span class="sxs-lookup"><span data-stu-id="4c97b-104">Describes how to send an XPS OM to a printer as an XPS document.</span></span>

<span data-ttu-id="4c97b-105">Pour obtenir des instructions sur l’impression d’un modèle OM XPS contenant un document XPS complet, consultez [imprimer un modèle d’objet XPS complet](#print-a-complete-xps-om).</span><span class="sxs-lookup"><span data-stu-id="4c97b-105">For instructions on how to print an XPS OM that contains a complete XPS document, see [Print a complete XPS OM](#print-a-complete-xps-om).</span></span> <span data-ttu-id="4c97b-106">Pour contenir un document XPS, un modèle d’objet XPS doit inclure les éléments listés dans [créer un modèle d’objet XPS vide](create-a-blank-xps-om.md).</span><span class="sxs-lookup"><span data-stu-id="4c97b-106">To contain an XPS document, an XPS OM must include the items listed in [Create a Blank XPS OM](create-a-blank-xps-om.md).</span></span>

<span data-ttu-id="4c97b-107">Pour obtenir des instructions sur l’impression d’un modèle d’objet XPS créé ou traité une seule page à la fois, consultez [imprimer un modèle OM](#incrementally-print-an-xps-om)de manière incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="4c97b-107">For instructions on how to print an XPS OM that is being created or processed one page at a time, see [Incrementally print an XPS OM](#incrementally-print-an-xps-om).</span></span>

<span data-ttu-id="4c97b-108">Avant d’utiliser ces exemples de code dans votre programme, lisez l’exclusion de responsabilité dans les [tâches de programmation de document XPS courantes](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="4c97b-108">Before using these code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

<span data-ttu-id="4c97b-109">Dans cette rubrique, vous allez apprendre à effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="4c97b-109">In this topic, you will learn how to perform the following tasks:</span></span>

-   [<span data-ttu-id="4c97b-110">Imprimer un modèle d’objet XPS complet</span><span class="sxs-lookup"><span data-stu-id="4c97b-110">Print a complete XPS OM</span></span>](#print-a-complete-xps-om)
-   [<span data-ttu-id="4c97b-111">Imprimer de manière incrémentielle un modèle OM XPS</span><span class="sxs-lookup"><span data-stu-id="4c97b-111">Incrementally print an XPS OM</span></span>](#incrementally-print-an-xps-om)
-   [<span data-ttu-id="4c97b-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c97b-112">Related topics</span></span>](#related-topics)

## <a name="print-a-complete-xps-om"></a><span data-ttu-id="4c97b-113">Imprimer un modèle d’objet XPS complet</span><span class="sxs-lookup"><span data-stu-id="4c97b-113">Print a complete XPS OM</span></span>

<span data-ttu-id="4c97b-114">Quand un modèle d’objet XPS contient un document XPS complet, la méthode [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) de l’interface [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) peut envoyer le contenu du modèle d’objet XPS à une imprimante ou à une file d’attente à l’impression.</span><span class="sxs-lookup"><span data-stu-id="4c97b-114">When an XPS OM contains a complete XPS document, the [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method of the [**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage) interface can send the contents of the XPS OM to a printer or a print queue.</span></span>

<span data-ttu-id="4c97b-115">Pour détecter le moment où le travail d’impression est terminé, créez un descripteur d’événement comme indiqué dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="4c97b-115">To detect when the print job has completed, create an event handle as shown in the following example.</span></span>


```C++
    HANDLE completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



<span data-ttu-id="4c97b-116">Pour imprimer un modèle d’objet XPS complet :</span><span class="sxs-lookup"><span data-stu-id="4c97b-116">To print a complete XPS OM:</span></span>

1.  <span data-ttu-id="4c97b-117">Créez un flux de travail d’impression en appelant [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="4c97b-117">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="4c97b-118">Envoyez le contenu du modèle d’objet XPS au flux en appelant la méthode [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) du package.</span><span class="sxs-lookup"><span data-stu-id="4c97b-118">Send the contents of the XPS OM to the stream by calling the package's [**WriteToStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackage-writetostream) method.</span></span>
3.  <span data-ttu-id="4c97b-119">Fermez le flux de travail d’impression en appelant la méthode **Close** du flux.</span><span class="sxs-lookup"><span data-stu-id="4c97b-119">Close the print job stream by calling the stream's **Close** method.</span></span>
4.  <span data-ttu-id="4c97b-120">Attendez que le travail d’impression signale qu’il est terminé.</span><span class="sxs-lookup"><span data-stu-id="4c97b-120">Wait for the print job to signal that it has completed.</span></span>
5.  <span data-ttu-id="4c97b-121">Vérifiez l’état d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="4c97b-121">Check the completion status.</span></span>
6.  <span data-ttu-id="4c97b-122">Fermer et libérer des ressources.</span><span class="sxs-lookup"><span data-stu-id="4c97b-122">Close and release resources.</span></span>


```C++
    IXpsPrintJob *job = NULL;
    IXpsPrintJobStream *jobStream = NULL;
    hr = StartXpsPrintJob(
                printerName,
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Write package to print job stream
    hr = package->WriteToStream (jobStream, FALSE);

    // Close the stream to tell the print job
    // that the entire document has been sent.
    hr = jobStream->Close();

    // Wait for the print job to finish spooling...
    if (NULL != completionEvent) {
        if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
        {
            // Get the print job status to see why the wait completed.
            //  Note that without waiting for a completion event, 
            //  the print job may not be complete when the status is queried.
            XPS_JOB_STATUS jobStatus;
            hr = job->GetJobStatus(&jobStatus);

            // Evaluate the job status returned.
            switch (jobStatus.completion)
            {
                case XPS_JOB_COMPLETED:
                    // The job completed as expected.
                    hr = S_OK;
                    break;
                case XPS_JOB_CANCELLED:
                    // The job was canceled.
                    hr = E_FAIL;
                    break;
                case XPS_JOB_FAILED:
                    // The job failed, 
                    // jobStatus.jobStatus has the reason.
                    hr = E_FAIL;
                    break;
                default:
                    // An unexpected value was returned.
                    hr = E_UNEXPECTED;
                    break;
            }
                
            // Release completion event handle
            CloseHandle(completionEvent);
        }
        else
        {    // there was a problem, set hr to error status
            hr  = HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // hr contains the result of the print operation

    CoUninitialize(); // if COM is no longer needed in this thread
```



## <a name="incrementally-print-an-xps-om"></a><span data-ttu-id="4c97b-123">Imprimer de manière incrémentielle un modèle OM XPS</span><span class="sxs-lookup"><span data-stu-id="4c97b-123">Incrementally print an XPS OM</span></span>

<span data-ttu-id="4c97b-124">Vous pouvez envoyer des composants de document d’un modèle OM XPS à un travail d’impression de manière incrémentielle, en créant un flux de travail d’impression XPS, puis en transmettant les composants de document individuels au flux de travail d’impression, l’un après l’autre.</span><span class="sxs-lookup"><span data-stu-id="4c97b-124">You can send the document components of an XPS OM to a printer job incrementally, by creating an XPS print job stream and then passing the individual document components to the print job stream, one at a time.</span></span> <span data-ttu-id="4c97b-125">L’ordre dans lequel les composants de document sont envoyés détermine la façon dont ils apparaîtront dans le document terminé.</span><span class="sxs-lookup"><span data-stu-id="4c97b-125">The sequence in which the document components are sent determines how they will appear in the finished document.</span></span> <span data-ttu-id="4c97b-126">Ainsi, avant qu’un programme puisse appeler le code dans cet exemple, il doit correctement organiser les composants de document.</span><span class="sxs-lookup"><span data-stu-id="4c97b-126">Thus, before a program can call the code in this example, it must correctly organize the document components.</span></span>

<span data-ttu-id="4c97b-127">Avant d’utiliser les interfaces du modèle d’objet XPS, initialisez COM dans le thread comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="4c97b-127">Before using XPS OM interfaces, initialize COM in the thread as shown in the following example code.</span></span>


```C++
    HRESULT hr;
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);
```



<span data-ttu-id="4c97b-128">Pour surveiller l’achèvement du travail d’impression, créez un descripteur d’événement comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="4c97b-128">To monitor the print job completion, create an event handle as shown in the following example code.</span></span>


```C++
    HANDLE completionEvent = NULL;
    completionEvent = CreateEvent(NULL, TRUE, FALSE, NULL);
    if (NULL == completionEvent)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        // The method can continue, but print spooling completion
        //  cannot be checked without a valid event handle.
    }
```



<span data-ttu-id="4c97b-129">Créez un flux de travail d’impression et un nouvel enregistreur de package.</span><span class="sxs-lookup"><span data-stu-id="4c97b-129">Create a new print job stream and a new package writer.</span></span> <span data-ttu-id="4c97b-130">Transmettez chacun des composants de document aux méthodes d’écriture de package correspondantes dans l’ordre dans lequel elles apparaissent dans le document terminé.</span><span class="sxs-lookup"><span data-stu-id="4c97b-130">Pass each of the document components to the corresponding package writer methods in the same sequence as they will appear in the finished document.</span></span>

<span data-ttu-id="4c97b-131">Démarrez chaque document nouveau, puis ajoutez-lui des pages.</span><span class="sxs-lookup"><span data-stu-id="4c97b-131">Start each document new, then add pages to it.</span></span> <span data-ttu-id="4c97b-132">Après avoir passé tous les composants de document au flux de travail d’impression, fermez le flux, attendez la fin du travail d’impression, puis fermez et libérez les ressources ouvertes.</span><span class="sxs-lookup"><span data-stu-id="4c97b-132">After passing all document components to the print job stream, close the stream, wait for the print job to complete, and then close and release open resources.</span></span>

1.  <span data-ttu-id="4c97b-133">Créez un flux de travail d’impression en appelant [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span><span class="sxs-lookup"><span data-stu-id="4c97b-133">Create a new print job stream by calling [**StartXpsPrintJob**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob).</span></span>
2.  <span data-ttu-id="4c97b-134">Créez un URI de composant pour la partie FixedDocumentSequence.</span><span class="sxs-lookup"><span data-stu-id="4c97b-134">Create a part URI for the FixedDocumentSequence part.</span></span>
3.  <span data-ttu-id="4c97b-135">Créez un nouvel enregistreur de package sur le flux de travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4c97b-135">Create a new package writer on the print job stream.</span></span>
4.  <span data-ttu-id="4c97b-136">Pour chaque document à écrire :</span><span class="sxs-lookup"><span data-stu-id="4c97b-136">For each document to be written:</span></span>
    1.  <span data-ttu-id="4c97b-137">Créez un nouvel URI de composant pour la partie FixedDocument.</span><span class="sxs-lookup"><span data-stu-id="4c97b-137">Create a new part URI for the FixedDocument part.</span></span>
    2.  <span data-ttu-id="4c97b-138">Démarrez un nouveau document dans le writer de package.</span><span class="sxs-lookup"><span data-stu-id="4c97b-138">Start a new document in the package writer.</span></span>
    3.  <span data-ttu-id="4c97b-139">Pour chaque page du document actif, créez un URI de composant pour la partie FixedPage et ajoutez la page au writer de package.</span><span class="sxs-lookup"><span data-stu-id="4c97b-139">For each page in the current document, create a part URI for the FixedPage part and add the page to the package writer.</span></span>
5.  <span data-ttu-id="4c97b-140">Une fois que toutes les pages ont été ajoutées au writer de package, fermez-la.</span><span class="sxs-lookup"><span data-stu-id="4c97b-140">After all pages have been added to the package writer, close it.</span></span>
6.  <span data-ttu-id="4c97b-141">Fermez le flux de travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4c97b-141">Close the print job stream.</span></span>
7.  <span data-ttu-id="4c97b-142">Attendez la fin du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4c97b-142">Wait for the print job to complete.</span></span>
8.  <span data-ttu-id="4c97b-143">Vérifiez l’état d’achèvement.</span><span class="sxs-lookup"><span data-stu-id="4c97b-143">Check the completion status.</span></span>
9.  <span data-ttu-id="4c97b-144">Fermer et libérer des ressources ouvertes.</span><span class="sxs-lookup"><span data-stu-id="4c97b-144">Close and release open resources.</span></span>


```C++
    IXpsPrintJob* job = NULL;
    IXpsPrintJobStream* jobStream = NULL;
    hr = StartXpsPrintJob(
                argv[1],
                NULL,
                NULL,
                NULL,
                completionEvent,
                NULL,
                0,
                &job,
                &jobStream,
                NULL);

    // Note the implicit requirement that CoInitializeEx 
    //  has previously been called from this thread.
    IXpsOMObjectFactory *xpsFactory = NULL;
    hr = CoCreateInstance(
                __uuidof(XpsOMObjectFactory),
                NULL,
                CLSCTX_INPROC_SERVER,
                __uuidof(IXpsOMObjectFactory),
                reinterpret_cast<void**>(&xpsFactory)
                );
    // Create part URI for FixedDocumentSequence part
    //  This can use a static string because there is only one
    //  FixedDocumentSequence part in the print job.
    IOpcPartUri *partUri = NULL;
    hr = xpsFactory->CreatePartUri(L"/FixedDocumentSequence.fdseq", &partUri);

    // Create the package writer on the print job stream
    //  Note that the interleaving parameter set to 
    //  XPS_INTERLEAVING_ON, the package writer will create
    //  empty print ticket parts when a NULL pointer is
    //  passed in the print ticket argument of this method,
    //  the StartNewDocument method, and the AddPage method.
    //  For more information, see the help for these methods.
    IXpsOMPackageWriter *packageWriter = NULL;
    hr = xpsFactory->CreatePackageWriterOnStream(
            jobStream,
            TRUE,
            XPS_INTERLEAVING_ON, // to create blank print ticket objects
            partUri,
            NULL,
            NULL,
            NULL,
            NULL,
            &packageWriter);
    // release partUri after it's been used to create new doc. seq.
    if (partUri)
    {
        partUri->Release();
        partUri = NULL;
    }

    // Add document content to the print job stream.
    int docNumber = 1;
    int docsInPackage = 1; // Change this value as required.
    while (docNumber <= docsInPackage) {

        // Create a unique part URI for the current document.
        WCHAR DocPartUri[MAX_PATH];
        hr = MakeDocumentPartUri (docNumber, MAX_PATH, DocPartUri);
        hr = xpsFactory->CreatePartUri(DocPartUri, &partUri);
        
        // Initialize the new document in the package writer.
        hr = packageWriter->StartNewDocument(partUri, NULL, NULL, NULL, NULL);

        // release part URI after it's been used to create new doc.
        if (partUri)
        {
            partUri->Release();
            partUri = NULL;
        }

        // Add the pages
        int pageNumber = 1;
        int pagesInDocument = 1; // Change this value as required.
        while (pageNumber <= pagesInDocument) {

            // Create a unique part URI for the current page
            WCHAR PagePartUri[MAX_PATH];
            hr = MakePagePartUri (
                docNumber, 
                pageNumber, 
                MAX_PATH, 
                PagePartUri);
            hr = xpsFactory->CreatePartUri(PagePartUri, &partUri);

            // create page in OM
            XPS_SIZE pageSize = {816, 1056};
            IXpsOMPage *xpsPage = NULL;
            hr = xpsFactory->CreatePage(
                &pageSize, 
                L"en-US", 
                partUri, 
                &xpsPage);

            // release pagePartUri after it's been used to create the page
            if (partUri)
            {
                partUri->Release();
                partUri = NULL;
            }

            // add content to the page or retrieve 
            //  the page from the XPS OM.
            //  (not shown in this example)

            // add page to document
            hr = packageWriter->AddPage(
                        xpsPage,
                        &pageSize,
                        NULL,
                        NULL,
                        NULL,
                        NULL);

             if (xpsPage)
              {
                 xpsPage->Release();
                 xpsPage = NULL;
             }

            // go to the next page
            pageNumber++;
        }
        // the fixed document does not need to be closed.
        // it will be closed when a new fixed doc is opened
        // or the package is closed.

        // go to the next document
        docNumber++;
    }

    // Close the package writer when finished
    hr = packageWriter->Close();

    if (SUCCEEDED(hr))
    {
        // Close the print stream to tell the print
        //  job that the all document contents have
        //  been sent
        hr = jobStream->Close();
        // Wait for the print job to finish spooling...
        if (NULL != completionEvent) {
            if (WaitForSingleObject(completionEvent, INFINITE) == WAIT_OBJECT_0)
            {
                // Get the print job status to see why the wait completed.
                //  Note that without waiting for a completion event, 
                //  the print job may not be complete when the status is queried.
                XPS_JOB_STATUS jobStatus;
                hr = job->GetJobStatus(&jobStatus);

                // Evaluate the job status returned.
                switch (jobStatus.completion)
                {
                    case XPS_JOB_COMPLETED:
                        // The job completed as expected.
                        hr = S_OK;
                        break;
                    case XPS_JOB_CANCELLED:
                        // The job was canceled.
                        hr = E_FAIL;
                        break;
                    case XPS_JOB_FAILED:
                        // The job failed, 
                        // jobStatus.jobStatus has the reason.
                        hr = E_FAIL;
                        break;
                    default:
                        // An unexpected value was returned.
                        hr = E_UNEXPECTED;
                        break;
                }
                    
                // Release completion event handle
                CloseHandle(completionEvent);
            }
            else
            {    // there was a problem, set hr to error status
                hr  = HRESULT_FROM_WIN32(GetLastError());
            }
        }
    } 
    else
    {
        // cancel the job, if one exists, because
        //  the close call returned an error
        if (job) job->Cancel();
    }
    // hr contains the result of the print operation

    // free/release pointers and handles used.

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

    CoUninitialize(); // If done with COM in this thread.
```



<span data-ttu-id="4c97b-145">Quand le programme écrit les composants du document de manière incrémentielle, comme indiqué dans cet exemple, il doit générer les noms des parties de chaque partie document qu’il envoie au flux du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="4c97b-145">When the program is writing the document components incrementally, as shown in this example, it must generate the part names for each document part that it sends to the print job stream.</span></span> <span data-ttu-id="4c97b-146">Dans l’exemple précédent, l’URI du composant FixedDocumentSequence est créé à partir d’une chaîne statique, car il n’y en a qu’une seule partie dans le document XPS.</span><span class="sxs-lookup"><span data-stu-id="4c97b-146">In the preceding example, the FixedDocumentSequence part URI is created from a static string because there is one and only one such part in the XPS document.</span></span> <span data-ttu-id="4c97b-147">L’URI de chaque partie FixedPage et FixedDocument doit être unique dans le document XPS.</span><span class="sxs-lookup"><span data-stu-id="4c97b-147">The URI of each FixedPage and FixedDocument part must be unique within the XPS document.</span></span> <span data-ttu-id="4c97b-148">La génération de l’URI du composant à l’aide de l’index de ces composants peut aider à garantir que la chaîne d’URI résultante est unique dans le document XPS.</span><span class="sxs-lookup"><span data-stu-id="4c97b-148">Building the part URI by using the index of these components can help ensure that the resulting URI string is unique within the XPS document.</span></span>


```C++
HRESULT MakeDocumentPartUri (
                              __in int docNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //  that was passed as an argument
    // for example, "/Documents/1/FixedDocument.fdoc"
    //  where "1" specifies the document number, which would
    //  change with each document printed
    return S_OK;
}
 
HRESULT MakePagePartUri (
                              __in int docNumber,
                              __in int pageNumber,
                              __in DWORD partUriStringLength,
                              __inout LPWSTR partUriStringBuffer
                              )
{
    // create a Part URI string using the document number
    //   and page number that were passed as an argument
    // for example: "/Documents/1/Pages/1.fpage"
    //  where the first "1" between Documents and Pages 
    //  specifies the document number, which would change with
    //  each document. The second "1" specifies the page number,
    //  which would change with each page in the document.
    return S_OK;
}
```



<span data-ttu-id="4c97b-149">Pour plus d’informations sur la structure d’un document XPS, consultez la [spécification Paper XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span><span class="sxs-lookup"><span data-stu-id="4c97b-149">For more information on the structure of an XPS document, see the [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c97b-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4c97b-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4c97b-151">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="4c97b-151">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="4c97b-152">Écrire un modèle OM XPS dans un document XPS</span><span class="sxs-lookup"><span data-stu-id="4c97b-152">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

<span data-ttu-id="4c97b-153">**Utilisé dans cette section**</span><span class="sxs-lookup"><span data-stu-id="4c97b-153">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="4c97b-154">**CoInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="4c97b-154">**CoInitializeEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
</dt> <dt>

[<span data-ttu-id="4c97b-155">**CreateEvent**</span><span class="sxs-lookup"><span data-stu-id="4c97b-155">**CreateEvent**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="4c97b-156">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="4c97b-156">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="4c97b-157">**IXpsOMPackage**</span><span class="sxs-lookup"><span data-stu-id="4c97b-157">**IXpsOMPackage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

[<span data-ttu-id="4c97b-158">**IXpsOMPackageWriter**</span><span class="sxs-lookup"><span data-stu-id="4c97b-158">**IXpsOMPackageWriter**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackagewriter)
</dt> <dt>

[<span data-ttu-id="4c97b-159">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="4c97b-159">**IXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjob)
</dt> <dt>

[<span data-ttu-id="4c97b-160">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="4c97b-160">**IXpsPrintJobStream**</span></span>](/windows/win32/api/xpsprint/nn-xpsprint-ixpsprintjobstream)
</dt> <dt>

[<span data-ttu-id="4c97b-161">**StartXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="4c97b-161">**StartXpsPrintJob**</span></span>](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob)
</dt> <dt>

[<span data-ttu-id="4c97b-162">**WaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="4c97b-162">**WaitForSingleObject**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject)
</dt> <dt>

<span data-ttu-id="4c97b-163">**Pour plus d’informations**</span><span class="sxs-lookup"><span data-stu-id="4c97b-163">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="4c97b-164">Initialiser un modèle d’objet XPS</span><span class="sxs-lookup"><span data-stu-id="4c97b-164">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="4c97b-165">Informations de référence sur l’API de document XPS</span><span class="sxs-lookup"><span data-stu-id="4c97b-165">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="4c97b-166">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="4c97b-166">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
