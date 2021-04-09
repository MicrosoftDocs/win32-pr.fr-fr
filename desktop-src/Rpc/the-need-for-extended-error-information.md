---
title: Besoin d’informations d’erreur étendues
description: Une difficulté principale associée à la résolution des problèmes RPC est le mappage d’un code d’erreur RPC au problème sous-jacent.
ms.assetid: aef3bcd6-ecaa-4639-b765-da90db6ddf82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d82fbbcaf0fac427b2bf64fbacbf1e85aeb4d06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028948"
---
# <a name="the-need-for-extended-error-information"></a>Besoin d’informations d’erreur étendues

Une difficulté principale associée à la résolution des problèmes RPC est le mappage d’un code d’erreur RPC au problème sous-jacent. Une erreur de configuration ou un problème réseau peut entraîner la réception d’erreurs RPC S par une ou plusieurs stations de travail \_ \_ \* , mais cette station de travail ne peut afficher que l’erreur, la faire une faute ou l’enregistrer dans un fichier journal. Quelle que soit l’approche utilisée, la personne qui dépanne le problème est démunie des informations essentielles :

-   Où l’erreur s’est produite. Il s’est peut-être produit sur l’ordinateur local, sur un ordinateur distant appelé par l’ordinateur local, ou sur un ordinateur distant appelé par un autre ordinateur distant.
-   Code d’erreur d’origine qui a provoqué le problème. Pour se conformer à la norme OSF, MS RPC mappe les codes d’erreur aux \_ codes RPC S \_ \* . \_ \_ \* Toutefois, les codes RPC S sont trop génériques et offrent peu d’informations de dépannage utiles.
-   Toutes les informations de contexte relatives à l’occurrence du problème. Avec les erreurs autres que RPC, les débogueurs peuvent arrêter le processus et examiner le contexte dans lequel l’erreur s’est produite. Les erreurs RPC sont souvent générées par un processus ou un ordinateur distant, qui continue le traitement après avoir retourné l’erreur et remplace tout contexte se rapportant à l’erreur.

 

 




