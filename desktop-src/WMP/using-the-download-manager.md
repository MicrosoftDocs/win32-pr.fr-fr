---
title: Utilisation du gestionnaire de téléchargement
description: Utilisation du gestionnaire de téléchargement
ms.assetid: f332a981-727f-4abc-a84e-76ab3e72b7f2
keywords:
- Windows Media Player Online stores, gestionnaire de téléchargement
- magasins en ligne, gestionnaire de téléchargement
- tapez 2 magasins en ligne, gestionnaire de téléchargement
- Lecteur Windows Media, gestionnaire de téléchargement
- Gestionnaire de téléchargement du lecteur Windows Media
- Gestionnaire de téléchargement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cecb7b99ae36d3881fdf80eaad7d851205b9b2e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380393"
---
# <a name="using-the-download-manager"></a>Utilisation du gestionnaire de téléchargement

Le kit de développement logiciel (SDK) Windows Media Player comprend un exemple de page Web illustrant l’utilisation du gestionnaire de téléchargement pour télécharger des fichiers sur l’ordinateur de l’utilisateur. Vous pouvez localiser l’exemple dans le dossier nommé page Web dans lequel vous avez installé le kit de développement logiciel (SDK). Le nom du fichier est Sample. asp. L’exemple fournit les fonctionnalités suivantes :

-   Crée l’objet **downloadmanager** .
-   Crée un objet **DownloadCollection** .
-   Démarre le téléchargement de cinq fichiers lorsque l’utilisateur clique sur **Télécharger**. Les chemins d’accès aux fichiers par défaut sont fournis dans l’exemple. Vous devez remplacer ces chemins par défaut par les emplacements des fichiers sur votre propre serveur. Vous pouvez modifier les chemins d’accès en modifiant les valeurs assignées au tableau global nommé g \_ sFiles.
-   Affiche les informations d’état d’un téléchargement lorsque l’utilisateur le sélectionne.
-   Fournit des contrôles pour suspendre, reprendre, annuler et supprimer un élément de téléchargement.
-   Gère les informations relatives aux regroupements de téléchargement entre les sessions à l’aide de cookies. C’est important, car l’utilisateur peut fermer le lecteur à tout moment. En outre, si l’utilisateur bascule les volets des tâches dans le lecteur, la session de la Banque en ligne se termine.
-   Utilise le téléchargement en temps réel par défaut. Vous pouvez modifier le comportement du téléchargement en arrière-plan en modifiant la valeur de la variable nommée g \_ sDLType. Le téléchargement en arrière-plan peut être utilisé avec le système d’exploitation Microsoft Windows XP.
-   Synchronise la couleur d’arrière-plan avec la couleur du joueur. Vous pouvez utiliser cette fonctionnalité pour modifier l’apparence de votre magasin en ligne lorsque l’utilisateur choisit de modifier la couleur du joueur.

Les sections suivantes fournissent plus d’informations :

-   [Initialisation de la page](initializing-the-page.md)
-   [Démarrage des téléchargements](starting-the-downloads.md)
-   [Récupération des informations d’État](retrieving-status-information.md)
-   [Gestion des informations de session](maintaining-session-information.md)
-   [Débogage de la page](debugging-the-page.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de programmation pour les magasins en ligne de type 2**](programming-guide-for-type-2-online-stores.md)
</dt> </dl>

 

 




