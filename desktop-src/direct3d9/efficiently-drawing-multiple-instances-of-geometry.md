---
description: Étant donné une scène qui contient de nombreux objets qui utilisent la même géométrie, vous pouvez dessiner de nombreuses instances de cette géométrie à différentes orientations, tailles, couleurs, et ainsi de meilleures performances en réduisant la quantité de données que vous devez fournir au convertisseur.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Dessin efficace de plusieurs instances de Geometry (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70586142b58076e5010083f61aeff360aa245a298e5d010fb487aed8b5843ec8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122365"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a>Dessin efficace de plusieurs instances de Geometry (Direct3D 9)

Étant donné une scène qui contient de nombreux objets qui utilisent la même géométrie, vous pouvez dessiner de nombreuses instances de cette géométrie à différentes orientations, tailles, couleurs, et ainsi de meilleures performances en réduisant la quantité de données que vous devez fournir au convertisseur.

Pour ce faire, vous pouvez utiliser deux techniques : la première pour dessiner une géométrie indexée et la seconde pour une géométrie non indexée. Les deux techniques utilisent deux mémoires tampons de vertex : une pour fournir les données géométriques et une pour fournir des données d’instance par objet. Les données d’instance peuvent être un large éventail d’informations, telles qu’une transformation, des données de couleur ou des données d’éclairage, en fait tout ce que vous pouvez décrire dans une déclaration de vertex. Le dessin de nombreuses instances de Geometry avec ces techniques peut réduire considérablement la quantité de données envoyées au convertisseur.

-   [Dessin d’une géométrie indexée](#drawing-indexed-geometry)
    -   [Comparaison des performances de la géométrie indexée](#indexed-geometry-performance-comparison)
-   [Dessin de géométrie non indexée](#drawing-non-indexed-geometry)
    -   [Comparaison des performances de la géométrie non indexée](#non-indexed-geometry-performance-comparison)
-   [Rubriques connexes](#related-topics)

## <a name="drawing-indexed-geometry"></a>Dessin d’une géométrie indexée

La mémoire tampon de vertex contient des données par vertex définies par une déclaration de vertex. Supposons que la partie de chaque vertex contient des données géométriques et qu’une partie de chaque vertex contient des données d’instance par objet, comme indiqué dans le diagramme suivant.

![diagramme d’une mémoire tampon de vertex pour une géométrie indexée](images/drawingmultipleinstances.png)

Cette technique nécessite un appareil qui prend en charge le \_ modèle de nuanceur de sommets 3 0. Cette technique fonctionne avec n’importe quel nuanceur programmable, mais pas avec le pipeline de fonctions fixe.

Pour les mémoires tampons de vertex indiquées ci-dessus, Voici les déclarations de mémoire tampon de vertex correspondantes :


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



Ces déclarations définissent deux mémoires tampons de vertex. La première déclaration (pour le flux 0, indiquée par les zéros de la colonne 1) définit les données geometry qui se composent des données de coordonnées : position, normal, tangente, Binormal et texture.

La deuxième déclaration (pour le flux 1, indiquée par celles de la colonne 1) définit les données de l’instance par objet. Chaque instance est définie par 4 4 chiffres à virgule flottante de composant et une couleur à quatre composants. Les quatre premières valeurs peuvent être utilisées pour initialiser une matrice 4x4, ce qui signifie que ces données sont dimensionnées de manière unique, positionnent et font pivoter chaque instance de la géométrie. Les quatre premiers composants utilisent une sémantique de coordonnée de texture qui, dans ce cas, signifie « il s’agit d’un nombre général de quatre composants ». Lorsque vous utilisez des données arbitraires dans une déclaration de vertex, utilisez une sémantique de coordonnée de texture pour la marquer. Le dernier élément du flux est utilisé pour les données de couleur. Cela peut être appliqué au nuanceur de sommets pour attribuer à chaque instance une couleur unique.

Avant le rendu, vous devez appeler [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) pour lier les flux de mémoire tampon de vertex à l’appareil. Voici un exemple qui lie les deux mémoires tampons de vertex :


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) utilise [D3DSTREAMSOURCE \_ INDEXEDDATA](other-direct3d-constants.md) pour identifier les données géométriques indexées. Dans ce cas, le flux 0 contient les données indexées qui décrivent la géométrie de l’objet. Cette valeur est associée logiquement au nombre d’instances de la géométrie à dessiner.

Notez que D3DSTREAMSOURCE \_ INDEXEDDATA et le nombre d’instances à dessiner doivent toujours être définis dans le flux zéro.

Dans le deuxième appel, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) utilise [D3DSTREAMSOURCE \_ INSTANCEDATA](other-direct3d-constants.md) pour identifier le flux contenant les données d’instance. Cette valeur est associée de manière logique à 1, car chaque vertex contient un jeu de données d’instance.

Les deux derniers appels à [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) lient les pointeurs de tampon de vertex à l’appareil.

Lorsque vous avez terminé de restituer les données de l’instance, veillez à réinitialiser la fréquence du flux du vertex à son état par défaut (qui n’utilise pas l’instanciation). Étant donné que cet exemple utilise deux flux, définissez les deux flux comme indiqué ci-dessous :


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a>Comparaison des performances de la géométrie indexée

Bien qu’il ne soit pas possible d’effectuer une seule conclusion sur l’ampleur de cette technique pour réduire le temps de rendu dans chaque application, considérez la différence entre la quantité de données transmises dans le runtime et le nombre de modifications d’État qui seront réduites si vous utilisez la technique d’instanciation. Cette séquence de rendu tire parti du dessin de plusieurs instances de la même géométrie :


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



Notez que la boucle de rendu est appelée une fois, que les données geometry sont diffusées une seule fois, et que n instances sont transmises en continu une seule fois. Cette séquence de rendu suivante est identique dans les fonctionnalités, mais ne tire pas parti de l’instanciation :


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



Notez que l’intégralité de la boucle de rendu est encapsulée par une seconde boucle pour dessiner chaque objet. Désormais, les données géométriques sont diffusées dans le convertisseur n fois (au lieu d’une fois) et tous les États de pipeline peuvent également être définis de manière redondante pour chaque objet dessiné. Cette séquence de rendu est très susceptible d’être beaucoup plus lente. Notez également que les paramètres de [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) n’ont pas changé entre les deux boucles de rendu.

## <a name="drawing-non-indexed-geometry"></a>Dessin de géométrie non indexée

Dans le [dessin de géométrie indexée](#drawing-indexed-geometry), les mémoires tampons de vertex ont été configurées pour dessiner plusieurs instances de géométrie indexée avec une plus grande efficacité. Vous pouvez également utiliser [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) pour dessiner une géométrie non indexée. Cela nécessite une disposition de mémoire tampon de vertex différente et a des contraintes différentes. Pour dessiner une géométrie non indexée, préparez vos mémoires tampons de vertex comme dans le diagramme suivant.

![diagramme d’une mémoire tampon de vertex pour une géométrie non indexée](images/olderstyleinstancing.png)

Cette technique n’est pas prise en charge par l’accélération matérielle sur un appareil. Il est uniquement pris en charge par le traitement du vertex logiciel et ne fonctionne qu’avec les nuanceurs [vs \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) .

Étant donné que cette technique fonctionne avec une géométrie non indexée, il n’y a pas de mémoire tampon d’index. Comme le montre le diagramme, la mémoire tampon de vertex qui contient Geometry contient n copies des données geometry. Pour chaque instance dessinée, les données de géométrie sont lues à partir de la première mémoire tampon de vertex et les données d’instance sont lues à partir de la deuxième mémoire tampon de vertex.

Les déclarations de mémoire tampon de vertex correspondantes sont les suivantes :


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



Ces déclarations sont identiques aux déclarations effectuées dans l’exemple de géométrie indexée. Là encore, la première déclaration (pour Stream 0) définit les données geometry et la deuxième déclaration (pour Stream 1) définit les données d’instance par objet. Lorsque vous créez la première mémoire tampon de vertex, veillez à la charger avec le nombre d’instances des données geometry que vous dessinerez.

Avant le rendu, vous devez configurer le séparateur qui indique au runtime comment diviser la première mémoire tampon vertex en n instances. Définissez ensuite le diviseur à l’aide de [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) comme suit :


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



Le premier appel à [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) indique que le flux 0 contient n instances de m vertex. [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) lie ensuite le flux 0 à la mémoire tampon de vertex Geometry.

Dans le deuxième appel, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifie le flux 1 comme la source des données de l’instance. Le deuxième paramètre est le nombre de vertex dans chaque objet (m). N’oubliez pas que le flux de données de l’instance doit toujours être déclaré comme second flux. [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) lie ensuite le flux 1 à la mémoire tampon de vertex qui contient les données d’instance.

Lorsque vous avez terminé de restituer les données d’instance, veillez à rétablir l’État par défaut de la fréquence du flux de vertex. Étant donné que cet exemple utilise deux flux, définissez les deux flux comme indiqué ci-dessous :


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a>Comparaison des performances de la géométrie non indexée

Le principal avantage de ce style d’instanciation est qu’il peut être utilisé sur une géométrie non indexée. Bien qu’il ne soit pas possible d’effectuer une seule conclusion sur l’ampleur de cette technique pour réduire le temps de rendu dans chaque application, considérez la différence entre la quantité de données transmises dans le runtime et le nombre de modifications d’État qui seront réduites pour la séquence de rendu suivante :


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



Notez que la boucle de rendu est appelée une fois. Les données geometry sont diffusées une seule fois, même si n instances de la géométrie sont diffusées en continu. Les données de la mémoire tampon de vertex d’instance sont diffusées une seule fois. Cette séquence de rendu suivante est identique dans les fonctionnalités, mais ne tire pas parti de l’instanciation :


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



Sans instanciation, la boucle de rendu doit être encapsulée par une seconde boucle pour dessiner chaque objet. En éliminant la deuxième boucle de rendu, vous devez obtenir de meilleures performances en raison de moins de modifications d’état de rendu appelées à l’intérieur de la boucle.

Globalement, il est raisonnable de s’attendre à ce que la technique indexée ([dessin de géométrie indexée](#drawing-indexed-geometry)) soit plus performante que la technique non indexée ([dessinant une géométrie non indexée](#drawing-non-indexed-geometry)), car la technique indexée diffuse uniquement une copie des données geometry. Notez que les paramètres de [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) n’ont pas changé pour l’une des séquences de rendu.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rubriques avancées](advanced-topics.md)
</dt> <dt>

[Exemple d’instanciation](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)
</dt> </dl>

 

 
