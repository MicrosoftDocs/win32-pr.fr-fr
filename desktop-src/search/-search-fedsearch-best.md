---
description: Cette rubrique répertorie les meilleures pratiques par le biais desquelles vous pouvez créer une banque de données basée sur le Web qui peut être recherchée à l’aide de Windows Federated Search et qui intègre vos sources de données distantes avec l’Explorateur Windows sans avoir à écrire ou à déployer du code côté client Windows.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Meilleures pratiques suivantes dans Windows Federated Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112459"
---
# <a name="following-best-practices-in-windows-federated-search"></a>Meilleures pratiques suivantes dans Windows Federated Search

Cette rubrique répertorie les meilleures pratiques par le biais desquelles vous pouvez créer une banque de données basée sur le Web qui peut être recherchée à l’aide de Windows Federated Search et qui intègre vos sources de données distantes avec l’Explorateur Windows sans avoir à écrire ou à déployer du code côté client Windows.

Cette rubrique est organisée comme suit :

-   [Meilleures pratiques pour Windows Federated Search](#best-practices-for-windows-federated-search)
-   [Meilleures pratiques pour la création d’une sortie RSS](#best-practices-for-creating-rss-output)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a>Meilleures pratiques pour Windows Federated Search

Les pratiques recommandées pour l’utilisation de [OpenSearch](https://github.com/dewitt/opensearch) dans Windows 7 sont les suivantes :

-   Prenez en charge les paramètres *{startIndex}* et *{Count}* , et veillez à toujours retourner le nombre d’éléments demandés, sauf si vous retournez le dernier des résultats.
-   Si vous connaissez l’extension de nom de fichier, mappez-la à la propriété de l’interpréteur de commandes Windows [System. FileExtension](../properties/props-system-fileextension.md) . L’utilisation des extensions de nom de fichier est un meilleur moyen d’identifier un type de fichier que le type MIME.
-   Assurez-vous que le type MIME ou l’extension de nom de fichier que vous spécifiez dans le RSS correspond au nom de fichier et au type MIME renvoyés dans l’en-tête HTTP par le serveur Web qui héberge l’élément lorsque le contenu de l’élément est demandé.
-   Si vous retournez des éléments de fichier, retournez une taille de fichier chaque fois que cela est possible. Cela garantit l’exactitude de la boîte de dialogue de progression du téléchargement.
-   Vérifiez que les demandes d’éléments au-delà de la fin du jeu de résultats ne retournent aucun résultat.
    > [!Note]  
    > Ne pas répéter les résultats.

     

-   Ne placez pas les balises HTML là où elles n’appartiennent pas. Conformément à la spécification RSS, elles sont valides dans le champ Description, mais pas dans le champ titre.
-   Ne créez pas de boîtiers pour des éléments de page Web. Par exemple, si vous créez un boîtier et que vous mappez une extension de nom de fichier. aspx, le fichier est téléchargé par l’Explorateur Windows dans le cache Internet et exécuté à partir de là. Les navigateurs Web ne gèrent pas le type de fichier. aspx. L’utilisateur obtient une boîte **de dialogue Ouvrir avec** , ou le fichier peut être ouvert par une application comme Microsoft Visual Studio. Évitez cela en retournant un élément Link uniquement pour les pages Web.
-   Fournissez une URL de restauration Web dans le fichier. fichier osdx à l’aide d’un modèle d’URL avec `format="text\html"` .
-   Fournissez une URL vers le dossier parent, le conteneur ou la page Web en mappant une valeur d’URL d’élément personnalisée à la propriété de l’interpréteur de commandes Windows [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) .

## <a name="best-practices-for-creating-rss-output"></a>Meilleures pratiques pour la création d’une sortie RSS

Les meilleures pratiques pour la création de la sortie RSS sont les suivantes :

-   Chaque élément doit retourner une URL `link` ou une `enclosure` valeur (ou un équivalent, tel que `media:content` )
-   N’incluez pas de balises de mise en forme HTML dans l’attribut **title** , ou ces balises apparaîtront dans le titre et seront affichées dans l’Explorateur Windows.
-   Pour l’élément **Description** :
    -   Affichez suffisamment d’informations afin que l’utilisateur sache pourquoi ce résultat peut être pertinent.
    -   N’incluez pas de mise en forme HTML. Le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) supprime la mise en forme, ce qui peut donner des résultats moins que souhaitables pour votre description.
    -   N’incluez pas de métadonnées déjà fournies dans d’autres éléments, telles que le nom de fichier du boîtier, la taille, la date de modification, etc., car l’Explorateur Windows affiche déjà les métadonnées. Son affichage dans l’élément **Description** est redondant.
-   Pour les URL de boîtier ou de contenu :
    -   Spécifiez l’attribut type comme type MIME valide.
    -   Spécifiez la taille du fichier en octets.
-   Si vous implémentez une sortie RSS dans .NET à l’aide de `DateTime` , testez votre flux dans Microsoft Internet Explorer pour voir s’il est valide avant de le déployer dans l’Explorateur Windows.

## <a name="additional-resources"></a>Ressources supplémentaires

Pour plus d’informations sur l’implémentation de la Fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

[Prise en main avec la recherche fédérée dans Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[Connexion de votre service Web dans la recherche fédérée Windows](-search-federated-search-web-service.md)
</dt> <dt>

[Activation de votre magasin de données dans la recherche fédérée Windows](-search-federated-search-data-store.md)
</dt> <dt>

[Création d’un fichier de description OpenSearch dans Windows Federated Search](-search-federated-search-osdx-file.md)
</dt> <dt>

[Déploiement de connecteurs de recherche dans la recherche fédérée Windows](-search-federated-search-deploying.md)
</dt> <dt>

[Extension de l’index](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
