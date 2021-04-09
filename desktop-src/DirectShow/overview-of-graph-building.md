---
description: Vue d’ensemble de la génération de graphiques
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Vue d’ensemble de la génération de graphiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109078"
---
# <a name="overview-of-graph-building"></a>Vue d’ensemble de la génération de graphiques

Pour créer un graphique de filtre, commencez par créer une instance du gestionnaire de graphes de filtre :


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



Le gestionnaire de graphes de filtre prend en charge les méthodes de création de graphiques suivantes :

-   [**IFilterGraph :: ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) essaie d’établir une connexion directe entre deux broches. Si les codes confidentiels ne peuvent pas se connecter, la méthode échoue.
-   [**IGraphBuilder :: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connecte deux broches. Si possible, il établit une connexion directe. Dans le cas contraire, il utilise des filtres intermédiaires pour terminer la connexion.
-   [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) commence à partir d’une broche de sortie et génère le reste du graphique. Cette méthode ajoute des filtres en fonction des besoins, en aval, jusqu’à ce qu’elle atteigne un filtre de convertisseur.
-   [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) crée un graphique de lecture de fichier complet.
-   [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) ajoute un filtre au graphique. Il ne connecte pas le filtre. Vous devez créer le filtre avant d’appeler cette méthode, soit en appelant **CoCreateInstance** , soit en utilisant le mappeur de filtre ou l’énumérateur de périphérique système.

Ces méthodes fournissent trois approches de base pour générer le graphique :

1.  Le gestionnaire de graphique de filtre crée le graphique entier.
2.  Le gestionnaire de graphique de filtre génère une partie du graphique.
3.  L’application génère le graphique entier.

**Le gestionnaire de graphique de filtre crée le graphique entier**

Si vous souhaitez simplement lire un fichier créé dans un format reconnu, par exemple AVI, MPEG, WAV ou MP3, utilisez la méthode **RenderFile** . L’article [Comment lire un fichier](how-to-play-a-file.md) montre comment procéder.

La méthode **RenderFile** commence par Rechercher dans le registre un filtre source qui peut analyser le fichier. Elle utilise le protocole (par exemple, « `https://` » dans l’URL), l’extension de fichier ou des modèles d’octets prédéfinis dans le fichier pour déterminer le filtre source. Pour plus d’informations, consultez [inscription d’un type de fichier personnalisé](registering-a-custom-file-type.md).

Pour créer le reste du graphique, le gestionnaire de graphes de filtre utilise un processus itératif dans lequel il prend les types de média qu’un filtre prend en charge sur ses broches de sortie, et recherche dans le registre les filtres qui acceptent ce type de média comme entrée. Il utilise plusieurs critères pour affiner la recherche et définir la priorité des filtres :

-   La *catégorie de filtre* identifie les fonctionnalités générales du filtre.
-   Le type de média décrit le type de données que le filtre peut accepter comme entrée ou remettre en sortie.
-   La *mérite* détermine l’ordre dans lequel les filtres sont essayés. Si deux filtres de la même catégorie de filtre prennent tous deux en charge les mêmes types d’entrée, le gestionnaire de graphes de filtre sélectionne celui dont la valeur mérite la plus élevée. Certains filtres reçoivent intentionnellement une valeur de faible valeur, car ils sont conçus à des fins spécialisées et doivent être ajoutés uniquement au graphique par l’application.

Le gestionnaire de graphique de filtre utilise l’objet [Mappeur de filtre](filter-mapper.md) pour rechercher dans le registre.

À mesure que chaque filtre est ajouté, le gestionnaire de graphes de filtre tente de le connecter à la broche de sortie du filtre précédent. Les filtres négocient pour déterminer s’ils peuvent se connecter et, le cas échéant, le type de média à utiliser pour la connexion. Si le nouveau filtre ne peut pas se connecter, le gestionnaire de graphes de filtres l’ignore et tente un autre filtre. Ce processus se poursuit jusqu’à ce que chaque flux soit rendu.

**Le gestionnaire de graphes de filtres génère une partie du graphique**

Pour effectuer une tâche allant au-delà de la simple exécution d’un fichier, votre application doit effectuer au moins une partie du travail de génération du graphique. Par exemple, une application de capture vidéo doit sélectionner un filtre de source de capture et l’ajouter au graphique. Si vous écrivez des données dans un fichier AVI, vous devez ajouter les filtres AVI MUX et writer de fichier au graphique. Toutefois, il est souvent possible de laisser le gestionnaire de graphes de filtres compléter le graphique. Par exemple, vous pouvez afficher un code confidentiel pour l’aperçu en appelant la méthode **Render** .

**L’application génère le graphique entier**

Dans certains scénarios, votre application peut avoir besoin de générer le graphique en ajoutant et en connectant chaque filtre. Dans ce cas, vous connaissez probablement spécifiquement les filtres qui doivent être ajoutés au graphique. Avec cette approche, l’application ajoute chaque filtre en appelant **AddFilter**, énumère les broches sur les filtres et les connecte en appelant **Connect** ou **ConnectDirect**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de graphiques à l’aide du générateur de graphiques de capture](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[Énumération des appareils et des filtres](enumerating-devices-and-filters.md)
</dt> <dt>

[Énumération d’objets dans un graphique de filtre](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Techniques d' Graph-Building générales](general-graph-building-techniques.md)
</dt> <dt>

[Génération du graphique de filtre](building-the-filter-graph.md)
</dt> </dl>

 

 



