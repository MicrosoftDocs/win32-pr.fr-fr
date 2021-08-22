---
description: Définit l’affectation de jeux d’UC sélectionnée pour le thread spécifié. Cette assignation remplace l’attribution de processus par défaut, si celle-ci est définie.
ms.assetid: A73F7118-CC4A-45E6-869A-DFF6924D10C8
title: SetThreadSelectedCpuSets, fonction (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d627c3ae0499cf19ba533c30d1a3fabb05c2dbf5782d99b2f716579f50125b0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031729"
---
# <a name="setthreadselectedcpusets-function"></a>SetThreadSelectedCpuSets fonction)

Définit l’affectation de jeux d’UC sélectionnée pour le thread spécifié. Cette assignation remplace l’attribution de processus par défaut, si celle-ci est définie.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SetThreadSelectedCpuSets(
  _In_       HANDLE Thread,
  _In_ const ULONG  *CpuSetIds,
  _In_       ULONG  CpuSetIdCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Thread* \[ dans\]
</dt> <dd>

Spécifie le thread sur lequel définir l’affectation de l’ensemble d’UC. Ce descripteur doit disposer \_ du \_ \_ droit d’accès limité aux informations du thread. La valeur retournée par [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) peut également être utilisée.

</dd> <dt>

*CpuSetIds* \[ dans\]
</dt> <dd>

Spécifie la liste des ID de jeu d’UC à définir comme l’ensemble d’UC sélectionné du thread. Si la valeur est NULL, l’API efface toutes les affectations, ce qui revient à traiter l’affectation par défaut si elle est définie.

</dd> <dt>

*CpuSetIdCount* \[ dans\]
</dt> <dd>

Spécifie le nombre d’ID dans la liste passée dans l’argument **CpuSetIds** . Si cette valeur est NULL, la valeur doit être 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction ne peut pas échouer quand des paramètres valides sont passés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau \| UWP apps\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau \| UWP apps\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
