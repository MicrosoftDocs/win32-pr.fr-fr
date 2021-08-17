---
title: Structure D3DX11_STATE_BLOCK_MASK (D3dx11effect. h)
description: Indique l’état de l’appareil.
ms.assetid: 42044a6d-6a11-4f90-889a-82e7954da6c7
keywords:
- Structure D3DX11_STATE_BLOCK_MASK Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_STATE_BLOCK_MASK
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8087f45ad94fe3e45f78a1be9d86b30f6f7e3f2c9161b9c4498865b12582436e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124934"
---
# <a name="d3dx11_state_block_mask-structure"></a>\_Structure de \_ masque de bloc d’État D3DX11 \_

Indique l’état de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _D3DX11_STATE_BLOCK_MASK {
  BYTE VS;
  BYTE VSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE VSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE VSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE VSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE HS;
  BYTE HSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE HSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE HSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE HSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE DS;
  BYTE DSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE DSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE DSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE DSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE GS;
  BYTE GSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE GSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE GSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE GSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PS;
  BYTE PSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE PSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE PSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE PSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE PSUnorderedAccessViews;
  BYTE CS;
  BYTE CSSamplers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_SAMPLER_SLOT_COUNT)];
  BYTE CSShaderResources[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE CSConstantBuffers[D3DX11_BYTES_FROM_BITS(D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT)];
  BYTE CSInterfaces[D3DX11_BYTES_FROM_BITS(D3D11_SHADER_MAX_INTERFACES)];
  BYTE CSUnorderedAccessViews;
  BYTE IAVertexBuffers[D3DX11_BYTES_FROM_BITS(D3D11_IA_VERTEX_INPUT_RESOURCE_SLOT_COUNT)];
  BYTE IAIndexBuffer;
  BYTE IAInputLayout;
  BYTE IAPrimitiveTopology;
  BYTE OMRenderTargets;
  BYTE OMDepthStencilState;
  BYTE OMBlendState;
  BYTE RSViewports;
  BYTE RSScissorRects;
  BYTE RSRasterizerState;
  BYTE SOBuffers;
  BYTE Predication;
} D3DX11_STATE_BLOCK_MASK;
```



## <a name="members"></a>Membres

<dl> <dt>

**COMPARATIF**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer l’état du nuanceur de sommets.

</dd> <dt>

**VSSamplers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau d’échantillonneurs vertex-shader. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’échantillonnage.

</dd> <dt>

**VSShaderResources**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de ressources de nuanceur de vertex. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.

</dd> <dt>

**VSConstantBuffers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de mémoires tampons constantes de nuanceur de vertex. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de mémoire tampon constante.

</dd> <dt>

**VSInterfaces**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau d’interfaces de nuanceur de sommets. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’interface.

</dd> <dt>

**SH**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer l’état du nuanceur de coque.

</dd> <dt>

**HSSamplers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau d’échantillonneurs de nuanceur de coque. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’échantillonnage.

</dd> <dt>

**HSShaderResources**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de ressources de nuanceur de coque. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.

</dd> <dt>

**HSConstantBuffers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de mémoires tampons constantes de nuanceur de coque. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de mémoire tampon constante.

</dd> <dt>

**HSInterfaces**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau d’interfaces de nuanceur de coque. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’interface.

</dd> <dt>

**Source de données**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer l’état du nuanceur de domaine.

</dd> <dt>

**DSSamplers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau d’échantillonneurs de nuanceur de domaine. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’échantillonnage.

</dd> <dt>

**DSShaderResources**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de ressources de nuanceur de domaine. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.

</dd> <dt>

**DSConstantBuffers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de mémoires tampons constantes de nuanceur de domaine. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de mémoire tampon.

</dd> <dt>

**DSInterfaces**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau d’interfaces de nuanceur de domaine. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’interface.

</dd> <dt>

**GS**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant si l’état du nuanceur Geometry doit être enregistré.

</dd> <dt>

**GSSamplers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau d’échantillonneurs Geometry-Shader. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’échantillonnage.

</dd> <dt>

**GSShaderResources**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de ressources Geometry-Shader. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.

</dd> <dt>

**GSConstantBuffers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de mémoires tampons constantes de nuanceur de géométrie. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de mémoire tampon.

</dd> <dt>

**GSInterfaces**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau d’interfaces Geometry-Shader. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’interface.

</dd> <dt>

**ALIMENTATION**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer l’état du nuanceur de pixels.

</dd> <dt>

**PSSamplers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau d’échantillonneurs de nuanceur de pixels. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’échantillonnage.

</dd> <dt>

**PSShaderResources**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de ressources de nuanceur de pixels. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.

</dd> <dt>

**PSConstantBuffers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de mémoires tampons constantes de nuanceur de pixels. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de mémoire tampon constante.

</dd> <dt>

**PSInterfaces**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau d’interfaces de nuanceur de pixels. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’interface.

</dd> <dt>

**PSUnorderedAccessViews**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer les vues d’accès non trié de nuanceur de pixels.

</dd> <dt>

**CS**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer l’état du nuanceur de calcul.

</dd> <dt>

**CSSamplers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau d’échantillonneurs de nuanceur de calcul. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’échantillonnage.

</dd> <dt>

**CSShaderResources**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de ressources de nuanceur de calcul. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.

</dd> <dt>

**CSConstantBuffers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de mémoires tampons constantes de nuanceur de calcul. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de mémoire tampon constante.

</dd> <dt>

**CSInterfaces**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau d’interfaces de nuanceur de calcul. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement d’interface.

</dd> <dt>

**CSUnorderedAccessViews**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer les vues d’accès non ordonnées du nuanceur de calcul.

</dd> <dt>

**IAVertexBuffers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tableau de mémoires tampons de vertex. Le tableau est un masque de bits à plusieurs octets où chaque bit représente un emplacement de ressource.

</dd> <dt>

**IAIndexBuffer**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer l’état de la mémoire tampon d’index.

</dd> <dt>

**IAInputLayout**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant si l’état de la disposition d’entrée doit être enregistré.

</dd> <dt>

**IAPrimitiveTopology**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer l’état de la topologie primitive.

</dd> <dt>

**OMRenderTargets**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer les États des cibles de rendu.

</dd> <dt>

**OMDepthStencilState**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer l’état de gabarit de profondeur.

</dd> <dt>

**OMBlendState**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer l’état de fusion.

</dd> <dt>

**RSViewports**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer les États des Viewports.

</dd> <dt>

**RSScissorRects**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer les États des rectangles de ciseaux.

</dd> <dt>

**RSRasterizerState**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer l’état du rastériseur.

</dd> <dt>

**SOBuffers**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer les États des mémoires tampons de sortie de flux.

</dd> <dt>

**Prédicat**
</dt> <dd>

Type : **[ **Byte**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valeur booléenne indiquant s’il faut enregistrer l’état du prédicat.

</dd> </dl>

## <a name="remarks"></a>Remarques

Un masque de bloc d’État indique les États de l’appareil qu’une réussite ou une technique change.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Effets 11 structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

