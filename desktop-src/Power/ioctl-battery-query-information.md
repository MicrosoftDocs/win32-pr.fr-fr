---
description: Récupère diverses informations pour la batterie.
ms.assetid: 4cc89b89-ab33-47c2-8327-9627cbd1595e
title: IOCTL_BATTERY_QUERY_INFORMATION le code de contrôle (Poclass. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IOCTL_BATTERY_QUERY_INFORMATION
api_type:
- HeaderDef
api_location:
- Poclass.h
- BatClass.h
ms.openlocfilehash: ee4010e055686c0df2987c34b48b133975b434ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007155"
---
# <a name="ioctl_battery_query_information-control-code"></a>\_Code de \_ contrôle des \_ informations sur les requêtes de batterie IOCTL

Récupère diverses informations pour la batterie.

Pour effectuer cette opération, appelez la fonction [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) avec les paramètres suivants.


```C++
BOOL DeviceIoControl(
  (HANDLE) hDevice,                // handle to battery
  IOCTL_BATTERY_QUERY_INFORMATION, // dwIoControlCode
  (LPVOID) lpInBuffer,             // input buffer
  (DWORD) nInBufferSize,           // size of input buffer
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

Handle vers la batterie sur laquelle les informations doivent être retournées. Pour récupérer un handle d’appareil, appelez la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

</dd> <dt>

*dwIoControlCode* 
</dt> <dd>

Code de contrôle de l’opération. Cette valeur identifie l’opération spécifique à effectuer et le type d’appareil sur lequel l’exécuter. Utilisez **les \_ \_ \_ informations de requête de batterie IOCTL** pour cette opération.

</dd> <dt>

*lpInBuffer* 
</dt> <dd>

Pointeur vers une structure [**d' \_ \_ informations de requête de batterie**](battery-query-information-str.md) .

</dd> <dt>

*nInBufferSize* 
</dt> <dd>

Taille de la mémoire tampon d’entrée, en octets.

</dd> <dt>

*lpOutBuffer* 
</dt> <dd>

Pointeur vers la mémoire tampon de retour. Le type de données (et, par conséquent, la taille) de la mémoire tampon de retour dépend des informations demandées dans le membre du niveau d’informations de la requête de batterie de la structure d' [**\_ \_ informations sur les requêtes**](battery-query-information-str.md) de la batterie d’entrée. **\_ \_ \_**

Le tableau suivant présente les données retournées par un niveau d’information donné.



| Niveau d’information                 | Données retournées                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BatteryDeviceName**             | Chaîne Unicode terminée par le caractère **null** qui spécifie le nom de la batterie.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **BatteryEstimatedTime**          | **ULong** qui spécifie la durée d’exécution estimée de la batterie, en secondes. Si le taux de drainage fourni dans le membre **AtRate** de la structure d' [**\_ \_ informations sur les requêtes**](battery-query-information-str.md) de la batterie est égal à zéro, ce calcul est basé sur le taux de drainage actuel. Si **AtRate** est différent de zéro, l’heure retournée correspond à la durée d’exécution attendue pour le taux donné. Si la durée estimée est inconnue (par exemple, si la batterie n’est pas en charge et que **AtRate** est égal à zéro), une **durée de batterie \_ inconnue \_** est retournée. Notez que cette valeur n’est pas très précise sur certains systèmes de batterie. La valeur peut varier considérablement en fonction de l’utilisation actuelle de l’alimentation, ce qui peut être affecté par l’activité du disque et d’autres facteurs. Il n’existe aucun mécanisme de notification pour les modifications de cette valeur. |
| **BatteryGranularityInformation** | Tableau de longueur variable de la [**batterie \_ signalant \_**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale) les structures d’échelle qui contient la granularité des rapports pour la capacité de la batterie qui est retournée par l’état de la [**\_ \_ requête \_ de batterie IOCTL**](ioctl-battery-query-status.md). Plusieurs entrées sont retournées lorsque la granularité dépend de la capacité actuelle de la batterie. Consultez Mise à l' **\_ \_ échelle des rapports de batterie** pour l’interprétation du tableau d’entrées. Le nombre d’entrées est indiqué par la taille de la mémoire tampon retournée et peut être calculé comme suit : (*lpBytesReturned* /sizeof (**\_ \_ Scale Reporting Scale**)). Le nombre maximal d’entrées qui sera retourné est de quatre.                                                                                                |
| **BatteryInformation**            | Structure [**d' \_ informations sur la batterie**](battery-information-str.md) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **BatteryManufactureDate**        | Structure [**de \_ \_ Date**](battery-manufacture-date-str.md) de la fabrication d’une batterie.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **BatteryManufactureName**        | Chaîne Unicode terminée par le caractère **null** qui contient le nom du fabricant de la batterie.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatterySerialNumber**           | Chaîne Unicode terminée par le caractère **null** qui contient le numéro de série de la batterie.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **BatteryTemperature**            | **ULong** qui contient la température actuelle de la batterie, en dixièmes de degré Kelvin.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **BatteryUniqueID**               | Chaîne Unicode terminée par le caractère **null** qui identifie de façon unique la batterie. Cette valeur peut être utilisée pour effectuer le suivi d’une batterie spécifique. Dans le cas de batteries intelligentes, cet ID correspond à la concaténation du nom du fabricant, du nom de l’appareil, de la date de fabrication et d’une représentation imprimable du numéro de série. Cette valeur n’est pas destinée à être affichée à l’utilisateur.<br/>                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*nOutBufferSize* 
</dt> <dd>

Taille de la mémoire tampon de sortie en octets. En fonction du niveau d’information des données demandées, il peut s’agir d’une mémoire tampon de taille variable.

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

Certaines informations sur les batteries sont facultatives ou n’ont pas de sens pour certaines batteries. Si le type de données particulier demandé n’est pas disponible pour la batterie actuelle, **la \_ \_ fonction d’erreur non valide** est retournée.

Toutes les demandes d’informations sur la batterie se terminent avec l’état **fichier d’erreur \_ \_ \_ introuvable** chaque fois que l’élément **BatteryTag** de la demande ne correspond pas à celui de la balise de batterie actuelle. Cela permet de s’assurer que les informations sur la batterie retournée correspondent à celles de la batterie demandée. (Pour plus d’informations, consultez [balises de batterie](battery-information.md) .)

## <a name="remarks"></a>Notes

Cette IOCTL de batterie récupère diverses informations pour la batterie. La structure des paramètres d’entrée, les [**\_ \_ informations sur les requêtes**](battery-query-information-str.md)de la batterie, indiquent le type d’informations à retourner et le moment où les informations sur la batterie doivent être retournées. Le type de données et le contenu de la mémoire tampon de sortie varient en fonction des données demandées.

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

[**\_informations sur la requête de batterie \_**](battery-query-information-str.md)
</dt> <dt>

[**mise à l’échelle de la batterie \_ \_**](/windows/desktop/api/WinNT/ns-winnt-battery_reporting_scale)
</dt> <dt>

[**État de la \_ requête de batterie IOCTL \_ \_**](ioctl-battery-query-status.md)
</dt> <dt>

[**\_ \_ balise de requête de batterie IOCTL \_**](ioctl-battery-query-tag.md)
</dt> <dt>

[**\_ \_ informations sur le jeu de batteries IOCTL \_**](ioctl-battery-set-information.md)
</dt> </dl>

 

