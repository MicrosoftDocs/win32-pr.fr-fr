---
description: Récupère l’état actuel de la batterie.
ms.assetid: 7a7bf429-9b2c-4faf-9f27-fb5fd8dd18df
title: IOCTL_BATTERY_QUERY_STATUS le code de contrôle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_STATUS
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: e2de9d3ab48aec13a9a5c1957a5f98aefbe6a09f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007151"
---
# <a name="ioctl_battery_query_status-control-code"></a>\_Code de \_ contrôle d' \_ État de la requête IOCTL

Récupère l’état actuel de la batterie.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,           // handle to battery
  IOCTL_BATTERY_QUERY_STATUS, // dwIoControlCode
  (LPVOID) lpInBuffer,        // input buffer
  (DWORD) nInBufferSize,      // size of input buffer
  (LPVOID) lpOutBuffer,       // output buffer
  (DWORD) nOutBufferSize,     // size of output buffer
  (LPDWORD) lpBytesReturned,  // number of bytes returned
  (LPOVERLAPPED) lpOverlapped // OVERLAPPED structure
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle de la batterie à partir de laquelle les informations doivent être retournées. Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Code de contrôle de l’opération. Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter. Utilisez l’état de la **\_ requête de batterie \_ \_ IOCTL** pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Pointeur vers une structure [**d' \_ \_ État d’attente**](battery-wait-status-str.md) de la batterie.

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Taille de la mémoire tampon d’entrée, en octets.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Pointeur vers une structure [**d' \_ État**](battery-status-str.md) de la batterie.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Taille de la mémoire tampon de sortie en octets.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Pointeur vers une variable qui reçoit la taille des données retournées dans la mémoire tampon *lpOutBuffer* , en octets.

Si la mémoire tampon de sortie est trop petite pour retourner des données, alors l’appel échoue, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur de code d’erreur **\_ \_ mémoire tampon insuffisante** et le nombre d’octets retourné est égal à zéro.

Si *lpOverlapped* a la **valeur null** (e/s nonoverlapped), *lpBytesReturned* ne peut pas avoir la **valeur null**.

Si *lpOverlapped* n’a pas la **valeur null** (e/s avec chevauchement), *LpBytesReturned* peut avoir la **valeur null**. S’il s’agit d’une opération avec chevauchement, vous pouvez récupérer le nombre d’octets retournés en appelant la fonction [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) . Si *hDevice* est associé à un port de terminaison d’e/s, vous pouvez récupérer le nombre d’octets renvoyés en appelant la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .

</dd> <dt>

*lpOverlapped* 
</dt> <dd>

Pointeur vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .

Si *hDevice* a été ouvert avec l’indicateur de **fichier avec indicateur de \_ \_ chevauchement** , *LPOVERLAPPED* doit pointer vers une structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) valide. Dans ce cas, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) est exécuté comme une opération Overlapped (asynchrone). Si l’appareil a été ouvert avec l’indicateur de **fichier avec \_ indicateur de \_ chevauchement** et que *lpOverlapped* a la **valeur null**, la fonction échoue de façon imprévisible.

Si *hDevice* a été ouvert sans que l’indicateur de fichier n’ait été spécifié, *lpOverlapped* est ignoré et la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) ne retourne pas tant que l’opération n’est pas terminée, soit jusqu’à ce qu’une erreur se produise. **\_ \_**

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.

Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Cette IOCTL de batterie récupère l’état de la batterie au moment où l’opération est retournée. La structure du paramètre d’entrée, l' [**\_ \_ État d’attente**](battery-wait-status-str.md)de la batterie, indique quand l’état de la batterie doit être traité et retourné.

Les demandes d’état de la batterie peuvent être pour un retour immédiat ou peuvent être définies pour attendre une condition particulière avant de se terminer. Par exemple, une demande d’informations sur la batterie peut être effectuée, qui attend que la capacité de la batterie atteigne un point spécifié ou que l’état de la batterie change.

Toutes les demandes d’informations sur la batterie se terminent avec l’état **fichier d’erreur \_ \_ \_ introuvable** chaque fois que l’élément **BatteryTag** de la demande ne correspond pas à celui de la balise de batterie actuelle. (Pour plus d’informations, consultez [balises de batterie](battery-information.md) .) Cela permet de s’assurer que les informations sur la batterie retournée correspondent à celles de la batterie demandée.

Pour connaître les implications des e/s avec chevauchement sur cette opération, consultez la section Notes de la rubrique [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez [énumération des unités de batterie](enumerating-battery-devices.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                                                                                                                                                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                                                                                                                                                                                |
| En-tête<br/>                   | <dl> <dt>Poclass. h ;</dt> <dt>BatClass. h sur Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows server 2003 et Windows XP</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Informations sur la batterie](battery-information.md)
</dt> <dt>

[Codes de contrôle de gestion de l’alimentation](power-management-control-codes.md)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**État de la batterie \_**](battery-status-str.md)
</dt> <dt>

[**\_État d’attente de la batterie \_**](battery-wait-status-str.md)
</dt> <dt>

[**\_ \_ informations sur les requêtes de batterie IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**\_ \_ balise de requête de batterie IOCTL \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**\_ \_ informations sur le jeu de batteries IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

