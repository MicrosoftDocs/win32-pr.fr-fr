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
ms.openlocfilehash: 7998b20815529b41c5e29204c0ef50fbc15e6288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519890"
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
| Client minimal pris en charge<br/> | Applications Windows 10 \[ Desktop Apps \| UWP\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ \| apps UWP\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

 
