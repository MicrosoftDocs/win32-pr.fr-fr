---
description: Les données alpha peuvent être fournies dans les données de vertex. Pour activer le vertex alpha, définissez D3DRS \_ DIFFUSEMATERIALSOURCE sur D3DMCS \_ COLOR1 afin que le runtime Direct3D prenne la valeur diffuse à partir de la couleur diffuse plutôt que du matériau.
ms.assetid: 2b0d842d-ee7d-4633-846d-96697153adc7
title: Vertex alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2443b14d62698e342b7cbb9c4b79d30d3e11e32be76a3f584823ddf74b16685
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984539"
---
# <a name="vertex-alpha-direct3d-9"></a>Vertex alpha (Direct3D 9)

Les données alpha peuvent être fournies dans les données de vertex. Pour activer le vertex alpha, définissez D3DRS \_ DIFFUSEMATERIALSOURCE sur D3DMCS \_ COLOR1 afin que le runtime Direct3D prenne la valeur diffuse à partir de la couleur diffuse plutôt que du matériau.


```
m_pd3dDevice->SetRenderState( D3DRS_DIFFUSEMATERIALSOURCE,  
                                D3DMCS_COLOR1 );
```



Ensuite, fournissez des valeurs alpha dans la couleur diffuse. La fonction AddAlphaToASphere ajoute des caractères alpha aux sommets d’une sphère. Voici un exemple de la façon de fournir les informations alpha à la fonction.


```
AddAlphaToASphere( m_pObstacleVertices, 12,  
                    D3DRGBA(light.dcvDiffuse.r, light.dcvDiffuse.g, 
                            light.dcvDiffuse.b, vAlpha ));
```



Voici à quoi ressemble la fonction.


```
 
void AddAlphaToASphere(D3DLVERTEX* pVertices, DWORD dwNumRings, D3DCOLOR lightcolor)
{
    WORD x, y;
    // rings around
    for( y=0; y < dwNumRings; y++ )
        for( x=0; x < (dwNumRings*2)+1; x++ )
            (pVertices++)->color = lightcolor;

    // top and bottom
    (pVertices++)->color = lightcolor;
    (pVertices++)->color = lightcolor;
}
```



AddAlphaToASphere modifie simplement le membre de couleur de chaque vertex, qui sont de type D3DLVERTEX, pour inclure les informations alpha.

D3DLVERTEX ressemble à ceci.


```
 
// Lit vertex
typedef struct {
    D3DVALUE x, y, z;
    DWORD dwReserved;
    D3DCOLOR color, specular;
    D3DVALUE tu, tv;
} D3DLVERTEX, *LPD3DLVERTEX;
```



Dessin de la sphère,


```
#define D3DFVF_LVERTEX ( D3DFVF_XYZ | D3DFVF_DIFFUSE | D3DFVF_SPECULAR | \
                        D3DFVF_TEX0 )

//...

// Draw the lit sphere
m_pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, D3DFVF_LVERTEX,
                                    m_pObstacleVertices, m_dwNumObstacleVertices,
                                    m_pObstacleIndices,  m_dwNumObstacleIndices, 0 );
```



produit une sphère transparente à l’aide du vertex alpha.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion alpha](alpha-blending.md)
</dt> </dl>

 

 



