---
description: Récupère la liste des ensembles d’UC dans l’ensemble de processus par défaut qui a été défini par SetProcessDefaultCpuSets. Si aucun jeu d’UC par défaut n’est défini pour un processus donné, RequiredIdCount a la valeur 0 et la fonction est exécutée correctement.
ms.assetid: 85DC5331-9EC0-4603-94FD-B49E725301B1
title: GetProcessDefaultCpuSets, fonction (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetProcessDefaultCpuSets
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: a5bd7c27b76efbbac923317837ac82b3a6700197
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518677"
---
# <a name="getprocessdefaultcpusets-function"></a>GetProcessDefaultCpuSets fonction)

Récupère la liste des ensembles d’UC dans l’ensemble de processus par défaut qui a été défini par [**SetProcessDefaultCpuSets**](setprocessdefaultcpusets.md). Si aucun jeu d’UC par défaut n’est défini pour un processus donné, **RequiredIdCount** a la valeur 0 et la fonction est exécutée correctement.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI GetProcessDefaultCpuSets(
  _In_      HANDLE Process,
  _Out_opt_ PULONG CpuSetIds,
  _In_      ULONG  CpuSetIdCount,
  _Out_     PULONG RequiredIdCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Processus* \[ dans\]
</dt> <dd>

Spécifie un handle de processus pour le processus à interroger. Ce descripteur doit disposer du droit d’accès au processus \_ requête \_ sur les \_ informations limitées. La valeur retournée par [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) peut également être spécifiée ici.

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

Spécifie la capacité requise de la mémoire tampon pour contenir l’intégralité de la liste des ensembles d’UC par défaut du processus. En cas de retour réussi, spécifie le nombre d’ID remplis dans la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette API retourne TRUE en cas de réussite. Si la mémoire tampon n’est pas assez grande, l’API retourne FALSe et la valeur de **GetLastError** est une \_ mémoire tampon d’erreur insuffisante \_ . Cette API ne peut pas échouer quand des paramètres valides sont transmis et que la mémoire tampon de retour est suffisamment grande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 10 \[ Desktop Apps \| UWP\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ \| apps UWP\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

