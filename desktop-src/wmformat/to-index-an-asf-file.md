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
ms.openlocfilehash: 08c2e41ed60ecb8fcee39da35dbc79ec44cece8db62f3e040d42aee3374c5690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845577"
---
# <a name="to-index-an-asf-file"></a>Pour indexer un fichier ASF

Le processus d’indexation d’un fichier ASF est très simple. Effectuez un appel à [**IWMIndexer :: StartIndexing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) et transmettez le nom de fichier. L’indexeur fait le reste. L’appel à **StartIndexing** est asynchrone, de sorte que l’État doit être surveillé à l’aide du rappel **OnStatus** .

Le code suivant montre comment indexer un fichier ASF. Si vous souhaitez configurer l’indexeur avant d’indexer le fichier, vous devez inclure le code de l’exemple fourni dans [pour configurer l’indexeur](to-configure-the-indexer.md).

Pour cet exemple, le handle qui pointe vers l’événement doit être créé en tant que variable globale afin d’être accessible par le rappel. La déclaration suivante doit apparaître dans une portée globale.


```C++
HANDLE g_hEvent = NULL;

```



Dans un scénario plus réaliste, le descripteur d’événement doit être un membre de données de la classe qui contient à la fois le rappel et la logique de démarrage de l’indexeur.

L’indexeur envoie plusieurs événements au rappel **OnStatus** après l’appel à **IWMIndexer :: StartIndexing**. Vous pouvez les intercepter en fonction des besoins de votre application. Au minimum, vous devez intercepter les valeurs WMT \_ fermées, qui sont envoyées lorsque l’indexation est terminée. Utilisez la logique suivante dans le commutateur de message dans votre implémentation du rappel **OnStatus** .


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



Pour cet exemple, il est supposé que votre implémentation du rappel **OnStatus** est accessible via un objet appelé MyCallBack. Pour plus d’informations sur l’utilisation des événements et des rappels avec ce kit de développement logiciel (SDK), consultez [utilisation des méthodes de rappel](using-the-callback-methods.md).


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMIndexer**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Pour configurer l’indexeur**](to-configure-the-indexer.md)
</dt> <dt>

[**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Utilisation des index**](working-with-indexes.md)
</dt> </dl>

 

 




