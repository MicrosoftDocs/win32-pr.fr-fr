---
description: Utilise le GPU pour calculer la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation de l’harmonique sphérique (SH). Le calcul de l’éclairage sur le GPU sera généralement beaucoup plus rapide que sur le processeur.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'ID3DXPRTEngine :: ComputeDirectLightingSHGPU, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120398"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a>ID3DXPRTEngine :: ComputeDirectLightingSHGPU, méthode

Utilise le GPU pour calculer la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation de l’harmonique sphérique (SH). Le calcul de l’éclairage sur le GPU sera généralement beaucoup plus rapide que sur le processeur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers l’objet d’appareil [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) utilisé pour exécuter la simulation sur le GPU. L’appareil doit prendre en charge les nuanceurs de pixels [PS \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) .

> [!Note]  
> Les fonctions de rappel ne doivent pas utiliser l’objet d’appareil [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) utilisé par le simulateur GPU.

 

</dd> <dt>

*Indicateurs* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Paramètre de simulation GPU qui définit la résolution de la mémoire tampon z de l’ombre. Doit être défini sur l’une des valeurs constantes de [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md). Pour spécifier une simulation de précision plus élevée, la \_ valeur highquality D3DXSHGPUSIMOPT peut être combinée avec l’une des \_ valeurs SHADOWRESxxx D3DXSHGPUSIMOPT.

</dd> <dt>

*Commande* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de l’évaluation SH. La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus. L’évaluation génère des coefficients de commande ². Le degré de l’évaluation est Order-1.

</dd> <dt>

*ZBias* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Décalage dans la direction normale.

</dd> <dt>

*ZAngleBias* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Décalage dans la direction normale, mis à l’échelle d’un moins le cosinus de l’angle avec le rayon de la lumière.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) . Cette mémoire tampon doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Dans cette méthode, le Albedo n’est pas multiplié par le signal lumineux, et seule la lumière entrante est intégrée dans le simulateur. En ne multipliant pas Albedo, vous pouvez modéliser la variation Albedo à une échelle plus fine que le luminance source, ce qui donne des résultats plus précis de la compression.

Appelez [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) pour multiplier chaque vecteur de transfert luminance (PRT) précalculé par le Albedo.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
