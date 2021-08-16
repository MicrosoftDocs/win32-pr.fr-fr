---
description: Le code de contrôle de mise en \_ \_ \_ mémoire tampon locale d’IOCTL LMR désactive \_ la mise en cache en mémoire côté client locale des données lors de la lecture ou de l’écriture de données dans un fichier distant. Il s’agit d’un code de contrôle défini en interne qui n’est pas disponible dans un en-tête public.
ms.assetid: a464671b-253c-4f35-84a2-2619cb15b009
title: Code de contrôle IOCTL_LMR_DISABLE_LOCAL_BUFFERING
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COPY_CHUNK
api_type:
- NA
api_location: ''
ms.openlocfilehash: 88a6fff0955fb9e0c57c7ea5fae99f532c7c6d4dcc3578a75e07da3f35867f9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117827183"
---
# <a name="ioctl_lmr_disable_local_buffering-control-code"></a>\_LMR IOCTL \_ désactiver \_ \_ le code de contrôle de mise en mémoire tampon locale

Le code de contrôle de mise en **\_ \_ \_ \_ mémoire tampon locale d’IOCTL LMR** désactive la mise en cache en mémoire côté client locale des données lors de la lecture ou de l’écriture de données dans un fichier distant. Il s’agit d’un code de contrôle défini en interne qui n’est pas disponible dans un en-tête public.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,             // handle to device
  IOCTL_LMR_DISABLE_LOCAL_BUFFERING, // dwIoControlCode
  (LPVOID) NULL,                // lpInBuffer
  (DWORD) 0,                    // nInBufferSize
  (LPVOID) NULL,                // lpOutBuffer
  (DWORD) 0,                    // nOutBufferSize
  (LPDWORD) lpBytesReturned,    // number of bytes returned
  (LPOVERLAPPED) lpOverlapped   // OVERLAPPED structure
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* \[ dans\]
</dt> <dd>

Handle du fichier distant. Pour obtenir ce descripteur, appelez la fonction [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* \[ dans\]
</dt> <dd>

Code de contrôle de l’opération. Utilisez la valeur 0x140390 pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilisé, doit avoir la **valeur null**.

</dd> <dt>

*nInBufferSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon d’entrée, en octets. Doit être zéro.

</dd> <dt>

*lpOutBuffer* \[ à\]
</dt> <dd>

Non utilisé, doit avoir la **valeur null**.

</dd> <dt>

*nOutBufferSize* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon de sortie en octets. Doit être zéro.

</dd> <dt>

*lpBytesReturned* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon de sortie, en octets.

Si la mémoire tampon de sortie est trop petite, l’appel échoue, la fonction [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l' **erreur \_ \_ mémoire tampon insuffisante** et *lpBytesReturned* est égal à zéro.

Si le paramètre *lpOverlapped* a la **valeur null**, *lpBytesReturned* ne peut pas avoir la **valeur null**. Même lorsqu’une opération ne retourne aucune donnée de sortie et que le paramètre *lpOutBuffer* a la **valeur null**, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) utilise *lpBytesReturned*. Après une telle opération, la valeur de *lpBytesReturned* est sans signification.

Si *lpOverlapped* n’a pas la **valeur null**, *LpBytesReturned* peut avoir la **valeur null**. Si *lpOverlapped* n’a pas la **valeur null** et que l’opération retourne des données, *lpBytesReturned* n’a aucun sens tant que l’opération avec chevauchement n’est pas terminée. Pour récupérer le nombre d’octets retournés, appelez la fonction [**GetOverlappedResult**](/windows/win32/api/ioapiset/nf-ioapiset-getoverlappedresult) . Si le paramètre *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) .

Si le paramètre *hDevice* a été ouvert sans spécifier d' **indicateur de fichier avec \_ \_ chevauchement**, *lpOverlapped* est ignoré.

Si *hDevice* a été ouvert avec l’indicateur de fichier avec l' **indicateur de \_ \_ chevauchement** , l’opération est exécutée en tant qu’opération Overlapped (asynchrone). Dans ce cas, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) valide qui contient un handle vers un objet d’événement. Dans le cas contraire, la fonction échoue de façon imprévisible.

Pour les opérations avec chevauchement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne immédiatement, et l’objet d’événement est signalé lorsque l’opération est terminée. Sinon, la fonction ne retourne pas jusqu’à ce que l’opération soit terminée ou jusqu’à ce qu’une erreur se produise.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération se termine correctement, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.

Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Le code de contrôle de **\_ mise en \_ \_ \_ mémoire tampon locale d’IOCTL LMR** est défini en interne par le système en tant que 0x140390 et non dans un fichier d’en-tête public. Il est utilisé par les applications à usage spécifique pour désactiver la mise en cache en mémoire côté client locale des données lors de la lecture ou de l’écriture de données dans un fichier distant. Une fois la mise en mémoire tampon locale désactivée, le paramètre reste en vigueur jusqu’à la fermeture de tous les descripteurs ouverts du fichier et le redirecteur nettoie ses structures de données internes.

Les applications à usage général ne doivent pas utiliser les **\_ LMR IOCTL \_ désactivent la \_ mise en \_ mémoire tampon locale**, car cela peut entraîner un trafic réseau excessif et une perte de performances. Le code de contrôle de **\_ mise en \_ \_ \_ mémoire tampon locale d’IOCTL LMR** doit être utilisé uniquement dans les applications spécialisées qui déplacent de grandes quantités de données sur le réseau tout en tentant d’optimiser l’utilisation de la bande passante réseau. Par exemple, les fonctions [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile) et [**CopyFileEx**](/windows/win32/api/winbase/nf-winbase-copyfileexa) utilisent **les \_ LMR IOCTL \_ désactivent la \_ mise en \_ mémoire tampon locale** pour améliorer les performances de copie de fichiers volumineux.

**IOCTL \_ La \_ désactivation de la \_ \_ mise en mémoire tampon locale LMR** n’est pas implémentée par les systèmes de fichiers locaux et échoue avec la fonction erreur erreur **\_ non valide \_**. L’émission du code de contrôle de **\_ mise en \_ \_ \_ mémoire tampon locale d’IOCTL LMR** sur les handles de répertoires distants échouera avec l’erreur erreur **\_ non \_ prise en charge**.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

 
