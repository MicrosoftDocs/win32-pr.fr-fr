---
description: En mode d’ombrage plat, la pyramide suivante s’affiche avec un bord aigu entre les faces adjacentes. Toutefois, en mode d’ombrage Gouraud, les valeurs d’ombrage sont interpolées à travers la périphérie, et l’apparence finale est celle d’une surface incurvée.
ms.assetid: efcaf3f7-b474-4719-adde-10096e296b9f
title: Comparaison des modes d’ombrage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b275f18aa7283a8109db5d6709595cff0ddd09be
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111662"
---
# <a name="comparing-shading-modes-direct3d-9"></a>Comparaison des modes d’ombrage (Direct3D 9)

En mode d’ombrage plat, la pyramide suivante s’affiche avec un bord aigu entre les faces adjacentes. Toutefois, en mode d’ombrage Gouraud, les valeurs d’ombrage sont interpolées à travers la périphérie, et l’apparence finale est celle d’une surface incurvée.

![illustration d’une pyramide avec des bords tranchants et des flèches pointant vers les normales de visage](images/shade2.png)

L’ombrage Gouraud illumine les surfaces plates plus réalistes que l’ombrage plat. Un visage dans le mode d’ombrage plat est une couleur uniforme, mais l’ombrage Gouraud permet à la lumière de tomber dans une face de manière plus appropriée. Cet effet est particulièrement évident s’il existe une source de point proche.

L’ombrage Gouraud lisse les bords nets entre les polygones visibles avec l’ombrage plat. Toutefois, cela peut entraîner des bandes Mach, qui sont des bandes de couleur ou de lumière qui ne sont pas lissées en douceur sur les polygones adjacents. Votre application peut réduire l’apparence des bandes Mach en accroissant le nombre de polygones dans un objet, en renforçant la résolution d’écran ou en renforçant la profondeur de couleur de l’application.

L’ombrage Gouraud peut manquer des détails. Par exemple, dans l’illustration suivante, une vedette est entièrement contenue dans une face de polygone.

![illustration d’une facette dans un polygone](images/gouraud.png)

Dans ce cas, l’ombrage Gouraud, qui interpole entre les sommets, ne manquera pas l’ensemble du projecteur. la face serait rendue comme si la Spotlight n’existait pas.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ombrage](shading.md)
</dt> </dl>

 

 



