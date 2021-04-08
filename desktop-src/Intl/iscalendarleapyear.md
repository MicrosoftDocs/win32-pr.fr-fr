---
description: Obsolète. Identifie si l’année spécifiée est une année bissextile au sein de l’ère donnée pour le calendrier spécifique.
ms.assetid: 91f58915-f0c6-4c7a-9d9a-96e255d799fd
title: IsCalendarLeapYear fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsCalendarLeapYear
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: 484531f8107bacb70f9e24ba2537090317825e26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865490"
---
# <a name="iscalendarleapyear-function"></a>IsCalendarLeapYear fonction)

Action déconseillée. Identifie si l’année spécifiée est une année bissextile au sein de l’ère donnée pour le calendrier spécifique.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsCalendarLeapYear(
  _In_ CALID calId,
  _In_ UINT  year,
  _In_ UINT  era
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*calId* \[ dans\]
</dt> <dd>

[Identificateur de calendrier](calendar-identifiers.md) à utiliser pour vérifier l’année bissextile.

</dd> <dt>

*année* \[ dans\]
</dt> <dd>

Année à vérifier.

</dd> <dt>

*ère* \[ dans\]
</dt> <dd>

L’ère à vérifier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si l’année spécifiée est une année bissextile, ou **false** dans le cas contraire. Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :

-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de fichier d’en-tête ou de fichier de bibliothèque associé. L’application peut appeler [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Kernel32.dll) pour obtenir un handle de module. Il peut ensuite appeler [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec ce handle de module et le nom de cette fonction pour recevoir l’adresse de la fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des langues nationales](national-language-support.md)
</dt> <dt>

[Fonctions de prise en charge linguistique nationale](national-language-support-functions.md)
</dt> </dl>

 

 
