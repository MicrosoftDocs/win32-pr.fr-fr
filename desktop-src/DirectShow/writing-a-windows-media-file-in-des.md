---
description: écriture d’un fichier multimédia Windows dans des
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: écriture d’un fichier multimédia Windows dans des
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05b954ae6046bb61027bd3e7f63bcd2fcaafa35020bc0a8a1bed278b99731ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650489"
---
# <a name="writing-a-windows-media-file-in-des"></a>écriture d’un fichier multimédia Windows dans des

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

cette section décrit comment écrire un fichier multimédia Windows à l’aide DES [Services d’édition DirectShow](directshow-editing-services.md) (DES).

> [!IMPORTANT]
> n’utilisez pas le moteur de rendu intelligent pour écrire Windows fichiers multimédias. Utilisez toujours le moteur de rendu de base (CLSID \_ RenderEngine).

 

pour écrire un fichier multimédia Windows, procédez comme suit :

1.  Appelez **SetSite** sur le moteur de rendu, avec un pointeur vers votre fournisseur de clés.
2.  Créez le composant frontal du graphique. (Consultez [rendu d’un Project](rendering-a-project.md).)
3.  Créez le filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) et ajoutez-le au graphique.
4.  Utilisez l’interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) sur le filtre du writer WM ASF pour définir le nom de fichier.
5.  configurez le Writer WM ASF pour utiliser un profil de média Windows. Chaque profil a un nombre prédéfini de flux. Vous devez choisir un profil qui correspond aux groupes de votre projet.

    L’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) contient différentes méthodes pour définir le profil. Par exemple, la méthode **ConfigureFilterUsingProfileGuid** spécifie un profil système comme GUID. vous pouvez utiliser Windows méthodes Media Format pour recevoir un pointeur **IWMProfile** , puis appeler [**IConfigAsfWriter :: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile). Pour plus d’informations, consultez [configuration de l’enregistreur ASF](configuring-the-asf-writer.md).

6.  Connecter le serveur frontal à l’enregistreur ASF. La partie frontale du graphique contient une broche de sortie pour chaque groupe. En supposant que vous avez spécifié un profil compatible, l’enregistreur ASF doit avoir un ensemble de broches d’entrée correspondant. Connecter chaque broche de sortie à la broche d’entrée correspondante. Le moyen le plus simple consiste à utiliser la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) . tout d’abord, créez une nouvelle instance de [Capture Graph Builder](capture-graph-builder.md) et initialisez-la avec un pointeur vers le gestionnaire de Graph de filtres :

    ```C++
    ICaptureGraphBuilder2 *pBuild = 0;
    hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 0, CLSCTX_INPROC_SERVER,
        IID_ICaptureGraphBuilder2, (void**)&pBuild);
    pBuild->SetFiltergraph(pGraph); 
    ```

    

    Ensuite, récupérez la broche de sortie pour chaque groupe en appelant la méthode [**IRenderEngine :: GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) . Appelez **RenderStream** pour connecter le pin à l’enregistreur ASF :

    ```C++
    long cGroups = 0;
    hr = pTimeline->GetGroupCount(&cGroups);
    for (long i = 0; i < cGroups; i++)
    {
        IPin *pPin;
        hr = pRenderEngine->GetGroupOutputPin(i, &pPin);
        if (SUCCEEDED(hr))
        {
            hr = pBuild->RenderStream(0, 0, pPin, 0, pASF);
        }
        pPin->Release();
    }
    pBuild->Release
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utilisation de Windows Media avec les Services d’édition DirectShow](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



