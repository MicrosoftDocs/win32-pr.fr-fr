---
description: Obsolète. Convertit une structure CALDATETIME spécifiée en une structure SYSTEMTIME.
ms.assetid: 0c3f602d-62de-4c27-95d9-d35738f3279d
title: ConvertCalDateTimeToSystemTime fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertCalDateTimeToSystemTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 9c317a31904e2d1b0b2110f6b2dc367ac3e2e0c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127240408"
---
# <a name="convertcaldatetimetosystemtime-function"></a>ConvertCalDateTimeToSystemTime fonction)

Action déconseillée. Convertit une structure [**CALDATETIME**](caldatetime.md) spécifiée en une structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) .

## <a name="syntax"></a>Syntaxe


```C++
BOOL ConvertCalDateTimeToSystemTime(
  _In_  const LPCALDATETIME lpCalDateTime,
  _Out_       SYSTEMTIME    *lpSysTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpCalDateTime* \[ dans\]
</dt> <dd>

Pointeur vers la structure [**CALDATETIME**](caldatetime.md) à convertir.

</dd> <dt>

*lpSysTime* \[ à\]
</dt> <dd>

Pointeur vers la structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) équivalente.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire. Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :

-   \_date \_ d’erreur \_ hors \_ limites. La date spécifiée était hors limites.
-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de fichier d’en-tête ou de fichier de bibliothèque associé. L’application peut appeler [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Kernel32.dll) pour obtenir un handle de module. Il peut ensuite appeler [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec le handle de module et le nom de cette fonction pour récupérer l’adresse de la fonction.

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

[Récupération des informations de date et d’heure](time-and-date.md)
</dt> </dl>

 

 
