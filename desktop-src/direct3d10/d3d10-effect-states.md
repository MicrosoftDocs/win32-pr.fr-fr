---
description: Les États d’effet sont des paires nom-valeur sous la forme d’une expression.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Groupes d’états d’effet (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4617f786b984c96b271600e05b3ea8da9b5701fd
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335567"
---
# <a name="effect-state-groups-direct3d-10"></a>Groupes d’états d’effet (Direct3D 10)

Les États d’effet sont des paires nom-valeur sous la forme d’une expression.

## <a name="blend-state"></a>État de fusion

| État de l’effet | Groupe |
|-|-|
| **ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK** | Membres de [ **D3D10 \_ Blend \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) |

## <a name="depth-and-stencil-state"></a>État de la profondeur et du stencil

| État de l’effet| Groupe |
|-|-|
| **DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK** | Membres de la [ **\_ Description du \_ stencil \_ de profondeur D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |
| **FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC** | Membre de [ **D3D10 \_ Depth \_ STENCILOP \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc) |

## <a name="rasterizer-state"></a>État du rastériseur

| État de l’effet| Groupe |
|-|-|
| FILLMODE | [**\_Mode de remplissage D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| CULLMODE | [**\_Mode d’élimination D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| **FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE** | Membres de [ **D3D10 \_ rastériseur \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc) |

## <a name="sampler-state"></a>État de l’échantillonneur

| État de l’effet | Groupe |
|-|-|
| **Filter**,  **adAddressW**, **AddressV**,, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD** | Membres de l' [ **\_ échantillonneur D3D10 \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) |

Pour obtenir des exemples, consultez [type d’échantillonneur (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) .

## <a name="effect-object-state"></a>État de l’objet d’effet

| Cet objet Effect | Correspond à |
|-|-|
| RASTERIZERSTATE | Objet d’état de l' [État du rastériseur](#rasterizer-state) . |
| DEPTHSTENCILSTATE | Objet d’état de [profondeur et](#depth-and-stencil-state) d’état de gabarit. |
| BLENDSTATE | Objet d’état de l' [État de fusion](#blend-state) . |
| VERTEXSHADER | Objet de nuanceur de sommets compilé. |
| PIXELSHADER | Objet de nuanceur de pixels compilé. |
| GEOMETRYSHADER | Objet de nuanceur Geometry compilé. |
| DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK | Membres de [**D3D10 \_ Pass \_ desc**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc). |

## <a name="defining-and-using-state-objects"></a>Définition et utilisation d’objets d’État

Les objets d’État sont déclarés dans des fichiers FX au format suivant. *StateObjectType* est l’un des États indiqués ci-dessus, et *MemberName* est le nom d’un membre qui aura une valeur non définie par défaut.

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

Par exemple, pour configurer un objet d’état de fusion avec AlphaToCoverageEnable et BlendEnable \[ 0 ayant \] la valeur **false**, le code suivant est utilisé.

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

L’objet d’État est appliqué à une technique Pass à l’aide de l’une des fonctions SetStateGroup décrites dans syntaxe de la [technique Effect (Direct3D 10)](d3d10-effect-technique-syntax.md). Par exemple, pour appliquer l’objet BlendState décrit ci-dessus, vous devez utiliser le code suivant.

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

Pour obtenir un didacticiel décrivant l’utilisation des États, consultez Gestion de l' [État](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).

## <a name="related-topics"></a>Rubriques connexes

* [Syntaxe de la technique Effect](d3d10-effect-technique-syntax.md)
* [Format d’effet (Direct3D 10)](d3d10-effect-format.md)
