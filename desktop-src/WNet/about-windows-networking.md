---
title: à propos de la mise en réseau Windows
description: Les applications peuvent utiliser les fonctions WNet pour ajouter et annuler des connexions réseau et récupérer des informations sur la configuration actuelle du réseau.
ms.assetid: 37ce0762-b0b2-4d68-9942-b7034f1b76b7
keywords:
- Windows réseau WNet, description
- WNet WNet, Description
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ae26c503456d803edaed0b976e33020565aaa2364e7fc465c17a62cadf9068c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760473"
---
# <a name="about-windows-networking"></a>à propos de la mise en réseau Windows

Les applications peuvent utiliser les fonctions WNet pour ajouter et annuler des connexions réseau et récupérer des informations sur la configuration actuelle du réseau.

L’illustration suivante montre la structure d’un réseau classique.

![structure de réseau classique](images/csnet-01.png)

dans la figure précédente, la hiérarchie des ressources Windows serveur NT/Windows 2000 est fournie en détail en tant que fournisseur réseau \# 1. Les ressources réseau d’autres fournisseurs ont des systèmes hiérarchiques différents. Une application n’a pas besoin d’informations sur la hiérarchie avant de commencer à travailler sur un réseau. Elle peut être exécutée à partir de la racine du réseau (autrement dit, la ressource conteneur la plus grande) et récupérer des informations sur les ressources du réseau, car les informations sont requises.

Les ressources réseau qui contiennent d’autres ressources sont appelées *conteneurs*. Les ressources de conteneur se trouvent dans les champs de la figure précédente.

Les ressources qui ne contiennent pas d’autres ressources sont appelées *objets*. Dans la figure précédente, SharePoint \# 1 et SharePoint \# 2 sont des objets. *SharePoint* est un objet accessible sur le réseau. Les imprimantes et les répertoires partagés sont des exemples de SharePoint.

 

 




