---
title: À propos de la mise en réseau Windows
description: Les applications peuvent utiliser les fonctions WNet pour ajouter et annuler des connexions réseau et récupérer des informations sur la configuration actuelle du réseau.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- Mise en réseau Windows WNet, Description
- WNet WNet, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c91f7c8f58d4e44439bac18a2b7d7b850b21f955
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029816"
---
# <a name="about-windows-networking"></a>À propos de la mise en réseau Windows

Les applications peuvent utiliser les fonctions WNet pour ajouter et annuler des connexions réseau et récupérer des informations sur la configuration actuelle du réseau.

L’illustration suivante montre la structure d’un réseau classique.

![structure de réseau classique](images/csnet-01.png)

Dans la figure précédente, la hiérarchie pour les ressources du serveur Windows NT Server/Windows 2000 est fournie en détail en tant que fournisseur réseau \# 1. Les ressources réseau d’autres fournisseurs ont des systèmes hiérarchiques différents. Une application n’a pas besoin d’informations sur la hiérarchie avant de commencer à travailler sur un réseau. Elle peut être exécutée à partir de la racine du réseau (autrement dit, la ressource conteneur la plus grande) et récupérer des informations sur les ressources du réseau, car les informations sont requises.

Les ressources réseau qui contiennent d’autres ressources sont appelées *conteneurs*. Les ressources de conteneur se trouvent dans les champs de la figure précédente.

Les ressources qui ne contiennent pas d’autres ressources sont appelées *objets*. Dans la figure précédente, SharePoint \# 1 et SharePoint \# 2 sont des objets. *SharePoint* est un objet accessible sur le réseau. Les imprimantes et les répertoires partagés sont des exemples de SharePoint.

 

 




