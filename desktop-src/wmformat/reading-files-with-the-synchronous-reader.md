---
title: Lecture des fichiers avec le lecteur synchrone
description: Lecture des fichiers avec le lecteur synchrone
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows Media Format SDK, lire des fichiers
- Windows Media Format SDK, lecteurs synchrones
- ASF (Advanced Systems Format), lecteurs synchrones
- ASF (format des systèmes avancés), lecteurs synchrones
- Fichiers ASF (Advanced Systems Format), lecture des fichiers
- ASF (format des systèmes avancés), lire les fichiers
- lecteurs synchrones, interface IWMReaderCallback
- IWMReaderCallback, lecteurs synchrones
- lecteurs synchrones, lire des fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404649"
---
# <a name="reading-files-with-the-synchronous-reader"></a>Lecture des fichiers avec le lecteur synchrone

Vous pouvez utiliser le lecteur synchrone pour lire un fichier ASF à l’aide d’appels synchrones au lieu des méthodes asynchrones dans l’objet lecteur. L’utilisation d’appels synchrones réduit le nombre de threads requis pour lire un fichier. Le lecteur asynchrone utilise plusieurs threads pour le traitement des flux. Pour les fichiers contenant plusieurs flux, le nombre de threads utilisés peut devenir très élevé. Le lecteur synchrone n’utilise qu’un seul thread.

Le lecteur synchrone a été conçu pour répondre aux besoins des applications de création de contenu et de modification de fichiers. Vous pouvez utiliser le lecteur synchrone pour d’autres applications, mais ses fonctionnalités sont limitées.

Le lecteur synchrone peut ouvrir des fichiers locaux ou des fichiers sur un réseau à l’aide du nom de chemin d’accès UNC (par exemple, « \\ \\ someshare \\ somedirectory \\ somefile. wmv »). Vous ne pouvez pas diffuser des fichiers vers le lecteur synchrone ou ouvrir des fichiers à partir d’un emplacement Internet. Le lecteur synchrone prend également en charge l’utilisation de l’interface com **IStream** comme source.

Le lecteur synchrone offre plus de polyvalence pour récupérer des exemples d’un fichier ASF que le lecteur asynchrone. Le lecteur synchrone peut fournir des échantillons par numéro de flux, ainsi que par sortie. Les exemples fournis par le numéro de flux peuvent être compressés ou non. Le lecteur synchrone peut également basculer entre les remises compressées et non compressées lors de la lecture. Cette fonctionnalité est appelée « édition rapide ». cette fonctionnalité permet à une application de modification de lire Windows contenu multimédia et de la transmettre directement à l’enregistreur jusqu’à ce qu’un frame souhaité soit atteint. À ce stade, l’application peut indiquer au lecteur de commencer à fournir du contenu non compressé, que l’application peut ensuite modifier et transmettre à l’enregistreur pour la recompression. Lorsque l’application a terminé la modification des frames spécifiés, elle peut demander au lecteur de démarrer à nouveau la diffusion des frames compressés.

Les fonctionnalités les plus basiques de l’objet lecteur synchrone peuvent être décomposées selon les étapes suivantes. dans ces étapes, « l’application » fait référence au programme que vous écrivez à l’aide du kit de développement logiciel (SDK) de Format multimédia Windows.

1.  L’application transmet au lecteur synchrone le nom d’un fichier à lire. Lorsque le lecteur synchrone ouvre le fichier, il attribue un numéro de sortie à chaque flux. Si le fichier utilise l’exclusion mutuelle, le lecteur assigne une seule sortie pour tous les flux qui s’excluent mutuellement.
2.  L’application obtient des informations sur la configuration des différentes sorties à partir du lecteur. Les informations collectées permettront à l’application de restituer correctement les exemples de supports.
3.  L’application commence à demander des exemples, l’un après l’autre, à partir du lecteur synchrone. Le lecteur synchrone remet chaque exemple dans un objet buffer pour lequel il remet l’interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .
4.  L’application est chargée du rendu des données une fois qu’elles sont fournies par le lecteur. le kit de développement logiciel (SDK) Windows Media Format ne fournit pas de routines de rendu. en règle générale, les applications utilisent d’autres kits de développement logiciel (sdk) pour restituer des données, comme le kit de développement logiciel (sdk) microsoft Direct X, ou les fonctions multimédias du kit sdk microsoft Windows platform.

Ces étapes sont illustrées dans l’exemple d’application WMSyncReader. Pour plus d’informations, consultez [exemples d’applications](sample-applications.md).

Le lecteur synchrone prend également en charge des fonctionnalités plus avancées. Le lecteur synchrone vous permet d’effectuer les opérations suivantes :

-   Spécifiez une plage d’échantillons à récupérer par heure ou par numéro de trame.
-   Contrôle de la sélection de flux pour les flux mutuellement exclusifs.
-   Ouvrez un fichier à l’aide de l’interface COM standard, **IStream**.
-   Lire les données de profil à partir de l’en-tête de fichier.
-   Lit les métadonnées de l’en-tête de fichier.
-   Basculer entre les exemples de flux et de sortie pendant la lecture.
-   Basculer entre les exemples de flux compressés et non compressés pendant la lecture.

Les sections suivantes décrivent en détail l’utilisation de l’objet lecteur synchrone.

-   [Pour créer un lecteur synchrone et ouvrir un fichier](to-create-a-synchronous-reader-and-open-a-file.md)
-   [Pour rechercher les numéros de flux et les numéros de sortie](to-find-stream-numbers-and-output-numbers.md)
-   [Pour récupérer des exemples de médias avec le lecteur synchrone](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [Pour effectuer une recherche par heure à l’aide du lecteur synchrone](to-seek-by-time-using-the-synchronous-reader.md)
-   [Pour rechercher par numéro de frame à l’aide du lecteur synchrone](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [Pour effectuer une recherche par code temporel SMPTE à l’aide du lecteur synchrone](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [Pour récupérer des exemples de flux avec le lecteur synchrone](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [Pour récupérer des exemples compressés avec le lecteur synchrone](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

**Exemple de code**

L’exemple de code suivant montre comment lire des exemples à partir d’un fichier ASF à l’aide du lecteur synchrone. Elle spécifie par numéro de trame une plage d’exemples à remettre.


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lecture des fichiers ASF**](reading-asf-files.md)
</dt> <dt>

[**Lecteur synchrone, objet**](synchronous-reader-object.md)
</dt> </dl>

 

 




