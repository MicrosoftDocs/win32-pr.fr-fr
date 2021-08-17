---
description: Définit l’affectation de jeux d’UC par défaut pour les threads dans le processus spécifié. Les threads créés, qui n’ont pas d’ensembles d’UC définis explicitement à l’aide de SetThreadSelectedCpuSets, héritent automatiquement des jeux spécifiés par SetProcessDefaultCpuSets.
ms.assetid: 7A510A8D-B06C-4B7B-9A87-BCFE0DE4D17B
title: SetProcessDefaultCpuSets, fonction (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 3e085f769e5b086c1f68d721df6463afa7f51a0e5f9f292c7fce1dadd0356535
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793176"
---
# <a name="setprocessdefaultcpusets-function"></a>SetProcessDefaultCpuSets fonction)

Définit l’affectation de jeux d’UC par défaut pour les threads dans le processus spécifié. Les threads créés, qui n’ont pas d’ensembles d’UC définis explicitement à l’aide de [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md), héritent automatiquement des jeux spécifiés par **SetProcessDefaultCpuSets** .

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SetProcessDefaultCpuSets(
  _In_     HANDLE Process,
  _In_opt_ ULONG  CpuSetIds,
  _In_     ULONG  CpuSetIdCound
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Processus* \[ dans\]
</dt> <dd>

Spécifie le processus pour lequel définir les ensembles d’UC par défaut. Ce descripteur doit avoir le droit de définir le processus d' \_ \_ \_ accès limité aux informations. La valeur retournée par [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) peut également être spécifiée ici.

</dd> <dt>

*CpuSetIds* \[ dans, facultatif\]
</dt> <dd>

Spécifie la liste des ID de jeu d’UC à définir en tant qu’ensemble d’UC de processus par défaut. Si la valeur est NULL, **SetProcessDefaultCpuSets** efface toutes les affectations.

</dd> <dt>

*CpuSetIdCound* \[ dans\]
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



 

 
