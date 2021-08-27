---
title: Conversion des couleurs et correspondance des couleurs
description: Le processus de conversion des couleurs d’un espace colorimétrique à un autre est appelé conversion des couleurs.
ms.assetid: 52f68779-d4d6-4f1e-88a4-f872e9e90054
keywords:
- Windows Système de couleurs (WCS), conversion de couleurs
- WCS (Windows color System), conversion de couleurs
- gestion des couleurs des images, conversion de couleurs
- gestion des couleurs, conversion de couleurs
- couleurs, conversion de couleurs
- conversion de couleurs
- Windows Système de couleurs (WCS), correspondance des couleurs
- WCS (Windows color System), correspondance des couleurs
- gestion des couleurs des images, correspondance des couleurs
- gestion des couleurs, correspondance des couleurs
- couleurs, correspondance des couleurs
- correspondance des couleurs
- Windows Système de couleurs (WCS), mappage des couleurs
- WCS (Windows color System), mappage des couleurs
- gestion des couleurs des images, mappage des couleurs
- gestion des couleurs, mappage des couleurs
- couleurs, mappage des couleurs
- mappage des couleurs
- point blanc
- colorants
- correction gamma
- AVERTISSEMENT
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0071e15c2d572c134d61aee7a018b41c8d09507e87963eeeed1488909cdafeba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110799"
---
# <a name="color-conversion-and-color-matching"></a>Conversion des couleurs et correspondance des couleurs

Le processus de conversion des couleurs d’un [espace colorimétrique](c.md) à un autre est appelé *conversion des couleurs*. Toutes les couleurs d’un espace colorimétrique sont fixes par rapport au [point blanc](w.md)de l’espace de couleurs. Étant donné que le point blanc d’un espace de couleurs varie d’un appareil à l’appareil, une couleur convertie doit ensuite être mise en correspondance avec sa couleur la plus proche de l’espace de couleur de destination. Ce processus est appelé « *mappage des couleurs*».

Par exemple, si vous avez créé une image numérique sur votre écran, elle peut se trouver dans un espace de couleurs RVB dépendant du périphérique. Si vous souhaitez l’imprimer sur une imprimante, celle-ci doit être convertie dans l’espace colorimétrique de l’imprimante. Étant donné que l’imprimante utilise probablement un espace colorimétrique CMJN dépendant du périphérique, toutes les valeurs RVB doivent être converties en CYMK. Il s’agit de la [conversion de couleurs](c.md). Une fois que les valeurs sont spécifiées en termes d’espace CYMK, elles doivent être mises en correspondance avec la couleur la plus proche que l’imprimante peut produire. C’est ce que l’on appelle le mappage des couleurs ou la [correspondance des couleurs](c.md).

La conversion des couleurs et le mappage des couleurs doivent prendre en compte un certain nombre de facteurs spécifiques à l’appareil. Par exemple, les blocs de construction des images d’écran sont des pixels. Chaque pixel a un nombre défini de bits pour stocker sa valeur d’index de couleur ou de couleur. Le nombre de bits par pixel dépend du type d’affichage et de la carte d’affichage utilisés, et du mode de définition de l’adaptateur. La plupart des types d’imprimante utilisent différents [colorants](c.md) et impriment à des résolutions particulières.

En outre, les caractéristiques de tonalité physique d’un appareil sont souvent différentes sur des appareils différents. Par exemple, lorsque des couleurs sont produites par des moniteurs d’ordinateur, elles peuvent être différentes si elles étaient produites sur une presse d’impression. Un facteur de correction, appelé *correction gamma*, est fréquemment utilisé pour compenser ces différences.

Le résultat de ces facteurs dépendants de l’appareil est que chaque périphérique de couleur a un ensemble particulier de couleurs qu’il peut produire. Ce jeu de couleurs est connu sous le nom de *gamme*. Pour effectuer une conversion des couleurs et un mappage des couleurs, les couleurs d’une image doivent être converties à partir de l’espace de couleurs et de la gamme de l’appareil source dans l’espace colorimétrique du périphérique de destination. Ils sont ensuite mis en correspondance avec la gamme de l’appareil de destination.

 

 




