---
title: Coordonnées de texture générées automatiquement (Direct3D 9)
description: Le système peut utiliser la position transformée de l’espace de caméra ou la normale d’un vertex comme coordonnées de texture, ou il peut calculer les trois vecteurs d’éléments utilisés pour adresser une carte d’environnement cubique.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa4354002c920f73667f97de9a4185579a8c4c7b4563aebf1f3328753c88d01
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608009"
---
# <a name="auto-generated-texture-coordinates-direct3d-9"></a>Coordonnées de texture générées automatiquement (Direct3D 9)

Le système peut utiliser la position transformée de l’espace de caméra ou la normale d’un vertex comme coordonnées de texture, ou il peut calculer les trois vecteurs d’éléments utilisés pour adresser une carte d’environnement cubique. À l’instar des coordonnées de texture que vous spécifiez explicitement dans un vertex, vous pouvez utiliser des coordonnées de texture générées automatiquement comme entrée pour les transformations de coordonnées de texture.

Les coordonnées de texture générées automatiquement peuvent réduire considérablement la bande passante requise pour les données géométriques en éliminant le besoin de coordonnées de texture explicites au format de vertex. Dans de nombreux cas, les coordonnées de texture générées par le système peuvent être utilisées avec les transformations pour produire des effets spéciaux. Bien entendu, il s’agit d’une fonctionnalité spéciale, qui vous permet d’utiliser des coordonnées de texture explicites pour de nombreuses occasions.

## <a name="configuring-automatically-generated-texture-coordinates"></a>Configuration des coordonnées de texture générées automatiquement

En C++, l' \_ État D3DTSS TEXCOORDINDEX texture-stage (à partir du type énuméré [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) ) contrôle la façon dont le système génère des coordonnées de texture.

Normalement, cet État indique au système d’utiliser un ensemble particulier de coordonnées de texture encodées au format de vertex. Lorsque vous incluez les \_ indicateurs D3DTSS TCI \_ CAMERASPACENORMAL, D3DTSS \_ TCI \_ CAMERASPACEPOSITION ou D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR dans la valeur que vous affectez à cet État, le comportement système est assez différent. Si l’un de ces indicateurs est présent, l’étape de texture ignore les coordonnées de texture dans le format de vertex en faveur des coordonnées générées par le système. La signification de chaque indicateur est indiquée dans la liste suivante.

-   D3DTSS \_ TCI \_ CAMERASPACENORMAL

    Utilisez la normale du vertex, transformée en espace de caméra, en tant que coordonnées de texture d’entrée.

-   D3DTSS \_ TCI \_ CAMERASPACEPOSITION

    Utilisez la position du vertex, transformée en espace de caméra, comme coordonnées de texture d’entrée.

-   D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR

    Utilisez le vecteur de réflexion, transformé en espace de caméra, en coordonnées de texture d’entrée. Le vecteur de réflexion est calculé à partir de la position du vertex d’entrée et du vecteur normal.

Les indicateurs d’index de la coordonnée de texture s’excluent mutuellement. Cet exemple utilise :

-   Position du vertex (dans l’espace de caméra) comme coordonnées de texture d’entrée pour cette étape de texture
-   Mode de renvoi à la ligne défini dans l' \_ État de rendu D3DRENDERSTATE WRAP1


```
// Assume d3dDevice is a valid pointer to an IDirect3DDevice9 interface
d3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 
                                   D3DTSS_TCI_CAMERASPACEPOSITION | 1);
```



Les coordonnées de texture générées automatiquement sont particulièrement utiles comme valeurs d’entrée pour une transformation de coordonnée de texture, ou pour éliminer la nécessité pour votre application de calculer des vecteurs à trois éléments pour les mappages d’environnements cubiques.

Sphere-Mapping utilise une carte de texture précalculée (au moment du modèle) qui contient l’environnement entier tel qu’il est reflété par une sphère chrome. Direct3D a une fonctionnalité de génération de coordonnée de texture utilisant l’état de rendu D3DTSS \_ TCI \_ CAMERASPACENORMAL, qui prend la normale du vertex dans l’espace de l’appareil photo et le place par le biais d’une transformation de texture pour générer des coordonnées de texture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Traitement des coordonnées de texture](texture-coordinate-processing.md)
</dt> <dt>

[Transformations de coordonnées de texture (Direct3D 9)](texture-coordinate-transformations.md)
</dt> <dt>

[Mappage d’environnement cubique (Direct3D 9)](cubic-environment-mapping.md)
</dt> </dl>

 

 
