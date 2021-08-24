---
description: La région de mise à jour identifie la partie d’une fenêtre qui est obsolète ou non valide et qui doit être redessinée.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: La région de mise à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a8f847a1e2d479200cfe6ea4e60a1b3a8ebf4c02aaf7c89fc719f62d91e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717969"
---
# <a name="the-update-region"></a>La région de mise à jour

La *région de mise à jour* identifie la partie d’une fenêtre qui est obsolète ou non valide et qui doit être redessinée. Le système utilise la région de mise à jour pour générer des messages de [**\_ peinture WM**](wm-paint.md) pour les applications et réduire le temps que les applications consacrent à mettre à jour le contenu de leur Windows. Le système ajoute uniquement la partie non valide de la fenêtre à la zone de mise à jour, ce qui requiert que cette partie soit dessinée uniquement.

Lorsque le système détermine qu’une fenêtre a besoin d’être mis à jour, il définit les dimensions de la région de mise à jour sur la partie non valide de la fenêtre. La définition de la région de mise à jour n’entraîne pas immédiatement le dessin de l’application. Au lieu de cela, l’application continue de récupérer les messages de la file d’attente de messages d’application jusqu’à ce qu’aucun message ne soit conservé. Le système vérifie ensuite la région de mise à jour et, si la région n’est pas vide (non NULL), elle envoie un message de [**\_ peinture WM**](wm-paint.md) à la procédure de fenêtre.

Une application peut utiliser la région de mise à jour pour générer ses messages de [**\_ peinture WM**](wm-paint.md) . Par exemple, une application qui charge des données à partir de fichiers ouverts définit généralement la région de mise à jour lors du chargement afin que les nouvelles données soient dessinées lors du traitement du message **WM de \_ peinture** suivant. En général, une application ne doit pas être dessinée au moment où ses données changent, mais acheminer toutes les opérations de dessin via le message de **\_ peinture WM** .

 

 



