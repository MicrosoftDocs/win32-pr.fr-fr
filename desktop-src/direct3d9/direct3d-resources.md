---
description: Les ressources sont les textures et les mémoires tampons utilisées pour le rendu d’une scène.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Ressources Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7745318db3d880711ee962edb086996764455ec8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109166"
---
# <a name="direct3d-resources-direct3d-9"></a>Ressources Direct3D (Direct3D 9)

Les ressources sont les textures et les mémoires tampons utilisées pour le rendu d’une scène. Les applications doivent créer, charger, copier et utiliser des ressources. Cette section fournit une brève introduction aux ressources et aux étapes et méthodes utilisées par les applications lors de l’utilisation de ressources.

Toutes les ressources, y compris les ressources Geometry [**IDirect3DIndexBuffer9**](/windows/desktop/api) et [**IDirect3DVertexBuffer9**](/windows/desktop/api), héritent de l’interface [**IDirect3DResource9**](/windows/desktop/api) . Les ressources de texture, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)et [**IDirect3DVolumeTexture9**](/windows/desktop/api), héritent également de l’interface [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) .

-   [Propriétés de ressource (Direct3D 9)](resource-properties.md)
-   [Manipulation des ressources (Direct3D 9)](manipulating-resources.md)
-   [Verrouillage des ressources (Direct3D 9)](locking-resources.md)
-   [Relations entre les ressources (Direct3D 9)](resource-relationships.md)
-   [Gestion des ressources (Direct3D 9)](managing-resources.md)
-   [Ressources gérées par l’application et stratégies d’allocation (Direct3D 9)](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [Mémoires tampons d’index (Direct3D 9)](index-buffers.md)
-   [Mémoires tampons de vertex (Direct3D 9)](vertex-buffers.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en main](getting-started.md)
</dt> </dl>

 

 
