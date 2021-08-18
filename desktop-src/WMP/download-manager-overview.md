---
title: Présentation du gestionnaire de téléchargement
description: Présentation du gestionnaire de téléchargement
ms.assetid: a13435ac-3784-4d4c-ba49-a51e373a2874
keywords:
- Lecteur Windows Media des magasins en ligne, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Lecteur Windows Media les magasins en ligne, le téléchargement en temps réel
- magasins en ligne, téléchargement en temps réel
- tapez 2 magasins en ligne, téléchargement en temps réel
- Lecteur Windows Media des magasins en ligne, téléchargement en arrière-plan
- magasins en ligne, téléchargement en arrière-plan
- tapez 2 magasins en ligne, téléchargement en arrière-plan
- Lecteur Windows Media, gestionnaire de téléchargement
- Lecteur Windows Media Gestionnaire de téléchargement
- Gestionnaire de téléchargement
- Téléchargement en temps réel
- Téléchargement en arrière-plan
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790466db4c09f7c2310729bd6f866bc5066348641a73756eb9199aa685a7fafe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997079"
---
# <a name="download-manager-overview"></a>Présentation du gestionnaire de téléchargement

Microsoft Lecteur Windows Media fournit des volets des tâches de la boutique en ligne qui contiennent une fenêtre de navigateur hébergée. Grâce aux magasins en ligne, les utilisateurs peuvent interagir avec les pages Web du magasin en ligne sur Internet.

le gestionnaire de téléchargement Lecteur Windows Media fournit un modèle d’objet que vous pouvez utiliser pour gérer les tâches associées au téléchargement de contenu sur l’ordinateur de l’utilisateur à partir d’Microsoft Internet Information Services (IIS) à l’aide du protocole http (Hypertext transfer Protocol). Avec le gestionnaire de téléchargement, vous pouvez :

-   Gérer plusieurs téléchargements simultanément en tant que collection.
-   Spécifiez une URL pour un fichier et démarrez le téléchargement à l’aide de HTTP.
-   Recherchez l’État et la progression du téléchargement.
-   Suspendre, reprendre ou annuler un téléchargement.
-   Spécifiez si un téléchargement est effectué en arrière-plan ou en temps réel. (le téléchargement en arrière-plan est uniquement disponible sur le système d’exploitation Microsoft Windows XP.) Consultez [à propos du téléchargement en temps réel et en arrière-plan](#about-background-and-real-time-downloading).
-   Spécifiez le mode d’affichage du contenu dans la bibliothèque. Consultez [à propos de l’intégration de la bibliothèque](#about-library-integration).

Le gestionnaire de téléchargement est la solution permettant de télécharger du contenu à partir de code de script dans des pages hébergées sur des pages Web. pour télécharger du contenu à l’aide de code C++, utilisez le Service de transfert intelligent en arrière-plan Windows XP (BITS). Pour plus d’informations, consultez [bits](bits.md).

## <a name="about-background-and-real-time-downloading"></a>À propos du téléchargement en temps réel et en arrière-plan

Le gestionnaire de téléchargement offre deux types de téléchargements : arrière-plan et en temps réel. Le type que vous utilisez dépend de vous, et il est possible de permettre à l’utilisateur de sélectionner également le type de téléchargement. Si vous choisissez d’autoriser l’utilisateur à sélectionner le type de téléchargement, veillez à expliquer les différences entre les deux types disponibles.

Le téléchargement en temps réel a lieu en même temps. Lorsque l’utilisateur démarre un téléchargement de fichier, le fichier entier est transféré à l’ordinateur de l’utilisateur dans un seul flux continu. L’utilisateur ne peut pas suspendre ou interrompre le téléchargement. si l’utilisateur choisit de fermer Lecteur Windows Media avant la fin du téléchargement, il perd tous les fichiers incomplets et doit les télécharger depuis le début pour obtenir le contenu.

Le principal avantage du téléchargement en temps réel est qu’il permet à l’utilisateur d’acquérir le contenu plus rapidement que le téléchargement en arrière-plan. le téléchargement en temps réel est disponible pour les utilisateurs de Windows xp, mais il s’agit du seul type de téléchargement disponible sur les versions du système d’exploitation Windows antérieures à Windows XP.

Le téléchargement en arrière-plan s’effectue de manière fragmentaire. Lorsque l’utilisateur démarre un téléchargement en arrière-plan, certaines parties du fichier sont transférées sur l’ordinateur de l’utilisateur lorsque le temps processeur est disponible. Il est possible de suspendre et de reprendre un téléchargement en arrière-plan. si l’utilisateur choisit de fermer Lecteur Windows Media avant la fin du téléchargement en arrière-plan, la condition de tous les fichiers incomplets est enregistrée et le téléchargement peut continuer en arrière-plan, même après le redémarrage de l’ordinateur.

Le téléchargement en arrière-plan peut prendre plus de temps que le téléchargement en temps réel, car le processus de téléchargement ne se produit que lorsque le processeur n’effectue pas d’autres tâches.

le téléchargement en arrière-plan est disponible uniquement lors de l’utilisation de Windows XP.

## <a name="about-library-integration"></a>À propos de l’intégration de bibliothèque

Lecteur Windows Media pouvez organiser automatiquement le contenu du magasin en ligne dans la bibliothèque. Pour ce faire, vous devez spécifier une valeur pour l’attribut **WM/ContentDistributor** pour chaque fichier multimédia numérique. lorsqu’un fichier multimédia numérique est ajouté à la bibliothèque, ce qui se produit automatiquement lors de l’utilisation du gestionnaire de téléchargement, le fichier est affiché automatiquement dans le nœud **Musique acheté** ou **vidéos achetées** . Par exemple, si la valeur de **WM/ContentDistributor** est « Proseware » et que le fichier multimédia numérique contient musique, le contenu apparaît dans la bibliothèque à l’emplacement suivant :

toutes les Musique/Purchased Musique/Proseware

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Gestionnaire de téléchargement**](download-manager.md)
</dt> <dt>

[**DownloadCollection.startDownload**](downloadcollection-startdownload.md)
</dt> </dl>

 

 




