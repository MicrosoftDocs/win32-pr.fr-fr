---
description: Marque toutes les opérations d’e/s en attente pour le handle de fichier spécifié. La fonction annule uniquement les opérations d’e/s dans le processus actuel, quel que soit le thread qui a créé l’opération d’e/s.
ms.assetid: a2ce13b8-7da6-4848-848d-901d9667c2e3
title: CancelIoEx, fonction (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIoEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 3de44762ad9a230a9d8cc410c4ba3ae7c2d9964e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524181"
---
# <a name="cancelioex-function"></a>CancelIoEx fonction)

Marque toutes les opérations d’e/s en attente pour le handle de fichier spécifié. La fonction annule uniquement les opérations d’e/s dans le processus actuel, quel que soit le thread qui a créé l’opération d’e/s.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CancelIoEx(
  _In_     HANDLE       hFile,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFile* \[ dans\]
</dt> <dd>

Handle du fichier.

</dd> <dt>

*lpOverlapped* \[ dans, facultatif\]
</dt> <dd>

Pointeur vers une structure de données avec [**chevauchement**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) qui contient les données utilisées pour les e/s asynchrones.

Si ce paramètre a la **valeur null**, toutes les demandes d’e/s pour le paramètre *hFile* sont annulées.

Si ce paramètre n’est pas **null**, seules les demandes d’e/s spécifiques qui ont été émises pour le fichier avec la structure OVERLAPPED *lpOverlapped* spécifiée sont marquées comme annulées, ce qui signifie que vous pouvez annuler une ou plusieurs requêtes, tandis que la fonction [**CancelIo**](cancelio.md) annule toutes les demandes en suspens sur un descripteur de fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est différente de zéro. L’opération d’annulation pour toutes les opérations d’e/s en attente émises par le processus appelant pour le handle de fichier spécifié a été correctement demandée. L’application ne doit pas libérer ou réutiliser la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) associée aux opérations d’e/s annulées tant qu’elles n’ont pas été terminées. Le thread peut utiliser la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) pour déterminer à quel moment les opérations d’e/s ont elles-mêmes été effectuées.

Si la fonction échoue, la valeur de retour est 0 (zéro). Pour afficher les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Si cette fonction ne peut pas trouver de demande d’annulation, la valeur de retour est 0 (zéro), et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ introuvable**.

## <a name="remarks"></a>Notes

La fonction **CancelIoEx** vous permet d’annuler des requêtes dans des threads autres que le thread appelant. La fonction [**CancelIo**](cancelio.md) annule uniquement les demandes dans le thread qui a appelé la fonction **CancelIo** . **CancelIoEx** annule uniquement les e/s en suspens sur le handle, mais ne modifie pas l’état du descripteur. Cela signifie que vous ne pouvez pas compter sur l’état du handle, car vous ne pouvez pas savoir si l’opération a été effectuée avec succès ou a été annulée.

Si des opérations d’e/s en attente sont en cours pour le handle de fichier spécifié, la fonction **CancelIoEx** les marque pour l’annulation. La plupart des types d’opérations peuvent être annulés immédiatement ; d’autres opérations peuvent continuer à se terminer avant qu’elles ne soient réellement annulées et que l’appelant soit notifié. La fonction **CancelIoEx** n’attend pas que toutes les opérations annulées soient terminées.

Si le descripteur de fichier est associé à un port de terminaison, un paquet de terminaison d’e/s n’est pas mis en file d’attente vers le port si une opération synchrone est correctement annulée. Pour les opérations asynchrones toujours en attente, l’opération d’annulation met en file d’attente un paquet de terminaison d’e/s.

L’opération qui est annulée se termine avec l’un des trois États suivants : vous devez vérifier l’état d’achèvement pour déterminer l’état d’achèvement. Les trois États sont les suivants :

-   L’opération s’est terminée normalement. Cela peut se produire même si l’opération a été annulée, car la demande d’annulation n’a peut-être pas été envoyée dans le temps pour annuler l’opération.
-   L'opération a été annulée. La fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne une erreur indiquant que l’opération a été **\_ \_ abandonnée**.
-   L’opération a échoué avec une autre erreur. La fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur approprié.

Dans Windows 8 et Windows Server 2012, cette fonction est prise en charge par les technologies suivantes.



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
| Client minimal pris en charge<br/> | Applications de bureau Windows Vista- \[ \| applications UWP\]<br/>                                                                                                                                                                                                                   |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ \| apps UWP\]<br/>                                                                                                                                                                                                             |
| En-tête<br/>                   | <dl> <dt>IoAPI. h (inclure Windows. h); </dt> <dt>WinBase. h sur Windows server 2008 R2, Windows 7, Windows server 2008 et Windows Vista (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CancelIo**](cancelio.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[Annulation d’opérations d’e/s en attente](canceling-pending-i-o-operations.md)
</dt> <dt>

[Fonctions de gestion de fichiers](file-management-functions.md)
</dt> <dt>

[E/s synchrones et asynchrones](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

