---
title: Méthode ID3DX11EffectDepthStencilVariable GetBackingStore (D3dx11effect. h)
description: Obtient un pointeur vers une variable qui contient l’état du gabarit de profondeur.
ms.assetid: 6aeed5ac-f0ee-4e8c-b87b-022f58c9094c
keywords:
- Méthode GetBackingStore Direct3D 11
- Méthode GetBackingStore Direct3D 11, interface ID3DX11EffectDepthStencilVariable
- Interface ID3DX11EffectDepthStencilVariable Direct3D 11, méthode GetBackingStore
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable.GetBackingStore
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9335817b9c954958c97294a88291f83bf0e967d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974582"
---
# <a name="id3dx11effectdepthstencilvariablegetbackingstore-method"></a>ID3DX11EffectDepthStencilVariable :: GetBackingStore, méthode

Obtient un pointeur vers une variable qui contient l’état du gabarit de profondeur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetBackingStore(
   UINT                     Index,
   D3D11_DEPTH_STENCIL_DESC *pDepthStencilDesc
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Index* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indexez dans un tableau de descriptions Depth-State-State. S’il n’existe qu’une seule variable de stencil de profondeur dans l’effet, utilisez 0.

</dd> <dt>

*pDepthStencilDesc* 
</dt> <dd>

Type : **[ **\_ Description du \_ stencil \_ de profondeur d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)\***

Pointeur vers une description de l’État Depth-stencil-(voir la description du [**\_ stencil d3d11 Depth \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Notes

Les variables d’effet sont enregistrées en mémoire dans le magasin de stockage ; Quand une technique est appliquée, les valeurs du magasin de stockage sont copiées sur l’appareil. Les données du magasin de stockage peuvent être utilisées pour recréer la variable si nécessaire.

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11EffectDepthStencilVariable](id3dx11effectdepthstencilvariable.md)
</dt> </dl>

 

