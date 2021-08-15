---
title: Méthode ID3DX11EffectSamplerVariable GetBackingStore (D3dx11effect. h)
description: Obtient un pointeur vers une variable qui contient l’état de l’échantillonneur.
ms.assetid: b188fb86-f54b-481e-9110-7b8af70ff303
keywords:
- Méthode GetBackingStore Direct3D 11
- Méthode GetBackingStore Direct3D 11, interface ID3DX11EffectSamplerVariable
- Interface ID3DX11EffectSamplerVariable Direct3D 11, méthode GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51bba7ff1c23a7b842fc6f41ea623b19096b4cbf1691e5645d32cc1df02a2bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534165"
---
# <a name="id3dx11effectsamplervariablegetbackingstore-method"></a>ID3DX11EffectSamplerVariable :: GetBackingStore, méthode

Obtient un pointeur vers une variable qui contient l’état de l’échantillonneur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBackingStore(
   UINT               Index,
   D3D11_SAMPLER_DESC *pSamplerDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index dans un tableau de descriptions de l’échantillonneur. S’il n’existe qu’une seule variable d’échantillonneur dans l’effet, utilisez 0.

</dd> <dt>

*pSamplerDesc* 
</dt> <dd>

Type : **[ **d3d11 \_ sampler \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)\***

Pointeur vers une description de l’échantillonneur (consultez [**d3d11 \_ sampler \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)).

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

 

