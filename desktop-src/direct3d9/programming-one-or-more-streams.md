---
description: Cette section décrit les nuanceurs qui peuvent être utilisés pour le modèle de flux programmable.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programmation d’un ou plusieurs flux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43210823911648ed11227faef44d980b60d0a335
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515905"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a>Programmation d’un ou plusieurs flux (Direct3D 9)

Cette section décrit les nuanceurs qui peuvent être utilisés pour le modèle de flux programmable.

## <a name="using-streams"></a>Utilisation des flux

DirectX 8 a introduit la notion de flux pour lier les données aux registres d’entrée pour une utilisation par les nuanceurs. Un flux est un tableau uniforme de données de composants, où chaque composant se compose d’un ou de plusieurs éléments qui représentent une entité unique telle que la position, la normale, la couleur, etc. Les flux permettent aux graphiques d’effectuer un accès direct à la mémoire à partir de plusieurs mémoires tampons de vertex en parallèle et fournissent également un mappage plus naturel à partir des données d’application. Ils activent également la multitexture triviale plutôt que la multipasse. Considérez-le comme suit :

-   Un vertex est composé de n flux.
-   Un flux est composé de m éléments.
-   Un élément est \[ position, couleur, normal et coordonnée de texture \] .

La méthode [**IDirect3DDevice9 :: SetStreamSource**](/windows/desktop/api) lie une mémoire tampon de vertex à un flux de données de périphérique, en créant une association entre les données de vertex et l’un des nombreux ports de flux de données qui alimentent les fonctions de traitement Primitives. Les références réelles aux données de flux ne se produisent pas tant qu’une méthode de dessin, telle que [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), n’est pas appelée.

Le mappage des éléments de vertex d’entrée aux registres d’entrée de vertex pour les nuanceurs de vertex programmables est défini dans la déclaration de nuanceur, mais les éléments de vertex d’entrée n’ont pas de sémantique spécifique concernant leur utilisation. L’interprétation des éléments de vertex d’entrée est programmée à l’aide des instructions du nuanceur. La fonction de nuanceur de sommets est définie par un tableau d’instructions qui sont appliquées à chaque vertex. Les registres de sortie de vertex sont écrits explicitement dans, à l’aide des instructions de la fonction de nuanceur.

Toutefois, dans le cas présent, il est moins nécessaire d’utiliser le mappage sémantique des éléments aux registres, ainsi que des informations supplémentaires sur la raison de l’utilisation des flux et le problème à résoudre à l’aide de flux. Le principal avantage des flux est qu’ils suppriment les coûts de données de vertex précédemment associés à la multitexturation. Avant les flux, un utilisateur devait dupliquer des jeux de données de vertex pour gérer le cas d’une seule et de plusieurs textures sans éléments de données inutilisés, ou transporter des éléments de données qui seraient inutilisés, sauf dans le cas de la multitexture.

Voici un exemple d’utilisation de deux jeux de données de vertex : un pour une texture unique et un pour la multitexturation.


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



L’alternative consistait à avoir un seul élément vertex qui contenait les deux jeux de coordonnées de texture.


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



Avec ces données de vertex, une seule copie des données de position et de couleur est transportée en mémoire, au détriment de l’acheminement des deux jeux de coordonnées de texture pour le rendu, même dans le cas de la texture unique.

Maintenant que le compromis est clair, les flux fournissent un correctif élégant à ce dilemme. Voici un ensemble de définitions de vertex pour la prise en charge de trois flux : l’un avec la position et la couleur, l’autre avec le premier jeu de coordonnées de texture et l’autre avec le deuxième jeu de coordonnées de texture.


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



La déclaration de vertex se présente comme suit :


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



Créez maintenant l’objet de déclaration de vertex et définissez-le comme indiqué :


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a>Exemples de combinaisons

### <a name="one-stream-diffuse-color"></a>Couleur diffuse d’une diffusion en continu

La déclaration de vertex et les paramètres de flux pour le rendu des couleurs diffuses se présentent comme suit :


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a>Deux flux avec la couleur et la texture

La déclaration de vertex et les paramètres de flux pour le rendu de la texture unique se présentent comme suit :


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a>Deux flux avec des couleurs et deux textures

La déclaration de vertex et les paramètres de flux pour le rendu de plusieurs textures à deux textures se présentent comme suit :


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



Dans tous les cas, l’appel de [**:D IDirect3DDevice9 rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) suivant suffit.


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



Cela montre la flexibilité des flux pour résoudre le problème de la duplication des données/la transmission redondante des données sur le bus (autrement dit, de gaspiller de la bande passante).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclaration de vertex](vertex-declaration.md)
</dt> </dl>

 

 
