---
title: Lecteur Windows Media Magasins en ligne
description: Lecteur Windows Media Magasins en ligne
ms.assetid: 81009d7b-5c2a-4447-a85e-138ab7834b7a
keywords:
- Lecteur Windows Media des magasins en ligne, à propos de
- magasins en ligne, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11cba4cabcaaae5e55a4e93dbbfe9e4c19e73b37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127216948"
---
# <a name="windows-media-player-online-stores"></a>Lecteur Windows Media Magasins en ligne

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

Lecteur Windows Media fournit des fonctionnalités qui permettent aux fournisseurs de contenu multimédia numérique d’intégrer leurs services à Lecteur Windows Media. L’intégration entre le lecteur et un magasin de supports numériques en ligne offre une expérience agréable et complète pour l’utilisateur, notamment la possibilité de rechercher du contenu, de télécharger et de gérer des fichiers, de lire du contenu et de copier du contenu sur des CD ou des appareils.

## <a name="contacting-microsoft"></a>Contacter Microsoft

si vous souhaitez que votre magasin de médias numériques en ligne soit intégré à Lecteur Windows Media, mais que vous n’avez pas encore contacté Microsoft, vous pouvez commencer par envoyer un message électronique à l’équipe virtuelle des Services Lecteur Windows Media. L’adresse de messagerie de l’équipe est mpsvctm@microsoft.com .

## <a name="for-more-information"></a>Pour plus d'informations

pour obtenir des conseils techniques sur l’utilisation d’un large éventail de kits de développement logiciel (sdk) Windows pour créer un service proposant du contenu multimédia numérique sous licence, accédez au [centre de développement multimédia Microsoft Windows](https://msdn.microsoft.com/windowsmedia/default.aspx) et recherchez « création d’un magasin en ligne d’abonnement Lecteur Windows Media 10 ».

## <a name="online-stores-in-windows-media-player-9-series"></a>magasins en ligne dans Lecteur Windows Media série 9

Lecteur Windows Media série 9 a introduit le concept de magasins en ligne. dans Lecteur Windows Media série 9, les fournisseurs de magasins en ligne peuvent intégrer leurs services dans la fonctionnalité **services Premium** de Lecteur Windows Media.

## <a name="online-stores-in-windows-media-player-10"></a>magasins en ligne dans Lecteur Windows Media 10

dans Lecteur Windows Media 10, les services premium ont été renommés magasins en ligne, et les nouvelles fonctionnalités suivantes ont été ajoutées :

-   Lecteur Windows Media fournit jusqu’à trois volets de tâches pour une utilisation par le magasin en ligne.
-   quand un utilisateur choisit, dans l’interface utilisateur du joueur, d’afficher plus d’informations sur le contenu multimédia numérique, Lecteur Windows Media appels sur le magasin en ligne pour fournir les informations.
-   lorsque l’utilisateur choisit, dans l’interface utilisateur du joueur, d’acheter un élément multimédia, Lecteur Windows Media appel sur le magasin en ligne pour gérer l’achat.
-   le magasin en ligne peut fournir un plug-in qui Lecteur Windows Media appelle pour obtenir de l’aide sur la gestion des droits numériques et le minutage du traitement en arrière-plan.
-   les magasins en ligne peuvent être intégrés à la configuration de Lecteur Windows Media.

## <a name="online-stores-in-windows-media-player-11"></a>magasins en ligne dans Lecteur Windows Media 11

Lecteur Windows Media 11 introduit un nouveau type de magasin de musique en ligne, qui est plus profondément intégré à l’interface utilisateur du joueur. dans Lecteur Windows Media 11, les nouvelles fonctionnalités suivantes ont été ajoutées pour prendre en charge ce nouveau type de magasin en ligne.

-   Lecteur Windows Media télécharge le catalogue de médias de la boutique en ligne, de sorte que l’utilisateur peut parcourir rapidement le contenu du magasin en ligne.
-   Lecteur Windows Media affiche le contenu musical de la boutique en ligne dans le contrôle d’affichage de l’arborescence de la bibliothèque.
-   Lorsque l’utilisateur navigue dans l’interface utilisateur du joueur, le lecteur appelle sur le magasin en ligne pour fournir des pages Web qui améliorent l’expérience de l’utilisateur.
-   le magasin en ligne fournit un plug-in qui gère tous les aspects de la communication entre Lecteur Windows Media et le magasin en ligne. Par exemple, le plug-in gère la connexion, le renouvellement de la licence, la mise à niveau du catalogue, le téléchargement du contenu et l’achat du contenu.
-   Lecteur Windows Media fournit une communication améliorée entre le lecteur et les pages web fournis par le magasin en ligne et hébergés dans le lecteur.

## <a name="types-of-online-stores"></a>Types de magasins en ligne

Il existe deux types de magasins en ligne : type 1 et type 2.

un magasin de type 1 fournit le niveau d’intégration le plus avancé avec Lecteur Windows Media. Il fournit un catalogue musical téléchargeable et est profondément intégré à l’interface utilisateur du joueur. les magasins de Type 1 sont pris en charge par Lecteur Windows Media 11 et versions ultérieures.

les magasins de Type 2, qui sont pris en charge par Lecteur Windows Media série 9 et versions ultérieures, disposent de deux sous-catégories : magasins de commerce et magasins musicaux.

Un magasin de commerce offre l’expérience la plus basique en fournissant jusqu’à trois volets Office de service qui affichent les pages Web du magasin.

Un magasin de musique offre une expérience plus intégrée à l’utilisateur qu’un magasin de commerce. dans un magasin de musique, les utilisateurs peuvent cliquer sur des boutons et des liens dans Lecteur Windows Media (en dehors des pages web fournies par le store) pour effectuer des actions telles que l’achat d’un CD ou d’un DVD, obtenir plus d’informations sur un élément multimédia particulier ou afficher le volet d’affichage du centre d’informations. dans chaque cas, Lecteur Windows Media appelle le magasin musical actuel pour gérer ces requêtes.

> [!Note]  
> Certains documents font référence aux magasins de commerce en tant que services commerciaux de base et font référence aux magasins musicaux en tant que services musicaux intégrés.

 

Le tableau suivant présente les fonctionnalités disponibles pour les différents types de magasins en ligne.




| Fonctionnalité | Magasin de commerce de type 2 | Magasin de musique de type 2 | Magasin de type 1 | 
|---------|-----------------------|--------------------|--------------|
| Volets des tâches de création de service<blockquote>[!Note]<br />Lecteur Windows Media 10 contient jusqu’à trois volets de tâches de service. Lecteur Windows Media 11 n’en a qu’un.</blockquote><br /> | Oui | Oui | Oui | 
| Modifiez l’apparence du magasin en modifiant des attributs tels que la couleur du bouton, la couleur de la barre des tâches et le texte du bouton. | Oui | Oui | Oui | 
| ajoutez des images de logo à la Lecteur Windows Media menu et à la barre des tâches du magasin en ligne. | Oui | Oui | Oui | 
| Naviguez de HTMLView vers le magasin en ligne. | Oui | Oui | Oui | 
| gérer Lecteur Windows Media les demandes d’achat d’un CD ou d’un DVD. | Non | Oui | Oui | 
| gérer les demandes de Lecteur Windows Media pour fournir des informations détaillées sur les albums. | Non | Oui | Oui | 
| Indiquez la page Web d’affichage du centre d’informations. | Non | Oui | Oui | 
| personnalisez Lecteur Windows Media programme d’installation pour spécifier un magasin en ligne initial. | Non | Oui | Oui | 
| Fournissez un plug-in qui implémente <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice"><strong>IWMPSubscriptionService</strong></a>.<blockquote>[!Note]<br />dans Lecteur Windows Media 10 et versions ultérieures, ce plug-in peut également implémenter <a href="/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2"><strong>IWMPSubscriptionService2</strong></a>.</blockquote><br /> | Non | Oui | Non | 
| fournir un catalogue musical téléchargé par Lecteur Windows Media | Non | Non | Oui | 
| Fournissez des pages Web personnalisées et des menus contextuels basés sur la navigation de l’utilisateur dans l’interface utilisateur du joueur. | Non | Non | Oui | 
| Fournissez un plug-in qui implémente <a href="/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner"><strong>IWMPContentPartner</strong></a>. | Non | Non | Oui | 




 

Le reste de la documentation sur les magasins en ligne est réparti dans les sections suivantes.



| Section                                                                                                                              | Description                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [Kit de bienvenue des magasins en ligne](online-stores-welcome-kit.md)                                                                           | contient des informations sur la façon de mettre un magasin de médias numériques en ligne dans Lecteur Windows Media.             |
| [Tapez 1 magasins en ligne](type-1-online-stores.md)                                                                                     | Contient des sections about, guide et Reference pour les magasins de type 1 en ligne.                                             |
| [Tapez 2 magasins en ligne](type-2-online-stores.md)                                                                                     | Contient des sections about, guide et Reference pour les magasins en ligne de type 2.                                             |
| [Informations communes aux magasins en ligne de type 1 et de type 2](information-common-to-type-1-and-type-2-online-stores.md)                   | Contient des informations qui s’appliquent aux magasins en ligne de type 1 et de type 2.                                          |
| [Actualisation des licences des magasins qui ont le logo PlaysForSure](refreshing-licenses-for-stores-that-have-the-playsforsure-logo.md) | contient des informations sur la façon dont les magasins en ligne qui ne sont pas intégrés à Lecteur Windows Media peuvent mettre à jour des licences. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Lecteur Windows Media SDK**](windows-media-player-sdk.md)
</dt> </dl>

 

 





