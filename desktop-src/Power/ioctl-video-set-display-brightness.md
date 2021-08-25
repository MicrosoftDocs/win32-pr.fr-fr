---
description: Définit les niveaux de rétroéclairage AC et DC actuels.
ms.assetid: baa77811-046d-4a07-b3df-2a31fba2d9a7
title: IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS le code de contrôle (Ntddvdeo. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS
api_type:
- HeaderDef
api_location:
- Ntddvdeo.h
ms.openlocfilehash: ec4bb5200378f9f530913f26d33bfbd485d81ae184c7b478a51c90bca18d95da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961849"
---
# <a name="ioctl_video_set_display_brightness-control-code"></a>\_Code de \_ contrôle de luminosité d' \_ affichage du jeu vidéo IOCTL \_

Définit les niveaux de rétroéclairage AC et DC actuels.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to device
  IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS, // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of the input buffer
  NULL,                        // lpOutBuffer
  0,                           // nOutBufferSize 
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped  // OVERLAPPED structure
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

Code de contrôle de l’opération. Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter. Utilisez la luminosité de l' **\_ affichage du jeu de vidéos \_ \_ \_ IOCTL** pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Pointeur vers une structure [**de \_ luminosité d’affichage**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) .

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Taille de la mémoire tampon vers laquelle pointe *lpOutBuffer*, en octets.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Non utilisé avec cette opération ; Affectez la valeur **null**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Non utilisé avec cette opération ; défini à zéro.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre réel d’octets retournés par la fonction dans la mémoire tampon de sortie.

Si *lpOverlapped* a la **valeur null** (e/s nonoverlapped), *lpBytesReturned* est utilisé en interne et ne peut pas avoir la **valeur null**.

Si *lpOverlapped* n’a pas la **valeur null** (e/s avec chevauchement), *LpBytesReturned* peut avoir la **valeur null**.

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

Les valeurs spécifiées dans les membres **ucACBrightness** et **ucDCBrightness** de la structure de [**\_ luminosité d’affichage**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85)) doivent avoir été retournées par la luminosité de la [**\_ requête vidéo IOCTL \_ \_ prise en charge \_**](ioctl-video-query-supported-brightness.md). Par exemple, si les valeurs prises en charge sont 10, 20, 30, 40, 50, 60, 70, 80, 90 et 100, l’utilisation d’une valeur de 33 serait une erreur.

le fichier d’en-tête utilisé pour créer des applications qui incluent cette fonctionnalité, Ntddvdeo. h, est inclus dans Microsoft Windows Driver Development Kit (DDK). Pour plus d’informations sur l’obtention du DDK, consultez [https://www.microsoft.com/whdc/devtools/ddk/default.mspx](https://msdn.microsoft.com/windows/hardware/gg454513) .

Vous pouvez également définir ce code de contrôle comme suit :

``` syntax
#define IOCTL_VIDEO_SET_DISPLAY_BRIGHTNESS \
  CTL_CODE(FILE_DEVICE_VIDEO, 0x127, METHOD_BUFFERED, FILE_ANY_ACCESS)
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista, Windows XP avec les \[ applications de bureau SP1 uniquement\]<br/>                   |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Ntddvdeo. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interface de contrôle de rétroéclairage](backlight-control-interface.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**luminosité de l’affichage \_**](/previous-versions/windows/desktop/legacy/aa372686(v=vs.85))
</dt> <dt>

[**luminosité de l' \_ \_ affichage des requêtes vidéo \_ IOCTL \_**](ioctl-video-query-display-brightness.md)
</dt> <dt>

[**\_ \_ \_ luminosité prise en charge des requêtes de vidéo IOCTL \_**](ioctl-video-query-supported-brightness.md)
</dt> </dl>

 

