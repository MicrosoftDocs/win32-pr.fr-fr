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
ms.openlocfilehash: b8b1f7c382d034e804d4ac7e63d58b8ec5853620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865058"
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
| Client minimal pris en charge<br/> | Applications Windows 10 \[ Desktop Apps \| UWP\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ \| apps UWP\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
