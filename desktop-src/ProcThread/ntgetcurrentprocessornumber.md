---
description: Récupère le nombre de processeurs sur lesquels le thread actuel s’exécutait pendant l’appel à cette fonction.
ms.assetid: f0141550-58e2-421a-934d-9a6c488d2b81
title: NtGetCurrentProcessorNumber fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGetCurrentProcessorNumber
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 96862836d3f9c16034ce1c2e751aebea2884d114
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324810"
---
# <a name="ntgetcurrentprocessornumber-function"></a>NtGetCurrentProcessorNumber fonction)

\[Les **NtGetCurrentProcessorNumber** peuvent être modifiés ou non disponibles dans les futures versions de Windows. Les applications doivent utiliser la fonction [**GetCurrentProcessorNumber**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocessornumber) à la place.\]

Récupère le nombre de processeurs sur lesquels le thread actuel s’exécutait pendant l’appel à cette fonction.

## <a name="syntax"></a>Syntaxe


```C++
ULONG WINAPI NtGetCurrentProcessorNumber(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

La fonction retourne le numéro de processeur actuel.

## <a name="remarks"></a>Notes

Cette fonction est utilisée pour fournir des informations sur l’estimation des performances du processus.

Cette fonction n’a pas de bibliothèque d’importation associée. Vous devez utiliser les fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Ntdll.dll.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------|--------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Plusieurs processeurs](multiple-processors.md)
</dt> <dt>

[Fonctions de processus et de thread](process-and-thread-functions.md)
</dt> <dt>

[Processus](child-processes.md)
</dt> </dl>

 

 
