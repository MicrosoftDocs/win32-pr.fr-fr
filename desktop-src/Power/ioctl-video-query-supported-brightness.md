---
description: Récupère les niveaux de rétroéclairage pris en charge.
ms.assetid: b4c1ee3f-af75-477e-b7ed-53be905374d7
title: IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS le code de contrôle (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: a5618ec29fd47ba690106b5f826e6fb145eac208
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524650"
---
# <a name="ioctl_video_query_supported_brightness-control-code"></a>\_Code de \_ contrôle de \_ luminosité pris en charge \_ pour la requête de vidéo IOCTL

Récupère les niveaux de rétroéclairage pris en charge.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS,  // dwIoControlCode
  NULL,                            // lpInBuffer
  0,                               // nInBufferSize
  (LPVOID) lpOutBuffer,            // output buffer
  (DWORD) nOutBufferSize,          // size of output buffer
  (LPDWORD) lpBytesReturned,       // number of bytes returned
  (LPOVERLAPPED) lpOverlapped      // OVERLAPPED structure
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle de \\ \\ . \\ Appareil LCD. Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Code de contrôle de l’opération. Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter. Utilisez la luminosité de la **\_ requête de vidéo IOCTL \_ \_ prise en charge \_** pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Non utilisé avec cette opération ; Affectez la valeur **null**.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Non utilisé avec cette opération ; défini à zéro.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit un tableau des niveaux d’alimentation disponibles. Cette mémoire tampon doit avoir une longueur de 256 octets.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Taille de la mémoire tampon de sortie en octets.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Pointeur vers une variable qui reçoit la taille, en octets, des données de sortie retournées.

Si la mémoire tampon de sortie est trop petite pour retourner des données, l’appel échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur de code d’erreur \_ mémoire tampon insuffisante \_ et le nombre d’octets retournés est égal à zéro.

Si la mémoire tampon de sortie est trop petite pour contenir toutes les données mais peut contenir des entrées, le système d’exploitation retourne autant d’éléments que vous le souhaitez, l’appel échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur \_ plus de \_ données, et *lpBytesReturned* indique la quantité de données retournées. Votre application doit à nouveau appeler [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec la même opération, en spécifiant un nouveau point de départ.

Si *lpOverlapped* a la **valeur null** (e/s nonoverlapped), *lpBytesReturned* ne peut pas avoir la **valeur null**.

Si *lpOverlapped* n’a pas la **valeur null** (e/s avec chevauchement), *LpBytesReturned* peut avoir la **valeur null**. S’il s’agit d’une opération avec chevauchement, vous pouvez récupérer le nombre d’octets retournés en appelant la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Si *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Si *hDevice* a été ouvert avec l’indicateur de fichier avec \_ indicateur de \_ chevauchement, *lpOverlapped* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide. Dans ce cas, l’opération est exécutée en tant qu’opération Overlapped (asynchrone). Si l’appareil a été ouvert avec l’indicateur de fichier avec \_ indicateur \_ de chevauchement et que *LpOverlapped* a la **valeur null**, la fonction échoue de façon imprévisible.

Si *hDevice* a été ouvert sans que l’indicateur de fichier n’ait été spécifié \_ \_ , *lpOverlapped* est ignoré et [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ne retourne pas tant que l’opération n’est pas terminée, ou jusqu’à ce qu’une erreur se produise.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.

Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Chaque élément du tableau *lpOutBuffer* est d’une longueur d’un octet. Par conséquent, lors du retour, le paramètre *lpBytesReturned* indique le nombre de niveaux pris en charge. Chaque niveau est une valeur comprise entre 0 et 100. Plus la valeur est grande, plus le rétroéclairage est clair. Tous les niveaux sont pris en charge, que la source d’alimentation soit AC ou DC.

Le fichier d’en-tête utilisé pour créer des applications qui incluent cette fonctionnalité, Ntddvdeo. h, est inclus dans le kit de développement de pilotes (DDK) Microsoft Windows. Pour plus d’informations sur l’obtention du DDK, consultez [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Vous pouvez également définir ce code de contrôle comme suit :

``` syntax
#define IOCTL_VIDEO_QUERY_SUPPORTED_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x125, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                   |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Ntddvdeo. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interface de contrôle de rétroéclairage](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> </dl>

 

