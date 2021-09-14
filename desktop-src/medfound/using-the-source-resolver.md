---
description: Utilisation du programme de résolution source
ms.assetid: 94e2a411-96b8-4506-8491-78f4f5f286ce
title: Utilisation du programme de résolution source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e992199b097ff3f3337f92216b684d68e46bca13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313670"
---
# <a name="using-the-source-resolver"></a>Utilisation du programme de résolution source

Le résolveur de la source crée la source multimédia appropriée pour un contenu donné à partir d'une URL ou d'un flux d'octets. Pour créer le programme de résolution source, appelez [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver). Cette fonction retourne un pointeur d’interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) .

Le programme de résolution source a des méthodes synchrones et asynchrones. Si vous utilisez le programme de résolution source à partir de votre thread d’application principal, les méthodes asynchrones rendent votre interface utilisateur plus réactive. Les méthodes synchrones peuvent se bloquer pour une durée perceptible, en particulier si le programme de résolution source doit ouvrir une ressource réseau.

Les méthodes synchrones sont les suivantes :

-   [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)
-   [**IMFSourceResolver::CreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfrombytestream)

Les méthodes asynchrones sont les suivantes :

-   [**IMFSourceResolver::BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl)
-   [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream)

Pour les méthodes asynchrones, chaque méthode a une méthode **end...** correspondante pour terminer la requête asynchrone et une méthode **Cancel...** pour annuler une requête en attente. Pour plus d’informations sur les méthodes asynchrones dans Media Foundation, consultez [méthodes de rappel asynchrones](asynchronous-callback-methods.md).

L’exemple de code suivant crée une source de média à partir d’une URL. Cet exemple utilise la méthode synchrone.


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolveur source](source-resolver.md)
</dt> </dl>

 

 



