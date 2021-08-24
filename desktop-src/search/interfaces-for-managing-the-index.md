---
description: découvrez comment Windows search vous permet de gérer l’index de recherche Windows avec le gestionnaire de recherche, le gestionnaire de catalogues et le gestionnaire de portée d’analyse.
ms.assetid: 80f0387c-5c91-41b8-9767-5f5e6563c112
title: Interfaces pour la gestion de l’index
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505752cc496d55057eece87bd673b31a323c6597
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476795"
---
# <a name="interfaces-for-managing-the-index"></a>Interfaces pour la gestion de l’index

Windows la recherche vous permet de gérer le Windows index de recherche avec trois composants principaux : le gestionnaire de recherche, le gestionnaire de catalogues et le gestionnaire de l’étendue de l’analyse. Certaines de ces interfaces de gestion peuvent être utilisées avec des privilèges d’utilisateur standard, mais celles qui modifient l’état de l’index requièrent des privilèges d’administrateur.

## <a name="about-the-interfaces-for-managing-the-index"></a>À propos des interfaces pour la gestion de l’index


| Composant | Interfaces | Description | 
|-----------|------------|-------------|
| Gestionnaire de recherche | <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager">ISearchManager</a> | fournit des méthodes pour récupérer et définir des informations sur la recherche Windows :<ul><li>Obtention d’une instance du gestionnaire de catalogues pour un catalogue spécifique.</li><li>Obtention ou définition d’informations de proxy.</li><li>obtention d’informations de version sur le moteur de recherche Windows.</li></ul>Pour plus d’informations, consultez <a href="-search-3x-wds-mngidx-searchmanager.md">utilisation du gestionnaire de recherche</a>.<br /> | 
| Gestionnaire de catalogues | <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager">ISearchCatalogManager</a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager2">ISearchCatalogManager2</a><br /> | Fournit des méthodes pour gérer un catalogue de recherche individuel, par exemple pour provoquer une réindexation ou définir des délais d’attente. Cette interface gère le catalogue dans quatre domaines :<ul><li>Contenu du catalogue : s’assurer que les nouvelles données sont indexées et que d’autres applications et composants fonctionnent correctement en forçant la réindexation de tout ou partie du catalogue ou en réinitialisant l’intégralité du catalogue.</li><li>Propriétés du catalogue-définition des propriétés qui déterminent comment le catalogue gère les délais d’attente lors de la connexion aux gestionnaires de protocole et comment les marques diacritiques sont traitées dans les recherches.</li><li>État du catalogue : obtention d’informations sur le catalogue, y compris l’État, la taille et l’état de l’activité actuelle.</li><li>Accès à d’autres interfaces : récupération d’autres interfaces relatives à la recherche requises par le gestionnaire de portée d’analyse, les notifications de modification de données et l’interface <a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper"><strong>ISearchQueryHelper</strong></a> .</li></ul>Pour plus d’informations, consultez <a href="-search-3x-wds-mngidx-catalog-manager.md">utilisation du gestionnaire de catalogues</a>.<br /> | 
| Gestionnaire de l’étendue de l’analyse | <a href="/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots"><strong>IEnumSearchRoots</strong></a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-ienumsearchscoperules">IEnumSearchScopeRules</a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager"><strong>ISearchCrawlScopeManager</strong></a><br /><a href="/windows/desktop/api/searchapi/nn-searchapi-isearchcrawlscopemanager2">ISearchCrawlScopeManager2</a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchroot"><strong>ISearchRoot</strong></a><br /><a href="/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule"><strong>ISearchScopeRule</strong></a><br /><a href="/windows/desktop/search/-search-isearchitem">ISearchItem</a><br /> | Fournit des méthodes pour informer le moteur de recherche des conteneurs à analyser ou à surveiller, et les éléments sous ces conteneurs à inclure ou exclure dans l’index. Vous pouvez également interroger le gestionnaire de l’étendue de l’analyse pour voir si une URL particulière se trouve dans l’étendue de l’analyse. Pour plus d’informations, consultez <a href="-search-3x-wds-extidx-csm.md">utilisation du gestionnaire de portée d’analyse</a>.<br /> | 


## <a name="related-topics"></a>Rubriques connexes

[Gestion de l’index](-search-3x-wds-mngidx-overview.md)

[Utilisation du gestionnaire de recherche](-search-3x-wds-mngidx-searchmanager.md)

[Utilisation du gestionnaire de catalogues](-search-3x-wds-mngidx-catalog-manager.md)

[Utilisation du gestionnaire de portée d’analyse](-search-3x-wds-extidx-csm.md)
