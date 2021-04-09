---
description: Créer une pompe de thread.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: D3DX10CreateThreadPump, fonction (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8a27f8df1f4eaa8e7f41e863d703063308f9c595
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953971"
---
# <a name="d3dx10createthreadpump-function"></a>D3DX10CreateThreadPump fonction)

Créer une pompe de thread.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cIoThreads* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de threads d’e/s à créer. Si la valeur 0 est spécifiée, Direct3D tente de calculer le nombre optimal de threads en fonction de la configuration matérielle.

</dd> <dt>

*cProcThreads* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de threads de processus à créer. Si la valeur 0 est spécifiée, Direct3D tente de calculer le nombre optimal de threads en fonction de la configuration matérielle.

</dd> <dt>

*ppThreadPump* \[ à\]
</dt> <dd>

Type : **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***

Pompe de thread créée. Voir [**interface ID3DX10ThreadPump**](id3dx10threadpump.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

Une pompe de thread est un objet très gourmand en ressources. Une seule pompe de threads doit être créée par application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
