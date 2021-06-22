---
title: Chargement de données de texture dans des mémoires tampons
description: Le chargement de données de texture 2D ou 3D est similaire au chargement de données 1D, à ceci près que les applications doivent être plus particulièrement attentifes à l’alignement des données liées au pas à pas.
ms.assetid: 22A25A94-A45C-482D-853A-FA6860EE7E4E
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72177be1fefbf102e901d28d47413c8bcff41ab
ms.sourcegitcommit: 39754f1af7853adff2525d0936afe9aad2066a9a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/22/2021
ms.locfileid: "112426963"
---
# <a name="uploading-texture-data-through-buffers"></a>Chargement de données de texture dans des mémoires tampons

Le chargement de données de texture 2D ou 3D est similaire au chargement de données 1D, à ceci près que les applications doivent être plus particulièrement attentifes à l’alignement des données liées au pas à pas. Les mémoires tampons peuvent être utilisées de façon orthogonale et simultanée à partir de plusieurs parties du pipeline graphique, et sont très flexibles.

-   [Charger les données de texture via des tampons](#upload-texture-data-via-buffers)
-   [Destination](#copying)
-   [Mappage et annulation du mappage](#mapping-and-unmapping)
-   [Alignement de la mémoire tampon](#buffer-alignment)
-   [Rubriques connexes](#related-topics)

## <a name="upload-texture-data-via-buffers"></a>Charger les données de texture via des tampons

Les applications doivent charger des données via [**ID3D12GraphicsCommandList :: CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) ou [**ID3D12GraphicsCommandList :: CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion). Les données de texture sont plus susceptibles d’être plus volumineuses, accessibles à plusieurs reprises et tirent parti de la cohérence améliorée du cache des dispositions de mémoire non linéaires par rapport aux autres données de ressources. Lorsque les mémoires tampons sont utilisées dans D3D12, les applications disposent d’un contrôle total sur l’emplacement et la disposition des données associées à la copie des données de ressources, à condition que les exigences d’alignement de la mémoire soient respectées.

L’exemple met en évidence l’emplacement où l’application aplatit simplement les données 2D en 1J avant de les placer dans la mémoire tampon. Pour le scénario 2D mipmap, l’application peut aplatir chaque sous-ressource discrètement et rapidement utiliser un algorithme de sous-allocation 1D, ou utiliser une technique de sous-allocation 2D plus complexe pour réduire l’utilisation de la mémoire vidéo. La première technique est censée être utilisée plus souvent, car elle est plus simple. La deuxième technique peut être utile lors de l’empaquetage de données sur un disque ou sur un réseau. Dans les deux cas, l’application doit toujours appeler les API de copie pour chaque sous-ressource.

``` syntax
// Prepare a pBitmap in memory, with bitmapWidth, bitmapHeight, and pixel format of DXGI_FORMAT_B8G8R8A8_UNORM. 
//
// Sub-allocate from the buffer for texture data.
//

D3D12_SUBRESOURCE_FOOTPRINT pitchedDesc = { 0 };
pitchedDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
pitchedDesc.Width = bitmapWidth;
pitchedDesc.Height = bitmapHeight;
pitchedDesc.Depth = 1;
pitchedDesc.RowPitch = Align(bitmapWidth * sizeof(DWORD), D3D12_TEXTURE_DATA_PITCH_ALIGNMENT);

//
// Note that the helper function UpdateSubresource in D3DX12.h, and ID3D12Device::GetCopyableFootprints 
// can help applications fill out D3D12_SUBRESOURCE_FOOTPRINT and D3D12_PLACED_SUBRESOURCE_FOOTPRINT structures.
//
// Refer to the D3D12 Code example for the previous section "Uploading Different Types of Resources"
// for the code for SuballocateFromBuffer.
//

SuballocateFromBuffer(
    pitchedDesc.Height * pitchedDesc.RowPitch,
    D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT
    );

D3D12_PLACED_SUBRESOURCE_FOOTPRINT placedTexture2D = { 0 };
placedTexture2D.Offset = m_pDataCur – m_pDataBegin;
placedTexture2D.Footprint = pitchedDesc;

//
// Copy texture data from DWORD* pBitmap->pixels to the buffer
//

for (UINT y = 0; y < bitmapHeight; y++)
{
  UINT8 *pScan = m_pDataBegin + placedTexture2D.Offset + y * pitchedDesc.RowPitch;
  memcpy( pScan, &(pBitmap->pixels[y * bitmapWidth]), sizeof(DWORD) * bitmapWidth );
}

//
// Create default texture2D resource.
//

D3D12_RESOURCE_DESC  textureDesc { ... };

CComPtr<ID3D12Resource> texture2D;
d3dDevice->CreateCommittedResource( 
        &CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT), 
        D3D12_HEAP_FLAG_NONE, &textureDesc, 
        D3D12_RESOURCE_STATE_COPY_DEST, 
        nullptr, 
        IID_PPV_ARGS(&texture2D) );

//
// Copy heap data to texture2D.
//

commandList->CopyTextureRegion( 
        &CD3DX12_TEXTURE_COPY_LOCATION( texture2D, 0 ), 
        0, 0, 0, 
        &CD3DX12_TEXTURE_COPY_LOCATION( m_spUploadHeap, placedTexture2D ), 
        nullptr );
```

Notez l’utilisation des structures d’assistance [**CD3DX12 les \_ \_ Propriétés du tas**](cd3dx12-heap-properties.md) et l' [**\_ \_ \_ emplacement de copie de texture CD3DX12**](cd3dx12-texture-copy-location.md), ainsi que les méthodes [**CreateCommittedResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommittedresource) et [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion).

## <a name="copying"></a>Copie

Les méthodes D3D12 permettent aux applications de remplacer D3D11 [**UpdateSubresource**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource), [**CopySubresourceRegion**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-copysubresourceregion)et les données initiales des ressources. Une sous-ressource 3D unique de données de texture de ligne principale peut se trouver dans les ressources de la mémoire tampon. [**CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion) peut copier les données de texture de la mémoire tampon vers une ressource de texture avec une disposition de texture inconnue, et vice versa. Les applications doivent préférer ce type de technique pour remplir les ressources GPU fréquemment sollicitées, en créant de grandes mémoires tampons dans un tas de chargement lors de la création des ressources GPU fréquemment utilisées dans un segment de mémoire par défaut qui n’a pas d’accès au processeur. Une telle technique prend en charge efficacement les GPU discrètes et leur grande quantité de mémoire inaccessible par le processeur, sans les architectures UMA les plus courantes.

Notez les deux constantes suivantes :

``` syntax
const UINT D3D12_TEXTURE_DATA_PITCH_ALIGNMENT = 256;
const UINT D3D12_TEXTURE_DATA_PLACEMENT_ALIGNMENT = 512;
```

-   [**Encombrement des sous- \_ ressources D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
-   [**Encombrement des sous- \_ ressources placé par D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint)
-   [**\_Emplacement de \_ copie de texture D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
-   [**\_Type de \_ copie de texture D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_copy_type)
-   [**ID3D12Device :: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**ID3D12CommandQueue::UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings)

## <a name="mapping-and-unmapping"></a>Mappage et annulation du mappage

[**Les**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) mappages et les [**mappages**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) peuvent être appelés par plusieurs threads en toute sécurité. Le premier appel à **Map** alloue une plage d’adresses virtuelles de processeur pour la ressource. Le dernier appel à la valeur de **mappage** libère la plage d’adresses virtuelles de l’UC. L’adresse virtuelle de l’UC est généralement retournée à l’application.

Chaque fois que des données sont transmises entre l’UC et le GPU via des ressources dans des segments de mémoire readback, [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) et [**DEMAPPAGE**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) doivent être utilisés pour prendre en charge tous les systèmes D3D12 est pris en charge sur. Conserver les plages aussi fortes que possible optimise l’efficacité sur les systèmes qui requièrent des plages (consultez la [**\_ page D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)).

Les performances des outils de débogage bénéficient non seulement de l’utilisation précise des plages sur tous les appels de [**mappage de mappage**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map)  /  [](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) , mais également des applications qui démappent les ressources lorsque les modifications de l’UC ne sont plus effectuées.

La méthode D3D11 de l’utilisation de [**Map**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-map) (avec le paramètre de rejet défini) pour renommer des ressources n’est pas prise en charge dans D3D12. Les applications doivent implémenter le changement de nom des ressources. Tous les appels **Map** ne sont IMPLICITement pas des \_ remplacements et des threads multithread. Il incombe à l’application de s’assurer que tout travail GPU approprié contenu dans les listes de commandes est terminé avant l’accès aux données avec le processeur. Les appels D3D12 à **Map** ne vident pas implicitement les mémoires tampons de commande et ne bloquent pas l’attente de la fin du travail du GPU. Par conséquent, le **mappage** et le [**mappage peuvent même**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-unmap) être optimisés dans certains scénarios.

## <a name="buffer-alignment"></a>Alignement de la mémoire tampon

Restrictions d’alignement de mémoire tampon :

-   La copie linéaire des sous-ressources doit être alignée sur 512 octets (avec le pas de la ligne aligné sur les octets d’alignement du pas de \_ données de texture D3D12 \_ \_ \_ ).
-   Les lectures de données constantes doivent être un multiple de 256 octets à partir du début du tas (c’est-à-dire uniquement des adresses qui sont alignées sur 256 octets).
-   Les lectures de données d’index doivent être un multiple de la taille de type de données d’index (c’est-à-dire uniquement à partir d’adresses qui sont naturellement alignées pour les données).
-   Les données [**ID3D12GraphicsCommandList :: ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) doivent provenir de décalages multiples de 4 (c’est-à-dire uniquement à partir d’adresses qui sont alignées sur la valeur DWORD).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Sous-allocation au sein des tampons](large-buffers.md)
</dt> </dl>

 

 
