---
description: cette rubrique répertorie les méthodes recommandées par le biais desquelles vous pouvez créer une banque de données basée sur le web qui peut être recherchée à l’aide d’Windows recherche fédérée et qui intègre vos sources de données distantes avec Windows Explorer sans avoir à écrire ou à déployer des Windows du code côté client.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: suivre les meilleures pratiques en matière de Windows la recherche fédérée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e52d2b74f245e4ec76550cbf0a1c56b63db0a8ca6afcf9e8b736f3c7b39a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463089"
---
# <a name="following-best-practices-in-windows-federated-search"></a>suivre les meilleures pratiques en matière de Windows la recherche fédérée

cette rubrique répertorie les méthodes recommandées par le biais desquelles vous pouvez créer une banque de données basée sur le web qui peut être recherchée à l’aide d’Windows recherche fédérée et qui intègre vos sources de données distantes avec Windows Explorer sans avoir à écrire ou à déployer des Windows du code côté client.

Cette rubrique est organisée comme suit :

-   [meilleures pratiques pour la recherche Windows fédérée](#best-practices-for-windows-federated-search)
-   [Meilleures pratiques pour la création d’une sortie RSS](#best-practices-for-creating-rss-output)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a>meilleures pratiques pour la recherche Windows fédérée

les pratiques recommandées pour l’utilisation de [OpenSearch](https://github.com/dewitt/opensearch) dans Windows 7 sont les suivantes :

-   Prenez en charge les paramètres *{startIndex}* et *{Count}* , et veillez à toujours retourner le nombre d’éléments demandés, sauf si vous retournez le dernier des résultats.
-   si vous connaissez l’extension de nom de fichier, mappez-la à la propriété [System. FileExtension](../properties/props-system-fileextension.md) Windows Shell. L’utilisation des extensions de nom de fichier est un meilleur moyen d’identifier un type de fichier que le type MIME.
-   Assurez-vous que le type MIME ou l’extension de nom de fichier que vous spécifiez dans le RSS correspond au nom de fichier et au type MIME renvoyés dans l’en-tête HTTP par le serveur Web qui héberge l’élément lorsque le contenu de l’élément est demandé.
-   Si vous retournez des éléments de fichier, retournez une taille de fichier chaque fois que cela est possible. Cela garantit l’exactitude de la boîte de dialogue de progression du téléchargement.
-   Vérifiez que les demandes d’éléments au-delà de la fin du jeu de résultats ne retournent aucun résultat.
    > [!Note]  
    > Ne pas répéter les résultats.

     

-   Ne placez pas les balises HTML là où elles n’appartiennent pas. Conformément à la spécification RSS, elles sont valides dans le champ Description, mais pas dans le champ titre.
-   Ne créez pas de boîtiers pour des éléments de page Web. par exemple, si vous créez un boîtier et que vous mappez une extension de nom de fichier. aspx, le fichier est téléchargé par Windows Explorer dans le cache Internet et exécuté à partir de là. Les navigateurs Web ne gèrent pas le type de fichier. aspx. L’utilisateur obtient une boîte **de dialogue Ouvrir avec** , ou le fichier peut être ouvert par une application comme Microsoft Visual Studio. Évitez cela en retournant un élément Link uniquement pour les pages Web.
-   Fournissez une URL de restauration Web dans le fichier. fichier osdx à l’aide d’un modèle d’URL avec `format="text\html"` .
-   fournissez une url vers le dossier parent, le conteneur ou la page web en mappant une valeur d’URL d’élément personnalisée à la propriété de Shell [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows.

## <a name="best-practices-for-creating-rss-output"></a>Meilleures pratiques pour la création d’une sortie RSS

Les meilleures pratiques pour la création de la sortie RSS sont les suivantes :

-   Chaque élément doit retourner une URL `link` ou une `enclosure` valeur (ou un équivalent, tel que `media:content` )
-   n’incluez pas de balises de mise en forme HTML dans l’attribut **titre** , ou ces balises apparaîtront dans le titre et seront affichées dans l’explorateur de Windows.
-   Pour l’élément **Description** :
    -   Affichez suffisamment d’informations afin que l’utilisateur sache pourquoi ce résultat peut être pertinent.
    -   N’incluez pas de mise en forme HTML. le fournisseur [OpenSearch](https://github.com/dewitt/opensearch) supprime la mise en forme, ce qui peut donner des résultats moins que souhaitables pour votre description.
    -   n’incluez pas de métadonnées déjà fournies dans d’autres éléments, telles que le nom de fichier du boîtier, la taille, la date de modification, etc., car Windows Explorer affiche déjà les métadonnées. Son affichage dans l’élément **Description** est redondant.
-   Pour les URL de boîtier ou de contenu :
    -   Spécifiez l’attribut type comme type MIME valide.
    -   Spécifiez la taille du fichier en octets.
-   si vous implémentez une sortie RSS dans .net à l’aide de `DateTime` , testez votre flux dans Microsoft Internet Explorer pour voir s’il est valide avant de le déployer dans Windows Explorer.

## <a name="additional-resources"></a>Ressources supplémentaires

pour plus d’informations sur l’implémentation de la fédération de recherche dans des magasins de données distants à l’aide des technologies OpenSearch dans Windows 7 et versions ultérieures, consultez « ressources supplémentaires » dans la rubrique [recherche fédérée dans Windows](/previous-versions//dd742958(v=vs.85)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

[Prise en main avec la recherche fédérée dans Windows](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[connexion de votre Service Web dans Windows recherche fédérée](-search-federated-search-web-service.md)
</dt> <dt>

[activation de votre magasin de données dans Windows recherche fédérée](-search-federated-search-data-store.md)
</dt> <dt>

[création d’un fichier de Description OpenSearch dans Windows recherche fédérée](-search-federated-search-osdx-file.md)
</dt> <dt>

[déploiement de connecteurs de recherche dans Windows recherche fédérée](-search-federated-search-deploying.md)
</dt> <dt>

[Extension de l’index](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
