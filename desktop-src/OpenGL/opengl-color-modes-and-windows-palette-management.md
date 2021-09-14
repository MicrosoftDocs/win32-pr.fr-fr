---
title: Modes de couleurs OpenGL et gestion de la Palette de Windows
description: l’implémentation Microsoft de OpenGL dans Windows prend en charge deux modes de données de pixels de couleur rvba et les modes d’index de couleurs. Windows fournir deux manières analogues de gérer la couleur et la gestion de la palette couleurs vraies.
ms.assetid: 4a731119-8704-4ae1-a564-4a1955051236
keywords:
- OpenGL sur Windows, modes de couleur
- OpenGL sur Windows, gestion de la palette
- gestion de la palette OpenGL
- modes de couleurs OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa3d63778301ec55b962f3f66e79d99cee09be9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233550"
---
# <a name="opengl-color-modes-and-windows-palette-management"></a>Modes de couleurs OpenGL et gestion de la Palette de Windows

l’implémentation Microsoft de OpenGL dans Windows prend en charge deux modes de données de pixels de couleur : rvba et les modes d’index de couleurs. Windows fournir deux manières analogues de gérer la couleur : la vraie gestion des couleurs et des palettes.

Les périphériques de couleur vraies, capables d’accepter 16, 24 ou plus d’informations de couleur par pixel, peuvent afficher des dizaines de milliers, des dizaines de millions ou plus de couleurs simultanément. Toutefois, les complexités surviennent quand une application doit gérer le mode RVBA ou index des couleurs sur un appareil de type palette. Les appareils de type palette, tels qu’un affichage VGA de 256 couleurs, sont limités dans le nombre de couleurs qu’ils peuvent afficher simultanément. Les applications doivent gérer un certain nombre de détails délicats pour utiliser avec succès des appareils de type palette. Étant donné que les programmes en mode d’index de couleurs n’utilisent pas de palette matérielle, ils sont plus difficiles à utiliser avec les périphériques de couleurs vraies que les programmes utilisant le mode RVBA.

 

 




