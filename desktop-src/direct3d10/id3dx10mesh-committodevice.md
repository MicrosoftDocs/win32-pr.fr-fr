---
description: Validez toutes les modifications apportées à un maillage sur l’appareil afin que les modifications puissent être rendues. Cela doit être appelé après la modification des données d’un maillage et avant son rendu. Un maillage ne peut pas être rendu, sauf s’il est validé sur l’appareil. Consultez la section Remarques.
ms.assetid: 26927553-d1d8-4745-85ad-a8a6fe949306
title: 'ID3DX10Mesh :: CommitToDevice, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CommitToDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 160f97a3a00ddc7bbf69989991b2794ab3d6e5e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043112"
---
# <a name="id3dx10meshcommittodevice-method"></a>ID3DX10Mesh :: CommitToDevice, méthode

Validez toutes les modifications apportées à un maillage sur l’appareil afin que les modifications puissent être rendues. Cela doit être appelé après la modification des données d’un maillage et avant son rendu. Un maillage ne peut pas être rendu, sauf s’il est validé sur l’appareil. Consultez la section Remarques.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CommitToDevice();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

Lorsqu’un maillage est chargé, ses données sont chargées dans des ressources intermédiaires, ce qui signifie que les données peuvent être modifiées mais pas rendues. Quand CommitToDevice est appelé, les données des ressources de mise en lots sont copiées dans les ressources de l’appareil afin qu’elles puissent être rendues. Bien que les données soient validées sur l’appareil, les ressources de mise en lots restent et peuvent être modifiées. Si des modifications sont apportées aux ressources intermédiaires, celles-ci doivent être réactivées sur l’appareil afin que ces modifications soient rendues à l’écran.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




