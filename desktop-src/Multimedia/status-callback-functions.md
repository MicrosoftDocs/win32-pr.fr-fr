---
title: Fonctions de rappel d’État
description: Fonctions de rappel d’État
ms.assetid: fe89fb97-0b56-4956-a1a6-f4ad2d06befa
keywords:
- Fonctions de rappel AVICap, état
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07539b016ea344f2a38d54a7274d01006532ed040ea3fa96990bff09e22d470
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037159"
---
# <a name="status-callback-functions"></a>Fonctions de rappel d’État

Une fenêtre de capture peut envoyer des messages à la fonction de rappel d’état lors de la capture de la vidéo sur le disque ou lors d’autres opérations de longue durée pour notifier votre application de la progression d’une opération. Les informations d’État incluent un identificateur de message et une chaîne de texte mise en forme prête pour l’affichage. Votre application peut utiliser l’identificateur de message pour filtrer les notifications et limiter les messages à présenter à l’utilisateur. Pendant les opérations de capture, le premier message envoyé à la fonction de rappel est toujours IDS \_ Cap \_ Begin et le dernier est toujours ID \_ Cap \_ end. Un identificateur de message égal à zéro indique qu’une nouvelle opération démarre et que la fonction de rappel doit effacer l’état actuel.

 

 




