---
title: Lecture de fichiers ASF dans DirectShow (kit de développement logiciel (SDK) Windows Media format 11)
description: Lecture de fichiers ASF dans DirectShow
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, lire des fichiers ASF
- Kit de développement logiciel (SDK) Windows Media format, filtre de lecteur ASF WM
- Windows Media Format SDK, interface IMediaSeeking
- ASF (Advanced Systems Format), DirectShow
- ASF (format avancé des systèmes), DirectShow
- Fichiers ASF (Advanced Systems Format), lecture des fichiers
- ASF (format des systèmes avancés), lire les fichiers
- ASF (Advanced Systems Format), filtre de lecteur ASF WM
- ASF (format des systèmes avancés), filtre de lecteur ASF WM
- ASF (Advanced Systems Format), interface IMediaSeeking
- ASF (format des systèmes avancés), interface IMediaSeeking
- DirectShow, lire des fichiers ASF
- DirectShow, filtre de lecteur ASF WM
- DirectShow, interface IMediaSeeking
- Filtre de lecteur ASF WM
- IMediaSeeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf7ba34444f4a3b46f4413958bd26ba4bafc8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104317034"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>Lecture de fichiers ASF dans DirectShow (kit de développement logiciel (SDK) Windows Media format 11)

La lecture des fichiers ASF est gérée par le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) . Lorsque le lecteur ASF WM lit un fichier, il crée automatiquement une broche de sortie pour chaque flux, y compris les flux Web, les flux de commandes de script et tout autre type de flux arbitraire. Dans le cas de plusieurs fichiers à vitesse de transmission, les codes confidentiels sont créés uniquement pour les flux actuellement sélectionnés.

Le lecteur ASF WM prend en charge l’interface DirectShow **IMediaSeeking** , qui permet aux applications d’effectuer une recherche temporelle dans le fichier. Toutefois, la lecture à des vitesses autres que 1,0 (comme spécifié dans **IMediaSeeking ::** sesente) n’est pas prise en charge.

Le filtre expose également plusieurs interfaces du kit de développement logiciel (SDK) du format Windows Media, comme décrit dans le tableau suivant.



| Interface                                        | Exposition                            | Commentaires                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Via **IServiceProvider** sur le filtre | Fourni pour les applications qui doivent lire du contenu protégé par des Rights Management numériques (DRM). Cette interface peut également être utilisée pour obtenir directement d’autres interfaces sur l’objet lecteur. |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** sur le filtre           | Fourni pour permettre aux applications de lire les attributs de fichier et de contenu, ainsi que les informations de marqueur et de script et les métadonnées.                                                                  |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** sur le filtre           | Partiellement implémenté sur le filtre afin que les applications puissent accéder aux méthodes d’information sur l’objet WM Reader.                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** sur le filtre           | Partiellement implémenté sur le filtre afin que les applications puissent accéder aux méthodes d’information sur l’objet lecteur.                                                                         |



 

Le filtre de [lecteur ASF WM](wm-asf-reader-filter.md) a été mis à disposition pour la première fois dans DirectShow 8,0. La version du filtre fourni avec DirectShow 8,1 et 9,0 prend en charge la version 7. *x* du kit de développement logiciel (SDK) du format Windows Media. La version la plus récente du filtre, avec les autres composants QASF, est fournie avec et prend en charge le kit de développement logiciel (SDK) Windows Media Format 9 Series, ainsi que les versions ultérieures, et remplace le filtre dans DirectX 9,0. Si vous installez le kit de développement logiciel (SDK) Windows Media format après l’installation de DirectX 8. *x* ou 9. *x* SDK, vous remplacerez la version DirectX de qasf.dll par la version 9 Series. Cela ne doit pas poser de problèmes, sauf dans un scénario où cela entraînerait un comportement différent dans la méthode DirectShow **IGraphBuilder :: RenderFile** . La version du kit de développement logiciel (SDK) de Windows Media Format 9 du lecteur ASF WM est le filtre source par défaut pour les extensions de nom de fichier. ASF,. wmv et. WMA. Cela signifie que le lecteur ASF WM est automatiquement créé et ajouté au graphique de filtre par le gestionnaire de graphique de filtre dans des méthodes telles que **IGraphBuilder :: RenderFile** ou **IGraphBuilder :: AddSourceFilter** lorsqu’un fichier de ce type est spécifié. Dans DirectX 9,0 et versions antérieures, et Windows XP Service Pack 1 et versions antérieures, la méthode **RenderFile** utilise l’ancien filtre source Windows Media. Ce comportement a été maintenu pour garantir la compatibilité descendante avec les applications qui utilisaient le lecteur Windows Media 6,4. Pour plus d’informations sur le filtre de source Windows Media hérité, consultez la documentation du kit de développement logiciel (SDK) DirectShow.

Pour lire un fichier ASF avec du contenu Windows Media à l’aide du lecteur ASF WM, les trois étapes principales sont la création d’une instance du gestionnaire de graphes de filtre, l’appel de **IGraphBuilder :: RenderFile** pour créer le graphique, puis l’appel de **IMediaControl :: Run** pour lire le fichier. L’exemple de code suivant est un programme complet qui lit un fichier ASF à l’aide de DirectShow. Pour exécuter cet exemple, vous devez avoir installé le kit de développement logiciel (SDK) DirectX et votre environnement de build doit être configuré conformément aux instructions de la rubrique de la documentation du kit de développement logiciel (SDK) DirectShow « configuration de l’environnement de génération ». En outre, vous devez spécifier un fichier sur votre ordinateur dans l’appel à **RenderFile**.


```C++
#include <dshow.h>
#include <stdio.h>

void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the Filter Graph Manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file
    // on your system.
    hr = pGraph->RenderFile(L"test.wmv", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}

```



Notez que le code de l’application pour cet exemple simple ne référence jamais spécifiquement le lecteur ASF WM. Ce filtre est créé, connecté, exécuté et finalement libéré par le gestionnaire de graphique de filtre. Toutefois, dans de nombreux scénarios, vous souhaiterez peut-être configurer le lecteur ASF WM avant de commencer la lecture.

 

 




