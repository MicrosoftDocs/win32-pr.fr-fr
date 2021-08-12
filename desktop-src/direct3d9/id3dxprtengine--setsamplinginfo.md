---
description: Définit les propriétés d’échantillonnage utilisées par le simulateur de transfert luminance (PRT) précalculé.
ms.assetid: a33963a7-fbcb-4e1c-a4f3-fb20a99fcf9f
title: 'ID3DXPRTEngine :: SetSamplingInfo, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetSamplingInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: db15bc2120f90cf52aa4f3c41eccecc7d308cc8392ae368cd4423a90f218f6ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293363"
---
# <a name="id3dxprtenginesetsamplinginfo-method"></a>ID3DXPRTEngine :: SetSamplingInfo, méthode

Définit les propriétés d’échantillonnage utilisées par le simulateur de transfert luminance (PRT) précalculé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSamplingInfo(
  [in] UINT  NumRays,
  [in] BOOL  UseSphere,
  [in] BOOL  UseCosine,
  [in] BOOL  Adaptive,
  [in] FLOAT AdaptiveThresh
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NumRays* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de rayons de lumière à diriger vers chaque échantillon. Doit être supérieur à zéro.

</dd> <dt>

*UseSphere* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Si la **valeur est true**, les échantillons sont calculés sur une sphère complète. Si la **valeur est false**, les échantillons sont calculés sur un hémisphère.

</dd> <dt>

*UseCosine* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Si la **valeur est true**, utilisez une pondération cosinus des échantillons. Si UseCosine et UseSphere ont tous les deux la **valeur true**, la méthode échoue et une erreur est retournée.

</dd> <dt>

*Adaptative* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Doit avoir la **valeur false**. L’échantillonnage adaptatif n’est actuellement pas implémenté.

</dd> <dt>

*AdaptiveThresh* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Ignoré.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, e \_ NOTIMPL, e \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
