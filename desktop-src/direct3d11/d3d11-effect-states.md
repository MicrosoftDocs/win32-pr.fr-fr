---
title: Groupes d’état des effets (Direct3D 11)
description: Les États d’effet sont des paires nom-valeur sous la forme d’une expression.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- effet, groupes d’États (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58def71b6362706eb831129b1d222ef3d1cc9341
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941018"
---
# <a name="effect-state-groups-direct3d-11"></a>Groupes d’état des effets (Direct3D 11)

Les États d’effet sont des paires nom-valeur sous la forme d’une expression.

-   [État de fusion](#blend-state)
-   [État de la profondeur et du stencil](#depth-and-stencil-state)
-   [État du rastériseur](#rasterizer-state)
-   [État de l’échantillonneur](#sampler-state)
-   [État de l’objet d’effet](#effect-object-state)
-   [Définition et utilisation d’objets d’État](#defining-and-using-state-objects)
-   [Rubriques connexes](#related-topics)

## <a name="blend-state"></a>État de fusion



|                                                                                                                       |                                                           |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK | Membres de [ **d3d11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) |



 

## <a name="depth-and-stencil-state"></a>État de la profondeur et du stencil



|                                                                                                                                                                |                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK                                                                                 | Membres de la [ **\_ Description du \_ stencil \_ de profondeur d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)    |
| FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC | Membre de [ **d3d11 \_ Depth \_ STENCILOP \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc) |



 

## <a name="rasterizer-state"></a>État du rastériseur



|                                                                                                                                 |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| FILLMODE                                                                                                                        | [**\_Mode de remplissage d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| CULLMODE                                                                                                                        | [**\_Mode d’élimination d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE | Membres de [ **d3d11 \_ rastériseur \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc) |



 

## <a name="sampler-state"></a>État de l’échantillonneur



|                                                                                                     |                                                               |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Filtre d’adresse AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD | Membres de l' [ **\_ échantillonneur d3d11 \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc) |



 

Pour obtenir des exemples, consultez [type d’échantillonneur (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) .

## <a name="effect-object-state"></a>État de l’objet d’effet



| Cet objet Effect                          | Correspond à                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| RASTERIZERSTATE                             | Objet d’état de l' [État du rastériseur](#rasterizer-state) .               |
| DEPTHSTENCILSTATE                           | Objet d’état de [profondeur et](#depth-and-stencil-state) d’état de gabarit. |
| BLENDSTATE                                  | Objet d’état de l' [État de fusion](#blend-state) .                         |
| VERTEXSHADER                                | Objet de nuanceur de sommets compilé.                                    |
| PIXELSHADER                                 | Objet de nuanceur de pixels compilé.                                     |
| GEOMETRYSHADER                              | Objet de nuanceur Geometry compilé.                                  |
| DS \_ STENCILREFAB \_ BLENDFACTORAB \_ SAMPLEMASK | Membres de [**D3DX11 \_ Pass \_ desc**](d3dx11-pass-desc.md).          |



 

## <a name="defining-and-using-state-objects"></a>Définition et utilisation d’objets d’État

Les objets d’État sont déclarés dans des fichiers FX au format suivant. StateObjectType est l’un des États listés ci-dessus et MemberName est le nom d’un membre qui aura une valeur non définie par défaut.


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



Par exemple, pour configurer un objet d’état de fusion avec AlphaToCoverageEnable et BlendEnable \[ 0 ayant \] la valeur **false** , le code suivant est utilisé.


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



L’objet d’État est appliqué à une technique Pass à l’aide de l’une des fonctions SetStateGroup décrites dans syntaxe de la [technique Effect (Direct3D 11)](d3d11-effect-technique-syntax.md). Par exemple, pour appliquer l’objet BlendState décrit ci-dessus, vous devez utiliser le code suivant.


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Syntaxe de la technique Effect](d3d11-effect-technique-syntax.md)
</dt> <dt>

[Format d’effet (Direct3D 11)](d3d11-effect-format.md)
</dt> </dl>

 

 