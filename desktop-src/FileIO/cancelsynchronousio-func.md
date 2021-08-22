---
description: Marque les opérations d’e/s synchrones en attente qui sont émises par le thread spécifié comme annulées.
ms.assetid: f362c8b2-2193-443e-bb69-78f8b4147117
title: CancelSynchronousIo, fonction (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelSynchronousIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 1bdae4682bcbabb09778bdf5f5d3421c16af17587eda72813c9103eb16f7037f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582549"
---
# <a name="cancelsynchronousio-function"></a>CancelSynchronousIo fonction)

Marque les opérations d’e/s synchrones en attente qui sont émises par le thread spécifié comme annulées.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CancelSynchronousIo(
  _In_ HANDLE hThread
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hThread* \[ dans\]
</dt> <dd>

Handle du thread.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est différente de zéro.

Si la fonction échoue, la valeur de retour est 0 (zéro). Pour afficher les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Si cette fonction ne peut pas trouver de demande d’annulation, la valeur de retour est 0 (zéro), et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ introuvable**.

## <a name="remarks"></a>Remarques

L’appelant doit disposer du droit d’accès de [ \_ terminaison du thread](/windows/desktop/ProcThread/thread-security-and-access-rights) .

Si des opérations d’e/s en attente sont en cours pour le thread spécifié, la fonction **CancelSynchronousIo** les marque pour l’annulation. La plupart des types d’opérations peuvent être annulés immédiatement ; d’autres opérations peuvent continuer à se terminer avant qu’elles ne soient réellement annulées et que l’appelant soit notifié. La fonction **CancelSynchronousIo** n’attend pas que toutes les opérations annulées soient terminées. Pour plus d’informations, consultez [instructions d’achèvement/annulation d’e/s](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).

L’opération qui est annulée se termine avec l’un des trois États suivants : vous devez vérifier l’état d’achèvement pour déterminer l’état d’achèvement. Les trois États sont les suivants :

-   **L’opération s’est terminée normalement.** Cela peut se produire même si l’opération a été annulée, car la demande d’annulation n’a peut-être pas été envoyée dans le temps pour annuler l’opération.
-   **L'opération a été annulée.** La fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur indiquant que l’opération a été **\_ \_ abandonnée**.
-   **L’opération a échoué avec une autre erreur.** La fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur approprié.

dans Windows 8 et Windows Server 2012, cette fonction est prise en charge par les technologies suivantes.



| Technology                                           | Pris en charge      |
|------------------------------------------------------|----------------|
| Protocole SMB (Server Message Block) 3,0<br/>   | Oui<br/> |
| Basculement transparent SMB 3,0 (TFO)<br/>        | Oui<br/> |
| SMB 3,0 avec des partages de fichiers avec montée en puissance parallèle (SO)<br/>   | Oui<br/> |
| Système de fichiers Volume partagé de cluster (CsvFS)<br/> | Oui<br/> |
| Système de fichiers résilient (ReFS)<br/>              | Oui<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                                                                                                                                                                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                                                                                                                                                                                    |
| En-tête<br/>                   | <dl> <dt>IoAPI. h (include Windows. h);</dt> <dt>WinBase. h sur Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista (include Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[Fonctions de gestion de fichiers](file-management-functions.md)
</dt> <dt>

[E/s synchrones et asynchrones](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

