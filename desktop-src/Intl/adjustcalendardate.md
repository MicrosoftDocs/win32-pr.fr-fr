---
description: Obsolète. Ajuste une date d’un nombre spécifié d’années, de mois, de semaines ou de jours.
ms.assetid: be8d61fd-efa3-4386-969f-30216c282ebc
title: AdjustCalendarDate fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdjustCalendarDate
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 061d0e246f7839345b0f1e55221d26d276f52af4997a7cb47d62b680d2638fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520619"
---
# <a name="adjustcalendardate-function"></a>AdjustCalendarDate fonction)

Action déconseillée. Ajuste une date d’un nombre spécifié d’années, de mois, de semaines ou de jours.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AdjustCalendarDate(
  _Inout_ LPCALDATETIME        lpCalDateTime,
  _In_    CALDATETIME_DATEUNIT calUnit,
  _Out_   INT                  amount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpCalDateTime* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**CALDATETIME**](caldatetime.md) qui contient les informations de date et de calendrier à ajuster.

</dd> <dt>

*calUnit* \[ dans\]
</dt> <dd>

Valeur d’énumération [**CALDATETIME \_ DATEUNIT**](caldatetime-dateunit.md) indiquant l’unité de date, par exemple, DayUnit.

</dd> <dt>

*quantité* \[ à\]
</dt> <dd>

Valeur d’ajustement de la date spécifiée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire. Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :

-   \_date \_ d’erreur \_ hors \_ limites. La date spécifiée était hors limites.
-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de fichier d’en-tête ou de fichier de bibliothèque associé. L’application peut appeler [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Kernel32.dll) pour obtenir un handle de module. Il peut ensuite appeler [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec le handle de module et le nom de cette fonction pour récupérer l’adresse de la fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des langues nationales](national-language-support.md)
</dt> <dt>

[Fonctions de prise en charge linguistique nationale](national-language-support-functions.md)
</dt> <dt>

[NLS : exemple d’API basées sur un nom](nls--name-based-apis-sample.md)
</dt> </dl>

 

 
