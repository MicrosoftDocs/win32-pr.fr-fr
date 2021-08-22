---
description: Cette rubrique décrit les trois étapes du processus d’indexation et les principaux composants impliqués dans chacun d’entre eux, explique le minutage de l’activité d’indexation et fournit des notes pour les développeurs tiers qui souhaitent des magasins de données ou des formats de fichiers indexés.
ms.assetid: cfba12eb-4123-4b57-8311-d4fc8f9f514e
title: processus d’indexation dans Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5f69306834c001a122a18087205d64b6164d51618226fe0e0fb735f7f5b905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094996"
---
# <a name="indexing-process-in-windows-search"></a>processus d’indexation dans Windows Search

Cette rubrique décrit les trois étapes du processus d’indexation et les principaux composants impliqués dans chacun d’entre eux, explique le minutage de l’activité d’indexation et fournit des notes pour les développeurs tiers qui souhaitent des magasins de données ou des formats de fichiers indexés.

Cette rubrique est organisée comme suit :

- [Vue d'ensemble](#overview)
- [Étape 1 : mise en file d’attente des URL pour l’indexation](#stage-1-queuing-urls-for-indexing)
- [Étape 2 : analyse des URL](#stage-2-crawling-urls)
- [Étape 3 : mise à jour de l’index](#stage-3-updating-the-index)
- [Planification de l’indexation](#how-indexing-is-scheduled)
- [Notes pour les responsables de l’implémentation](#notes-to-implementers)
- [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Windows la recherche prend en charge l’indexation de propriétés et de contenu à partir de fichiers de différents formats de fichiers, tels que des formats de .doc ou. jpeg, et de magasins de données, tels que le système de fichiers ou Windows Outlook boîtes aux lettres. Il existe deux types d’index : les index de valeur qui permettent le filtrage et le tri par la valeur entière d’une propriété et les index inversés qui indexent les mots dans les propriétés textuelles ou le contenu. si vous disposez d’un format de fichier personnalisé ou d’un magasin de données, vous devez comprendre comment Windows index de recherche pour que vos éléments soient indexés correctement.

le processus d’indexation s’effectue en trois étapes, contrôlées par un composant de recherche Windows appelé rassembleur. Dans la première étape, le rassembleur ajoute des URL aux files d’attente. Les URL identifient les éléments à indexer et les files d’attente sont simplement des listes de priorités d’URL. au cours de la deuxième étape, le rassembleur coordonne les autres Windows la recherche et les composants tiers pour accéder aux éléments et collecter des données à leur sujet. Enfin, dans la troisième étape, les données collectées sont ajoutées à l’index.

Le diagramme suivant montre les principaux composants et le workflow des données via le processus d’indexation. Un certain nombre de composants sont impliqués dans la collecte de données pour l’index. certaines d’entre elles font partie de la recherche Windows, et d’autres proviennent d’applications tierces. si vous avez un magasin de données ou un format de fichier personnalisé, Windows recherche s’appuie sur le gestionnaire de protocole et le filtre pour accéder aux url et émettre des propriétés pour l’indexation. Windows Les composants de recherche sont affichés en bleu et les composants tiers sont affichés en vert.

![Diagramme montrant l’interaction entre les composants pendant le processus d’indexation](images/indexingcompoverview.jpg)

## <a name="stage-1-queuing-urls-for-indexing"></a>Étape 1 : mise en file d’attente des URL pour l’indexation

Lors de la première étape de l’indexation, le rassembleur collecte des informations sur les mises à jour des magasins de données, compare ces informations à l’étendue de l’analyse connue, puis crée une file d’attente d’URL à parcourir pour collecter les données de l’index. Pour les sources qui ne sont pas basées sur la notification, telles que les lecteurs FAT, le rassembleur initie régulièrement une traversée complète de l’étendue de l’analyse afin que les données de l’index soient actualisées. Pour les sources telles que NTFS, il n’existe qu’une seule analyse et tout le reste est géré par les notifications à partir du [Journal des modifications USN](/windows/desktop/FileIO/change-journals). Il n’y a pas non plus d’analyse de Microsoft Outlook. Le diagramme suivant présente une vue d’ensemble du processus de mise en file d’attente pour l’indexation sans analyse.

![Diagramme montrant le processus d’interrogation pour l’indexation non-analyse](images/queuingurls.jpg)

le reste de cette section explique comment Windows recherche détermine les url à analyser et définit des termes importants en cours de route.

**Étendue** de l’analyse  la portée de l’analyse est un ensemble d’url que Windows recherche parcourt pour collecter des données sur les éléments que l’utilisateur souhaite indexer pour accélérer les recherches. Windows La recherche ajoute des URL à l’étendue de l’analyse par défaut, comme les chemins d’accès aux dossiers **documents** et **images** des utilisateurs. D’autres URL peuvent être ajoutées par des applications tierces, des utilisateurs et des stratégie de groupe. Enfin, les utilisateurs et les stratégie de groupe peuvent exclure explicitement des URL. Windows La recherche prend toutes les URL ajoutées et supprime les URL exclues pour déterminer la portée de l’analyse. Il s’agit de la plage de travail des URL à partir de laquelle le rassembleur commence son travail.

**Rassembleur**  le rassembleur est un composant de recherche Windows qui collecte des informations sur les url au sein de l’étendue de l’analyse et crée une file d’attente d’url à analyser par l’indexeur. Lorsqu’un élément de la portée d’analyse est ajouté, supprimé ou mis à jour, le rassembleur est averti par le fournisseur de notifications de la Banque de données. Il existe une analyse initiale où le rassembleur démarre à la racine de l’étendue de l’analyse. L’URL est transmise au gestionnaire de protocole puis au [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)approprié. Le filtre est généralement une énumération de répertoires qui génère plus d’URL. Les notifications sont à l’état stable. En règle générale, chaque magasin de données a son propre gestionnaire de protocole qui fournit ces notifications. Par exemple, sur le système de fichiers local, le [Journal des modifications USN](/windows/desktop/FileIO/change-journals) agit comme un fournisseur de notifications pour toutes les URL sous le protocole file://. de même, Microsoft Outlook agit comme un fournisseur de notifications pour toutes les url sous le protocole mapi://. lorsqu’un utilisateur reçoit, déplace ou supprime un e-mail, Outlook informe le rassembleur de l’état modifié de l’e-mail. À partir de ces notifications, le rassembleur crée des files d’attente d’indexation des URL à analyser.

**Indexation des files d’attente**  Les files d’attente d’indexation sont des listes d’URL qui identifient les éléments qui doivent être indexés ou réindexés. Le rassembleur compare les URL qu’il reçoit des fournisseurs de notification aux URL dans l’étendue de l’analyse. Chaque URL des fournisseurs de notifications qui se trouve dans l’étendue de l’analyse est ajoutée à une file d’attente utilisée par le rassembleur pour hiérarchiser les URL à traiter par la suite.

Il existe trois files d’attente : les notifications de haute priorité, les notifications normales et les analyses périodiques. La file d’attente à priorité élevée concerne les notifications qui doivent être traitées immédiatement. par exemple, lorsqu’un utilisateur modifie la propriété de titre d’un élément dans l’explorateur de Windows, la vue de l’explorateur de Windows doit être mise à jour immédiatement après la modification. La file d’attente de notifications normale concerne toutes les notifications de modifications restantes. Les files d’attente de notification sont traitées avant la file d’attente d’analyse, car les éléments modifiés sont plus susceptibles d’intéresser un utilisateur. Le rassembleur accède aux données des URL sur chaque file d’attente dans l’ordre premier entré, premier sorti (FIFO).

pour plus d’informations sur la hiérarchisation et les api d’événements introduites dans Windows 7, consultez [indexation des événements d’ensemble de priorités et d’ensembles de lignes dans Windows 7](indexing-prioritization-and-rowset-events.md). Pour plus d’informations sur la gestion des étendues de l’analyse et les notifications, consultez [fourniture de notifications de modification](-search-3x-wds-notifyingofchanges.md) et [utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md).

## <a name="stage-2-crawling-urls"></a>Étape 2 : analyse des URL

Au cours de la deuxième étape de l’indexation, le rassembleur analyse les files d’attente, en accédant aux magasins de données et en récupérant les flux d’éléments. Tout d’abord, le rassembleur recherche le gestionnaire de protocole approprié pour chaque URL. Ensuite, le rassembleur passe l’URL au gestionnaire de protocole. Le gestionnaire de protocole accède à l’élément et retourne les métadonnées d’élément au Rassembleur. Le rassembleur utilise les métadonnées pour identifier le filtre correct.

Le diagramme suivant présente une vue d’ensemble du processus d’analyse d’URL. Cette étape comprend une coordination et une communication considérables entre les composants.

![Diagramme montrant le processus d’analyse des URL et d’accès aux éléments](images/crawlingqueues.jpg)

le reste de cette section décrit comment Windows recherche accède à des éléments pour l’indexation et explique les rôles de chacun des composants impliqués.

**Rassembleur**  À l’étape 2, la phase d’analyse, le rassembleur traite les URL dans les files d’attente, en commençant par la file d’attente à priorité élevée. Chaque URL est examinée pour identifier son protocole. Le rassembleur recherche ensuite le gestionnaire de protocole inscrit pour ce protocole et l’instancie dans le processus hôte du protocole de recherche.

**Hôte de protocole de recherche**  L’hôte de protocole de recherche est simplement un processus hôte boxed pour les gestionnaires de protocole. en règle générale, Windows recherche crée deux processus hôtes de ce type, un qui s’exécute dans le contexte de sécurité système et un qui s’exécute dans le contexte de sécurité de l’utilisateur. Cette séparation garantit que les données spécifiques à un utilisateur ne sont jamais exécutées dans le contexte du système.

Windows La recherche utilise également le processus hôte pour isoler une instance d’un gestionnaire de protocole à partir d’autres processus ou applications. De cette façon, aucune application externe ne peut accéder à cette instance spécifique du gestionnaire de protocole et si le gestionnaire de protocole échoue de façon inattendue, seul le processus d’indexation est affecté. étant donné que le processus hôte exécute du code tiers (gestionnaires de protocole), Windows recherche recycle régulièrement le processus afin de réduire le temps nécessaire à une attaque pour exploiter les informations du processus. Au-delà, l’hôte de protocole de recherche n’affecte pas l’analyse des URL ou l’indexation des éléments.

**Gestionnaires de protocole**  Les gestionnaires de protocole permettent d’accéder aux éléments d’un magasin de données à l’aide du protocole du magasin de données. Par exemple, le gestionnaire de protocole NTFS fournit l’accès aux fichiers sur un lecteur local à l’aide du protocole file://. Le gestionnaire de protocole sait comment parcourir le magasin de données, identifier les éléments nouveaux ou mis à jour et notifier le rassembleur. Ensuite, lorsque l’analyse commence, le gestionnaire de protocole fournit un objet [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) au Rassembleur pour établir une liaison avec le flux sous-jacent de l’élément et retourner des métadonnées d’élément, telles que des restrictions de sécurité et l’heure de dernière modification.

> [!NOTE]  
> les gestionnaires de protocole ne sont pas Windows des composants de recherche ; Il s’agit de composants du protocole et du magasin de données spécifiques auxquels ils sont destinés à accéder. Si vous avez un magasin de données personnalisé que vous souhaitez indexer, vous devez implémenter un gestionnaire de protocole. Pour plus d’informations sur les gestionnaires de protocole et sur la façon d’en implémenter un, consultez [développement de gestionnaires de protocole](-search-3x-wds-phaddins.md).

**Métadonnées et flux**  À l’aide des métadonnées retournées par l’objet [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) du gestionnaire de protocole, le rassembleur identifie le filtre correct pour l’URL. Le rassembleur analyse l’extension de nom de fichier de l’élément et recherche le filtre inscrit pour cette extension. si le rassembleur ne parvient pas à trouver un filtre, Windows recherche utilise les métadonnées pour dériver un ensemble minimal d’informations sur les propriétés système (telles que system. ItemName) et met à jour l’index. Dans le cas contraire, si le rassembleur trouve le filtre, la troisième étape de l’indexation commence.

## <a name="stage-3-updating-the-index"></a>Étape 3 : mise à jour de l’index

Au cours de la troisième étape de l’indexation, le rassembleur instancie le filtre correct pour l’URL et initialise le filtre avec le flux de l’objet [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) . Le filtre accède ensuite à l’élément et retourne le contenu de l’index. si vous disposez d’un format de fichier personnalisé, Windows recherche s’appuie sur votre filtre pour accéder aux url et émettre du contenu et des propriétés pour l’indexation.

Le diagramme suivant présente une vue d’ensemble du processus d’accès aux données. Cette étape comprend une coordination et une communication considérables entre les composants.

![Diagramme montrant les données d’élément émises pour l’index](images/filteringdata.jpg)

le reste de cette section décrit comment Windows recherche accède aux données d’élément pour l’indexation et explique les rôles de chacun des composants impliqués.

**Rassembleur**  Au début de cette étape, le rôle du Rassembleur est d’instancier le filtre correct pour l’élément et de lui passer le flux de l’élément. À la fin de cette étape, le rassembleur prend le contenu et les propriétés émis par le gestionnaire de propriétés et le filtre et met à jour l’index.

**Hôte de filtre**  L’hôte de filtre est simplement un processus hôte pour les filtres et les gestionnaires de propriétés et sert d’objectif similaire à l’hôte de protocole de recherche. Le processus hôte isole les filtres et les gestionnaires de propriétés du reste du système pour les mêmes raisons de sécurité et de stabilité que celles que les processus hôtes de protocole de recherche isolent les gestionnaires de protocole. Le processus hôte s’exécute avec des droits minimaux (il ne peut même pas accéder au système de fichiers) et il est parfois recyclé pour vous protéger contre les attaques de sécurité. Windows La recherche surveille également l’utilisation des ressources, de sorte que si un filtre consomme un trop grand nombre de ressources, le processus hôte est recyclé.

**Filtres**  Les filtres sont des composants essentiels du processus d’indexation qui émettent des informations sur les éléments du Rassembleur. Les filtres sont nommés d’après l’interface principale utilisée dans leur implémentation, l’interface [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) et, par conséquent, sont parfois appelés IFilters. Il existe deux types de filtres : un qui interagit avec des éléments individuels tels que des fichiers et un autre qui interagit avec des conteneurs tels que des dossiers. Les deux fournissent des données pour l’index.

À l’aide des métadonnées retournées par l’objet [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) du gestionnaire de protocole, le rassembleur identifie le filtre correct pour une URL particulière et le transmet au flux. Le rassembleur identifie le filtre correct à l’aide d’un gestionnaire de protocole ou de l’extension de nom de fichier, du type MIME ou de l’identificateur de classe (CLSID). Si l’URL pointe vers un conteneur, le filtre émet des propriétés pour le conteneur et énumère les éléments dans le conteneur (URL enfants). Si l’URL pointe vers un élément, le filtre retourne le contenu textuel, si la lecture des propriétés est plus complexe que les gestionnaires de propriétés. En général, nous recommandons que les filtres émettent le contenu des éléments alors que les gestionnaires de propriétés émettent des propriétés d’élément. Toutefois, si votre filtre doit fonctionner avec des applications plus anciennes qui ne reconnaissent pas les gestionnaires de propriétés, vous pouvez également implémenter le filtre pour émettre des propriétés.

> [!NOTE]  
> les filtres ne sont pas Windows des composants de recherche ; Il s’agit de composants liés au format de fichier spécifique ou au conteneur auquel ils sont destinés à accéder. pour plus d’informations sur les filtres et sur la façon d’en implémenter un pour un format de fichier ou un conteneur personnalisé, consultez [meilleures pratiques pour la création de gestionnaires de filtres dans Windows Search](-search-3x-wds-extidx-filters.md).

Le tableau suivant répertorie les résultats que le rassembleur reçoit d’un filtre ([**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)) et d’un gestionnaire de propriétés ([**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)) pendant le processus d’indexation.

|                            | [**Filtres**](/windows/win32/api/filter/nn-filter-ifilter) | [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) |
|----------------------------|------------------------------------|-------------------------------------------------|
| **Autoriser l’écriture**                | Non                                 | Oui                                             |
| **Mélanger le contenu et les propriétés** | Oui                                | Non                                              |
| **Multilingue**               | Oui                                | Non                                              |
| **Émettre des liens**                 | Oui                                | Non                                              |
| **MIME**                       | Oui                                | Non                                              |
| **Limites du texte**            | Phrase, paragraphe, chapitre       | Aucun                                            |
| **Client/serveur**            | Les deux                               | Client                                          |
| **Implémentation**             | Complex                            | Simple                                          |

**Gestionnaires de propriétés**  Les gestionnaires de propriétés sont des composants qui lisent et écrivent des propriétés pour un format de fichier particulier. Ils accèdent aux éléments et émettent des propriétés pour le rassembleur de la même façon que les filtres pour le contenu. Les gestionnaires de propriétés sont plus faciles à implémenter que les filtres. Si un format de fichier texte est très simple ou si les fichiers sont censés être très petits, le gestionnaire de propriétés peut émettre des propriétés et du contenu.

> [!NOTE]  
> les gestionnaires de propriétés ne sont pas Windows des composants de recherche ; Il s’agit de composants liés au format de fichier spécifique auquel ils sont destinés à accéder. pour plus d’informations sur les gestionnaires de propriétés et sur la façon d’en implémenter un pour un format de fichier personnalisé, consultez [développement de gestionnaires de propriétés pour la recherche de Windows](-search-3x-wds-extidx-propertyhandlers.md).

**propriétés** Windows la recherche fournit un [système](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) de propriétés qui inclut une grande bibliothèque de propriétés. Une propriété peut apparaître sur n’importe quel élément tel que défini par le gestionnaire de filtres ou de propriétés. Si vous disposez d’un format de fichier personnalisé, vous pouvez mapper les propriétés de votre format de fichier à ces propriétés système, et vous pouvez créer des propriétés personnalisées. Lorsque votre gestionnaire de filtres ou de propriétés émet ces propriétés, le rassembleur met à jour l’index afin que les utilisateurs puissent effectuer une recherche à l’aide de vos propriétés. Pour plus d’informations sur la création et l’inscription de propriétés personnalisées pour un format de fichier, consultez [système de propriétés](../properties/building-property-handlers.md).

**SystemIndex**  L’index, appelé SystemIndex, stocke les données indexées et se compose d’un magasin de propriétés et d’index sur les propriétés et le contenu des propriétés d’élément, ainsi qu’un index inversé pour le contenu textuel et les propriétés. une fois que le rassembleur a mis à jour l’index, l’index peut être interrogé par Windows recherche et d’autres applications. Pour plus d’informations sur les méthodes d’interrogation de l’index, consultez [interrogation de l’index par programmation](-search-3x-wds-qryidx-overview.md).

> [!NOTE]  
> N’oubliez pas que lorsque vous réinscrivez un schéma, les modifications apportées aux attributs des propriétés précédemment définies peuvent ne pas être respectées par l’indexeur. La solution consiste soit à reconstruire l’index, soit à introduire de nouvelles propriétés reflétant les modifications au lieu de mettre à jour les anciennes. Pour plus d’informations, consultez la section [Remarque sur les implémenteurs](#notes-to-implementers) dans la [vue d’ensemble du système de propriétés](../properties/property-system-overview.md).

## <a name="how-indexing-is-scheduled"></a>Planification de l’indexation

lorsque Windows recherche est installée pour la première fois, il effectue une indexation complète de l’étendue de l’analyse, en s’interrompant pendant les périodes d’e/s élevées et d’activité utilisateur. l’étendue de l’analyse par défaut se compose des emplacements de bibliothèque par défaut, tels que les **Documents**, les **Musique**, les **images** et les **vidéos**. Les notifications sont traitées avant la fin de l’analyse initiale. Parfois, le rassembleur analyse les URL à partir de l’étendue de l’analyse complète. Ces analyses complètes garantissent que les données de l’index sont actualisées. par exemple, si un fournisseur de notification ne parvient pas à envoyer des notifications ou si le service de recherche de Windows se termine de manière inattendue, le rassembleur n’aurait aucune connaissance des éléments nouveaux ou modifiés et n’indexerait pas ces éléments. Il existe deux types de sources : notification uniquement et notification activée. Dans les deux sources, le rassembleur analyse initialement l’index. Après l’analyse initiale, les sources de notification uniquement ne réeffectuent jamais une analyse complète à moins qu’il y ait un échec, tel que le [Journal des modifications USN](/windows/desktop/FileIO/change-journals) . Les sources activées pour les notifications effectuent une analyse incrémentielle lorsque l’indexeur est démarré, mais écoutent ensuite les notifications lors de l’exécution. les Outlook NTFS et Microsoft sont uniquement des notifications. La notification est activée pour Internet Explorer et FAT.

## <a name="notes-to-implementers"></a>Notes pour les responsables de l’implémentation

La qualité des données dans l’index et l’efficacité du processus d’indexation dépendent en grande partie de votre implémentation de filtre et de gestionnaire de propriétés. Étant donné que le filtre est appelé chaque fois qu’une URL identifie votre format de fichier, le processus d’indexation peut ralentir considérablement si votre filtre est inefficace. Si votre gestionnaire de propriétés ne mappe pas correctement toutes les propriétés du fichier aux propriétés système ou n’émet pas correctement ces propriétés, les données de l’index sont incorrectes et les recherches ultérieures de ces propriétés renverront des résultats incorrects. Si votre gestionnaire de filtres ou de propriétés échoue, l’indexeur ne peut pas indexer les données.

les Applications et les processus autres que Windows recherche s’appuient sur des gestionnaires de protocole, des filtres et des gestionnaires de propriétés. Vos implémentations peuvent affecter ces applications de façon inattendue. le [Guide de développement Windows Search](-search-developers-guide-entry-page.md) fournit des conseils sur les choix de conception et sur le test de chacun de ces composants.

## <a name="related-topics"></a>Rubriques connexes

[indexation, interrogation et notifications dans Windows Search](-search-3x-wds-included-in-index.md)

[Ce qui est inclus dans l’index](-search-indexing-process-overview.md)

[interrogation du processus dans Windows la recherche](querying-process--windows-search-.md)

[processus de notifications dans Windows Search](-search-3x-wds-support.md)

[Configuration requise pour la mise en forme des URL](url-formatting-requirements.md)
