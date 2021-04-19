---
title: Pour indexer un fichier ASF
description: Pour indexer un fichier ASF
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows Media Format SDK, indexation de fichiers ASF
- ASF (Advanced Systems Format), indexation de fichiers
- ASF (format des systèmes avancés), indexation des fichiers
- index, indexation de fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7206e1856abb9705e18e885ba06cb8253a93c84b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509633"
---
# <a name="to-index-an-asf-file"></a><span data-ttu-id="a4525-107">Pour indexer un fichier ASF</span><span class="sxs-lookup"><span data-stu-id="a4525-107">To Index an ASF File</span></span>

<span data-ttu-id="a4525-108">Le processus d’indexation d’un fichier ASF est très simple.</span><span class="sxs-lookup"><span data-stu-id="a4525-108">The process of indexing an ASF file is very simple.</span></span> <span data-ttu-id="a4525-109">Effectuez un appel à [**IWMIndexer :: StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) et transmettez le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="a4525-109">Make a call to [**IWMIndexer::StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) and pass the file name.</span></span> <span data-ttu-id="a4525-110">L’indexeur fait le reste.</span><span class="sxs-lookup"><span data-stu-id="a4525-110">The indexer does the rest.</span></span> <span data-ttu-id="a4525-111">L’appel à **StartIndexing** est asynchrone, de sorte que l’État doit être surveillé à l’aide du rappel **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="a4525-111">The call to **StartIndexing** is asynchronous, so status must be monitored using the **OnStatus** callback.</span></span>

<span data-ttu-id="a4525-112">Le code suivant montre comment indexer un fichier ASF.</span><span class="sxs-lookup"><span data-stu-id="a4525-112">The following code shows how to index an ASF file.</span></span> <span data-ttu-id="a4525-113">Si vous souhaitez configurer l’indexeur avant d’indexer le fichier, vous devez inclure le code de l’exemple fourni dans [pour configurer l’indexeur](to-configure-the-indexer.md).</span><span class="sxs-lookup"><span data-stu-id="a4525-113">If you want to configure the indexer prior to indexing the file, you will need to include code from the example included in [To Configure the Indexer](to-configure-the-indexer.md).</span></span>

<span data-ttu-id="a4525-114">Pour cet exemple, le handle qui pointe vers l’événement doit être créé en tant que variable globale afin d’être accessible par le rappel.</span><span class="sxs-lookup"><span data-stu-id="a4525-114">For this example, the handle that points to the event must be created as a global variable so it will be accessible by the callback.</span></span> <span data-ttu-id="a4525-115">La déclaration suivante doit apparaître dans une portée globale.</span><span class="sxs-lookup"><span data-stu-id="a4525-115">The following declaration should appear in a global scope.</span></span>


```C++
HANDLE g_hEvent = NULL;

```



<span data-ttu-id="a4525-116">Dans un scénario plus réaliste, le descripteur d’événement doit être un membre de données de la classe qui contient à la fois le rappel et la logique de démarrage de l’indexeur.</span><span class="sxs-lookup"><span data-stu-id="a4525-116">In a more realistic scenario, the event handle should be a data member of the class that contains both the callback and the logic for starting the indexer.</span></span>

<span data-ttu-id="a4525-117">L’indexeur envoie plusieurs événements au rappel **OnStatus** après l’appel à **IWMIndexer :: StartIndexing**.</span><span class="sxs-lookup"><span data-stu-id="a4525-117">The indexer sends several events to the **OnStatus** callback after the call to **IWMIndexer::StartIndexing**.</span></span> <span data-ttu-id="a4525-118">Vous pouvez les intercepter en fonction des besoins de votre application.</span><span class="sxs-lookup"><span data-stu-id="a4525-118">You can trap them as needed for your application.</span></span> <span data-ttu-id="a4525-119">Au minimum, vous devez intercepter les valeurs WMT \_ fermées, qui sont envoyées lorsque l’indexation est terminée.</span><span class="sxs-lookup"><span data-stu-id="a4525-119">At a minimum, you need to trap WMT\_CLOSED, which is sent when indexing is complete.</span></span> <span data-ttu-id="a4525-120">Utilisez la logique suivante dans le commutateur de message dans votre implémentation du rappel **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="a4525-120">Use the following logic within the message switch in your implementation of the **OnStatus** callback.</span></span>


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



<span data-ttu-id="a4525-121">Pour cet exemple, il est supposé que votre implémentation du rappel **OnStatus** est accessible via un objet appelé MyCallBack.</span><span class="sxs-lookup"><span data-stu-id="a4525-121">For this example it is assumed that your implementation of the **OnStatus** callback is accessed through an object called MyCallback.</span></span> <span data-ttu-id="a4525-122">Pour plus d’informations sur l’utilisation des événements et des rappels avec ce kit de développement logiciel (SDK), consultez [utilisation des méthodes de rappel](using-the-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="a4525-122">For more information about using events and callbacks with this SDK, see [Using the Callback Methods](using-the-callback-methods.md).</span></span>


```C++
IWMIndexer* pMyIndexer     = NULL;
HRESULT     hr             = S_OK;
WCHAR       pwszFileName[] = L"C:\SomeFile.wmv";

// Initialize COM.
hr = CoInitialize(NULL);

// Create an event for asynchronous calls.
g_hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

// Create an indexer.
hr = WMCreateIndexer(&pMyIndexer);

// TODO: Configure the indexer if needed. See To Configure the Indexer.

// Start the indexer.
hr = pMyIndexer->StartIndexing(pwszFileName, &MyCallback, NULL);

// Wait for the indexer to finish.
WaitForSingleObject(g_hEvent, INFINITE);

// Clean up.
pMyIndexer->Release();
pMyIndexer = NULL

CloseHandle(g_hEvent);
g_hEvent = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="a4525-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4525-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4525-124">**Interface IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="a4525-124">**IWMIndexer Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[<span data-ttu-id="a4525-125">**Pour configurer l’indexeur**</span><span class="sxs-lookup"><span data-stu-id="a4525-125">**To Configure the Indexer**</span></span>](to-configure-the-indexer.md)
</dt> <dt>

[<span data-ttu-id="a4525-126">**WMCreateIndexer**</span><span class="sxs-lookup"><span data-stu-id="a4525-126">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="a4525-127">**Utilisation des index**</span><span class="sxs-lookup"><span data-stu-id="a4525-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




