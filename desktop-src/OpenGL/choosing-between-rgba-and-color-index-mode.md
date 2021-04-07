---
title: Choix entre le mode RVBA et le mode de Color-Index
description: En général, utilisez le mode RVBA pour vos applications OpenGL. Il offre plus de flexibilité que le mode index des couleurs pour les effets tels que l’ombrage, l’éclairage, le mappage des couleurs, le brouillard, l’anticrénelage et la fusion.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL sur Windows, mode RVBA
- OpenGL sur Windows, mode index des couleurs
- Mode RVBA OpenGL
- mode d’index de couleurs OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0368461d6ece7b823a8627f664daace027fd76c9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673149"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a>Choix entre le mode RVBA et le mode de Color-Index

En général, utilisez le mode RVBA pour vos applications OpenGL. Il offre plus de flexibilité que le mode index des couleurs pour les effets tels que l’ombrage, l’éclairage, le mappage des couleurs, le brouillard, l’anticrénelage et la fusion.

Envisagez d’utiliser le mode d’index des couleurs dans les cas suivants :

-   Si vous disposez d’un nombre limité de bitplanes disponibles ; le mode d’index des couleurs peut produire un ombrage moins grossier que le mode RVBA.
-   Si vous ne vous inquiétez pas de l’utilisation de couleurs « réelles »; par exemple, en utilisant plusieurs couleurs dans une carte topographiques pour désigner des élévations relatives.
-   Lorsque vous déployez une application existante qui utilise largement le mode d’index de couleurs.
-   Lorsque vous souhaitez utiliser l’animation et les effets de la carte des couleurs dans votre application. (Cela n’est pas possible sur les périphériques de couleurs vraies.)

 

 




