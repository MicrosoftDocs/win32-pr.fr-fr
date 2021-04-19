---
description: Ajoute un autre nom de réseau local pour l’ordinateur à partir duquel il est appelé.
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: AddLocalAlternateComputerName fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 6027752a0e60f135f0cc8a1c0cdd536c59c09621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543287"
---
# <a name="addlocalalternatecomputername-function"></a>AddLocalAlternateComputerName fonction)

Ajoute un autre nom de réseau local pour l’ordinateur à partir duquel il est appelé.

## <a name="syntax"></a>Syntaxe


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpDnsFQHostname* \[ dans\]
</dt> <dd>

Autre nom à ajouter. Le nom doit être au format **ComputerNameDnsFullyQualified** , tel que défini dans l’énumération de [**\_ \_ format de nom d’ordinateur**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) , et la fonction [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) doit être en mesure de la valider avec son format défini sur **DnsNameHostnameFull**.

</dd> <dt>

*ulFlags* \[ dans\]
</dt> <dd>

Ce paramètre est réservé et doit avoir la valeur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la fonction retourne une **erreur de \_ réussite**. Si la fonction échoue, elle retourne un code d’erreur différent de zéro. Parmi les codes d’erreur qu’elle retourne, citons les suivantes :



| Code de retour                                                                                               | Description                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**paramètre d’erreur \_ non valide \_**</dt> </dl>  | Indique que le paramètre *lpDnsFQHostname* ne pointe pas vers un nom DNS valide ou que le paramètre *ulFlags* n’est pas égal à zéro.<br/> |
| <dl> <dt>**ERREUR \_ de \_ mémoire insuffisante \_**</dt> </dl> | La mémoire disponible est insuffisante pour terminer cette opération.<br/>                                                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| Bibliothèque<br/>                | <dl> <dt>Kernel32.lib</dt> </dl>               |
| DLL<br/>                    | <dl> <dt>Kernel32.dll</dt> </dl>               |
| Noms Unicode et ANSI<br/> | **AddLocalAlternateComputerNameW** (Unicode) et **AddLocalAlternateComputerNameA** (ANSI)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_format du nom de l’ordinateur \_**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 
