---
description: Les cartes d’environnement sphériques, ou cartes de sphère, sont des textures spéciales qui contiennent une image de la scène entourant un objet ou les effets d’éclairage autour de l’objet.
ms.assetid: b4a8defc-876f-4a23-a12e-e7423a1e8f89
title: Mappage d’environnement sphérique (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be4347b71a041aaa8d7057ac2bb7523bfa235fe59f84fe1ba54c54283cd2159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746385"
---
# <a name="spherical-environment-mapping-direct3d-9"></a>Mappage d’environnement sphérique (Direct3D 9)

Les cartes d’environnement sphériques, ou cartes de sphère, sont des textures spéciales qui contiennent une image de la scène entourant un objet ou les effets d’éclairage autour de l’objet. Contrairement aux cartes d’environnement cubiques, les cartes de sphère ne représentent pas directement les environs d’un objet. La rubrique image théière dans le [mappage d’environnement (Direct3D 9)](environment-mapping.md) affiche les effets de réflexion que vous pouvez obtenir avec le mappage de sphère. Une carte de sphère est une représentation 2D de la vue complète de 360 de la scène entourant un objet, comme si elle était placée à l’aide d’un objectif de poisson, comme indiqué dans l’illustration suivante.

![illustration d’une carte de sphère de l’intérieur d’une construction](images/spheremap.png)

## <a name="texture-coordinates-for-spherical-environment-maps"></a>coordonnées de Texture pour l’environnement sphérique Cartes

Les coordonnées de texture que vous spécifiez pour chaque vertex recevant un mappage d’environnement doivent traiter la texture comme une fonction de la distorsion réfléchissante créée par la courbure de la surface. Les applications doivent calculer ces coordonnées de texture pour chaque vertex pour obtenir l’effet souhaité. Une façon simple et efficace de générer des coordonnées de texture utilise le vertex normal comme entrée. Bien que plusieurs méthodes existent, l’équation suivante est courante parmi les applications qui effectuent le mappage d’environnement avec les cartes de sphère.

![équation de coordonnées de texture Computing pour une carte de sphère](images/spheremap-formula.png)

Dans ces formules, vous et v sont les coordonnées de texture calculées, et N<sub>x</sub> et n<sub>y</sub> sont les composants x et y de la normale du vertex de l’espace de caméra. La formule est simple mais efficace. Si le normal a un composant x positif, le point normal est vers la droite, et la coordonnée u est ajustée pour traiter la texture de manière appropriée. De même pour la coordonnée v : positif y indique que le point normal est normal. L’inverse est vrai pour les valeurs négatives de chaque composant.

Si les points normaux se trouvent directement à l’appareil photo, les coordonnées résultantes ne doivent pas recevoir de distorsions. Le décalage + 0,5 vers les deux coordonnées place le point de distorsion zéro au centre de la carte de sphère, et la normale au sommet de (0, 0, z) résout ce point. Cette formule n’est pas prise en compte pour le composant z de la normale, mais les applications qui utilisent la formule peuvent optimiser les calculs en ignorant les vertex avec un normal qui a un élément z positif. Cela fonctionne pour les objets à ombrage constant, car, dans l’espace de l’appareil photo, si les points normaux s’éloignent de l’appareil photo (z positif), le sommet est éliminé lors du rendu de l’objet. Pour les objets ombrés Gouraud, un normal peut pointer à distance de l’appareil photo (x positif) et le triangle contenant le sommet peut encore être visible. Si vous ne Calculez pas et v pour ce vertex, la face peut encore être utilisée, ce qui entraîne un comportement inattendu.

## <a name="applying-spherical-environment-maps"></a>application d’un Cartes d’environnement sphérique

Vous appliquez un mappage d’environnement aux objets de la même façon que pour toute autre texture, en affectant à la texture l’étape de texture appropriée à l’aide de la méthode [**IDirect3DDevice9 :: SetTexture**](/windows/desktop/api) . Définissez le premier paramètre sur l’index de l’étape de texture souhaitée, puis définissez le deuxième paramètre sur l’adresse de l’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) retournée lorsque vous avez créé la texture de la carte d’environnement. Vous pouvez définir les opérations et les arguments de fusion alpha et de couleur si nécessaire pour obtenir les effets de fusion de texture souhaités.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage d’environnement](environment-mapping.md)
</dt> </dl>

 

 
