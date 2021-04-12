---
description: Utilisation du programme de résolution source
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: Utilisation du programme de résolution source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e992199b097ff3f3337f92216b684d68e46bca13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202245"
---
# <a name="using-the-source-resolver"></a><span data-ttu-id="71e25-103">Utilisation du programme de résolution source</span><span class="sxs-lookup"><span data-stu-id="71e25-103">Using the Source Resolver</span></span>

<span data-ttu-id="71e25-104">Le résolveur de la source crée la source multimédia appropriée pour un contenu donné à partir d'une URL ou d'un flux d'octets.</span><span class="sxs-lookup"><span data-stu-id="71e25-104">The source resolver takes a URL or byte stream and creates the appropriate media source for that content.</span></span> <span data-ttu-id="71e25-105">Pour créer le programme de résolution source, appelez [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver).</span><span class="sxs-lookup"><span data-stu-id="71e25-105">To create the source resolver, call [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver).</span></span> <span data-ttu-id="71e25-106">Cette fonction retourne un pointeur d’interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .</span><span class="sxs-lookup"><span data-stu-id="71e25-106">This function returns an [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) interface pointer.</span></span>

<span data-ttu-id="71e25-107">Le programme de résolution source a des méthodes synchrones et asynchrones.</span><span class="sxs-lookup"><span data-stu-id="71e25-107">The source resolver has both synchronous and asynchronous methods.</span></span> <span data-ttu-id="71e25-108">Si vous utilisez le programme de résolution source à partir de votre thread d’application principal, les méthodes asynchrones rendent votre interface utilisateur plus réactive.</span><span class="sxs-lookup"><span data-stu-id="71e25-108">If you are using the source resolver from your main application thread, the asynchronous methods will make your user interface more responsive.</span></span> <span data-ttu-id="71e25-109">Les méthodes synchrones peuvent se bloquer pour une durée perceptible, en particulier si le programme de résolution source doit ouvrir une ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="71e25-109">The synchronous methods can block for a noticeable amount of time, particularly if the source resolver must open a network resource.</span></span>

<span data-ttu-id="71e25-110">Les méthodes synchrones sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="71e25-110">The synchronous methods are:</span></span>

-   [<span data-ttu-id="71e25-111">**IMFSourceResolver::CreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="71e25-111">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [<span data-ttu-id="71e25-112">**IMFSourceResolver::CreateObjectFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="71e25-112">**IMFSourceResolver::CreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

<span data-ttu-id="71e25-113">Les méthodes asynchrones sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="71e25-113">The asynchronous methods are:</span></span>

-   [<span data-ttu-id="71e25-114">**IMFSourceResolver::BeginCreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="71e25-114">**IMFSourceResolver::BeginCreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [<span data-ttu-id="71e25-115">**IMFSourceResolver::BeginCreateObjectFromByteStream**</span><span class="sxs-lookup"><span data-stu-id="71e25-115">**IMFSourceResolver::BeginCreateObjectFromByteStream**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

<span data-ttu-id="71e25-116">Pour les méthodes asynchrones, chaque méthode a une méthode **end...** correspondante pour terminer la requête asynchrone et une méthode **Cancel...** pour annuler une requête en attente.</span><span class="sxs-lookup"><span data-stu-id="71e25-116">For the asynchronous methods, each method has a corresponding **End...** method to complete the asynchronous request, and a **Cancel...** method to cancel a pending request.</span></span> <span data-ttu-id="71e25-117">Pour plus d’informations sur les méthodes asynchrones dans Media Foundation, consultez [méthodes de rappel asynchrones](asynchronous-callback-methods.md).</span><span class="sxs-lookup"><span data-stu-id="71e25-117">For more information about asynchronous methods in Media Foundation, see [Asynchronous Callback Methods](asynchronous-callback-methods.md).</span></span>

<span data-ttu-id="71e25-118">L’exemple de code suivant crée une source de média à partir d’une URL.</span><span class="sxs-lookup"><span data-stu-id="71e25-118">The following code example creates a media source from a URL.</span></span> <span data-ttu-id="71e25-119">Cet exemple utilise la méthode synchrone.</span><span class="sxs-lookup"><span data-stu-id="71e25-119">This example uses the synchronous method.</span></span>


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="71e25-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="71e25-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71e25-121">Résolveur source</span><span class="sxs-lookup"><span data-stu-id="71e25-121">Source Resolver</span></span>](source-resolver.md)
</dt> </dl>

 

 



