---
description: Annule toutes les opérations d’entrée et de sortie (e/s) en attente émises par le thread appelant pour le fichier spécifié.
ms.assetid: b28162dc-0da8-41c6-9901-29381d2d72c4
title: CancelIo, fonction (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CancelIo
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-1.dll
- KernelBase.dll
- MinKernelBase.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: 900a47d51df882ce1f2931489ea93b5e3b4c498b8d5cc0f35e521e015e12c1d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075339"
---
# <a name="cancelio-function"></a>CancelIo fonction)

Annule toutes les opérations d’entrée et de sortie (e/s) en attente émises par le thread appelant pour le fichier spécifié. La fonction n’annule pas les opérations d’e/s émises par d’autres threads pour un handle de fichier.

Pour annuler les opérations d’e/s d’un autre thread, utilisez la fonction [**CancelIoEx**](cancelioex-func.md) .

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI CancelIo(
  _In_ HANDLE hFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hFile* \[ dans\]
</dt> <dd>

Handle du fichier.

La fonction annule toutes les opérations d’e/s en attente pour ce descripteur de fichier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est différente de zéro. L’opération d’annulation pour toutes les opérations d’e/s en attente émises par le thread appelant pour le handle de fichier spécifié a été correctement demandée. Le thread peut utiliser la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) pour déterminer à quel moment les opérations d’e/s ont elles-mêmes été effectuées.

Si la fonction échoue, la valeur de retour est zéro (0). Pour afficher les informations d’erreur étendues, appelez la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Remarques

Si des opérations d’e/s en cours sont en cours pour le handle de fichier spécifié et qu’elles sont émises par le thread appelant, la fonction **CancelIo** les annule. **CancelIo** annule uniquement les e/s en suspens sur le handle, mais ne modifie pas l’état du descripteur. Cela signifie que vous ne pouvez pas compter sur l’état du handle, car vous ne pouvez pas savoir si l’opération a été effectuée avec succès ou a été annulée.

Les opérations d’e/s doivent être émises en tant qu’e/s avec chevauchement. Si ce n’est pas le cas, les opérations d’e/s ne retournent pas pour permettre au thread d’appeler la fonction **CancelIo** . L’appel de la fonction **CancelIo** avec un descripteur de fichier qui n’est pas ouvert avec l' **indicateur de fichier \_ \_ OVERLAPPED** n’a aucun effet.

Toutes les opérations d’e/s qui sont annulées avec l’erreur erreur d’erreur ont été **\_ \_ annulées**, et toutes les notifications de fin d’exécution des opérations d’e/s se produisent normalement.

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
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP pour applications \[ \| UWP\]<br/>                                                                                                                                                                                                                                                       |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2003 \[ \| applications UWP\]<br/>                                                                                                                                                                                                                                              |
| En-tête<br/>                   | <dl> <dt>IoAPI. h (include Windows. h);</dt> <dt>WinBase. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 et Windows XP (include Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl>                                                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl>                                                                                                                                                                                                                  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CancelIoEx**](cancelioex-func.md)
</dt> <dt>

[**CancelSynchronousIo**](cancelsynchronousio-func.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[Fonctions de gestion de fichiers](file-management-functions.md)
</dt> <dt>

[**LockFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-lockfileex)
</dt> <dt>

[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile)
</dt> <dt>

[**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)
</dt> <dt>

[E/s synchrones et asynchrones](synchronous-and-asynchronous-i-o.md)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile)
</dt> <dt>

[**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)
</dt> </dl>

 

