---
title: Type de texture
description: Utilisez la syntaxe suivante pour déclarer une variable de texture.
ms.assetid: 54db5432-dab8-4a4d-a4de-93c6fa640535
keywords:
- Type de texture HLSL
topic_type:
- apiref
api_name:
- Texture type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89568dc5cf24af38f916375795eea052c8b39200
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2020
ms.locfileid: "103723985"
---
# <a name="texture-type"></a>Type de texture

Utilisez la syntaxe suivante pour déclarer une variable de texture.

|                |
|----------------|
| **Nom de type ;** |

## <a name="parameters"></a>Paramètres
| Élément                                                                                     | Description                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Entrer**<br/> | L’un des types suivants : texture (non typée, pour la compatibilité descendante), Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, TextureCube. La taille de l’élément doit être contenue dans des quantités de 4 32 bits.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomme**<br/> | Chaîne ASCII qui identifie de façon unique le nom de la variable.<br/>                                                                                                                                                   |
## <a name="remarks"></a>Notes

Il existe trois parties à l’utilisation d’une texture.

1.  Déclaration d’une variable de texture. Cette opération s’effectue à l’aide de la syntaxe indiquée ci-dessus. Par exemple, il s’agit de déclarations valides.

    ```
    texture g_MeshTexture;
    ```

    \- ou -

    ```
    Texture2D g_MeshTexture;
    ```

2.  Déclaration et initialisation d’un objet d’échantillonnage. Cette opération est effectuée avec une syntaxe légèrement différente dans Direct3D 9 et Direct3D 10. Pour plus d’informations sur la syntaxe des objets d’échantillonnage, consultez [type d’échantillonneur (DirectX HLSL)](dx-graphics-hlsl-sampler.md).
3.  Appel d’une fonction de texture dans un nuanceur.

Différences entre Direct3D 9 et Direct3D 10 :

Direct3D 9 utilise des [fonctions de texture intrinsèques](dx-graphics-hlsl-intrinsic-functions.md) pour effectuer des opérations de texture. Cet exemple provient de l' [exemple BasicHLSL](/previous-versions/windows/desktop/bb153287(v%3Dvs.85)) et utilise [tex2D (s, t) (DirectX HLSL)](dx-graphics-hlsl-tex2d.md) pour effectuer l’échantillonnage de texture.

<code>Output.RGBColor = tex2D(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

Direct3D 10 utilise à la place des [objets de texture basés](dx-graphics-hlsl-to-type.md) sur des modèles. Voici un exemple de l’opération de texture équivalente.

<code>Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) * In.Diffuse;</code>

## <a name="see-also"></a>Voir aussi

[Types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
