---
description: Permet à une application d’interroger les ensembles d’UC disponibles sur le système, ainsi que leur état actuel.
ms.assetid: 168B00AB-1B11-44A0-B548-903CA3F4BBDE
title: GetSystemCpuSetInformation, fonction (Processthreadapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSystemCpuSetInformation
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-ProcessThreads-L1-1-3.dll
- KernelBase.dll
ms.openlocfilehash: d8ce490e3377e45a81b24523504d06941755de49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202855"
---
# <a name="getsystemcpusetinformation-function"></a>GetSystemCpuSetInformation fonction)

Permet à une application d’interroger les ensembles d’UC disponibles sur le système, ainsi que leur état actuel.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI GetSystemCpuSetInformation(
  _Out_opt_  PSYSTEM_CPU_SET_INFORMATION  Information,
  _In_       ULONG                        BufferLength,
  _Out_      PULONG                       ReturnedLength,
  _In_opt_   HANDLE                       Process,
  _Reserved_ ULONG                        Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Informations* \[ out, facultatif\]
</dt> <dd>

Pointeur vers une structure [**d' \_ \_ \_ informations de jeu d’UC système**](/windows/desktop/api/winnt/ns-winnt-system_cpu_set_information) qui reçoit les données du jeu d’UC. Transmettez la valeur NULL avec une longueur de mémoire tampon de 0 pour déterminer la taille de mémoire tampon requise.

</dd> <dt>

*BufferLength* \[ dans\]
</dt> <dd>

Longueur, en octets, de la mémoire tampon de sortie passée comme argument d’information.

</dd> <dt>

*ReturnedLength* \[ à\]
</dt> <dd>

Longueur, en octets, des données valides dans la mémoire tampon de sortie si la mémoire tampon est suffisamment grande, ou la taille requise de la mémoire tampon de sortie. Si aucun ensemble d’UC n’existe, cette valeur est 0.

</dd> <dt>

*Processus* \[ dans, facultatif\]
</dt> <dd>

Handle facultatif d’un processus. Ce processus est utilisé pour déterminer la valeur de l’indicateur **AllocatedToTargetProcess** dans la structure d’informations du jeu d' \_ UC système \_ \_ . Si un ensemble d’UC est alloué au processus spécifié, l’indicateur est défini. Dans le cas contraire, il est clair. Ce descripteur doit disposer du droit d’accès au processus \_ requête \_ sur les \_ informations limitées. La valeur retournée par [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) peut également être spécifiée ici.

</dd> <dt>

*Indicateurs* 
</dt> <dd>

Réservé, doit avoir la valeur 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’API fonctionne correctement, elle retourne TRUE. En cas d’échec, la raison de l’erreur est disponible par le biais de **GetLastError**. Si la mémoire tampon d’informations était NULL ou n’est pas assez grande, l’erreur de code d’erreur « \_ mémoire tampon insuffisante » \_ est retournée. Cette API ne peut pas échouer quand des paramètres valides ont été transmis et une mémoire tampon suffisamment grande pour contenir toutes les données de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 10 \[ Desktop Apps \| UWP\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2016 \[ \| apps UWP\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Processthreadsapi. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Windows. h</dt> </dl>          |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>       |



 

