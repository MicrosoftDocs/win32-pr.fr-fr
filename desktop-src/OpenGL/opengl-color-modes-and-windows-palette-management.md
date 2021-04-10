---
title: Modes de couleurs OpenGL et gestion de la palette Windows
description: L’implémentation Microsoft de OpenGL dans Windows prend en charge deux modes de données de pixels de couleur RVBA et les modes d’index de couleurs. Windows propose deux méthodes de gestion des couleurs et des palettes de couleurs vraies.
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL sur Windows, modes de couleur
- OpenGL sur Windows, gestion de palette
- gestion de la palette OpenGL
- modes de couleurs OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3d63778301ec55b962f3f66e79d99cee09be9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309789"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a>Modes de couleurs OpenGL et gestion de la palette Windows

L’implémentation Microsoft de OpenGL dans Windows prend en charge deux modes de données en pixels de couleur : RVBA et les modes d’index de couleurs. Windows propose deux méthodes de gestion des couleurs analogues : la véritable gestion des couleurs et des palettes.

Les périphériques de couleur vraies, capables d’accepter 16, 24 ou plus d’informations de couleur par pixel, peuvent afficher des dizaines de milliers, des dizaines de millions ou plus de couleurs simultanément. Toutefois, les complexités surviennent quand une application doit gérer le mode RVBA ou index des couleurs sur un appareil de type palette. Les appareils de type palette, tels qu’un affichage VGA de 256 couleurs, sont limités dans le nombre de couleurs qu’ils peuvent afficher simultanément. Les applications doivent gérer un certain nombre de détails délicats pour utiliser avec succès des appareils de type palette. Étant donné que les programmes en mode d’index de couleurs n’utilisent pas de palette matérielle, ils sont plus difficiles à utiliser avec les périphériques de couleurs vraies que les programmes utilisant le mode RVBA.

 

 




