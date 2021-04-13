---
description: Votre application manipule les ressources afin d’afficher une scène.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Manipulation des ressources (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886dfee3af024d103dab8666687f1b053a5fb46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385492"
---
# <a name="manipulating-resources-direct3d-9"></a>Manipulation des ressources (Direct3D 9)

Votre application manipule les ressources afin d’afficher une scène. Tout d’abord, une application doit créer une ressource de texture avec l’une des méthodes suivantes :

-   [**IDirect3DDevice9::CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

Une ressource de texture peut être créée à la place avec l’une des fonctions de texturation D3DXCreatexxx.

Les objets de texture retournés par les méthodes de création de texture sont des conteneurs pour les surfaces ou les volumes ; ces conteneurs sont génériquement appelés mémoires tampons. Les mémoires tampons détenues par la ressource héritent des utilisations, du format et du pool de la ressource, mais ont leur propre type. Pour plus d’informations, consultez [Propriétés des ressources (Direct3D 9)](resource-properties.md).

L’application obtient l’accès aux surfaces contenues, à des fins de chargement d’illustrations, en appelant les méthodes suivantes. Pour plus d’informations, consultez [verrouillage des ressources (Direct3D 9)](locking-resources.md).

-   [**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [**IDirect3DVolumeTexture9 :: LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

Les méthodes Lock acceptent les arguments qui dénotent la surface contenue (par exemple, la face du sous-niveau ou du cube mipmap des pointeurs de texture et de retour aux pixels). L’application typique n’utilise jamais directement un objet surface.

Créez des ressources orientées géométrie en appelant [**IDirect3DDevice9 :: CreateIndexBuffer**](/windows/desktop/api) ou [**IDirect3DDevice9 :: CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).

Verrouillez et remplissez les ressources de mémoire tampon en appelant [**IDirect3DIndexBuffer9 :: Lock**](/windows/desktop/api) ou [**IDirect3DVertexBuffer9 :: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), en fonction de la ressource.

Pour les ressources de texture managée, le processus de création de ressource se termine ici. Pour les ressources de texture non managées, une application promeut des ressources mémoire système vers des ressources accessibles par l’appareil (pour l’accélération matérielle) en appelant [**IDirect3DDevice9 :: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).

Pour présenter des images rendues à partir de ressources, l’application a également besoin de mémoires tampons de stencil de couleur et de profondeur. Pour les applications classiques, la mémoire tampon de couleur appartient à la chaîne de permutation de l’appareil, qui est une collection de surfaces de mémoire tampon d’arrière-plan, et est implicitement créée avec l’appareil. Les surfaces de stencil de profondeur peuvent être créées implicitement ou explicitement créées à l’aide de la méthode [**IDirect3DDevice9 :: CreateDepthStencilSurface**](/windows/desktop/api) . L’application associe un appareil et sa mémoire tampon de profondeur et de couleur à un appel à [**IDirect3DDevice9 :: SetRenderTarget**](/windows/desktop/api) ou [**IDirect3DDevice9 :: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).

Pour plus d’informations sur la présentation de l’image finale, consultez [présentation d’une scène (Direct3D 9)](presenting-a-scene.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
