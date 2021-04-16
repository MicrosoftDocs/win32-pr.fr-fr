---
description: 'La méthode IDirect3DDevice9 :: SetStreamSource lie une mémoire tampon de vertex à un flux de données de périphérique, en créant une association entre les données de vertex et l’un des nombreux ports de flux de données qui alimentent les fonctions de traitement Primitives.'
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Définition de la source de flux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d0c296b79d258be6eee2d683979081673d5d04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521911"
---
# <a name="setting-the-stream-source-direct3d-9"></a>Définition de la source de flux (Direct3D 9)

La méthode [**IDirect3DDevice9 :: SetStreamSource**](/windows/desktop/api) lie une mémoire tampon de vertex à un flux de données de périphérique, en créant une association entre les données de vertex et l’un des nombreux ports de flux de données qui alimentent les fonctions de traitement Primitives. Les références réelles aux données de flux ne se produisent pas tant qu’une méthode de dessin, telle que [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), n’est pas appelée.

Un flux est défini comme un tableau uniforme de données de composants, où chaque composant se compose d’un ou de plusieurs éléments représentant une entité unique, par exemple position, normal, couleur, etc. Le paramètre Stride spécifie la taille du composant, en octets.

Le code suivant illustre la définition de la source de flux et le dessin de son contenu. La \_ variable g pVB est un LPDIRECT3DVERTEXBUFFER9 qui contient des données de vertex.


```
if( SUCCEEDED( g_pd3dDevice->BeginScene() ) )
{
    // Setup the world, view, and projection matrices
    SetupMatrices();

    // Render the vertex buffer contents
    g_pd3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
    g_pd3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
    g_pd3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 1 );

    // End the scene
    g_pd3dDevice->EndScene();
}
```



Pour plus d’informations sur ce code, consultez le didacticiel suivant : [didacticiel 3 : utilisation de matrices](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu des primitives](rendering-primitives.md)
</dt> </dl>

 

 
