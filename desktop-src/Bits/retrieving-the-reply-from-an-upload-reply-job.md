---
title: Récupération de la réponse d’un travail de Upload-Reply
description: Pour charger des données dans une application serveur et faire en sorte qu’elles retournent des données au client, spécifiez la tâche en tant que tâche de \_ réponse de chargement du type de tâche BG \_ \_ \_ .
ms.assetid: bab28a2c-1e2f-4b76-9dc6-57df26f7efec
ms.topic: article
ms.date: 11/29/2018
ms.openlocfilehash: 582a37a31c13c5cc3e0b44c51a767cfbe465c64c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007699"
---
# <a name="retrieving-the-reply-from-an-upload-reply-job"></a>Récupération de la réponse d’un travail de Upload-Reply

Un travail de Upload-Reply BITS, en plus de charger un fichier sur un serveur, examine également une URL de réponse envoyée dans le cadre de la réponse du serveur, puis suit automatiquement l’URL de réponse et télécharge une réponse à partir de celle-ci. Pour plus d’informations sur la valeur d’en-tête BITS-reply-URL, consultez la documentation du [fragment ACK](/windows/desktop/Bits/ack-for-fragment) .

Définissez le type de travail en \_ \_ \_ \_ réponse à chargement de type de tâche BG pour créer un travail de type Upload-Reply. Les données de réponse sont disponibles pour le client une fois que le travail a passé à l’état de la \_ tâche BG \_ \_ transféré. Pour récupérer la réponse, appelez l’une des méthodes suivantes :

-   [**IBackgroundCopyJob2::GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata)

    Fournit une copie en mémoire des données de réponse. Utilisez cette méthode pour lire les données de réponse avant ou après l’appel de la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Si les données de réponse dépassent 1 Mo, l’application doit appeler la méthode [**IBackgroundCopyJob2 :: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) pour récupérer le nom du fichier de réponse et lire directement son contenu.

-   [**IBackgroundCopyJob2::GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename)

    Fournit le nom du fichier qui contient la réponse. Vous devez appeler la méthode **méthode ibackgroundcopyjob :: Complete** avant d’ouvrir et de lire le fichier de réponse ; le fichier de réponse n’est pas disponible pour le client tant que vous n’avez pas appelé la méthode **Complete** .

Appelez ces méthodes dans votre méthode [**IBackgroundCopyCallback :: JobTransferred**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopycallback-jobtransferred) uniquement si la réponse est petite et peut être traitée rapidement afin de ne pas bloquer le thread de rappel. Si vous utilisez la [**notification de ligne de commande**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setnotifycmdline) au lieu du rappel, transmettez l’identificateur de tâche au fichier exécutable. Le fichier exécutable utilise l’identificateur de tâche pour appeler la méthode **complète** afin de rendre le fichier de réponse disponible.

Les exemples suivants montrent comment utiliser chaque méthode pour récupérer les données de réponse.

-   [Utilisation de GetReplyData](#using-getreplydata)
-   [Utilisation de GetReplyFileName](#using-getreplyfilename)

## <a name="using-getreplydata"></a>Utilisation de GetReplyData

L’exemple suivant montre comment récupérer les données de réponse à l’aide de la méthode [**IBackgroundCopyJob2 :: GetReplyData**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplydata) . L’exemple suppose que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) est valide, que le type du travail est upload-reply et que l’état de la tâche est un \_ État de travail BG \_ \_ transféré.


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



## <a name="using-getreplyfilename"></a>Utilisation de GetReplyFileName

L’exemple suivant montre comment récupérer les données de réponse à l’aide de la méthode [**IBackgroundCopyJob2 :: GetReplyFileName**](/windows/desktop/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-getreplyfilename) . L’exemple part du principe que le pointeur d’interface [**méthode ibackgroundcopyjob**](/windows/desktop/api/Bits/nn-bits-ibackgroundcopyjob) est valide, que le type de travail est chargement-réponse et que l’état du travail est \_ État du travail BG \_ \_ transféré.


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



 

 




