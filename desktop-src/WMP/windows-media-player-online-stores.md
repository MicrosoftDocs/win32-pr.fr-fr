---
title: Windows Media Player Online stores
description: Windows Media Player Online stores
ms.assetid: 81009d7b-5c2a-4447-a85e-138ab7834b7a
keywords:
- Magasins en ligne du lecteur Windows Media, à propos de
- magasins en ligne, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55046508b1e3a4d0a3a254fd294e5f271a2802f5
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724074"
---
# <a name="windows-media-player-online-stores"></a>Windows Media Player Online stores

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

Le lecteur Windows Media fournit des fonctionnalités qui permettent aux fournisseurs de contenus multimédias numériques d’intégrer leurs services au lecteur Windows Media. L’intégration entre le lecteur et un magasin de supports numériques en ligne offre une expérience agréable et complète pour l’utilisateur, notamment la possibilité de rechercher du contenu, de télécharger et de gérer des fichiers, de lire du contenu et de copier du contenu sur des CD ou des appareils.

## <a name="contacting-microsoft"></a>Contacter Microsoft

Si vous souhaitez que votre magasin de médias numériques en ligne soit intégré au lecteur Windows Media, mais que vous n’avez pas encore contacté Microsoft, vous pouvez commencer par envoyer un message électronique à l’équipe virtuelle des services de lecteur Windows Media. L’adresse de messagerie de l’équipe est mpsvctm@microsoft.com .

## <a name="for-more-information"></a>Pour plus d'informations

Pour obtenir des conseils techniques sur l’utilisation de divers kits de développement logiciel (SDK) Windows Media pour créer un service proposant du contenu multimédia numérique sous licence, accédez au [Centre de développement Microsoft Windows Media](https://msdn.microsoft.com/windowsmedia/default.aspx) et recherchez « création d’un magasin en ligne d’abonnement Windows Media Player 10 ».

## <a name="online-stores-in-windows-media-player-9-series"></a>Magasins en ligne dans le lecteur Windows Media série 9

Le lecteur Windows Media série 9 a introduit le concept de magasins en ligne. Dans le lecteur Windows Media série 9, les fournisseurs de magasins en ligne peuvent intégrer leurs services dans la fonctionnalité **Services Premium** du lecteur Windows Media.

## <a name="online-stores-in-windows-media-player-10"></a>Magasins en ligne dans le lecteur Windows Media 10

Dans le lecteur Windows Media 10, les services Premium ont été renommés magasins en ligne, et les nouvelles fonctionnalités suivantes ont été ajoutées :

-   Le lecteur Windows Media fournit jusqu’à trois volets de tâches pour une utilisation par le magasin en ligne.
-   Quand un utilisateur choisit, dans l’interface utilisateur du joueur, d’afficher plus d’informations sur le contenu multimédia numérique, les appels du lecteur Windows Media sur le magasin en ligne pour fournir les informations.
-   Lorsque l’utilisateur choisit, dans l’interface utilisateur du joueur, d’acheter un élément multimédia, le lecteur Windows Media appelle sur le magasin en ligne pour gérer l’achat.
-   Le magasin en ligne peut fournir un plug-in que le lecteur Windows Media appelle pour obtenir de l’aide sur la gestion des droits numériques et le minutage du traitement en arrière-plan.
-   Les magasins en ligne peuvent être intégrés à la configuration du lecteur Windows Media.

## <a name="online-stores-in-windows-media-player-11"></a>Magasins en ligne dans le lecteur Windows Media 11

Le lecteur Windows Media 11 introduit un nouveau type de magasin de musique en ligne, qui est plus profondément intégré à l’interface utilisateur du joueur. Dans le lecteur Windows Media 11, les nouvelles fonctionnalités suivantes ont été ajoutées pour prendre en charge ce nouveau type de magasin en ligne.

-   Le lecteur Windows Media télécharge le catalogue de médias de la boutique en ligne, ce qui permet à l’utilisateur de parcourir rapidement le contenu du magasin en ligne.
-   Le lecteur Windows Media affiche le contenu musical de la boutique en ligne dans le contrôle d’affichage de l’arborescence de la bibliothèque.
-   Lorsque l’utilisateur navigue dans l’interface utilisateur du joueur, le lecteur appelle sur le magasin en ligne pour fournir des pages Web qui améliorent l’expérience de l’utilisateur.
-   Le magasin en ligne fournit un plug-in qui gère tous les aspects de la communication entre le lecteur Windows Media et le magasin en ligne. Par exemple, le plug-in gère la connexion, le renouvellement de la licence, la mise à niveau du catalogue, le téléchargement du contenu et l’achat du contenu.
-   Le lecteur Windows Media offre une meilleure communication entre le lecteur et les pages Web fournis par le magasin en ligne et hébergés dans le lecteur.

## <a name="types-of-online-stores"></a>Types de magasins en ligne

Il existe deux types de magasins en ligne : type 1 et type 2.

Un magasin de type 1 offre le niveau d’intégration le plus avancé avec le lecteur Windows Media. Il fournit un catalogue musical téléchargeable et est profondément intégré à l’interface utilisateur du joueur. Les magasins de type 1 sont pris en charge par le lecteur Windows Media 11 et les versions ultérieures.

Les magasins de type 2, qui sont pris en charge par le lecteur Windows Media 9 et versions ultérieures, disposent de deux sous-catégories : magasins de commerce et magasins musicaux.

Un magasin de commerce offre l’expérience la plus basique en fournissant jusqu’à trois volets Office de service qui affichent les pages Web du magasin.

Un magasin de musique offre une expérience plus intégrée à l’utilisateur qu’un magasin de commerce. Dans un magasin de musique, les utilisateurs peuvent cliquer sur des boutons et des liens dans le lecteur Windows Media (en dehors des pages Web fournies par le Store) pour effectuer des actions telles que l’achat d’un CD ou d’un DVD, obtenir plus d’informations sur un élément multimédia particulier ou afficher le volet d’informations du centre d’informations. Dans chaque cas, le lecteur Windows Media appelle le magasin musical actuel pour gérer ces requêtes.

> [!Note]  
> Certains documents font référence aux magasins de commerce en tant que services commerciaux de base et font référence aux magasins musicaux en tant que services musicaux intégrés.

 

Le tableau suivant présente les fonctionnalités disponibles pour les différents types de magasins en ligne.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Fonctionnalité</th>
<th>Magasin de commerce de type 2</th>
<th>Magasin de musique de type 2</th>
<th>Magasin de type 1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Volets des tâches de création de service
<blockquote>
[!Note]<br />
Le lecteur Windows Media 10 contient jusqu’à trois volets de tâches de service. Le lecteur Windows Media 11 n’en a qu’un.
</blockquote>
<br/></td>
<td>Oui</td>
<td>Oui</td>
<td>Oui</td>
</tr>
<tr class="even">
<td>Modifiez l’apparence du magasin en modifiant des attributs tels que la couleur du bouton, la couleur de la barre des tâches et le texte du bouton.</td>
<td>Oui</td>
<td>Oui</td>
<td>Oui</td>
</tr>
<tr class="odd">
<td>Ajoutez des images de logo au menu et à la barre des tâches Windows Media Player Online Store.</td>
<td>Oui</td>
<td>Oui</td>
<td>Oui</td>
</tr>
<tr class="even">
<td>Naviguez de HTMLView vers le magasin en ligne.</td>
<td>Oui</td>
<td>Oui</td>
<td>Oui</td>
</tr>
<tr class="odd">
<td>Gérez les demandes du lecteur Windows Media pour acheter un CD ou un DVD.</td>
<td>Non</td>
<td>Oui</td>
<td>Oui</td>
</tr>
<tr class="even">
<td>Gérez les demandes du lecteur Windows Media pour fournir des informations d’album enrichies.</td>
<td>Non</td>
<td>Oui</td>
<td>Oui</td>
</tr>
<tr class="odd">
<td>Indiquez la page Web d’affichage du centre d’informations.</td>
<td>Non</td>
<td>Oui</td>
<td>Oui</td>
</tr>
<tr class="even">
<td>Personnalisez le programme d’installation du lecteur Windows Media pour spécifier un magasin en ligne initial.</td>
<td>Non</td>
<td>Oui</td>
<td>Oui</td>
</tr>
<tr class="odd">
<td>Fournissez un plug-in qui implémente <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice"><strong>IWMPSubscriptionService</strong></a>.
<blockquote>
[!Note]<br />
Dans le lecteur Windows Media 10 et versions ultérieures, ce plug-in peut également implémenter <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2"><strong>IWMPSubscriptionService2</strong></a>.
</blockquote>
<br/></td>
<td>Non</td>
<td>Oui</td>
<td>Non</td>
</tr>
<tr class="even">
<td>Fournir un catalogue musical téléchargé par le lecteur Windows Media</td>
<td>Non</td>
<td>Non</td>
<td>Oui</td>
</tr>
<tr class="odd">
<td>Fournissez des pages Web personnalisées et des menus contextuels basés sur la navigation de l’utilisateur dans l’interface utilisateur du joueur.</td>
<td>Non</td>
<td>Non</td>
<td>Oui</td>
</tr>
<tr class="even">
<td>Fournissez un plug-in qui implémente <a href="/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner"><strong>IWMPContentPartner</strong></a>.</td>
<td>Non</td>
<td>Non</td>
<td>Oui</td>
</tr>
</tbody>
</table>



 

Le reste de la documentation sur les magasins en ligne est réparti dans les sections suivantes.



| Section                                                                                                                              | Description                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Kit de bienvenue des magasins en ligne](online-stores-welcome-kit.md)                                                                           | Contient des informations sur la façon de mettre un magasin de médias numériques en ligne sur un tableau dans le lecteur Windows Media.             |
| [Tapez 1 magasins en ligne](type-1-online-stores.md)                                                                                     | Contient des sections about, guide et Reference pour les magasins de type 1 en ligne.                                             |
| [Tapez 2 magasins en ligne](type-2-online-stores.md)                                                                                     | Contient des sections about, guide et Reference pour les magasins en ligne de type 2.                                             |
| [Informations communes aux magasins en ligne de type 1 et de type 2](information-common-to-type-1-and-type-2-online-stores.md)                   | Contient des informations qui s’appliquent aux magasins en ligne de type 1 et de type 2.                                          |
| [Actualisation des licences des magasins qui ont le logo PlaysForSure](refreshing-licenses-for-stores-that-have-the-playsforsure-logo.md) | Contient des informations sur la façon dont les magasins en ligne qui ne sont pas intégrés au lecteur Windows Media peuvent mettre à jour des licences. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**SDK du lecteur Windows Media**](windows-media-player-sdk.md)
</dt> </dl>

 

 





