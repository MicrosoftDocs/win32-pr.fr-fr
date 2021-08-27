---
description: Connecter intelligente
ms.assetid: 938ba1b0-822e-4871-8786-b7eeee243867
title: Connecter intelligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2248dc936076dfcad1b2ad934da4ef6a8b1e28a260ff75ebca3a63ec6356bf6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107699"
---
# <a name="intelligent-connect"></a>Connecter intelligente

le Connecter Intelligent est le mécanisme utilisé par le gestionnaire de Graph de filtres pour créer des graphiques de filtres. Il se compose de plusieurs algorithmes associés qui sélectionnent des filtres et les ajoutent au graphique de filtre.

Lisez cette rubrique si vous avez des difficultés à créer un graphique de filtre et que vous souhaitez résoudre le problème, ou si vous écrivez votre propre filtre et que vous souhaitez le rendre disponible pour la génération automatique de graphiques.

la Connecter intelligente implique les méthodes [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) suivantes :

-   [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)
-   [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)
-   [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)
-   [**IGraphBuilder :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)

### <a name="igraphbuilderaddsourcefilter"></a>IGraphBuilder::AddSourceFilter

La méthode [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) ajoute un filtre source qui peut restituer un fichier spécifié. Tout d’abord, il consulte le registre et les correspondances avec le protocole (par exemple `https://` ,), l’extension de nom de fichier ou un ensemble d' *octets de vérification* prédéterminés, qui sont des octets à des décalages particuliers dans le fichier qui correspondent à certains modèles. Pour plus d’informations, consultez [inscription d’un type de fichier personnalisé](registering-a-custom-file-type.md). En supposant que la méthode localise un filtre source approprié, elle crée ensuite une instance de ce filtre, l’ajoute au graphique et appelle la méthode [**IFileSourceFilter :: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) du filtre avec le nom de fichier.

### <a name="igraphbuilderrender"></a>IGraphBuilder :: Render

La méthode [**IGraphBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) génère une sous-section d’un graphique. Il démarre à partir d’une broche de sortie non connectée et fonctionne en aval, en ajoutant de nouveaux filtres en fonction des besoins. Le filtre de départ doit déjà figurer dans le graphique. À chaque étape, la méthode **Render** recherche un filtre qui peut se connecter au filtre précédent. Le flux peut créer une branche si un filtre de connexion a plusieurs broches de sortie. La recherche s’arrête lorsque chaque flux a un convertisseur. Si la méthode **Render** est bloquée, elle peut être sauvegardée et réessayer, à l’aide d’un autre jeu de filtres.

Pour connecter chaque broche de sortie, la méthode [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) effectue les opérations suivantes :

1.  si le code pin prend en charge l’interface [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) , le gestionnaire de Graph de filtre délègue l’ensemble du processus à la méthode [**IStreamBuilder :: Render**](/windows/desktop/api/Strmif/nf-strmif-istreambuilder-render) du pin. En exposant cette interface, le code PIN assume la responsabilité de la création du reste du graphique, vers le convertisseur. Toutefois, très peu de pin prennent en charge cette interface.
2.  le gestionnaire de Graph de filtre tente d’utiliser les filtres qui sont mis en cache dans la mémoire, le cas échéant. tout au long du processus de Connecter Intelligent, le gestionnaire de Graph de filtres peut mettre en cache les filtres des étapes précédentes du processus. (consultez également [génération de Graph dynamique](dynamic-graph-building.md).)
3.  si le graphique de filtre contient des filtres avec des broches d’entrée non connectées, le gestionnaire de Graph de filtre les essaie ensuite. Vous pouvez forcer la méthode [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) à essayer un filtre particulier en ajoutant ce filtre au graphique avant d’appeler **Render**.
4.  à partir de Windows 7, DirectShow contient une liste de filtres préférés pour certains sous-types de médias. s’il existe un filtre par défaut pour le type de média restitué, le gestionnaire de Graph de filtre tente de filtrer la suite. Une application peut modifier la liste des filtres préférés à l’aide de l’interface [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) . Les modifications apportées à la liste affectent le processus actuel de l’application et sont ignorées une fois le processus terminé.
5.  enfin, si aucun filtre approprié n’a été trouvé, le gestionnaire de Graph de filtre recherche le registre à l’aide de la méthode [**IFilterMapper2 :: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) . Il tente de faire correspondre les types de média préférés du pin de sortie par rapport aux types de média indiqués dans le registre.

    Chaque filtre est inscrit avec un *mérite*, une valeur numérique qui indique le degré de préférence du filtre par rapport à d’autres filtres. La méthode [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) retourne des filtres par ordre de mérite, avec un mérite minimal de **mérite \_ n' \_ \_ utilise pas** + 1. Il ignore les filtres avec un mérite **de \_ mérite \_ n' \_ utilise pas** ou moins. Les filtres sont également regroupés en catégories, définies par GUID. Les catégories elles-mêmes ont un mérite, et la méthode **EnumMatchingFilters** ignore toute catégorie avec un mérite de **mérite \_ n' \_ \_ utilise pas** ou moins, même si les filtres de cette catégorie ont des valeurs de mérite plus élevées.

    à partir de Windows 7, DirectShow contient une liste de filtres bloqués pour certains sous-types de médias. le gestionnaire de Graph de filtre ignore les filtres de cette liste. Une application peut modifier la liste des filtres bloqués à l’aide de l’interface [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) . Les modifications apportées à cette liste affectent le processus en cours de l’application et sont ignorées une fois le processus terminé.

Pour résumer, la méthode [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) tente des filtres dans l’ordre suivant :

1.  Utilisez [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder).
2.  Essayez les filtres mis en cache.
3.  Essayez des filtres dans le graphique.
4.  Windows 7 ou version ultérieure : essayez le filtre par défaut pour le type de média, le cas échéant.
5.  Recherchez des filtres dans le registre.

### <a name="igraphbuilderrenderfile"></a>IGraphBuilder :: RenderFile

La méthode [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) crée un graphique de lecture par défaut à partir d’un nom de fichier. En interne, cette méthode utilise [**AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) pour localiser le filtre source correct, et [**restituer**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) pour générer le reste du graphique.

### <a name="igraphbuilderconnect"></a>IGraphBuilder :: Connecter

la méthode [**IGraphBuilder :: Connecter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connecte une broche de sortie à une broche d’entrée. Cette méthode ajoute des filtres intermédiaires, si nécessaire, à l’aide d’une variation de l’algorithme décrit pour la méthode [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) :

1.  Essayez une connexion directe entre les filtres, sans filtres intermédiaires.
2.  Essayez les filtres mis en cache.
3.  Essayez des filtres dans le graphique.
4.  Windows 7 ou version ultérieure : essayez le filtre par défaut pour le type de média, le cas échéant.
5.  Recherchez des filtres dans le registre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtrer les catégories](filter-categories.md)
</dt> <dt>

[Mérite](merit.md)
</dt> <dt>

[simulation d’Graph génération avec GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[Génération du filtre Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



