---
description: Publie un paquet de terminaison d’e/s sur un port de terminaison d’e/s.
ms.assetid: 69a9b1e5-2d40-42de-a14a-f7b6f29bf571
title: PostQueuedCompletionStatus, fonction (IoAPI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostQueuedCompletionStatus
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-io-l1-1-0.dll
- KernelBase.dll
- MinKernelBase.dll
- API-MS-Win-Core-io-l1-1-1.dll
- api-ms-win-downlevel-kernel32-l1-1-0.dll
ms.openlocfilehash: e56bad8b9de85f22836f9446b67340d22e71fe83552da6796e7864d3baddae4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683359"
---
# <a name="postqueuedcompletionstatus-function"></a>PostQueuedCompletionStatus fonction)

Publie un paquet de terminaison d’e/s sur un port de terminaison d’e/s.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI PostQueuedCompletionStatus(
  _In_     HANDLE       CompletionPort,
  _In_     DWORD        dwNumberOfBytesTransferred,
  _In_     ULONG_PTR    dwCompletionKey,
  _In_opt_ LPOVERLAPPED lpOverlapped
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CompletionPort* \[ dans\]
</dt> <dd>

Handle vers un port de terminaison d’e/s sur lequel le paquet d’achèvement d’e/s doit être publié.

</dd> <dt>

*dwNumberOfBytesTransferred* \[ dans\]
</dt> <dd>

Valeur à retourner via le paramètre *lpNumberOfBytesTransferred* de la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*dwCompletionKey* \[ dans\]
</dt> <dd>

Valeur à retourner via le paramètre *lpCompletionKey* de la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* \[ dans, facultatif\]
</dt> <dd>

Valeur à retourner via le paramètre *lpOverlapped* de la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro. Pour afficher les informations d’erreur étendues, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

## <a name="remarks"></a>Remarques

Le paquet d’achèvement d’e/s répondra à un appel en suspens de la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) . Cette fonction retourne avec les trois valeurs passées comme deuxième, troisième et quatrième paramètres de l’appel à **PostQueuedCompletionStatus**. Le système n’utilise pas ou ne valide pas ces valeurs. En particulier, le paramètre *lpOverlapped* n’a pas besoin de pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

dans Windows 8 et Windows Server 2012, cette fonction est prise en charge par les technologies suivantes.



| Technology                                           | Pris en charge      |
|------------------------------------------------------|----------------|
| Protocole SMB (Server Message Block) 3,0<br/>   | Oui<br/> |
| Basculement transparent SMB 3,0 (TFO)<br/>        | Oui<br/> |
| SMB 3,0 avec des partages de fichiers avec montée en puissance parallèle (SO)<br/>   | Oui<br/> |
| Système de fichiers Volume partagé de cluster (CsvFS)<br/> | Oui<br/> |
| Système de fichiers résilient (ReFS)<br/>              | Oui<br/> |



 

CsvFs effectue une redirection des e/s pour les fichiers compressés.

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

[**CreateIoCompletionPort**](createiocompletionport.md)
</dt> <dt>

[Fonctions de gestion de fichiers](file-management-functions.md)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**AVEC chevauchement**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped)
</dt> </dl>

 

