---
title: À propos de la configuration de l’analyse
description: À propos de la configuration de l’analyse
ms.assetid: 66345021-41e8-429a-bbf7-a4aa72a57337
keywords:
- moniteur, à propos de
- moniteur, étalonnage des couleurs
- moniteur, réglage de la zone d’affichage du moniteur
- surveiller, enregistrer les paramètres de l’analyse
- surveiller, restaurer les paramètres d’analyse
- moniteur, fonctionnalités du fournisseur
- étalonnage des couleurs
- réglage de la zone d’affichage du moniteur
- enregistrement des paramètres de l’analyse
- restauration des paramètres d’analyse
- fonctionnalités du fournisseur
- configuration de l’analyse, étalonnage des couleurs
- configuration de l’analyse, à propos de
- surveiller la configuration, ajuster la zone d’affichage du moniteur
- surveiller la configuration, enregistrer les paramètres de l’analyse
- surveiller la configuration, restaurer les paramètres d’analyse
- configuration de l’analyse, fonctionnalités du fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f5f3d8c56521c07d704fe586f486298d0e679d1bfc33e25a29d943aa92dd66e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146182"
---
# <a name="about-monitor-configuration"></a>À propos de la configuration de l’analyse

Les fonctions de configuration de l’analyse sont les suivantes :

-   Étalonnage des couleurs. Une analyse correctement étalonnée reproduit correctement les couleurs. En règle générale, une application d’étalonnage des couleurs affiche un modèle de test et dispose de contrôles pour modifier un paramètre d’analyse. L’utilisateur modifie le paramètre jusqu’à ce qu’une condition soit remplie et répète ce processus pour chaque paramètre de l’analyse jusqu’à ce que l’analyseur soit étalonné.
-   Ajustement de la zone d’affichage du moniteur. Les fonctions de configuration de l’analyse peuvent être utilisées pour modifier la taille et la position de la zone d’affichage d’un moniteur. Par exemple, lorsqu’un moniteur LCD est connecté à un ordinateur à l’aide d’un connecteur analogique, la meilleure qualité d’image est obtenue lorsqu’il existe un mappage un-à-un entre les pixels de la mémoire tampon de trame de la carte graphique et les pixels sur l’écran LCD.
-   Enregistrement et restauration des paramètres d’analyse. Certains utilisateurs ont besoin de plusieurs ensembles de paramètres d’analyse, car différents scénarios nécessitent différents paramètres d’analyse. Par exemple, les paramètres de surveillance optimaux pour les applications de bureau ne sont pas optimaux pour regarder la télévision.
-   Utilisation des fonctionnalités d’analyse spécifiques au fournisseur. À l’aide des fonctions de configuration de l’analyse, les fabricants peuvent créer des applications qui utilisent les fonctionnalités spécifiques au fournisseur du moniteur.

Les fonctions de configuration de l’analyse sont divisées en fonctions de haut niveau et de bas niveau. Les fonctions de haut niveau sont plus faciles à utiliser que les fonctions de bas niveau. Pour utiliser les fonctions de haut niveau, vous n’avez rien à savoir sur l’interface de commande DDC/CI. Toutefois, les fonctions de haut niveau ne vous donnent pas accès aux fonctionnalités spécifiques au fournisseur du moniteur.

Les fonctions de bas niveau sont un wrapper léger autour des commandes DDC/CI. Pour utiliser les fonctions de bas niveau, vous devez être familiarisé avec la norme DDC/CI et avec la norme du jeu de commandes de contrôle du moniteur VESA (MCCS). En général, vous devez utiliser les fonctions de haut niveau, sauf si vous avez besoin d’utiliser des fonctionnalités qui sont uniquement disponibles dans les fonctions de bas niveau.

Les fonctions de configuration de l’analyse de haut niveau sont conçues de façon à ce qu’une application ne puisse pas mettre un moniteur dans un état inutilisable. Les fonctions de bas niveau peuvent être utilisées pour envoyer des codes VCP à l’analyse. Toutefois, sachez que certains codes VCP peuvent désactiver des fonctionnalités importantes ou placer l’analyse dans un État où l’utilisateur ne peut pas voir l’image d’affichage. Pour plus d’informations, consultez la norme du jeu de commandes de contrôle du moniteur VESA (MCCS).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration de l’analyse](monitor-configuration.md)
</dt> </dl>

 

 




