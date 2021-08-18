---
description: Obsolète. Convertit une structure SYSTEMTIME spécifiée en une structure CALDATETIME.
ms.assetid: d21f75bc-1a93-4cb9-8b9b-6fa0e81886bf
title: ConvertSystemTimeToCalDateTime fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertSystemTimeToCalDateTime
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 01eb78f9045e43db3e97b252a8fdf8fe8ed7297905174efeff2f3b2bbe1a5171
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746039"
---
# <a name="convertsystemtimetocaldatetime-function"></a>ConvertSystemTimeToCalDateTime fonction)

Action déconseillée. Convertit une structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) spécifiée en une structure [**CALDATETIME**](caldatetime.md) .

## <a name="syntax"></a>Syntaxe


```C++
BOOL ConvertSystemTimeToCalDateTime(
  _In_  const SYSTEMTIME   *lpSysTime,
  _In_        CALID         calId,
  _Out_       LPCALDATETIME lpCalDateTime

);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpSysTime* \[ dans\]
</dt> <dd>

Pointeur vers la structure [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) à convertir.

</dd> <dt>

*calId* \[ dans\]
</dt> <dd>

Identificateur de [calendrier](calendar-identifiers.md) système à utiliser lors de la conversion.

</dd> <dt>

*lpCalDateTime* \[ à\]
</dt> <dd>

Pointeur vers la structure [**CALDATETIME**](caldatetime.md) équivalente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire. Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :

-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Remarques

La première Date prise en charge par cette fonction est le 1er janvier 1601.

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

[Récupération des informations de date et d’heure](time-and-date.md)
</dt> </dl>

 

 
