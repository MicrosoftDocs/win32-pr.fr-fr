---
title: Registre à virgule flottante constante (référence HLSL VS)
description: Registre d’entrée du nuanceur de sommets pour une constante à virgule flottante à quatre composants. Définissez un registre de constante avec Def-vs ou SetVertexShaderConstantF.
ms.assetid: 45a14258-52d5-4c22-885f-5af20ae36251
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c81cc05a40ebb7ede53fb14c957584f289a14a15045a2b69f557072c6885c9ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949929"
---
# <a name="constant-float-register-hlsl-vs-reference"></a>Registre à virgule flottante constante (référence HLSL VS)

Registre d’entrée du nuanceur de sommets pour une constante à virgule flottante à quatre composants. Définissez un registre de constante avec [def-vs](def---vs.md) ou [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf).

Le fichier de registre de constante est en lecture seule du point de vue du nuanceur de sommets. Toute instruction unique ne peut accéder qu’à un seul registre de constantes. Toutefois, chaque source de cette instruction peut Swizzle et inverser ce vecteur au fur et à mesure de sa lecture.

Le comportement des constantes de nuanceur a changé entre Direct3D 8 et Direct3D 9.

-   Pour Direct3D 9, les constantes définies avec defx affectent des valeurs à l’espace constant du nuanceur. La durée de vie d’une constante déclarée avec defx est limitée à l’exécution de ce nuanceur uniquement. À l’inverse, les constantes définies à l’aide des API SetXXXShaderConstantX initialisent des constantes dans l’espace global. Les constantes dans l’espace global ne sont pas copiées dans l’espace local (visible par le nuanceur) tant que SetxxxShaderConstants n’est pas appelé.
-   Pour Direct3D 8, les constantes définies avec defx ou les API attribuent des valeurs à l’espace de constante de nuanceur. Chaque fois que le nuanceur est exécuté, les constantes sont utilisées par le nuanceur actuel, quelle que soit la technique utilisée pour les définir.

Un registre de constante est désigné comme étant absolu ou relatif :


```
c[n]           ; absolute
c[a0.x + n]    ; relative - supported only in version 1_1
```



Le registre de constante peut être lu, par conséquent, soit à l’aide d’un index absolu, soit à l’aide d’un index relatif à partir d’un registre d’adresses. Les lectures à partir des registres hors limites sont retournées (0,0, 0,0, 0,0, 0,0).

## <a name="examples"></a>Exemples

Voici un exemple de déclaration de deux constantes à virgule flottante dans un nuanceur.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Ces constantes sont chargées chaque fois que [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) est appelé.

Voici un exemple d’utilisation de l’API.


```
    // Set up the vertex shader constants.
    {
        D3DXMATRIXA16 mat;
        D3DXMatrixMultiply( &mat, &m_matView, &m_matProj );
        D3DXMatrixTranspose( &mat, &mat );

        D3DXVECTOR4 vA( sinf(m_fTime)*15.0f, 0.0f, 0.5f, 1.0f );
        D3DXVECTOR4 vD( D3DX_PI, 1.0f/(2.0f*D3DX_PI), 2.0f*D3DX_PI, 0.05f );

        // Taylor series coefficients for sin and cos.
        D3DXVECTOR4 vSin( 1.0f, -1.0f/6.0f, 1.0f/120.0f, -1.0f/5040.0f );
        D3DXVECTOR4 vCos( 1.0f, -1.0f/2.0f, 1.0f/ 24.0f, -1.0f/ 720.0f );

        m_pd3dDevice->SetVertexShaderConstantF(  0, (float*)&mat,  4 );
        m_pd3dDevice->SetVertexShaderConstantF(  4, (float*)&vA,   1 );
        m_pd3dDevice->SetVertexShaderConstantF(  7, (float*)&vD,   1 );
        m_pd3dDevice->SetVertexShaderConstantF( 10, (float*)&vSin, 1 );
        m_pd3dDevice->SetVertexShaderConstantF( 11, (float*)&vCos, 1 );
    }
```



Si vous définissez des valeurs constantes avec l’API, aucune déclaration de nuanceur n’est requise.



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|-------|------|------|-------|
| Registre de constante      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 