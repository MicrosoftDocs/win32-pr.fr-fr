---
title: Choix entre le mode RVBA et le mode de Color-Index
description: En général, utilisez le mode RVBA pour vos applications OpenGL. Il offre plus de flexibilité que le mode index des couleurs pour les effets tels que l’ombrage, l’éclairage, le mappage des couleurs, le brouillard, l’anticrénelage et la fusion.
ms.assetid: 13644a7c-bdc6-4dac-ba16-4723c72b15e5
keywords:
- OpenGL sur Windows, mode rvba
- OpenGL sur Windows, mode index des couleurs
- Mode RVBA OpenGL
- mode d’index de couleurs OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa78096369ec9ba01d6e0dcd3d67535a0d368ef7a5018d3679f9f64dcdf74d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554629"
---
# <a name="choosing-between-rgba-and-color-index-mode"></a>Choix entre le mode RVBA et le mode de Color-Index

En général, utilisez le mode RVBA pour vos applications OpenGL. Il offre plus de flexibilité que le mode index des couleurs pour les effets tels que l’ombrage, l’éclairage, le mappage des couleurs, le brouillard, l’anticrénelage et la fusion.

Envisagez d’utiliser le mode d’index des couleurs dans les cas suivants :

-   Si vous disposez d’un nombre limité de bitplanes disponibles ; le mode d’index des couleurs peut produire un ombrage moins grossier que le mode RVBA.
-   Si vous ne vous inquiétez pas de l’utilisation de couleurs « réelles »; par exemple, en utilisant plusieurs couleurs dans une carte topographiques pour désigner des élévations relatives.
-   Lorsque vous déployez une application existante qui utilise largement le mode d’index de couleurs.
-   Lorsque vous souhaitez utiliser l’animation et les effets de la carte des couleurs dans votre application. (Cela n’est pas possible sur les périphériques de couleurs vraies.)

 

 




