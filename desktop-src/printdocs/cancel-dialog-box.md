---
description: Cette rubrique explique comment afficher la progression du travail d’impression à l’utilisateur et lui attribuer la possibilité d’annuler un travail d’impression en cours.
ms.assetid: 2b7a0ab7-bf7e-473d-ab43-8b79478d4453
title: 'Comment : afficher la progression du travail d’impression'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec61c07844262b258fb052d08d8d20e9285a8f7e9bb83808ea61eddaf32f3a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950609"
---
# <a name="how-to-display-the-print-job-progress"></a>Comment : afficher la progression du travail d’impression

Cette rubrique explique comment afficher la progression du travail d’impression à l’utilisateur et lui attribuer la possibilité d’annuler un travail d’impression en cours.

## <a name="overview"></a>Vue d’ensemble

Une procédure de boîte de dialogue d’avancement de l’impression effectue généralement les fonctions suivantes.

-   Affichez la progression du travail d’impression à l’utilisateur.
-   Démarrez le thread de traitement de l’impression.
-   Affichez un bouton **Annuler** pour que l’utilisateur puisse arrêter un travail d’impression avant qu’il ne se termine.

À proprement parler, la seule chose que la procédure de la boîte de dialogue de progression de l’impression doit faire est d’afficher la progression du travail d’impression à l’utilisateur. Toutefois, étant donné que les deux autres fonctions de la liste précédente sont étroitement liées, elles ont également été incluses dans ce module.

## <a name="displaying-print-job-progress"></a>Affichage de la progression du travail d’impression

Une procédure de la boîte de dialogue progression de l’impression gère les messages de fenêtre suivants.

-   **\_INITDIALOG WM**

    Initialise les contrôles que la boîte de dialogue utilise.

-   **\_SETCURSOR WM**

    Définit le curseur sur un pointeur lorsque l’utilisateur est en mesure d’annuler un travail d’impression, et au curseur d’attente lorsque le travail d’impression se trouve à un point où il ne peut pas être annulé.

-   **impression du \_ début d’impression de \_ \_ l’utilisateur**

    Définit les paramètres de barre de progression pour le travail d’impression et crée le thread d’impression pour démarrer le traitement du travail d’impression.

    Il s’agit d’un message de fenêtre spécifique à l’application.

-   **\_commande WM-IDCANCEL**

    Définit l’événement CANCEL pour indiquer au thread de traitement de l’impression d’annuler le travail d’impression.

-   **\_ \_ \_ mise à jour de l’état d’impression de l’utilisateur**

    Met à jour la barre de progression et le texte d’État pour afficher l’état actuel du travail d’impression.

    Il s’agit d’un message de fenêtre spécifique à l’application.

-   **fermeture de l’impression de l’utilisateur \_ \_**

    Définit le texte d’état de fermeture dans la boîte de dialogue de progression pour indiquer que le travail d’impression est en cours de fermeture.

    Il s’agit d’un message de fenêtre spécifique à l’application.

-   **impression de l’utilisateur \_ \_ terminée**

    Affiche le message « travail d’impression terminé » pour l’utilisateur et libère les descripteurs et les événements qui ont été utilisés dans ce travail d’impression.

    Il s’agit d’un message de fenêtre spécifique à l’application.

 

 



