---
description: Une ressource de texture est une collection structurée de données.
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: Création de ressources de texture (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950666"
---
# <a name="creating-texture-resources-direct3d-10"></a>Création de ressources de texture (Direct3D 10)

Une ressource de [texture](d3d10-graphics-programming-guide-resources-types.md) est une collection structurée de données. En règle générale, les valeurs de couleur sont stockées dans des textures et sont accessibles pendant le rendu par le [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) à différentes étapes à la fois pour l’entrée et la sortie. La création de textures et la définition de la façon dont elles seront utilisées sont une partie importante du rendu des scènes attrayantes dans Direct3D 10.

Bien que les textures contiennent généralement des informations de couleur, la création de textures à l’aide de différents [**\_ formats de dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) leur permet de stocker différents types de données. Ces données peuvent ensuite être exploitées par le pipeline Direct3D 10 de manière non traditionnelle.

Toutes les textures ont des limites sur la quantité de mémoire qu’elles consomment et le nombre de texels qu’elles contiennent. Ces limites sont spécifiées par des [constantes de ressources](d3d10-graphics-reference-resource-constants.md).

-   [Créer une texture à partir d’un fichier](#create-a-texture-from-a-file)
    -   [Créer une texture et une vue séparément](#create-texture-and-view-separately)
    -   [Créer une texture et une vue simultanément](#create-texture-and-view-simultaneously)
-   [Création de textures vides](#creating-empty-textures)
    -   [Rendu dans une texture](#rendering-to-a-texture)
    -   [Remplissage manuel des textures](#filling-textures-manually)
-   [Plusieurs Rendertargets](#multiple-rendertargets)
-   [Rubriques connexes](#related-topics)

## <a name="create-a-texture-from-a-file"></a>Créer une texture à partir d’un fichier

> [!Note]  
> La [bibliothèque de l’utilitaire D3DX](d3d10-graphics-reference-d3dx10.md) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 

Lorsque vous créez une texture dans Direct3D 10, vous devez également créer une [vue](d3d10-graphics-programming-guide-resources-access-views.md). Une vue est un objet qui indique à l’appareil Comment accéder à une texture pendant le rendu. La méthode la plus courante pour accéder à une texture est de la lire à l’aide d’un [nuanceur](../direct3dhlsl/dx-graphics-hlsl.md). Un affichage des ressources de nuanceur indique à un nuanceur comment lire à partir d’une texture pendant le rendu. Le type de vue qu’une texture utilisera doit être spécifié au moment de sa création.

La création d’une texture et le chargement de ses données initiales peuvent être effectuées de deux manières différentes : créer une texture et une vue séparément, ou créer la texture et la vue en même temps. L’API fournit les deux techniques pour vous permettre de choisir celle qui répond le mieux à vos besoins.

### <a name="create-texture-and-view-separately"></a>Créer une texture et une vue séparément

Le moyen le plus simple de créer une texture est de le charger à partir d’un fichier image. Pour créer la texture, il suffit de remplir une structure et de fournir le nom de la texture à [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



La fonction D3DX [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) effectue trois opérations : tout d’abord, elle crée un objet de texture Direct3D 10. Deuxièmement, il lit le fichier image d’entrée ; Troisièmement, il stocke les données de l’image dans l’objet texture. Dans l’exemple ci-dessus, un fichier BMP est chargé, mais la fonction peut charger divers types de fichiers.

L’indicateur de liaison indique que la texture sera créée en tant que ressource de nuanceur, ce qui permet à une étape du nuanceur de lire à partir de la texture pendant le rendu.

L’exemple ci-dessus ne spécifie pas tous les paramètres de chargement. En fait, il est souvent préférable de simplement réinitialiser les paramètres de chargement, car cela permet à D3DX de choisir des valeurs appropriées en fonction de l’image d’entrée. Si vous souhaitez que l’image d’entrée détermine tous les paramètres avec lesquels la texture est créée, spécifiez simplement la **valeur null** pour le paramètre **loadInfo** comme suit :


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



La spécification de **null** pour les informations de chargement est un raccourci simple mais puissant.

Maintenant qu’une texture a été créée, vous devez créer un affichage des ressources de nuanceur afin que la texture puisse être liée en tant qu’entrée à un nuanceur. Étant donné que [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) retourne un pointeur vers une ressource et non un pointeur vers une texture, vous devez déterminer le type exact de ressource qui a été chargé, puis vous pouvez créer une vue de ressource de nuanceur à l’aide de [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



Bien que l’exemple ci-dessus crée une vue de ressource de nuanceur 2D, le code permettant de créer d’autres types d’affichage des ressources de nuanceur est très similaire. Une étape de nuanceur peut maintenant utiliser cette texture comme entrée.

L’utilisation de [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) et de [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) pour créer une texture et de sa vue associée est une façon de préparer une texture à être liée à une étape de nuanceur. Une autre façon de procéder consiste à créer la texture et sa vue en même temps, ce qui est abordé dans la section suivante.

### <a name="create-texture-and-view-simultaneously"></a>Créer une texture et une vue simultanément

Direct3D 10 nécessite à la fois une texture et une vue de ressource de nuanceur pour lire à partir d’une texture pendant l’exécution. Étant donné que la création d’une texture et d’une vue de la ressource Shader est une tâche courante, D3DX fournit le [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) pour le faire pour vous.


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



Avec un seul appel D3DX, les affichages texture et shader-Resource sont créés. La fonctionnalité du paramètre **loadInfo** est inchangée. vous pouvez l’utiliser pour personnaliser la manière dont la texture est créée, ou dériver les paramètres nécessaires du fichier d’entrée en spécifiant la **valeur null** pour le paramètre **loadInfo** .

L’objet [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) retourné par la fonction [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) peut être utilisé ultérieurement pour récupérer l’interface [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) d’origine, si nécessaire. Pour ce faire, vous pouvez appeler la méthode [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) .

D3DX fournit une fonction unique pour créer une texture et une vue de ressource de nuanceur en tant que convienience. C’est à vous de choisir la méthode de création d’une texture et d’afficher le mieux adapté aux besoins de votre application.

Maintenant que vous savez comment créer une texture et son affichage des ressources de nuanceur, la section suivante vous montre comment vous pouvez échantillonner (Lire) à partir de cette texture à l’aide d’un nuanceur.

## <a name="creating-empty-textures"></a>Création de textures vides

Parfois, les applications veulent créer une texture et calculer les données à stocker dans la texture, ou utiliser le [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) graphique pour effectuer le rendu sur cette texture et utiliser ultérieurement les résultats dans un autre traitement. Ces textures peuvent être mises à jour par le pipeline graphique ou par l’application elle-même, selon le type d' [**utilisation**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) spécifié pour la texture lors de sa création.

### <a name="rendering-to-a-texture"></a>Rendu dans une texture

Le cas le plus courant de la création d’une texture vide à remplir avec des données pendant l’exécution est le cas où une application souhaite effectuer un rendu sur une texture, puis utiliser les résultats de l’opération de rendu dans une passe suivante. Les textures créées à cet effet doivent spécifier [**l’utilisation**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)par défaut.

L’exemple de code suivant crée une texture vide à partir de laquelle le pipeline peut être rendu et utilisé par la suite comme entrée d’un [nuanceur](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



La création de la texture requiert que l’application spécifie des informations sur les propriétés que la texture aura. La largeur et la hauteur de la texture dans texels sont définies sur 256. Pour cette cible de rendu, un seul niveau de mipmap est tout ce dont nous avons besoin. Une seule cible de rendu est nécessaire pour que la taille du tableau soit définie sur 1. Chaque Texel contient des valeurs à virgule flottante 4 32 bits qui peuvent être utilisées pour stocker des informations très précises (consultez le [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). Un échantillon par pixel est tout ce qui sera nécessaire. L’utilisation est définie sur la valeur par défaut, car elle permet l’emplacement le plus efficace de la cible de rendu en mémoire. Enfin, le fait que la texture soit liée en tant que cible de rendu et qu’une ressource de nuanceur à différents moments dans le temps est spécifié.

Les textures ne peuvent pas être liées directement au pipeline ; Utilisez une vue de cible de rendu comme indiqué dans l’exemple de code suivant.


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



Le format de l’affichage de la cible de rendu est simplement défini sur le format de la texture d’origine. Les informations de la ressource doivent être interprétées comme une texture 2D et nous voulons uniquement utiliser le premier niveau de mipmap de la cible de rendu.

De la même façon qu’une vue de cible de rendu doit être créée afin que la cible de rendu puisse être liée pour la sortie au pipeline, une vue de ressource de nuanceur doit être créée afin que la cible de rendu puisse être liée au pipeline en tant qu’entrée. L’exemple de code suivant illustre cela.


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



Les paramètres des descriptions des affichages des ressources de nuanceur sont très similaires à ceux des descriptions de la vue de la cible de rendu et ont été choisis pour les mêmes raisons.

### <a name="filling-textures-manually"></a>Remplissage manuel des textures

Parfois, les applications souhaitent calculer des valeurs au moment de l’exécution, les placer dans une texture manuellement, puis faire en sorte que le [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) graphique utilise cette texture dans les opérations de rendu ultérieures. Pour ce faire, l’application doit créer une texture vide de manière à permettre au processeur d’accéder à la mémoire sous-jacente. Cela s’effectue en créant une texture dynamique et en obtenant l’accès à la mémoire sous-jacente en appelant une méthode particulière. L'exemple de code suivant montre comment procéder.


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



Notez que le format est défini sur 32 bits par pixel, où chaque composant est défini par 8 bits. Le paramètre d’utilisation est défini sur dynamique, tandis que les indicateurs de liaison sont définis pour spécifier que la texture sera accessible par un nuanceur. Le reste de la description de la texture est semblable à la création d’une cible de rendu.

Le [**mappage**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) d’appel permet à l’application d’accéder à la mémoire sous-jacente de la texture. Le pointeur récupéré est ensuite utilisé pour remplir la texture avec les données. Cela peut être observé dans l’exemple de code suivant.


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a>Plusieurs Rendertargets

Jusqu’à huit vues de cible de rendu peuvent être liées au pipeline à la fois (avec [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)). Pour chaque pixel (ou pour chaque échantillon si l’échantillonnage multiple est activé), la fusion est effectuée indépendamment pour chaque affichage de la cible de rendu. Deux des variables d’état de fusion-BlendEnable et RenderTargetWriteMask-sont des tableaux de huit, chaque membre de tableau correspond à une vue de cible de rendu. Quand vous utilisez plusieurs cibles de rendu, chaque cible de rendu doit être du même [type de ressource](d3d10-graphics-programming-guide-resources-types.md) (tampon, texture 1D, tableau de texture 2D, etc.) et doit avoir la même dimension (largeur, hauteur, profondeur pour les textures 3D et taille de tableau pour les tableaux de texture). Si les cibles de rendu sont échantillonnées, elles doivent toutes avoir le même nombre d’échantillons par pixel.

Il ne peut y avoir qu’une seule mémoire tampon de stencil de profondeur active, quel que soit le nombre de cibles de rendu actives. Lorsque vous utilisez des tableaux de texture comme cibles de rendu, toutes les dimensions de vue doivent correspondre. Les cibles de rendu n’ont pas besoin d’avoir le même format de texture.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
