---
title: À propos des magasins en ligne de type 1
description: À propos des magasins en ligne de type 1
ms.assetid: 754b0097-5d28-4c1f-9847-a19cf23beaea
keywords:
- Windows Media Player Online stores, tapez 1 magasins en ligne
- magasins en ligne, type 1 magasins en ligne
- tapez 1 magasins en ligne, à propos de
- Windows Media Player, type 1 magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ecd939a03734fed121dcaa22c0d7ae89127476
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106512299"
---
# <a name="about-type-1-online-stores"></a>À propos des magasins en ligne de type 1

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

Le lecteur Microsoft Windows Media 11 prend en charge deux types de magasins en ligne : type 1 et type 2. Les magasins de type 1 sont plus profondément intégrés au lecteur Windows Media que les magasins de type 2. Un magasin en ligne de type 1 fournit un catalogue musical téléchargeable afin que le lecteur Windows Media puisse mettre le contenu du magasin à la disposition de l’utilisateur comme si le contenu se trouvait dans la bibliothèque multimédia locale de l’utilisateur.

Un magasin en ligne de type 1 doit fournir un plug-in qui implémente l’interface [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) . Lorsque l’utilisateur navigue dans l’interface utilisateur du lecteur Windows Media, le lecteur appelle le plug-in afin que le magasin en ligne puisse améliorer l’expérience de l’utilisateur en fournissant des pages Web qui s’affichent dans le lecteur.

Les fonctionnalités des magasins en ligne de type 1 qui les distinguent des magasins de type 2 sont les suivantes :

-   **Facilité d’utilisation.** Les utilisateurs peuvent rechercher de la musique dans le catalogue du magasin en ligne à l’aide de la même interface utilisateur du lecteur Windows Media que celle qui est utilisée actuellement pour gérer leur bibliothèque personnelle. Les utilisateurs ne peuvent afficher qu’un seul catalogue de magasins en ligne dans la fonctionnalité parcourir à un moment donné.
-   **Pure.** Les utilisateurs peuvent échantillonner ou acheter de la musique sans passer de la fonctionnalité parcourir à une autre partie de l’interface utilisateur du lecteur Windows Media.
-   **Fonctionnalités enrichies.** Étant donné que le catalogue du magasin en ligne est stocké de manière similaire à la bibliothèque de l’utilisateur, de nombreuses fonctionnalités de la bibliothèque du lecteur Windows Media peuvent être appliquées au catalogue. Par exemple, les utilisateurs peuvent utiliser le mot Wheel de la fonctionnalité parcourir pour filtrer le catalogue du magasin en ligne.

Pour un fournisseur de magasin en ligne, les avantages de la fourniture d’un magasin de type 1 au lieu d’un magasin de type 2 sont les suivants :

-   Nœud personnalisé très visible dans l’arborescence de la bibliothèque du lecteur Windows Media.
-   Système conçu pour les achats musicaux.
-   Connexions améliorées aux processus du lecteur.
-   Gestionnaire de téléchargement plus facile à utiliser.
-   Possibilité de naviguer entre les différentes fonctionnalités du lecteur (y compris l’ouverture d’un nœud d’arborescence de bibliothèque spécifique).
-   Notifications relatives à l’expiration de la licence pour le contenu de l’abonnement.
-   Notifications pour l’utilisation de lecteurs musicaux portables connectés.

Les sections suivantes fournissent des informations générales sur les magasins de type 1 en ligne.



| Section                                                                                              | Description                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Catalogue musical](music-catalog.md)                                                                   | Décrit le catalogue musical fourni par le magasin en ligne. Décrit le compilateur de catalogue fourni par Microsoft.                                                                     |
| [Conteneurs de contenu](content-containers.md)                                                         | Décrit l’interface de conteneur de contenu ([IWMPContentContainer](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)), qui est utilisée pour représenter une collection d’éléments multimédias à acheter ou à télécharger. |
| [Intégration de la bibliothèque](library-integration.md)                                                       | Décrit comment le catalogue de musique de la boutique en ligne est intégré à la vue Bibliothèque du lecteur.                                                                                        |
| [Pages de découverte](discovery-pages.md)                                                               | Décrit l’interaction entre le lecteur Windows Media et les pages Web fournies par le magasin en ligne.                                                                                   |
| [Menus contextuels](context-menus.md)                                                                   | Décrit comment le magasin en ligne peut fournir des menus contextuels au fur et à mesure que l’utilisateur navigue dans l’interface utilisateur du joueur.                                                                         |
| [Flux audio](audio-streams.md)                                                                   | Décrit comment le magasin en ligne fournit le lecteur Windows Media avec l’URL de diffusion en continu de contenu audio.                                                                              |
| [Document ServiceInfo pour une boutique en ligne de type 1](serviceinfo-document-for-a-type-1-online-store.md) | Décrit le document XML ServiceInfo fourni par un magasin en ligne de type 1.                                                                                                           |
| [Type 1 plug-in de magasin en ligne](type-1-online-store-plug-in.md)                                       | Décrit le plug-in qu’un magasin en ligne de type 1 doit fournir.                                                                                                                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Tapez 1 magasins en ligne**](type-1-online-stores.md)
</dt> </dl>

 

 




