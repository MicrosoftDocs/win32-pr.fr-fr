---
title: D3D12CalcSubresource, fonction (D3dx12. h)
description: Calcule un index de sous-ressource pour une texture.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- D3D12CalcSubresource fonction)
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c704be7087d95d739685bc2823ec1c31a027b4406a3110986220927fdbbffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751719"
---
# <a name="d3d12calcsubresource-function"></a>D3D12CalcSubresource fonction)

Calcule un index de sous-ressource pour une texture.

## <a name="syntax"></a>Syntaxe


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MipSlice* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index de base zéro pour le niveau de mipmap à traiter ; 0 indique le premier niveau de mipmap, le plus détaillé.

</dd> <dt>

*ArraySlice* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index de base zéro pour le niveau de tableau à traiter ; Utilisez toujours 0 pour les textures de volume (3D).

</dd> <dt>

*PlaneSlice* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index de base zéro pour le niveau de plan à traiter.

</dd> <dt>

*Miplevels a* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre de niveaux de mipmap dans la ressource.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre d’éléments dans le tableau.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Index qui est égal à MipSlice + (ArraySlice \* miplevels a).

## <a name="remarks"></a>Remarques

Une mémoire tampon est une ressource non structurée et est donc définie comme contenant une seule sous-ressource. Les API qui prennent des mémoires tampons n’ont pas besoin d’un index de sous-ressources. Une texture en revanche est très structurée. Chaque objet texture peut contenir une ou plusieurs sous-ressources en fonction de la taille du tableau et du nombre de niveaux de mipmap.

Pour les textures de volume (3D), toutes les tranches d’un niveau de mipmap donné sont un index de sous-ressource unique.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothèque<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance pour D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Sous-ressources](subresources.md)
</dt> </dl>

 

