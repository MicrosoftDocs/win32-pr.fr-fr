---
title: Fonctions de rappel d’État
description: Fonctions de rappel d’État
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Fonctions de rappel AVICap, état
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b4b4bf4cad5f689f1e146986f9d1b55b00f1aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379942"
---
# <a name="status-callback-functions"></a>Fonctions de rappel d’État

Une fenêtre de capture peut envoyer des messages à la fonction de rappel d’état lors de la capture de la vidéo sur le disque ou lors d’autres opérations de longue durée pour notifier votre application de la progression d’une opération. Les informations d’État incluent un identificateur de message et une chaîne de texte mise en forme prête pour l’affichage. Votre application peut utiliser l’identificateur de message pour filtrer les notifications et limiter les messages à présenter à l’utilisateur. Pendant les opérations de capture, le premier message envoyé à la fonction de rappel est toujours IDS \_ Cap \_ Begin et le dernier est toujours ID \_ Cap \_ end. Un identificateur de message égal à zéro indique qu’une nouvelle opération démarre et que la fonction de rappel doit effacer l’état actuel.

 

 




