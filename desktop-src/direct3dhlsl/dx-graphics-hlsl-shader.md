---
title: Type de nuanceur
description: La syntaxe permettant de déclarer une variable de nuanceur dans un effet a changé de Direct3D 9 à Direct3D 10.
ms.assetid: d24ae9ad-1b3a-4a05-b28b-b6a0583c3da8
keywords:
- Type de nuanceur HLSL
topic_type:
- apiref
api_name:
- Shader Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ca3332c441279d7f9221efe8cfa7638908ddc44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126941163"
---
# <a name="shader-type"></a>Type de nuanceur

La syntaxe permettant de déclarer une variable de nuanceur dans un effet a changé de Direct3D 9 à Direct3D 10.

## <a name="shader-type-for-direct3d-10"></a>Type de nuanceur pour Direct3D 10

Déclarez une variable de nuanceur dans une passe d’effet (dans Direct3D 10) à l’aide de la syntaxe du type de nuanceur :



|                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SetPixelShader** Compile ( **ShaderTarget, ShaderFunction** ); **SetGeometryShader** Compile ( **ShaderTarget, ShaderFunction** ); **SetVertexShader** Compile ( **ShaderTarget, ShaderFunction** ); |



 

### <a name="parameters"></a>Paramètres



| Élément                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SetXXXShader"></span><span id="setxxxshader"></span><span id="SETXXXSHADER"></span>**SetXXXShader**<br/>         | Appel de l’API Direct3D qui crée l’objet Shader. Peut avoir la valeur : **SetPixelShader** ou **SetGeometryShader** ou **SetVertexShader**.<br/>                                                                                                                                                                                                                                                                                                   |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>         | Modèle de nuanceur à compiler. Cela est valide pour toutes les cibles, y compris toutes les cibles Direct3D 9 et les cibles du [modèle de nuanceur 4](dx-graphics-hlsl-sm4.md) : vs \_ 4 \_ 0, GS \_ 4 \_ 0 et PS \_ 4 \_ 0.<br/>                                                                                                                                                                                                                                          |
| <span id="ShaderFunction"></span><span id="shaderfunction"></span><span id="SHADERFUNCTION"></span>**ShaderFunction**<br/> | Chaîne ASCII qui contient le nom de la fonction de point d’entrée du nuanceur ; Il s’agit de la fonction qui commence l’exécution lorsque le nuanceur est appelé. Le (...) représente les arguments du nuanceur ; Ce sont les mêmes arguments que ceux passés à l’API de création de nuanceur : [**VSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshader) ou [**GSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshader) ou [**PSSetShader**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshader).<br/> |



 

### <a name="example"></a>Exemple

Voici un exemple qui crée un nuanceur de sommets et un objet nuanceur de pixels, compilé pour un modèle de nuanceur particulier. Dans l’exemple Direct3D 10, il n’y a aucun nuanceur Geometry, donc le pointeur est défini sur **null**.


```
// Direct3D 10
technique10 Render
{
    pass P0
    {
        SetVertexShader( CompileShader( vs_4_0, VS() ) );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PS() ) );
    }
}
```



## <a name="shader-type-for-direct3d-9"></a>Type de nuanceur pour Direct3D 9

Déclarez une variable de nuanceur dans une passe d’effet (pour Direct3D 9) à l’aide de la syntaxe du type de nuanceur :



|                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------|
| **PixelShader** = compile **ShaderTarget ShaderFunction (...); VertexShader** = compile **ShaderTarget ShaderFunction (...);** |



 

### <a name="parameters"></a>Paramètres



| Élément                                                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="XXXShader"></span><span id="xxxshader"></span><span id="XXXSHADER"></span>**XXXShader**<br/>                                         | Variable de nuanceur, qui représente le nuanceur compilé. Peut avoir la valeur : **PixelShader** ou **VertexShader**.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="ShaderTarget"></span><span id="shadertarget"></span><span id="SHADERTARGET"></span>**ShaderTarget**<br/>                             | [Modèle de nuanceur](dx-graphics-hlsl-models.md) à compiler ; dépend du type de variable de nuanceur.<br/>                                                                                                                                                                                                                                                                                            |
| <span id="ShaderFunction_..._"></span><span id="shaderfunction_..._"></span><span id="SHADERFUNCTION_..._"></span>**ShaderFunction(...)**<br/> | Chaîne ASCII qui contient le nom de la fonction de point d’entrée du nuanceur ; Il s’agit de la fonction qui commence l’exécution lorsque le nuanceur est appelé. Le (...) représente les arguments du nuanceur ; Ce sont les mêmes arguments que ceux passés à l’API de création de nuanceur : [**SetVertexShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) ou [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader).<br/> |



 

### <a name="example"></a>Exemple

Voici un exemple d’objet Vertex Shader et de nuanceur de pixels, compilé pour un modèle de nuanceur particulier.


```
// Direct3D 9
technique RenderSceneWithTexture1Light
{
    pass P0
    {          
        VertexShader = compile vs_2_0 RenderSceneVS( 1, true, true );
        PixelShader  = compile ps_2_0 RenderScenePS( true );
    }
}
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

