---
description: La discussion sur la transformation universelle présente les concepts de base et fournit des détails sur la configuration d’une transformation universelle.
ms.assetid: c3d3b247-e482-4750-a6fb-724f81ee2b19
title: Transformation universelle (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e192f8ce4350c767122ef60f3cd36777753d2e22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392415"
---
# <a name="world-transform-direct3d-9"></a>Transformation universelle (Direct3D 9)

La discussion sur la transformation universelle présente les concepts de base et fournit des détails sur la configuration d’une transformation universelle.

## <a name="what-is-a-world-transform"></a>Qu’est-ce qu’une transformation universelle ?

Une transformation universelle change les coordonnées de l’espace de modèle, où les vertex sont définis par rapport à l’origine locale d’un modèle, à l’espace universel, où les vertex sont définis par rapport à une origine commune à tous les objets d’une scène. En résumé, la transformation universelle place un modèle dans le monde entier. donc son nom. Le diagramme suivant montre la relation entre le système de coordonnées universelles et le système de coordonnées local d’un modèle.

![diagramme de la relation entre les coordonnées universelles et les coordonnées locales](images/worldcrd.png)

La transformation universelle peut inclure n’importe quelle combinaison de traductions, de rotations et de mises à l’échelle.

## <a name="setting-up-a-world-matrix"></a>Configuration d’une matrice mondiale

Comme pour toute autre transformation, créez la transformation universelle en concaténant une série de matrices dans une matrice unique qui contient la somme totale de leurs effets. Dans le cas le plus simple, lorsqu’un modèle est à l’origine mondiale et que ses axes de coordonnées locales sont orientés de la même façon que l’espace universel, la matrice universelle est la matrice d’identité. Plus généralement, la matrice universelle est une combinaison d’une traduction en espace universel et éventuellement d’une ou plusieurs rotations pour transformer le modèle en fonction des besoins.

L’exemple suivant, issu d’une classe de modèle 3D fictive écrite en C++, utilise les fonctions d’assistance incluses dans la bibliothèque de l’utilitaire D3DX pour créer une matrice universelle qui inclut trois rotations pour orienter un modèle et une translation pour le déplacer par rapport à sa position dans l’espace universel.


```
/*
 * For the purposes of this example, the following variables
 * are assumed to be valid and initialized.
 *
 * The m_xPos, m_yPos, m_zPos variables contain the model's
 * location in world coordinates.
 *
 * The m_fPitch, m_fYaw, and m_fRoll variables are floats that 
 * contain the model's orientation in terms of pitch, yaw, and roll
 * angles, in radians.
 */
 
void C3DModel::MakeWorldMatrix( D3DXMATRIX* pMatWorld )
{
    D3DXMATRIX MatTemp;  // Temp matrix for rotations.
    D3DXMATRIX MatRot;   // Final rotation matrix, applied to 
                         // pMatWorld.
 
    // Using the left-to-right order of matrix concatenation,
    // apply the translation to the object's world position
    // before applying the rotations.
    D3DXMatrixTranslation(pMatWorld, m_xPos, m_yPos, m_zPos);
    D3DXMatrixIdentity(&MatRot);

    // Now, apply the orientation variables to the world matrix
    if(m_fPitch || m_fYaw || m_fRoll) {
        // Produce and combine the rotation matrices.
        D3DXMatrixRotationX(&MatTemp, m_fPitch);         // Pitch
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationY(&MatTemp, m_fYaw);           // Yaw
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
        D3DXMatrixRotationZ(&MatTemp, m_fRoll);          // Roll
        D3DXMatrixMultiply(&MatRot, &MatRot, &MatTemp);
 
        // Apply the rotation matrices to complete the world matrix.
        D3DXMatrixMultiply(pMatWorld, &MatRot, pMatWorld);
    }
}
```



Après avoir préparé la matrice universelle, appelez la méthode [**IDirect3DDevice9 :: setTransform**](/windows/desktop/api) pour la définir, en spécifiant la macro [**D3DTS \_ World**](d3dts-world.md) pour le premier paramètre.

> [!Note]  
> Direct3D utilise les matrices universelles et de vue que vous avez définies pour configurer plusieurs structures de données internes. Chaque fois que vous définissez une nouvelle matrice de monde ou d’affichage, le système recalcule les structures internes associées. La définition fréquente de ces matrices, par exemple, des milliers de fois par trame, prend beaucoup de temps. Vous pouvez réduire le nombre de calculs requis en concaténant votre monde et en vue des matrices dans une matrice de vue universelle que vous définissez comme matrice universelle, puis en définissant la matrice de vue sur l’identité. Conservez les copies mises en cache des matrices de monde et de vue individuelles afin de pouvoir modifier, concaténer et réinitialiser la matrice universelle en fonction des besoins. Par souci de clarté, dans cette documentation, les exemples Direct3D utilisent rarement cette optimisation.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transformations](transforms.md)
</dt> </dl>

 

 



