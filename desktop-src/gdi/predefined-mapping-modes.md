---
description: Parmi les six modes de mappage prédéfinis, l’un est dépendant du périphérique (texte de MM \_ ) et les cinq autres (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC et mm \_ TWIPS) sont indépendants des appareils.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Modes de mappage prédéfinis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f252f587e98a739306a84450a1d9669ed21873cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972563"
---
# <a name="predefined-mapping-modes"></a>Modes de mappage prédéfinis

Parmi les six modes de mappage prédéfinis, l’un est dépendant du périphérique (texte de MM \_ ) et les cinq autres (mm \_ HIENGLISH, mm \_ LOENGLISH, MM \_ HIMETRIC, mm \_ LOMETRIC et mm \_ TWIPS) sont indépendants des appareils.

Le mode de mappage par défaut est le texte de MM \_ . Une unité logique est égale à un pixel. Le x positif est à droite, et le y positif est inactif. Ce mode est mappé directement au système de coordonnées de l’appareil. Le mappage logique-physique implique uniquement un décalage en x et y qui est défini par la fenêtre contrôlée par l’application et les origines de la fenêtre d’affichage. La fenêtre d’affichage et les étendues de fenêtre ont toutes la valeur 1, ce qui crée un mappage un-à-un.

Les applications qui affichent des formes géométriques (cercles, carrés, polygones, etc.) utilisent l’un des modes de mappage indépendants du périphérique. Par exemple, si vous écrivez une application pour fournir des fonctionnalités graphiques à un programme de feuille de calcul et que vous souhaitez vous assurer que le diamètre de chaque graphique à secteurs est de 2 pouces, utilisez le \_ mode de mappage mm LOENGLISH et appelez les fonctions appropriées pour dessiner et remplir le graphique. Si vous spécifiez MM \_ LOENGLISH, vous garantissez que le diamètre du graphique est cohérent sur l’écran ou l’imprimante. Si le \_ texte de mm est utilisé à la place de mm \_ LOENGLISH, un graphique qui apparaît circulaire sur un écran VGA apparaîtra elliptique sur un écran EGA et serait très petit sur une imprimante laser 300 ppp (points par pouce).

 

 



