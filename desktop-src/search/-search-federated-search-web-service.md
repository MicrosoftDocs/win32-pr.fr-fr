---
description: cette rubrique décrit les étapes nécessaires à la connexion d’un service web entre votre magasin de données et Windows la recherche fédérée, et comment envoyer des requêtes et retourner des résultats de recherche dans RSS ou Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: connexion de votre Service Web dans Windows recherche fédérée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4980b2d62f766806cf89856b8ef9e5231284be0dfea3258d2e5d5155e7a46598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456719"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a>connexion de votre Service Web dans Windows recherche fédérée

cette rubrique décrit les étapes nécessaires à la connexion d’un service web entre votre magasin de données et Windows la recherche fédérée, et comment envoyer des requêtes et retourner des résultats de recherche dans RSS ou Atom.

Cette rubrique est organisée comme suit :

-   [Connecter Votre service Web](#connect-your-web-service)
-   [Inscrire une banque de données distante existante](#register-an-existing-remote-data-store)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="connect-your-web-service"></a>Connecter Votre service Web

**Pour connecter le service Web de votre magasin de données à la recherche fédérée, procédez comme suit :**

1.  Créez un fichier. fichier osdx.
2.  Fournissez le fichier. fichier osdx aux utilisateurs afin qu’ils puissent ajouter le service à la demande en ouvrant le fichier. fichier osdx.
3.  Générez un connecteur de recherche et déployez-le activement dans votre entreprise.

## <a name="register-an-existing-remote-data-store"></a>Inscrire une banque de données distante existante

un utilisateur inscrit un nouveau magasin de données distant avec Windows recherche fédérée en ouvrant un fichier de Description de OpenSearch (. fichier osdx). Lorsque l’utilisateur le fait, les événements suivants se produisent :

1.  un fichier. searchconnector-ms (connecteur de recherche) est créé dans le dossier recherches Windows (% userprofile%/Searches).
2.  Un raccourci vers le fichier. searchconnector-MS est créé dans le dossier des liens (% UserProfile%/Links).
3.  un raccourci s’affiche dans le volet **favoris** de navigation Windows Explorer, ce qui permet à l’utilisateur de naviguer dans le nouveau magasin de données et d’interroger le service web.

> [!Note]  
> un magasin de données qui dispose déjà d’un service web [OpenSearch](https://github.com/dewitt/opensearch) qui est compatible avec Windows recherche fédérée peut être ajouté à Windows Explorer lorsqu’un utilisateur ouvre un fichier. fichier osdx.

 

## <a name="additional-resources"></a>Ressources supplémentaires

pour plus d’informations sur l’implémentation de la fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

[Prise en main avec la recherche fédérée dans Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[activation de votre magasin de données dans Windows recherche fédérée](-search-federated-search-data-store.md)
</dt> <dt>

[création d’un fichier de Description OpenSearch dans Windows recherche fédérée](-search-federated-search-osdx-file.md)
</dt> <dt>

[suivre les meilleures pratiques en matière de Windows la recherche fédérée](-search-fedsearch-best.md)
</dt> <dt>

[déploiement de connecteurs de recherche dans Windows recherche fédérée](-search-federated-search-deploying.md)
</dt> </dl>

 

 
