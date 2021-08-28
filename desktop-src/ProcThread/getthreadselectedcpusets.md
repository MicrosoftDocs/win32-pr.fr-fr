---
description: Retourne l’attribution de jeu d’UC explicite du thread spécifié, si une affectation a été définie à l’aide de l’API SetThreadSelectedCpuSets. Si aucune assignation explicite n’est définie, RequiredIdCount a la valeur 0 et la fonction retourne la valeur TRUE.
ms.assetid: 9ACF72F8-A64C-4FFF-B340-C920E80238CA
title: GetThreadSelectedCpuSets, fonction (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetThreadSelectedCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: 76e8fb9ff9fb540d15c8610a673ff52c5586f0ab57eb06668ef5e586db7513d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119978779"
---
# <a name="getthreadselectedcpusets-function"></a>GetThreadSelectedCpuSets fonction)

Retourne l’attribution de jeu d’UC explicite du thread spécifié, si une affectation a été définie à l’aide de l’API [**SetThreadSelectedCpuSets**](setthreadselectedcpusets.md) . Si aucune assignation explicite n’est définie, **RequiredIdCount** a la valeur 0 et la fonction retourne la valeur true.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI GetThreadSelectedCpuSets(
  _In_      HANDLE Thread,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Thread* \[ dans\]
</dt> <dd>

Spécifie le thread pour lequel interroger les ensembles d’UC sélectionnés. Ce descripteur doit avoir \_ le \_ \_ droit d’accès aux informations limitées du thread. La valeur retournée par [**GetCurrentThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentthread) peut également être spécifiée ici.

</dd> <dt>

*CpuSetIds* \[ out, facultatif\]
</dt> <dd>

Spécifie une mémoire tampon facultative pour récupérer la liste des identificateurs d’ensembles d’UC.

</dd> <dt>

*CpuSetIdCount* \[ dans\]
</dt> <dd>

Spécifie la capacité de la mémoire tampon spécifiée dans **CpuSetIds**. Si la mémoire tampon est NULL, cette valeur doit être 0.

</dd> <dt>

*RequiredIdCount* \[ à\]
</dt> <dd>

Spécifie la capacité requise de la mémoire tampon pour contenir l’intégralité de la liste des ensembles d’UC sélectionnés du thread. En cas de retour réussi, spécifie le nombre d’ID remplis dans la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette API retourne TRUE en cas de réussite. Si la mémoire tampon n’est pas assez grande, la valeur de **GetLastError** est une \_ mémoire tampon d’erreur insuffisante \_ . Cette API ne peut pas échouer quand des paramètres valides sont transmis et que la mémoire tampon de retour est suffisamment grande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau \| UWP apps\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau \| UWP apps\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

