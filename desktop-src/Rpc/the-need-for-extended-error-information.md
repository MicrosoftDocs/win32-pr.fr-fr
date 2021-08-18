---
title: Besoin d’informations d’erreur étendues
description: Une difficulté principale associée à la résolution des problèmes RPC est le mappage d’un code d’erreur RPC au problème sous-jacent.
ms.assetid: aef3bcd6-ecaa-4639-b765-da90db6ddf82
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bce13e2cb30c7cd9f2db4d7f518eb0a747cd15b2ba1ff7962cf5f41fbc9cf552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016799"
---
# <a name="the-need-for-extended-error-information"></a>Besoin d’informations d’erreur étendues

Une difficulté principale associée à la résolution des problèmes RPC est le mappage d’un code d’erreur RPC au problème sous-jacent. Une erreur de configuration ou un problème réseau peut entraîner la réception d’erreurs RPC S par une ou plusieurs stations de travail \_ \_ \* , mais cette station de travail ne peut afficher que l’erreur, la faire une faute ou l’enregistrer dans un fichier journal. Quelle que soit l’approche utilisée, la personne qui dépanne le problème est démunie des informations essentielles :

-   Où l’erreur s’est produite. Il s’est peut-être produit sur l’ordinateur local, sur un ordinateur distant appelé par l’ordinateur local, ou sur un ordinateur distant appelé par un autre ordinateur distant.
-   Code d’erreur d’origine qui a provoqué le problème. Pour se conformer à la norme OSF, MS RPC mappe les codes d’erreur aux \_ codes RPC S \_ \* . \_ \_ \* Toutefois, les codes RPC S sont trop génériques et offrent peu d’informations de dépannage utiles.
-   Toutes les informations de contexte relatives à l’occurrence du problème. Avec les erreurs autres que RPC, les débogueurs peuvent arrêter le processus et examiner le contexte dans lequel l’erreur s’est produite. Les erreurs RPC sont souvent générées par un processus ou un ordinateur distant, qui continue le traitement après avoir retourné l’erreur et remplace tout contexte se rapportant à l’erreur.

 

 




