---
description: le gestionnaire de portée d’analyse (CSM) vous permet d’ajouter et de supprimer des racines de recherche pour vos magasins de données depuis et vers la portée de l’analyse de recherche Windows.
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: Gestion des racines de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758d3c10a4c69f336202274cd1fb40528848b0ddb431fd58646cf700d2b2d736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119095286"
---
# <a name="managing-search-roots"></a>Gestion des racines de recherche

le gestionnaire de portée d’analyse (CSM) vous permet d’ajouter et de supprimer des racines de recherche pour vos magasins de données depuis et vers la portée de l’analyse de recherche Windows.

Cette rubrique traite des sujets suivants :

-   [À propos des racines de recherche](#about-search-roots)
-   [Avant de commencer](#before-you-begin)
-   [Windows 7 : nouvelle API du gestionnaire de l’étendue de l’analyse](#windows-7-new-crawl-scope-manager-api)
-   [Ajout de racines à l’étendue de l’analyse](#adding-roots-to-the-crawl-scope)
-   [Suppression de racines de l’étendue de l’analyse](#removing-roots-from-the-crawl-scope)
-   [Énumération des racines dans l’étendue de l’analyse](#enumerating-roots-in-the-crawl-scope)
-   [Rubriques connexes](#related-topics)

 

## <a name="about-search-roots"></a>À propos des racines de recherche

Une racine de recherche définit la base d’un espace de noms Shell dans lequel des étendues spécifiques peuvent être incluses ou exclues, et est généralement le conteneur de niveau le plus élevé dans un protocole qui peut être énuméré. Elle ne spécifie pas les parties de ce magasin qui doivent ou ne doivent pas être indexées ; Il signale simplement qu’un magasin de contenu existe et est associé à un gestionnaire de protocole inscrit. La syntaxe permettant d’identifier une URL racine de recherche comprend le protocole, l’identificateur de sécurité de l’utilisateur ou du magasin, le chemin d’accès et éventuellement un élément spécifique (par exemple, un fichier). Les exemples suivants illustrent deux formes de syntaxe pour une racine de recherche.


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



Le <protocol> segment doit être suivi de deux (2) barres obliques (« / »), sauf s’il s’agit du fichier : Protocol, qui requiert trois barres obliques (file:///). Le <site or SID> segment représente soit un magasin de contenu, soit un identificateur de sécurité de l’utilisateur si la racine de recherche est destinée à être spécifique à l’utilisateur. Le <path> segment est un ensemble de conteneurs, comme des répertoires ou des dossiers, et peut inclure le caractère générique « \* ». Les <item> le segment est facultatif et peut également inclure le caractère générique « \* ». Si vous n’incluez pas d’élément, veillez à terminer le segment de chemin d’accès par une barre oblique ou l’indexeur supposera que le dernier sous-conteneur est un élément.

Par exemple, supposons que vous avez implémenté un gestionnaire de protocole (myPH) pour gérer les fichiers de type \* . myext pour une application personnalisée. Tous ces fichiers se trouvent dans le dossier WorkteamA \\ ProjectFiles sur un ordinateur local. La racine de recherche de qui peut se présenter comme suit :

-   myPH:///C : \\ WorkteamA \\ ProjectFiles\\

Supposons que vous envisagez d’inclure tous les fichiers. myext, mais rien d’autre de ce conteneur dans l’index. La racine de recherche de qui peut se présenter comme suit :

-   myPH:///C : \\ WorkteamA \\ ProjectFiles \\ \* . myext.

Les modèles de caractères génériques définissent des URL en utilisant le caractère générique « \* » et sont considérés comme un modèle plutôt qu’une URL, mais la terminologie est souvent utilisée de façon interchangeable. Par exemple, file:///C : \\ \\ \* \\ les données ProjectA \\ correspondent aux URL suivantes :

-   C : \\ ProjectA \\ **version1** \\ données\\
-   C : \\ ProjectA \\ **version2** \\ données\\

Mais ce modèle ne correspond pas à cette URL :

-   C : \\ ProjectA \\ **version1 \\**- \\ données temporaires\\

Vous devez créer de nouvelles racines de recherche pour les conteneurs qui ne se trouvent pas déjà dans l’étendue de l’analyse de l’indexeur. Si le chemin d’accès C : \\ ParentScope est déjà inclus dans l’étendue de l’analyse, vous n’avez pas besoin d’ajouter une nouvelle racine de recherche pour C : \\ ParentScope \\ ChildScope, sauf si vous savez que l’étendue enfant a été précédemment exclue.

l’interface utilisateur permettant de définir Windows options de recherche affiche les racines de recherche pour les utilisateurs afin qu’ils puissent affiner les règles d’étendue pour leurs recherches. Dans le cadre du processus d’installation de votre gestionnaire de protocole personnalisé, de votre conteneur et/ou de votre application, vous pouvez définir une étendue d’analyse par défaut avec des règles d’inclusion et d’exclusion. Ces règles sont présentées aux utilisateurs finaux en tant qu’emplacements. Les utilisateurs peuvent naviguer dans les sous-répertoires de votre racine de recherche prédéfinie et sélectionner ceux qu’ils souhaitent inclure dans les recherches ou effacer ceux qu’ils souhaitent exclure.

 

## <a name="before-you-begin"></a>Avant de commencer

Avant de pouvoir utiliser l’une des interfaces CSM (Analysis Scope Manager), vous devez effectuer les étapes préalables suivantes :

1.  Créez l’objet **CrawlSearchManager** et obtenez son interface [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .
2.  Appelez [**ISearchManager :: getCatalog,**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) pour « SystemIndex » pour obtenir une instance d’une interface [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .
3.  Appelez [**ISearchCatalogManager :: GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) pour obtenir une instance de l’interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) .

Après avoir apporté des modifications au gestionnaire de l’étendue de l’analyse (CSM), vous devez appeler [**ISearchCrawlScopeManager ::**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall)saproduction. Cette méthode ne prend pas de paramètres et retourne S \_ OK en cas de réussite.

 

## <a name="windows-7-new-crawl-scope-manager-api"></a>Windows 7 : nouvelle API du gestionnaire de l’étendue de l’analyse

dans **Windows 7 et versions ultérieures**, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) étend les fonctionnalités de l’interface [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) . La méthode [**ISearchCrawlScopeManager2 :: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) obtient la version du gestionnaire de portée d’analyse (CSM), qui informe les clients si l’état du CSM a changé. **ISearchCrawlScopeManager2 :: GetVersion** n’entraîne pas d’appel interprocessus. Si la fonction est réussie, le pointeur retourné reste valide jusqu’à ce que le client appelle **UnmapViewOfFile** sur le pointeur et **CloseHandle** sur le handle retourné.

 

## <a name="adding-roots-to-the-crawl-scope"></a>Ajout de racines à l’étendue de l’analyse

Le [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) indique au moteur de recherche les conteneurs à analyser et/ou à surveiller, ainsi que les éléments sous ces conteneurs à inclure ou exclure. Pour ajouter une nouvelle racine de recherche, instanciez un objet [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) , définissez les attributs racine, puis appelez [**ISearchCrawlScopeManager :: AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) et transmettez-lui un pointeur vers votre objet **ISearchRoot** . L’URL racine de recherche prend la même forme que la racine de recherche décrite précédemment.

Le tableau suivant décrit les méthodes put pertinentes pour [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot); les autres méthodes put de l’interface ne sont pas utilisées actuellement par Windows la recherche. Pour une meilleure sécurité, nous vous recommandons d’inclure les identificateurs de sécurité (SID) des utilisateurs dans toutes les racines. Les racines par utilisateur sont plus sécurisées, car les requêtes sont exécutées dans un processus par utilisateur, ce qui garantit qu’un utilisateur ne peut pas voir les éléments indexés à partir de la boîte de réception d’un autre utilisateur, par exemple.



| Méthode                     | Description                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| put \_ ProvidesNotifications | Affectez la valeur **true** si un gestionnaire de protocole ou une autre application informe le moteur de recherche des modifications apportées aux URL sous la racine de recherche. La notification indique que les URL doivent être réindexées. |
| put \_ RootURL               | Définit l’URL racine de la recherche actuelle. L’URL prend le formulaire racine de recherche décrit précédemment.                                                                                                      |



 

 

Par défaut, l’indexeur n’analyse pas une étendue lorsque vous ajoutez une racine de recherche. Vous devez également ajouter une règle d’inclusion pour la racine. Si vous souhaitez ajouter une racine spécifique à l’utilisateur pour une application, cette application doit ajouter les racines appropriées pour les nouveaux utilisateurs au démarrage de l’application.

Pour ajouter les racines appropriées pour les nouveaux utilisateurs :

1.  Obtient le SID de l’utilisateur.
2.  Énumérer toutes les racines pour vérifier si elle existe pour ce SID.
3.  Ajoutez une nouvelle racine, en utilisant le SID, si nécessaire.

 

## <a name="removing-roots-from-the-crawl-scope"></a>Suppression de racines de l’étendue de l’analyse

Vous pouvez utiliser [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) pour supprimer une racine de l’étendue de l’analyse lorsque vous ne voulez plus que cette URL soit indexée. La suppression d’une racine entraîne également la suppression de toutes les règles d’étendue pour cette URL. Par exemple, supposons que vous souhaitez désinstaller un magasin de contenu et/ou son gestionnaire de protocole d’un système. Vous pouvez désinstaller l’application, supprimer toutes les données, puis supprimer la racine de recherche de l’étendue de l’analyse, et le gestionnaire de l’étendue de l’analyse supprime la racine et toutes les règles d’étendue associées à la racine.

Pour supprimer une racine de recherche existante, appelez [**ISearchCrawlScopeManager :: RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) avec la racine de recherche que vous souhaitez supprimer. L’URL racine de recherche prend la même forme que la racine de recherche décrite précédemment. Cette méthode retourne S \_ false si la racine est introuvable et un code d’erreur si une erreur s’est produite lors de la suppression d’une racine qui a été trouvée.

la suppression d’une racine de recherche supprime également l’URL de l’interface utilisateur pour Windows options de recherche, de sorte que les utilisateurs peuvent ne pas être en mesure de rajouter ce conteneur ou cet emplacement à l’aide de l’interface utilisateur. Il est également possible de supprimer tous les remplacements définis par l’utilisateur d’une racine de recherche et de rétablir les règles de la racine et de l’étendue de la recherche d’origine. Pour plus d’informations, consultez [gestion des règles d’étendue](-search-3x-wds-extidx-csm-scoperules.md).

> [!Note]  
> sur Windows Vista, si les utilisateurs sont supprimés via les profils utilisateur dans le panneau de configuration, CSM supprime toutes les règles et toutes les racines avec leur SID et supprime leurs éléments indexés du catalogue. sur Windows XP, vous devez supprimer manuellement les racines et les règles des utilisateurs.

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a>Énumération des racines dans l’étendue de l’analyse

CSM énumère les racines de recherche à l’aide d’une interface d’énumérateur de style COM standard, [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots). Vous pouvez utiliser cette interface pour énumérer les racines de recherche à plusieurs fins. Par exemple, vous pouvez afficher l’intégralité de l’étendue de l’analyse dans une interface utilisateur ou déterminer si une racine particulière ou l’enfant d’une racine se trouve déjà dans l’étendue de l’analyse.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
</dt> <dt>

[**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[Gestion des règles d’étendue](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



