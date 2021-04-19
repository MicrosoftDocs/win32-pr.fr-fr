---
description: Écriture d’un fichier Windows Media dans DES
ms.assetid: 741ebcbc-62fb-4c7f-845f-a361f5b63f8c
title: Écriture d’un fichier Windows Media dans DES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0626a3ef609dee87d90a6d3c2caa023e9ac9a29a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106537174"
---
# <a name="writing-a-windows-media-file-in-des"></a>Écriture d’un fichier Windows Media dans DES

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Cette section décrit comment écrire un fichier Windows Media à l’aide des [services de modification DirectShow](directshow-editing-services.md) (des).

> [!IMPORTANT]
> N’utilisez pas le moteur de rendu intelligent pour écrire des fichiers Windows Media. Utilisez toujours le moteur de rendu de base (CLSID \_ RenderEngine).

 

Pour écrire un fichier Windows Media, procédez comme suit :

1.  Appelez **SetSite** sur le moteur de rendu, avec un pointeur vers votre fournisseur de clés.
2.  Créez le composant frontal du graphique. (Consultez [rendu d’un projet](rendering-a-project.md).)
3.  Créez le filtre d' [enregistreur ASF WM](wm-asf-writer-filter.md) et ajoutez-le au graphique.
4.  Utilisez l’interface [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) sur le filtre du writer WM ASF pour définir le nom de fichier.
5.  Configurez l’enregistreur ASF WM pour utiliser un profil Windows Media. Chaque profil a un nombre prédéfini de flux. Vous devez choisir un profil qui correspond aux groupes de votre projet.

    L’interface [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter) contient différentes méthodes pour définir le profil. Par exemple, la méthode **ConfigureFilterUsingProfileGuid** spécifie un profil système comme GUID. Vous pouvez utiliser les méthodes de format Windows Media pour récupérer un pointeur **IWMProfile** , puis appeler [**IConfigAsfWriter :: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile). Pour plus d’informations, consultez [configuration de l’enregistreur ASF](configuring-the-asf-writer.md).

6.  Connectez le serveur frontal à l’enregistreur ASF. La partie frontale du graphique contient une broche de sortie pour chaque groupe. En supposant que vous avez spécifié un profil compatible, l’enregistreur ASF doit avoir un ensemble de broches d’entrée correspondant. Connectez chaque broche de sortie à la broche d’entrée correspondante. Le moyen le plus simple consiste à utiliser la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) . Tout d’abord, créez une nouvelle instance du [Générateur de graphiques de capture](capture-graph-builder.md) et initialisez-la avec un pointeur vers le gestionnaire de graphique de filtre :

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

[Utilisation de Windows Media avec les services de modification DirectShow](using-windows-media-with-directshow-editing-services.md)
</dt> </dl>

 

 



