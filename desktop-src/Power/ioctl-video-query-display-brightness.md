---
description: Récupère les niveaux de rétroéclairage AC et DC actuels et l’état d’alimentation actuel.
ms.assetid: c7b7c302-6e92-46a7-b9a6-e3f2a3e44d1b
title: IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS le code de contrôle (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: 547501a28492aecfe06f63f95b0e007fc80d3d02
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007144"
---
# <a name="ioctl_video_query_display_brightness-control-code"></a>Code de contrôle de luminosité de l' \_ \_ affichage des requêtes vidéo \_ IOCTL \_

\[Ce code de contrôle peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise. la prise en charge de ce code de contrôle a été supprimée dans Windows Server 2008 et Windows Vista. Utilisez la classe [**WmiMonitorBrightness**](/windows/desktop/WmiCoreProv/wmimonitorbrightness) à la place.\]

Récupère les niveaux de rétroéclairage AC et DC actuels et l’état d’alimentation actuel.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to device
  IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS,  // dwIoControlCode
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

Code de contrôle de l’opération. Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter. Utilisez la luminosité de l' **\_ \_ \_ affichage \_ des requêtes vidéo IOCTL** pour cette opération.

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

Pointeur vers une mémoire tampon qui reçoit une structure [**de \_ luminosité**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) de l’affichage.

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

## <a name="return-value"></a>Valeur de retour

Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.

Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

le fichier d’en-tête utilisé pour créer des applications qui incluent cette fonctionnalité, Ntddvdeo. h, est inclus dans Microsoft Windows Driver Development Kit (DDK). Pour plus d’informations sur l’obtention du DDK, consultez [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Vous pouvez également définir ce code de contrôle comme suit :

``` syntax
#define IOCTL_VIDEO_QUERY_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x126, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| Fin de la prise en charge des clients<br/>    | Windows XP SP2<br/>                                                        |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003 R2<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Ntddvdeo. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interface de contrôle de rétroéclairage](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**luminosité de l’affichage \_**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**luminosité de l’affichage du jeu de \_ vidéos IOCTL \_ \_ \_**](ioctl-video-set-display-brightness.md)
</dt> </dl>

 

