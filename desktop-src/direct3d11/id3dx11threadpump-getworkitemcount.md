---
title: Méthode ID3DX11ThreadPump GetWorkItemCount (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Obtient le nombre d’éléments de travail dans la pompe de thread.'
ms.assetid: 04883b25-64dc-41a3-849f-710a59e9d3da
keywords:
- Méthode GetWorkItemCount Direct3D 11
- Méthode GetWorkItemCount Direct3D 11, interface ID3DX11ThreadPump
- Interface ID3DX11ThreadPump Direct3D 11, méthode GetWorkItemCount
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.GetWorkItemCount
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29668e66dd3d8c6d29cbfc69a4ef12a2fdfd18b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974530"
---
# <a name="id3dx11threadpumpgetworkitemcount-method"></a>ID3DX11ThreadPump :: GetWorkItemCount, méthode

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 

Obtient le nombre d’éléments de travail dans la pompe de thread.

## <a name="syntax"></a>Syntaxe


```C++
UINT GetWorkItemCount();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Nombre d’éléments de travail mis en file d’attente dans la pompe de thread.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

