---
title: Lecture des valeurs de couleur à partir du trame
description: Lorsque vous utilisez des fonctions qui lisent les valeurs de couleur à partir du trame, n’oubliez pas les différences entre la lecture des valeurs RVBA et des valeurs d’index de couleurs sur les périphériques à couleurs vraies et sur les périphériques basés sur la palette.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL sur Windows, lecture des valeurs de couleur à partir de framebuffers
- lecture des valeurs de couleur à partir de framebuffers OpenGL
- framebuffers, lecture des valeurs de couleur OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65beb6dae04019637fc8683220ce12e671c4a52d4f015ae9f8d45e70db67bb36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794766"
---
# <a name="reading-color-values-from-the-framebuffer"></a>Lecture des valeurs de couleur à partir du trame

Lorsque vous utilisez des fonctions qui lisent les valeurs de couleur à partir du trame, n’oubliez pas les différences entre la lecture des valeurs RVBA et des valeurs d’index de couleurs sur les périphériques à couleurs vraies et sur les périphériques basés sur la palette.

Sur un appareil de couleur vraies :

-   Les valeurs RVBA sont limitées au canal dans l’appareil.
-   Les valeurs d’index de couleurs sont stockées sous forme de valeurs RVBA dans le trame. Lorsque vous utilisez ces valeurs, vous devez effectuer une translation inverse de RVBA à l’index de palette logique. Si deux index logiques ont les mêmes valeurs RVBA, un index incorrect peut être retourné.

Sur un appareil basé sur une palette :

-   Les valeurs RVBA sont lues à partir d’un index dans la palette système. L’index logique est obtenu à partir d’une table inverse, et les composants RVBA sont extraits.
-   Les valeurs d’index de couleurs sont lues à partir d’un index dans la palette système et une table inverse est utilisée pour obtenir l’index de palette logique.

 

 




