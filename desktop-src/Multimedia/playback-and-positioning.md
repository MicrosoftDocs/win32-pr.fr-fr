---
title: Lecture et positionnement
description: Lecture et positionnement
ms.assetid: fbf9294e-c644-45c7-ab60-dd903409a44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1efbd6256fbd0d258f5d5c9d3da9b01c72a203dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110838"
---
# <a name="playback-and-positioning"></a>Lecture et positionnement

Un certain nombre de commandes MCI, telles que [**lecture**](play.md) ([**\_ lecture MCI**](mci-play.md)), [**arrêt**](stop.md) (MCI), [**Pause**](pause.md) ([**\_ Pause MCI**](mci-pause.md)), [**reprise**](resume.md) ([**\_ reprise MCI**](mci-resume.md)) et [**recherche**](seek.md) ([**MCI \_ Seek**](mci-seek.md)), affectent la lecture ou le positionnement d’un fichier multimédia.[**\_**](mci-stop.md) Si un périphérique MCI reçoit une commande de lecture alors qu’une autre commande de lecture est en cours, il accepte la commande et arrête ou remplace la commande précédente.

De nombreuses commandes MCI, telles que [**Set**](set.md) ([**MCI \_ Set**](mci-set.md)), n’affectent pas la lecture. Une notification de l’une de ces commandes n’interfère pas avec les commandes de lecture ou de position en attente tant que les notifications ne sont pas exécutées à partir de la même instance du pilote. Par exemple, vous pouvez émettre une commande **Set** ou [**Status**](status.md) ([**\_ État MCI**](mci-status.md)) quand un appareil exécute une commande **Seek** sans arrêter ni remplacer la commande **Seek** .

Toutefois, il ne peut y avoir qu’une seule notification en attente. Par exemple, si une application demande une notification pour la **lecture** et suit la demande avec l' **État** « démarrer la notification de la position », la notification de **lecture** retourne « remplacé » et la notification pour la commande Status est renvoyée lorsqu’elle est terminée. Dans ce cas, toutefois, la commande de **lecture** est toujours réussie, même si l’application n’a pas reçu la notification.

 

 




