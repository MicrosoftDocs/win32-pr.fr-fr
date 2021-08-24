---
description: Récupère simultanément plusieurs entrées de port de terminaison.
ms.assetid: 3996c02c-562c-4697-a091-e241ad54b239
title: GetQueuedCompletionStatusEx, fonction (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetQueuedCompletionStatusEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: f81bc0c997e3637fa941cb5a23f6394ba1f585566c8d633cadb00c9fd75ac805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696119"
---
# <a name="getqueuedcompletionstatusex-function"></a>GetQueuedCompletionStatusEx fonction)

Récupère simultanément plusieurs entrées de port de terminaison. Elle attend la fin des opérations d’e/s en attente associées au port de terminaison spécifié.

Pour défiler les paquets de fin d’exécution d’e/s une à la fois, utilisez la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI GetQueuedCompletionStatusEx(
  _In_  HANDLE             CompletionPort,
  _Out_ LPOVERLAPPED_ENTRY lpCompletionPortEntries,
  _In_  ULONG              ulCount,
  _Out_ PULONG             ulNumEntriesRemoved,
  _In_  DWORD              dwMilliseconds,
  _In_  BOOL               fAlertable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CompletionPort* \[ dans\]
</dt> <dd>

Handle vers le port de terminaison. Pour créer un port de terminaison, utilisez la fonction [**CreateIoCompletionPort**](createiocompletionport.md) .

</dd> <dt>

*lpCompletionPortEntries* \[ à\]
</dt> <dd>

En entrée, pointe vers un tableau pré-alloué de structures d' [**\_ entrée avec chevauchement**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) .

Lors de la sortie, reçoit un tableau de structures d' [**\_ entrée avec chevauchement**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry) qui contiennent les entrées. Le nombre d’éléments du tableau est fourni par *ulNumEntriesRemoved*.

Le nombre d’octets transférés au cours de chaque e/s, la clé de saisie semi-automatique qui indique sur quel fichier chaque e/s s’est produite, et l’adresse de la structure OVERLAPPED utilisée dans chaque e/s d’origine sont toutes retournées dans le tableau *lpCompletionPortEntries* .

</dd> <dt>

*ulCount* \[ dans\]
</dt> <dd>

Nombre maximal d’entrées à supprimer.

</dd> <dt>

*ulNumEntriesRemoved* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’entrées réellement supprimées.

</dd> <dt>

*dwMilliseconds* \[ dans\]
</dt> <dd>

Nombre de millisecondes pendant lesquelles l’appelant est disposé à attendre qu’un paquet d’achèvement apparaisse sur le port de terminaison. Si un paquet de saisie semi-automatique n’apparaît pas dans le délai spécifié, la fonction expire et retourne **false**.

Si *dwMilliseconds* est **infini** (0xFFFFFFFF), la fonction n’expire jamais. Si *dwMilliseconds* est égal à zéro et qu’il n’y a pas d’opération d’e/s à défiler, la fonction expire immédiatement.

</dd> <dt>

*fAlertable* \[ dans\]
</dt> <dd>

Si ce paramètre a la **valeur false**, la fonction ne retourne pas de valeur tant que le délai d’attente n’est pas écoulé ou qu’une entrée n’a pas été récupérée.

Si le paramètre a la **valeur true** et qu’il n’y a pas d’entrées disponibles, la fonction exécute une attente signalable. Le thread retourne lorsque le système met en file d’attente une routine d’exécution d’e/s ou un APC dans le thread et que le thread exécute la fonction.

Une routine de saisie semi-automatique est mise en file d’attente lorsque la fonction [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) ou [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) dans laquelle elle a été spécifiée est terminée, et le thread appelant est le thread qui a initié l’opération. Un APC est mis en file d’attente lorsque vous appelez [**QueueUserAPC**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-queueuserapc).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro (**true**) en cas de réussite ou zéro (**false**) dans le cas contraire.

Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Cette fonction associe un thread au port de terminaison spécifié. Un thread peut être associé à au plus un port de terminaison.

Cette fonction retourne la **valeur true** lorsqu’au moins une e/s en attente est terminée, mais il est possible qu’une ou plusieurs opérations d’e/s aient échoué. Notez qu’il revient à l’utilisateur de cette fonction de vérifier la liste des entrées retournées dans le paramètre *lpCompletionPortEntries* pour déterminer celles qui correspondent à toutes les opérations d’e/s ayant échoué, en examinant l’État contenu dans le membre **lpOverlapped** de chaque [**\_ entrée Overlapped**](/windows/desktop/api/MinWinBase/ns-minwinbase-overlapped_entry).

Cette fonction retourne la **valeur false** lorsqu’aucune opération d’e/s n’a été déplacée dans la file d’attente. Cela signifie généralement qu’une erreur s’est produite lors du traitement des paramètres de cet appel, ou que le handle *CompletionPort* a été fermé ou qu’il n’est pas valide. La fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) fournit des informations d’erreur étendues.

Si un appel à [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) échoue parce que le descripteur qui lui est associé est fermé, la fonction retourne **false** et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une **erreur d' \_ attente abandonnée \_ \_ 0**.

Les applications serveur peuvent avoir plusieurs threads appelant la fonction **GetQueuedCompletionStatusEx** pour le même port de terminaison. À mesure que les opérations d’e/s se terminent, elles sont mises en file d’attente sur ce port dans l’ordre First-in-First-Out. Si un thread attend activement cet appel, une ou plusieurs demandes mises en file d’attente terminent l’appel de ce thread uniquement.

Pour plus d’informations sur la théorie, l’utilisation et les fonctions associées du port de terminaison d’e/s, consultez [ports de terminaison d’e/s](i-o-completion-ports.md).

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
| Client minimal pris en charge<br/> | Windows \[Applications UWP pour applications de bureau Vista \|\]<br/>                                                                                                                                                                                                                   |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2008 \[ \| applications UWP\]<br/>                                                                                                                                                                                                             |
| En-tête<br/>                   | <dl> <dt>IoAPI. h (include Windows. h);</dt> <dt>WinBase. h sur Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista (include Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Rubriques de présentation**
</dt> <dt>

[Fonctions de gestion de fichiers](file-management-functions.md)
</dt> <dt>

[Ports de terminaison d’e/s](i-o-completion-ports.md)
</dt> <dt>

[utilisation des en-têtes de Windows](/windows/desktop/WinProg/using-the-windows-headers)
</dt> <dt>

**Fonctions**
</dt> <dt>

[**ConnectNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)
</dt> <dt>

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](getqueuedcompletionstatusex-func.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**PostQueuedCompletionStatus**](postqueuedcompletionstatus.md)
</dt> <dt>

[**TransactNamedPipe**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)
</dt> <dt>

[**WaitCommEvent**](/windows/desktop/api/winbase/nf-winbase-waitcommevent)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> </dl>

 

