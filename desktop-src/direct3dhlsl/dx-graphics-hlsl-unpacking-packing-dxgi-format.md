---
title: DXGI_FORMAT de décompression et d’empaquetage pour la modification d’image In-Place
description: Le \_ fichier D3DX DXGIFormatConvert. inl contient des fonctions de conversion de format Inline que vous pouvez utiliser dans le nuanceur de calcul ou le nuanceur de pixels sur du matériel Direct3D 11.
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c613a3f0068537733961b58a8a4c2b4528d21f25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309577"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a>Décompresser et compresser le \_ format DXGI pour la modification des images In-Place

Le \_ fichier D3DX DXGIFormatConvert. inl contient des fonctions de conversion de format Inline que vous pouvez utiliser dans le nuanceur de calcul ou le nuanceur de pixels sur du matériel Direct3D 11. Vous pouvez utiliser ces fonctions dans votre application pour lire et écrire simultanément dans une texture. Autrement dit, vous pouvez effectuer une modification d’image sur place. Pour utiliser ces fonctions de conversion de format Inline, incluez le \_ fichier D3DX DXGIFormatConvert. inl dans votre application.

La vue d’accès non ordonnée (UAV) de Direct3D 11 d’une ressource Texture1D, Texture2D ou Texture3D prend en charge les lectures et écritures d’accès aléatoires dans la mémoire à partir d’un nuanceur de calcul ou d’un nuanceur de pixels. Toutefois, Direct3D 11 prend en charge simultanément la lecture et l’écriture dans uniquement le \_ format de texture dxgi format \_ R32 \_ uint. Par exemple, Direct3D 11 ne prend pas en charge simultanément la lecture et l’écriture dans d’autres formats plus utiles, tels que le \_ format dxgi \_ R8G8B8A8 \_ UNORM. Vous pouvez utiliser uniquement un UAV pour l’accès aléatoire en écriture dans de tels formats, ou vous pouvez utiliser uniquement un nuanceur Affichage des ressources (SRV) pour accéder de manière aléatoire à la lecture à partir d’autres formats. Le matériel de conversion de format n’est pas disponible pour la lecture et l’écriture simultanées dans d’autres formats.

Toutefois, vous pouvez toujours simultanément lire et écrire dans ces autres formats en convertissant la texture au format de texture DXGI \_ format \_ R32 \_ uint lorsque vous créez un UAV, à condition que le format d’origine de la ressource prenne en charge le cast au \_ format dxgi \_ R32 \_ uint. La plupart des formats d’élément de 32 bits prennent en charge la conversion au \_ format dxgi \_ R32 \_ uint. En effectuant un cast de la texture au \_ format de texture dxgi format \_ R32 \_ uint lorsque vous créez un UAV, vous pouvez effectuer des lectures et des écritures simultanées dans la texture tant que le nuanceur effectue une décompression de format manuel lors de la lecture et de l’empaquetage en écriture.

L’avantage de la conversion de la texture au \_ format de texture dxgi au format \_ R32 \_ uint est que, par la suite, vous pouvez utiliser le format approprié (par exemple, DXGI \_ format \_ R16G16 \_ float) avec d’autres vues sur la même texture, telles que les vues de cible de rendu (RTVs) ou SRVs. Par conséquent, le matériel peut effectuer le DÉCOMPRESSION et l’empaquetage standard du format automatique, peut effectuer un filtrage de texture, et ainsi de suite lorsqu’il n’existe aucune limitation matérielle.

Dans le scénario suivant, une application doit effectuer la séquence d’actions suivante pour effectuer une modification d’image sur place.

Supposons que vous souhaitiez créer une texture sur laquelle vous pouvez utiliser un nuanceur de pixels ou un nuanceur de calcul pour effectuer une modification sur place, et que vous souhaitez que les données de texture soient stockées dans un format qui est un descendant de l’un des formats non TYPÉs suivants :

-   DXGI \_ format \_ R10G10B10A2 non \_ typé
-   DXGI \_ format \_ R8G8B8A8 non \_ typé
-   DXGI \_ format \_ B8G8R8A8 non \_ typé
-   DXGI \_ format \_ B8G8R8X8 non \_ typé
-   DXGI \_ format \_ R16G16 non \_ typé

Par exemple, le format \_ dxgi \_ R10G10B10A2 \_ UNORM est un descendant du format dxgi \_ \_ R10G10B10A2 \_ type. Par conséquent, \_ le format dxgi \_ R10G10B10A2 \_ UNORM prend en charge le modèle d’utilisation décrit dans l’ordre suivant. Les formats qui descendent du \_ format dxgi \_ R32 \_ sans type, comme dxgi \_ format \_ R32 \_ float, sont pris en charge de manière triviale, sans nécessiter l’aide de conversion de format décrite dans l’ordre suivant.

**Pour effectuer une modification d’image sur place**

1.  Créez une texture avec le format approprié sans TYPE, qui est spécifié dans le scénario précédent avec les indicateurs de liaison requis, par exemple D3D11 \_ lier les \_ ressources d’accès non trié \_ \| d3d11 \_ lier le \_ nuanceur \_ .
2.  Pour la modification d’image sur place, créez un UAV avec le \_ \_ format dxgi R32 \_ uint. En général, l’API Direct3D 11 n’autorise pas la conversion entre des familles de format différentes. Toutefois, l’API Direct3D 11 fait une exception avec le format \_ dxgi \_ R32 \_ uint.
3.  Dans le nuanceur de calcul ou le nuanceur de pixels, utilisez les fonctions de Pack de format inline et de décompression appropriées fournies dans le \_ fichier D3DX DXGIFormatConvert. inl. Par exemple, supposons que le \_ format dxgi \_ R32 \_ uint UAV de la texture contienne vraiment les \_ données au format dxgi R10G10B10A2 UNORM \_ \_ . Une fois que l’application a lu un uint à partir du UAV dans le nuanceur, elle doit appeler la fonction suivante pour décompresser le format de la texture :

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    Ensuite, pour écrire dans le UAV dans le même nuanceur, l’application appelle la fonction suivante pour empaqueter les données de nuanceur dans un uint que l’application peut écrire dans le UAV :

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  L’application peut ensuite créer d’autres vues, telles que SRVs, avec le format requis. Par exemple, l’application peut créer un SRV avec le format \_ dxgi \_ R10G10B10A2 \_ UNORM si la ressource a été créée en tant que \_ format dxgi R10G10B10A2 sans \_ \_ type. Lorsqu’un nuanceur accède à ce SRV, le matériel peut effectuer une conversion automatique de type comme d’habitude.

> [!Note]  
> Si le nuanceur doit écrire uniquement dans un UAV ou être lu en tant que SRV, aucune de ces tâches de conversion n’est nécessaire, car vous pouvez utiliser UAVs ou SRVs entièrement typé. Les fonctions de conversion de format fournies dans D3DX \_ DXGIFormatConvert. inl sont potentiellement utiles uniquement si vous souhaitez effectuer des opérations de lecture et d’écriture simultanées dans le UAV d’une texture.

 

La liste suivante répertorie les fonctions de conversion de format incluses dans le \_ fichier D3DX DXGIFormatConvert. inl. Ces fonctions sont classées par le \_ format dxgi qu’elles décompressent et compressent. Chacun des formats pris en charge descend de l’un des formats non TYPÉs listés dans le scénario précédent et prend en charge le casting au \_ format dxgi \_ R32 \_ uint en tant que UAV.

<dl> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI \_ format \_ R10G10B10A2 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI \_ format \_ R10G10B10A2 \_ uint
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI \_ format \_ R8G8B8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI \_ format \_ R8G8B8A8 \_ UNORM \_ sRVB
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> La \_ fonction inexact-type utilise des instructions de nuanceur qui n’ont pas une précision suffisamment élevée pour fournir la réponse exacte. La fonction alternative utilise une table de recherche stockée dans le nuanceur pour fournir une conversion de virgule flottante en SRGB >exacte.

 

</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI \_ format \_ R8G8B8A8 \_ uint
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>\_Format dxgi \_ R8G8B8A8 \_ ronfler
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>\_Format dxgi \_ R8G8B8A8 \_ Saint-
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI \_ format \_ B8G8R8A8 \_ UNORM
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI \_ format \_ B8G8R8A8 \_ UNORM \_ sRVB
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> La \_ fonction inexact-type utilise des instructions de nuanceur qui n’ont pas une précision suffisamment élevée pour fournir la réponse exacte. La fonction alternative utilise une table de recherche stockée dans le nuanceur pour fournir une conversion de virgule flottante en SRGB >exacte.

 

</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI \_ format \_ B8G8R8X8 \_ UNORM
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI \_ format \_ B8G8R8X8 \_ UNORM \_ sRVB
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> La \_ fonction inexact-type utilise des instructions de nuanceur qui n’ont pas une précision suffisamment élevée pour fournir la réponse exacte. La fonction alternative utilise une table de recherche stockée dans le nuanceur pour fournir une conversion de virgule flottante en SRGB >exacte.

 

</dd> <dt>

<span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI \_ format \_ R16G16 \_ float
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI \_ format \_ R16G16 \_ UNORM
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI \_ format \_ R16G16 \_ uint
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>\_Format dxgi \_ R16G16 \_ ronfler
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>\_Format dxgi \_ R16G16 \_ Saint-
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




