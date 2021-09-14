---
description: Définit les propriétés de matériau de maillage dans la scène 3D. Utilisez cette méthode pour spécifier les paramètres de diffusion de sous-surface.
ms.assetid: 830d73be-bba6-454d-8476-341d291a5b2e
title: 'ID3DXPRTEngine :: SetMeshMaterials, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetMeshMaterials
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c90ae72cab5d7a20c2c65b940d28a9b57902d2d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918340"
---
# <a name="id3dxprtenginesetmeshmaterials-method"></a>ID3DXPRTEngine :: SetMeshMaterials, méthode

Définit les propriétés de matériau de maillage dans la scène 3D. Utilisez cette méthode pour spécifier les paramètres de diffusion de sous-surface.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMeshMaterials(
  [in] const D3DXSHMATERIAL **ppMaterials,
  [in]       UINT           NumMeshes,
  [in]       UINT           NumChannels,
  [in]       BOOL           bSetAlbedo,
  [in]       FLOAT          fLengthScale
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppMaterials* \[ dans\]
</dt> <dd>

Type : **const [**D3DXSHMATERIAL**](d3dxshmaterial.md) \* \***

Adresse d’un pointeur vers les propriétés du matériau de maillage souhaité. Consultez [**D3DXSHMATERIAL**](d3dxshmaterial.md).

</dd> <dt>

*NumMeshes* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index du maillage sur lequel définir les propriétés du matériau.

</dd> <dt>

*NumChannels* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de canaux de couleur à définir dans le maillage. Définissez la valeur 1 pour spécifier les matières grises (R = G = B), ou 3 pour activer les effets de dépassement des couleurs. Si vous envisagez de modifier ce paramètre, commencez par définir le Albedo à l’aide d’une autre méthode telle que [**ID3DXPRTEngine :: SetPerTexelAlbedo**](id3dxprtengine--setpertexelalbedo.md) ou [**ID3DXPRTEngine :: SetPerVertexAlbedo**](id3dxprtengine--setpervertexalbedo.md).

</dd> <dt>

*bSetAlbedo* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Si la **valeur est true**, définit le Albedo du maillage sur ppMaterials, en remplaçant toutes les valeurs de Texel et de vertex Albedo existantes. Si la **valeur est false**, conserve toutes les valeurs de Texel et vertex Albedo existantes définies par d’autres méthodes. NumChannels doit correspondre au paramètre NumChannels utilisé pour créer la mémoire tampon dans [**D3DXCreatePRTBuffer**](d3dxcreateprtbuffer.md) ou [**D3DXCreatePRTBufferTex**](d3dxcreateprtbuffertex.md).

</dd> <dt>

*fLengthScale* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Échelle de la scène 3D par rapport à un cube de 1 mm. Utilisé pour les calculs de diffusion de sous-surface.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
