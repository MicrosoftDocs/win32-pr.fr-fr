---
description: Windows Le programme d’installation de contient les fonctionnalités permettant d’afficher un indicateur de progression dans une boîte de dialogue d’affichage des actions.
ms.assetid: cfc2d974-4f2d-4f52-9835-eab1dc091c9b
title: Création d’un contrôle ProgressBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b872ed2dd36fb8ed04ee48fd69e4680fce002a18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092518"
---
# <a name="authoring-a-progressbar-control"></a>Création d’un contrôle ProgressBar

Windows Le programme d’installation de contient les fonctionnalités permettant d’afficher un indicateur de progression dans une boîte de dialogue d’affichage des actions. Le [contrôle ProgressBar](progressbar-control.md) représente graphiquement l’installation de composants individuels et signale le temps total écoulé par rapport au temps restant ou la durée totale restante, jusqu’à ce que l’installation soit terminée.

Pour déterminer la durée totale prévue pour l’installation, le programme d’installation suit le nombre total de cycles de progression prévus par chaque action pendant la génération du script d’exécution. Lorsque la génération du script est terminée, le total des cycles de progression est stocké et l’installation commence.

Les messages de progression détaillant le nombre de cycles de progression écoulés sont envoyés au gestionnaire de messages actifs à mesure que chaque action dans le script est exécutée. À chaque message de progression, le programme d’installation diffuse un [ControlEvent, SetProgress](setprogress-controlevent.md) dans la boîte de dialogue actuellement active. La séquence d’interface utilisateur doit être créée pour créer la boîte de dialogue d’affichage des actions lors de l’exécution du script afin de recevoir les messages SetProgress ControlEvent, du programme d’installation.

Quand la boîte de dialogue Affichage des actions reçoit un ControlEvent, SetProgress, il vérifie la [table EventMapping](eventmapping-table.md) pour tous les contrôles qui s’abonnent à ControlEvent,. Le contrôle ProgressBar de la boîte de dialogue Affichage des actions est abonné à avec l’attribut contrôle de progression spécifié dans la colonne attributs. L’attribut de contrôle Progress spécifie que le contrôle ProgressBar recevra les valeurs « ticksSoFar » et « totalTicks » avec le ControlEvent, SetProgress. Le contrôle de barre de progression utilise ces informations pour avancer la barre graphique de gauche à droite pour une installation et de droite à gauche pour une opération de [restauration](rollback-installation.md) .

En outre, le programme d’installation diffuse un [ControlEvent, TimeRemaining](timeremaining-controlevent.md) sur chaque message de progression. La durée totale restante pour l’installation est déterminée en calculant d’abord la fréquence d’exécution, qui est le nombre total de cycles écoulés, divisé par le temps total écoulé depuis le début de l’installation. Le nombre total de cycles restants divisé par la fréquence d’exécution indique le temps restant approximatif.

Quand la boîte de dialogue Affichage des actions reçoit le ControlEvent, TimeRemaining, elle recherche à nouveau dans la table EventMapping les contrôles qui sont abonnés. Pour afficher le temps restant, un contrôle de [texte](text-control.md) doit être abonné au ControlEvent, TimeRemaining avec l' [attribut de contrôle TimeRemaining](timeremaining-control-attribute.md) spécifié dans la colonne attributs.

Le contrôle de texte abonné interroge la [table UIText](uitext-table.md) pour une chaîne de modèle paramétrable nommée « TimeRemaining ». Cette chaîne a deux paramètres, \[ 1 \] pour les minutes et \[ 2 \] pour secondes. Le contrôle de texte convertit chaque valeur en minutes et secondes, évalue la chaîne de modèle TimeRemaining et met à jour le contrôle de texte avec les nouvelles informations.

Si le niveau d’affichage de l’interface utilisateur est défini sur basique ou inférieur, le programme d’installation affiche une boîte de dialogue par défaut contenant une barre de progression et un champ de texte TimeRemaining. Pour plus d’informations, consultez niveaux de l' [interface utilisateur](user-interface-levels.md).

 

 



