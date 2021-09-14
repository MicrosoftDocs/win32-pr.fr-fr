---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- Périphériques MCI, pilote MCIAVI
- Commandes MCI, pilote MCIAVI
- Pilote MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194983"
---
# <a name="mciavi"></a>MCIAVI

Un fichier AVI peut contenir plus de deux flux, par exemple une séquence vidéo, une piste audio anglaise et une bande son française. Votre application peut utiliser un flux indépendamment des autres flux du fichier.

Le type d’appareil **Digitalvideo** contrôle les fichiers vidéo. Pour obtenir la liste des commandes MCI reconnues par les périphériques vidéo numériques, consultez [jeu de commandes vidéo numérique](digital-video-command-set.md).

Le pilote MCIAVI lit les séquences vidéo et d’autres flux de données sous le contrôle de commandes MCI. Les flux de données peuvent contenir des images, des données audio et des palettes. Les données de l’image peuvent se composer d’images avec des palettes de couleurs ou des informations de couleurs vraies.

L’audio est synchronisé avec la vidéo dans un trentième de seconde. Toutefois, si le matériel audio n’est pas disponible, le pilote ne lit que le flux vidéo. Le pilote MCIAVI peut supprimer des images vidéo, si nécessaire, pour lire un flux sans interruption audio.

Votre application peut utiliser les services de la classe de fenêtre MCIWnd au lieu de l’interface de commande MCI pour contrôler tout pilote MCI. Cette classe de fenêtre gère la plupart des détails de la gestion de la fenêtre qui prend en charge le périphérique MCI et simplifie la programmation requise pour envoyer les commandes MCI. Votre application peut utiliser directement les services de bibliothèque MCIWnd pour contrôler l’appareil MCI, ou elle peut avoir des MCIWnd afficher une barre d’outils, une barre de défilement et des menus qui permettent à l’utilisateur de contrôler l’appareil. Pour plus d’informations sur la classe de fenêtre MCIWnd, consultez [classe de fenêtre MCIWnd](mciwnd-window-class.md).

 

 




