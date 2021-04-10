---
description: Cette rubrique décrit les étapes nécessaires à la connexion d’un service Web entre votre magasin de données et la recherche fédérée de Windows, et explique comment envoyer des requêtes et retourner des résultats de recherche dans RSS ou Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Connexion de votre service Web dans la recherche fédérée Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112462"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a>Connexion de votre service Web dans la recherche fédérée Windows

Cette rubrique décrit les étapes nécessaires à la connexion d’un service Web entre votre magasin de données et la recherche fédérée de Windows, et explique comment envoyer des requêtes et retourner des résultats de recherche dans RSS ou Atom.

Cette rubrique est organisée comme suit :

-   [Connexion de votre service Web](#connect-your-web-service)
-   [Inscrire une banque de données distante existante](#register-an-existing-remote-data-store)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="connect-your-web-service"></a>Connexion de votre service Web

**Pour connecter le service Web de votre magasin de données à la recherche fédérée, procédez comme suit :**

1.  Créez un fichier. fichier osdx.
2.  Fournissez le fichier. fichier osdx aux utilisateurs afin qu’ils puissent ajouter le service à la demande en ouvrant le fichier. fichier osdx.
3.  Générez un connecteur de recherche et déployez-le activement dans votre entreprise.

## <a name="register-an-existing-remote-data-store"></a>Inscrire une banque de données distante existante

Un utilisateur inscrit un nouveau magasin de données distant auprès de Windows Federated Search en ouvrant un fichier de description OpenSearch (. fichier osdx). Lorsque l’utilisateur le fait, les événements suivants se produisent :

1.  Un fichier. searchconnector-ms (connecteur de recherche) est créé dans le dossier recherches Windows (% UserProfile%/Searches).
2.  Un raccourci vers le fichier. searchconnector-MS est créé dans le dossier des liens (% UserProfile%/Links).
3.  Un raccourci s’affiche dans le volet **favoris** de navigation de l’Explorateur Windows, ce qui permet à l’utilisateur de naviguer dans le nouveau magasin de données et d’interroger le service Web.

> [!Note]  
> Un magasin de données qui dispose déjà d’un service Web [OpenSearch](https://github.com/dewitt/opensearch) qui est compatible avec Windows Federated Search peut être ajouté à l’Explorateur Windows lorsqu’un utilisateur ouvre un fichier. fichier osdx.

 

## <a name="additional-resources"></a>Ressources supplémentaires

Pour plus d’informations sur l’implémentation de la Fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

[Prise en main avec la recherche fédérée dans Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Activation de votre magasin de données dans la recherche fédérée Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md)
</dt> <dt>

[Meilleures pratiques suivantes dans Windows Federated Search](-search-fedsearch-best.md)
</dt> <dt>

[Déploiement de connecteurs de recherche dans la recherche fédérée Windows](-search-federated-search-deploying.md)
</dt> </dl>

 

 
