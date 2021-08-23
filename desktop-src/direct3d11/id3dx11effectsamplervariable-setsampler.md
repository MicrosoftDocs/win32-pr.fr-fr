---
title: Méthode ID3DX11EffectSamplerVariable SetSampler (D3dx11effect. h)
description: Définissez l’état de l’échantillonneur.
ms.assetid: 1826923d-d770-4d79-818a-a42a279f0a8c
keywords:
- Méthode SetSampler Direct3D 11
- Méthode SetSampler Direct3D 11, interface ID3DX11EffectSamplerVariable
- Interface ID3DX11EffectSamplerVariable Direct3D 11, méthode SetSampler
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.SetSampler
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4667b8261b46b1ecb1732c1ecc77efcf93d327426f0ea20f6c7710e94ed825e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791939"
---
# <a name="id3dx11effectsamplervariablesetsampler-method"></a>ID3DX11EffectSamplerVariable :: SetSampler, méthode

Définissez l’état de l’échantillonneur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSampler(
   UINT               Index,
   ID3D11SamplerState *pSampler
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index dans un tableau d’interfaces d’échantillonneur. S’il n’existe qu’une seule interface d’échantillonnage, utilisez 0.

</dd> <dt>

*pSampler* 
</dt> <dd>

Type : **[ **ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate)\***

Pointeur vers une interface [**ID3D11SamplerState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11samplerstate) contenant l’état de l’échantillonneur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Remarques

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectSamplerVariable](id3dx11effectsamplervariable.md)
</dt> </dl>

 

