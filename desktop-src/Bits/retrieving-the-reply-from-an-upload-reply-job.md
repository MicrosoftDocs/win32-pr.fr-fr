---
title: Récupération de la réponse d’un travail de Upload-Reply
description: Pour charger des données dans une application serveur et faire en sorte qu’elles retournent des données au client, spécifiez la tâche en tant que tâche de \_ réponse de chargement du type de tâche BG \_ \_ \_ .
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 582a37a31c13c5cc3e0b44c51a767cfbe465c64c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939705"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a><span data-ttu-id="be35a-103">Récupération de la réponse d’un travail de Upload-Reply</span><span class="sxs-lookup"><span data-stu-id="be35a-103">Retrieving the Reply from an Upload-Reply Job</span></span>

<span data-ttu-id="be35a-104">Un travail de Upload-Reply BITS, en plus de charger un fichier sur un serveur, examine également une URL de réponse envoyée dans le cadre de la réponse du serveur, puis suit automatiquement l’URL de réponse et télécharge une réponse à partir de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="be35a-104">A BITS Upload-Reply job, in addition to uploading a file to a server, will also examine a reply URL sent as part of the server reply and then automatically follow the reply URL and download a response from it.</span></span> <span data-ttu-id="be35a-105">Pour plus d’informations sur la valeur d’en-tête BITS-reply-URL, consultez la documentation du [fragment ACK](/windows/desktop/Bits/ack-for-fragment) .</span><span class="sxs-lookup"><span data-stu-id="be35a-105">See the [Ack for Fragment](/windows/desktop/Bits/ack-for-fragment) documentation for more details about the BITS-Reply-URL header value.</span></span>

<span data-ttu-id="be35a-106">Définissez le type de travail en \_ \_ \_ \_ réponse à chargement de type de tâche BG pour créer un travail de type Upload-Reply.</span><span class="sxs-lookup"><span data-stu-id="be35a-106">Set the job type as BG\_JOB\_TYPE\_UPLOAD\_REPLY to create an Upload-Reply type job.</span></span> <span data-ttu-id="be35a-107">Les données de réponse sont disponibles pour le client une fois que le travail a passé à l’état de la \_ tâche BG \_ \_ transféré.</span><span class="sxs-lookup"><span data-stu-id="be35a-107">The reply data is available to the client after the job enters the BG\_JOB\_STATE\_TRANSFERRED state.</span></span> <span data-ttu-id="be35a-108">Pour récupérer la réponse, appelez l’une des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="be35a-108">To retrieve the reply, call one of the following methods:</span></span>

-   [<span data-ttu-id="be35a-109">**IBackgroundCopyJob2::GetReplyData**</span><span class="sxs-lookup"><span data-stu-id="be35a-109">**IBackgroundCopyJob2::GetReplyData**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    <span data-ttu-id="be35a-110">Fournit une copie en mémoire des données de réponse.</span><span class="sxs-lookup"><span data-stu-id="be35a-110">Provides an in-memory copy of the reply data.</span></span> <span data-ttu-id="be35a-111">Utilisez cette méthode pour lire les données de réponse avant ou après l’appel de la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) .</span><span class="sxs-lookup"><span data-stu-id="be35a-111">Use this method to read the reply data before or after calling the [**IBackgroundCopyJob::Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) method.</span></span> <span data-ttu-id="be35a-112">Si les données de réponse dépassent 1 Mo, l’application doit appeler la méthode [**IBackgroundCopyJob2 :: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) pour récupérer le nom du fichier de réponse et lire directement son contenu.</span><span class="sxs-lookup"><span data-stu-id="be35a-112">If the reply data exceeds 1 MB, the application must call the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method to retrieve the name of the reply file and read its contents directly.</span></span>

-   [<span data-ttu-id="be35a-113">**IBackgroundCopyJob2::GetReplyFileName**</span><span class="sxs-lookup"><span data-stu-id="be35a-113">**IBackgroundCopyJob2::GetReplyFileName**</span></span>](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    <span data-ttu-id="be35a-114">Fournit le nom du fichier qui contient la réponse.</span><span class="sxs-lookup"><span data-stu-id="be35a-114">Provides the name of the file that contains the reply.</span></span> <span data-ttu-id="be35a-115">Vous devez appeler la méthode **méthode ibackgroundcopyjob :: Complete** avant d’ouvrir et de lire le fichier de réponse ; le fichier de réponse n’est pas disponible pour le client tant que vous n’avez pas appelé la méthode **Complete** .</span><span class="sxs-lookup"><span data-stu-id="be35a-115">You must call the **IBackgroundCopyJob::Complete** method before opening and reading the reply file; the reply file is not available to the client until you call the **Complete** method.</span></span>

<span data-ttu-id="be35a-116">Appelez ces méthodes dans votre méthode [**IBackgroundCopyCallback :: JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) uniquement si la réponse est petite et peut être traitée rapidement afin de ne pas bloquer le thread de rappel.</span><span class="sxs-lookup"><span data-stu-id="be35a-116">Call these methods in your [**IBackgroundCopyCallback::JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) method only if the reply is small and can be processed quickly so as to not block the callback thread.</span></span> <span data-ttu-id="be35a-117">Si vous utilisez la [**notification de ligne de commande**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) au lieu du rappel, transmettez l’identificateur de tâche au fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="be35a-117">If you use [**command line notification**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) instead of the callback, pass the job identifier to the executable file.</span></span> <span data-ttu-id="be35a-118">Le fichier exécutable utilise l’identificateur de tâche pour appeler la méthode **complète** afin de rendre le fichier de réponse disponible.</span><span class="sxs-lookup"><span data-stu-id="be35a-118">The executable file uses the job identifier to call the **Complete** method to make the reply file available.</span></span>

<span data-ttu-id="be35a-119">Les exemples suivants montrent comment utiliser chaque méthode pour récupérer les données de réponse.</span><span class="sxs-lookup"><span data-stu-id="be35a-119">The following examples show how to use each method to retrieve the reply data.</span></span>

-   [<span data-ttu-id="be35a-120">Utilisation de GetReplyData</span><span class="sxs-lookup"><span data-stu-id="be35a-120">Using GetReplyData</span></span>](#using-getreplydata)
-   [<span data-ttu-id="be35a-121">Utilisation de GetReplyFileName</span><span class="sxs-lookup"><span data-stu-id="be35a-121">Using GetReplyFileName</span></span>](#using-getreplyfilename)

## <a name="using-getreplydata"></a><span data-ttu-id="be35a-122">Utilisation de GetReplyData</span><span class="sxs-lookup"><span data-stu-id="be35a-122">Using GetReplyData</span></span>

<span data-ttu-id="be35a-123">L’exemple suivant montre comment récupérer les données de réponse à l’aide de la méthode [**IBackgroundCopyJob2 :: GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) .</span><span class="sxs-lookup"><span data-stu-id="be35a-123">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) method.</span></span> <span data-ttu-id="be35a-124">L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) est valide, que le type du travail est upload-reply et que l’état de la tâche est un \_ État de travail BG \_ \_ transféré.</span><span class="sxs-lookup"><span data-stu-id="be35a-124">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of the job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
BYTE* pReply = NULL;
UINT64 ReplySize;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyData method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyData(&pReply, &ReplySize);
    if (S_OK == hr))
    {
        if (pReply)
        {
            //Do something with the data.
            CoTaskMemFree(pReply);
        }
        else
        {
            //The server application did not return a reply.
        }
    }
    else if (BG_E_TOO_LARGE == hr)
    {
        //The reply exceeds 1 MB. To retrieve the reply, get the reply file name,
        //complete the job, open the reply file, and read the reply.
    }
    else
    {
        //Handle the error
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



## <a name="using-getreplyfilename"></a><span data-ttu-id="be35a-125">Utilisation de GetReplyFileName</span><span class="sxs-lookup"><span data-stu-id="be35a-125">Using GetReplyFileName</span></span>

<span data-ttu-id="be35a-126">L’exemple suivant montre comment récupérer les données de réponse à l’aide de la méthode [**IBackgroundCopyJob2 :: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) .</span><span class="sxs-lookup"><span data-stu-id="be35a-126">The following example shows how to retrieve the reply data using the [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) method.</span></span> <span data-ttu-id="be35a-127">L’exemple part du principe que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) est valide, que le type de travail est chargement-réponse et que l’état du travail est \_ État du travail BG \_ \_ transféré.</span><span class="sxs-lookup"><span data-stu-id="be35a-127">The example assumes the [**IBackgroundCopyJob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) interface pointer is valid, the type of job is upload-reply, and the state of the job is BG\_JOB\_STATE\_TRANSFERRED.</span></span>


```C++
HRESULT hr;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
WCHAR* pszFileName = NULL;

//Need to query the IBackgroundCopyJob interface for an IBackgroundCopyJob2
//interface pointer. The IBackgroundCopyJob2 interface contains the GetReplyFileName method.
hr = pJob->QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&pJob2);
if (SUCCEEDED(hr))
{
    hr = pJob2->GetReplyFileName(&pszFileName);
    if (SUCCEEDED(hr))
    {
        //Calling the Complete method removes the job from the queue, 
        //so make sure you maintain an interface pointer to this job 
        //or retrieve any job related information that you require 
        //when processing the reply.
        hr = pJob->Complete();

        //Open, read the file, and do something with the data.
        CoTaskMemFree(pszFileName);
    }

    pJob2->Release(); //When done, release the interface.
}
else
{
    //Handle error. QueryInterface will return E_NOINTERFACE if the version of BITS
    //running on the computer is less than BITS 1.5.
}
```



 

 




