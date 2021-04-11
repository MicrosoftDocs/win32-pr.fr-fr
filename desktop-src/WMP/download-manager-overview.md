---
title: Présentation du gestionnaire de téléchargement
description: Présentation du gestionnaire de téléchargement
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Windows Media Player Online stores, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Windows Media Player Online stores, téléchargement en temps réel
- magasins en ligne, téléchargement en temps réel
- tapez 2 magasins en ligne, téléchargement en temps réel
- Windows Media Player Online stores, téléchargement en arrière-plan
- magasins en ligne, téléchargement en arrière-plan
- tapez 2 magasins en ligne, téléchargement en arrière-plan
- Lecteur Windows Media, gestionnaire de téléchargement
- Gestionnaire de téléchargement du lecteur Windows Media
- Gestionnaire de téléchargement
- Téléchargement en temps réel
- Téléchargement en arrière-plan
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b709df13e239b0fbd7f5c5403998b8c996c228d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029755"
---
# <a name="download-manager-overview"></a>Présentation du gestionnaire de téléchargement

Le lecteur Microsoft Windows Media fournit des volets des tâches de la boutique en ligne qui contiennent une fenêtre de navigateur hébergée. Grâce aux magasins en ligne, les utilisateurs peuvent interagir avec les pages Web du magasin en ligne sur Internet.

Le gestionnaire de téléchargement du lecteur Windows Media fournit un modèle d’objet que vous pouvez utiliser pour gérer les tâches associées au téléchargement de contenu sur l’ordinateur de l’utilisateur à partir de Microsoft Internet Information Services (IIS) à l’aide du protocole HTTP (Hypertext Transfer Protocol). Avec le gestionnaire de téléchargement, vous pouvez :

-   Gérer plusieurs téléchargements simultanément en tant que collection.
-   Spécifiez une URL pour un fichier et démarrez le téléchargement à l’aide de HTTP.
-   Recherchez l’État et la progression du téléchargement.
-   Suspendre, reprendre ou annuler un téléchargement.
-   Spécifiez si un téléchargement est effectué en arrière-plan ou en temps réel. (Le téléchargement en arrière-plan est uniquement disponible sur le système d’exploitation Microsoft Windows XP.) Consultez [à propos du téléchargement en temps réel et en arrière-plan](#about-background-and-real-time-downloading).
-   Spécifiez le mode d’affichage du contenu dans la bibliothèque. Consultez [à propos de l’intégration de la bibliothèque](#about-library-integration).

Le gestionnaire de téléchargement est la solution permettant de télécharger du contenu à partir de code de script dans des pages hébergées sur des pages Web. Pour télécharger du contenu à l’aide de code C++, utilisez le Service de transfert intelligent en arrière-plan Windows XP (BITS). Pour plus d’informations, consultez [bits](bits.md).

## <a name="about-background-and-real-time-downloading"></a>À propos du téléchargement en temps réel et en arrière-plan

Le gestionnaire de téléchargement offre deux types de téléchargements : arrière-plan et en temps réel. Le type que vous utilisez dépend de vous, et il est possible de permettre à l’utilisateur de sélectionner également le type de téléchargement. Si vous choisissez d’autoriser l’utilisateur à sélectionner le type de téléchargement, veillez à expliquer les différences entre les deux types disponibles.

Le téléchargement en temps réel a lieu en même temps. Lorsque l’utilisateur démarre un téléchargement de fichier, le fichier entier est transféré à l’ordinateur de l’utilisateur dans un seul flux continu. L’utilisateur ne peut pas suspendre ou interrompre le téléchargement. Si l’utilisateur choisit de fermer le lecteur Windows Media avant la fin du téléchargement, il perd tous les fichiers incomplets et doit les télécharger depuis le début pour obtenir le contenu.

Le principal avantage du téléchargement en temps réel est qu’il permet à l’utilisateur d’acquérir le contenu plus rapidement que le téléchargement en arrière-plan. Le téléchargement en temps réel est disponible pour les utilisateurs de Windows XP, mais il s’agit du seul type de téléchargement disponible sur les versions du système d’exploitation Windows antérieures à Windows XP.

Le téléchargement en arrière-plan s’effectue de manière fragmentaire. Lorsque l’utilisateur démarre un téléchargement en arrière-plan, certaines parties du fichier sont transférées sur l’ordinateur de l’utilisateur lorsque le temps processeur est disponible. Il est possible de suspendre et de reprendre un téléchargement en arrière-plan. Si l’utilisateur choisit de fermer le lecteur Windows Media avant la fin du téléchargement en arrière-plan, la condition de tous les fichiers incomplets est enregistrée et le téléchargement peut continuer en arrière-plan, même après le redémarrage de l’ordinateur.

Le téléchargement en arrière-plan peut prendre plus de temps que le téléchargement en temps réel, car le processus de téléchargement ne se produit que lorsque le processeur n’effectue pas d’autres tâches.

Le téléchargement en arrière-plan est disponible uniquement lors de l’utilisation de Windows XP.

## <a name="about-library-integration"></a>À propos de l’intégration de bibliothèque

Le lecteur Windows Media peut automatiquement organiser le contenu de la boutique en ligne dans la bibliothèque. Pour ce faire, vous devez spécifier une valeur pour l’attribut **WM/ContentDistributor** pour chaque fichier multimédia numérique. Lorsqu’un fichier multimédia numérique est ajouté à la bibliothèque, ce qui se produit automatiquement lors de l’utilisation du gestionnaire de téléchargement, le fichier est automatiquement listé dans le nœud **musique achetée** ou **vidéos achetées** . Par exemple, si la valeur de **WM/ContentDistributor** est « Proseware » et que le fichier multimédia numérique contient musique, le contenu apparaît dans la bibliothèque à l’emplacement suivant :

Toute la musique/musique achetée/Proseware

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestionnaire de téléchargement**](download-manager.md)
</dt> <dt>

[**DownloadCollection.startDownload**](downloadcollection-startdownload.md)
</dt> </dl>

 

 




