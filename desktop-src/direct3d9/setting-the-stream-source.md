---
description: 'La méthode IDirect3DDevice9 :: SetStreamSource lie une mémoire tampon de vertex à un flux de données de périphérique, en créant une association entre les données de vertex et l’un des nombreux ports de flux de données qui alimentent les fonctions de traitement Primitives.'
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Définition de la source de flux (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91bd760b23204de2c6ccd313b164ac7536c7db2d3e2da26d7e40b7d98daa60a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044237"
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

 

 
