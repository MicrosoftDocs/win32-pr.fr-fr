---
title: ID3DX11Effect Optimize, méthode (D3dx11effect. h)
description: Réduisez la quantité de mémoire requise pour un effet.
ms.assetid: fa1d0769-6746-44f6-9979-31a534646884
keywords:
- Optimiser la méthode Direct3D 11
- Optimiser la méthode Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode Optimize
topic_type:
- apiref
api_name:
- ID3DX11Effect.Optimize
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33fd6d200f6b22af46e648040e8299f40ec9ebae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403378"
---
# <a name="id3dx11effectoptimize-method"></a>ID3DX11Effect :: Optimize, méthode

Réduisez la quantité de mémoire requise pour un effet.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Optimize();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Notes

Un effet utilise l’espace mémoire de deux façons différentes : pour stocker les informations requises par le runtime pour exécuter un effet, et pour stocker les métadonnées requises pour répercuter les informations dans une application à l’aide de l’API. Vous pouvez réduire la quantité de mémoire requise par un effet en appelant **ID3DX11Effect :: Optimize** , qui supprime les métadonnées de réflexion de la mémoire. Les méthodes d’API pour lire des variables ne fonctionnent plus une fois que les données de réflexion ont été supprimées.

Les méthodes suivantes échouent après l’appel de la méthode Optimize sur un effet.

-   [**ID3DX11Effect::GetConstantBufferByIndex**](id3dx11effect-getconstantbufferbyindex.md)
-   [**ID3DX11Effect::GetConstantBufferByName**](id3dx11effect-getconstantbufferbyname.md)
-   [**ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md)
-   [**ID3DX11Effect::GetDevice**](id3dx11effect-getdevice.md)
-   [**ID3DX11Effect::GetTechniqueByIndex**](id3dx11effect-gettechniquebyindex.md)
-   [**ID3DX11Effect::GetTechniqueByName**](id3dx11effect-gettechniquebyname.md)
-   [**ID3DX11Effect::GetVariableByIndex**](id3dx11effect-getvariablebyindex.md)
-   [**ID3DX11Effect::GetVariableByName**](id3dx11effect-getvariablebyname.md)
-   [**ID3DX11Effect::GetVariableBySemantic**](id3dx11effect-getvariablebysemantic.md)

> [!Note]  
> Les références récupérées avec ces méthodes avant d’appeler **ID3DX11Effect :: Optimize** sont toujours valides après l’appel de **ID3DX11Effect :: Optimize** . Cela permet à l’application d’accéder à toutes les variables, techniques et passes qu’elle utilise, d’appeler Optimize, puis d’utiliser l’effet.

 

> [!Note]  
> Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets. Vous devez utiliser la source Effects 11 pour créer votre application Effects-type. Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Bibliothèque<br/> | <dl> <dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11Effect](id3dx11effect.md)
</dt> </dl>

 

 





