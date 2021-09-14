---
description: Obsolète. Obtient le jour de la semaine qui correspond à un jour spécifié et remplit le membre DayOfWeek dans la structure CALDATETIME spécifiée avec cette valeur.
ms.assetid: b9ae250a-73bb-4ec2-bb0d-e1f8b25c173c
title: UpdateCalendarDayOfWeek fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateCalendarDayOfWeek
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 316af539e6ca0476f0f8d575a160fcd7c3219e90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224116"
---
# <a name="updatecalendardayofweek-function"></a>UpdateCalendarDayOfWeek fonction)

Action déconseillée. Obtient le jour de la semaine qui correspond à un jour spécifié et remplit le membre **DayOfWeek** dans la structure [**CALDATETIME**](caldatetime.md) spécifiée avec cette valeur.

## <a name="syntax"></a>Syntaxe


```C++
BOOL UpdateCalendarDayOfWeek(
  _Inout_ LPCALDATETIME lpCalDateTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpCalDateTime* \[ in, out\]
</dt> <dd>

Pointeur vers la structure [**CALDATETIME**](caldatetime.md) contenant la date pour laquelle définir le jour de la semaine.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire. Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :

-   \_date \_ d’erreur \_ hors \_ limites. La date spécifiée était hors limites.
-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de fichier d’en-tête ou de fichier de bibliothèque associé. L’application peut appeler [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Kernel32.dll) pour obtenir un handle de module. Il peut ensuite appeler [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec ce handle de module et le nom de cette fonction pour recevoir l’adresse de la fonction.

## <a name="requirements"></a>Spécifications



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

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 
