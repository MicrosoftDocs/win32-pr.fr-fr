---
description: Récupère la balise actuelle des piles.
ms.assetid: 0bbe59ba-e037-47ce-a54a-6500ea7c9bc5
title: IOCTL_BATTERY_QUERY_TAG le code de contrôle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_TAG
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: c68c9dc2385803155a6c0f8fd2a5b7c84cedaa8e78c98ae2baca6909104e7315
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143512"
---
# <a name="ioctl_battery_query_tag-control-code"></a>\_Code de \_ contrôle de balise de requête de batterie IOCTL \_

Récupère la balise actuelle de la batterie.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,            // handle to battery
  IOCTL_BATTERY_QUERY_TAG,     // dwIoControlCode
  (LPVOID) lpInBuffer,         // input buffer
  (DWORD) nInBufferSize,       // size of input buffer
  (LPVOID) lpOutBuffer,        // output buffer
  (DWORD) nOutBufferSize,      // size of output buffer
  (LPDWORD) lpBytesReturned,   // number of bytes returned
  (LPOVERLAPPED) lpOverlapped);// OVERLAPPED structure
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle de la batterie à partir de laquelle la balise doit être récupérée. Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Code de contrôle de l’opération. Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter. Utilisez **la \_ \_ \_ balise de requête de batterie IOCTL** pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Pointeur vers une mémoire tampon d’entrée **ULong** . La valeur indique le nombre de millisecondes à attendre s’il n’y a aucune batterie. La valeur-1 indique que la demande attend indéfiniment (ou jusqu’à ce qu’elle soit annulée par un autre événement).

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Taille de la mémoire tampon d’entrée, en octets.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Pointeur vers une mémoire tampon de sortie **ULong** . En cas de réussite, cette mémoire tampon contient la balise de batterie actuelle, qui peut être toute valeur à l’exception de la \_ balise de batterie \_ non valide. En cas d’échec, si [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le fichier d’erreur de code d’erreur **\_ \_ \_ introuvable**, cette mémoire tampon contient la **balise de batterie de valeur \_ \_ non valide**.

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Taille de la mémoire tampon de sortie en octets.

</dd> <dt>

*lpBytesReturned* 
</dt> <dd>

Pointeur vers une variable qui reçoit la taille des données stockées dans la mémoire tampon *lpOutBuffer* , en octets.

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

## <a name="return-value"></a>Valeur retournée

Si l’opération se termine correctement, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne une valeur différente de zéro.

Si l’opération échoue ou est en attente, [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) retourne la valeur zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Cette IOCTL de batterie récupère la balise actuelle de la batterie. La balise de batterie est une valeur différente de zéro unique qui change lorsque la batterie physique est réinsérée, remplacée ou subit des modifications caractéristiques. Consultez la section balises de batterie dans la rubrique vue d’ensemble des informations sur la batterie pour plus d' [informations](battery-information.md) sur la modification d’une balise de batterie, sur la façon de détecter la modification et sur la manière dont une application doit se poursuivre après une modification de la balise de batterie. Lorsqu’une batterie n’est pas présente, cette demande attend l’heure indiquée et, si aucune batterie n’est présente, elle retourne le fichier d' **erreur \_ \_ \_ introuvable** et définit la balise de batterie sur la **\_ balise de batterie \_ non valide**. (Pour plus d’informations, consultez les informations relatives à la batterie.)

Toutes les demandes d’autres informations sur la batterie requièrent que l’appelant fournisse la balise de batterie correspondante. Cela garantit que l’appelant reçoit des informations pour la même batterie pour chaque demande et s’assure que l’appelant est conscient des modifications de la batterie sans interrogation constante.

Pour connaître les implications des e/s avec chevauchement sur cette opération, consultez la section Notes de la rubrique [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez [énumération des unités de batterie](enumerating-battery-devices.md).

## <a name="requirements"></a>Configuration requise



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

[**\_ \_ informations sur les requêtes de batterie IOCTL \_**](ioctl-battery-query-information.md)
</dt> <dt>

[**État de la \_ requête de batterie IOCTL \_ \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_ \_ informations sur le jeu de batteries IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

