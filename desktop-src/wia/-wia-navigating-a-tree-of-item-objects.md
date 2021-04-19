---
description: 'En savoir plus sur : navigation dans une arborescence d’objets d’élément'
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: Navigation dans une arborescence d’objets Item
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515038"
---
# <a name="navigating-a-tree-of-item-objects"></a>Navigation dans une arborescence d’objets Item

> [!Note]  
> Ce système de script a été remplacé par la couche d’automatisation de l’acquisition d’images Windows (WIA). Voir [couche d’automatisation de l’acquisition d’image Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

Une application ou un script parcourt l’arborescence d’éléments d’un appareil WIA (Windows Image Acquisition) pour rechercher et sélectionner des images sur cet appareil. À l’aide de cette technique, une application sélectionne et acquiert une image sans utiliser de boîte de dialogue.

Un appareil WIA est représenté en tant qu’élément racine dans une arborescence d’objets d' [**élément**](-wia-item.md) . Les éléments enfants de l’arborescence représentent des dossiers et des images pour un appareil photo ou des lits d’analyse pour un scanneur.

Après vous être connecté à un appareil, appelez la propriété [**Children**](-wia-iwiadispatchitem-children.md) de l’objet [**Item**](-wia-item.md) qui représente l’appareil (l’élément racine de l’arborescence) pour obtenir une collection des éléments enfants (images ou lits d’analyse) de l’appareil.

Énumère cette collection (de manière récursive, si nécessaire) pour naviguer dans l’arborescence de l’élément.

 

 
