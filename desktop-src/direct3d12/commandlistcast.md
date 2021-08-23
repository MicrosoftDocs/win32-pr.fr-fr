---
title: CommandListCast, fonction (D3dx12. h)
description: Ce modèle de fonction convertit un pointeur constant en une liste de commandes en pointeur const vers un ID3D12CommandList.
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- CommandListCast fonction)
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 977c7f70a3a69f228627bacb7429e6d1d0b5977242ccc2474c94393d028c573d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118807654"
---
# <a name="commandlistcast-function"></a>CommandListCast fonction)

Ce modèle de fonction convertit un pointeur constant en une liste de commandes en pointeur const vers un ID3D12CommandList.

Ce cast est utile pour passer des pointeurs de liste de commandes fortement typés dans [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

## <a name="syntax"></a>Syntaxe


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*p* 
</dt> <dd>

Type : **t \_ CommandListType \* \* const**

Liste de commandes fortement typée à convertir.

L’argument de modèle **t \_ CommandListType** spécifie un objet de liste de commandes fortement typé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **ID3D12CommandList \* const \***

Liste de commandes fortement typées, réinterprétée comme un [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).

## <a name="remarks"></a>Remarques

CommandListCast effectue un **\_ cast de réinterprétation**. Le cast est valide tant que le caractère const de la liste de commandes est respecté.

La fonction CommandListCast est définie comme suit :


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothèque<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’assistance pour D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





