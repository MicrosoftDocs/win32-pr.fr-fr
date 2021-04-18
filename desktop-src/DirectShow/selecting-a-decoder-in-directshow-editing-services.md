---
description: Sélection d’un décodeur dans les services de modification DirectShow
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: Sélection d’un décodeur dans les services de modification DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 956ad0284722eb394590b1b0065f167c55b3cf51
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481512"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a>Sélection d’un décodeur dans les services de modification DirectShow

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Lorsque les [services d’édition DirectShow](directshow-editing-services.md) affichent un projet de montage vidéo, le moteur de rendu sélectionne automatiquement les décodeurs nécessaires. Cela peut se produire à l’intérieur de la méthode [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) , ou de manière dynamique pendant le rendu.

Un utilisateur peut installer plusieurs décodeurs capable de décoder un fichier particulier. Quand plusieurs décodeurs sont disponibles, l’algorithme DES utilise l’algorithme de [connexion intelligente](intelligent-connect.md) pour sélectionner le décodeur.

Il n’existe aucun moyen pour l’application de spécifier directement le décodeur à utiliser. Toutefois, vous pouvez choisir le décodeur indirectement par le biais de l’interface de rappel [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) . En implémentant cette interface dans votre application, vous pouvez recevoir des notifications pendant le processus de création de graphiques et rejeter certains filtres du graphique.

Commencez par implémenter une classe qui expose l’interface [**IAMGraphBuilderCallback**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) :


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



Créez ensuite une instance du gestionnaire de graphes de filtres et enregistrez votre classe pour recevoir des notifications de rappel :


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



Ensuite, créez le moteur de rendu et appelez la méthode [**IRenderEngine :: SetFilterGraph**](irenderengine-setfiltergraph.md) avec un pointeur vers le gestionnaire de graphique de filtre. Cela garantit que le moteur de rendu ne crée pas son propre gestionnaire de graphes de filtre, mais utilise à la place l’instance que vous avez configurée pour les rappels.


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



Lorsque le projet est rendu, la méthode [**IAMGraphBuilderCallback :: SelectedFilter**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) de l’application est appelée immédiatement avant que le gestionnaire de graphique de filtre crée un nouveau filtre. La méthode **SelectedFilter** reçoit un pointeur vers une interface **IMoniker** qui représente un moniker pour le filtre. Examinez le moniker et, si vous décidez de rejeter le filtre, retournez un code d’erreur à partir de la méthode **SelectedFilter** .

La partie difficile consiste à identifier les monikers qui représentent des décodeurs, et en particulier les monikers qui représentent des décodeurs que vous souhaitez rejeter. Une solution est la suivante :

-   Avant de restituer le projet, utilisez la méthode [**IFilterMapper2 :: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) pour créer une liste de filtres inscrits comme acceptant le type d’entrée souhaité. Pour les types de compression vidéo ou audio, cette liste doit être mappée à un ensemble de décodeurs.
-   La méthode **EnumMatchingFilters** retourne une collection de monikers. Pour chaque moniker de la collection, récupérez la propriété **DisplayName** , comme décrit dans [utilisation du mappeur de filtre](using-the-filter-mapper.md).
-   Stockez une liste des noms complets, mais omettez le nom complet qui correspond au filtre que vous souhaitez utiliser pour le décodage. Les noms d’affichage des filtres logiciels se présentent sous la forme suivante :

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    where

    ```C++
    CategoryGUID
    ```

    

    est le GUID de la catégorie de filtre, et

    ```C++
    FilterCLSID
    ```

    

    est le CLSID du filtre. Pour DMOs, le format est le même, mais il prend la `sw` valeur `dmo` .

    La liste contient maintenant des noms complets pour chaque filtre qui génère le type de média souhaité, mais n’est pas votre filtre préféré.

-   Dans la méthode **SelectedFilter** , récupérez la propriété **DisplayName** sur le moniker proposé et vérifiez-le par rapport à la liste stockée. Si le nom complet correspond à une entrée de la liste, rejeter ce filtre. Dans le cas contraire, acceptez-le en renvoyant S \_ OK.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’un projet](rendering-a-project.md)
</dt> </dl>

 

 



