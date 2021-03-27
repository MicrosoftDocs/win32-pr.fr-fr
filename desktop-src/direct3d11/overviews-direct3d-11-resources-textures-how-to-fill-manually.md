---
title: Comment initialiser une texture par programmation
description: Cette rubrique contient plusieurs exemples montrant comment initialiser des textures créées avec différents types d’utilisation.
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5584885b885f6026ee32a3e4c52a24aad78c3c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840309"
---
# <a name="how-to-initialize-a-texture-programmatically"></a>Comment : initialiser une texture par programmation

Vous pouvez initialiser une texture pendant la création de l’objet, ou vous pouvez remplir l’objet par programme après sa création. Cette rubrique contient plusieurs exemples montrant comment initialiser des textures créées avec différents types d’utilisation. Cet exemple suppose que vous savez déjà comment [créer une texture](overviews-direct3d-11-resources-textures-create.md).

-   [Utilisation par défaut](#default-usage)
-   [Utilisation dynamique](#dynamic-usage)
-   [Utilisation intermédiaire](#staging-usage)
-   [Rubriques connexes](#related-topics)

## <a name="default-usage"></a>Utilisation par défaut

Le type d’utilisation le plus courant est l’utilisation par défaut. Pour remplir une texture par défaut (une par défaut créée avec **\_ l' \_ utilisation de d3d11**), vous pouvez :

-   Appelez [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) et initialisez *pInitialData* pour pointer vers les données fournies par une application.

    or

-   Après l’appel de [**ID3D11Device :: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), utilisez [**ID3D11DeviceContext :: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) pour remplir la texture par défaut avec les données d’un pointeur fourni par l’application.

## <a name="dynamic-usage"></a>Utilisation dynamique

Pour remplir une texture dynamique (créée avec **\_ l’utilisation \_ dynamique de d3d11**) :

1.  Obtient un pointeur vers la mémoire de texture en passant la valeur d’écriture de la carte de d3d11 lors de l’appel de [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map). **\_ \_ \_**
2.  Écrire des données dans la mémoire.
3.  Appelez [**ID3D11DeviceContext :: DEMAPPAGE**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) lorsque vous avez fini d’écrire des données.

## <a name="staging-usage"></a>Utilisation intermédiaire

Pour remplir une texture intermédiaire (un créé avec **d3d11 \_ usage \_ Staging**) :

1.  Obtient un pointeur vers la mémoire de texture en passant **l' \_ \_ écriture** de la carte de d3d11 lors de l’appel de [**ID3D11DeviceContext :: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).
2.  Écrire des données dans la mémoire.
3.  Appelez [**ID3D11DeviceContext :: DEMAPPAGE**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) lorsque vous avez fini d’écrire des données.

Une texture intermédiaire peut ensuite être utilisée comme paramètre source de [**ID3D11DeviceContext :: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) ou [**ID3D11DeviceContext :: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) pour remplir une ressource par défaut ou dynamique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Textures](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




