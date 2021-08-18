---
description: Obsolète.
ms.assetid: eb2622bc-a98d-42bd-ab59-7a849000d79d
title: GetCalendarDateFormatEx fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCalendarDateFormatEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-calendar-l1-1-0.dll
- kernel32legacy.dll
ms.openlocfilehash: db6bf4fc20c24e91a0af29dc8ee81f7a77ef5cb1c0f0e0f6c5a0a792e52eb903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068219"
---
# <a name="getcalendardateformatex-function"></a>GetCalendarDateFormatEx fonction)

Action déconseillée. Récupère une chaîne de date correctement mise en forme pour les paramètres régionaux spécifiés à l’aide de la date et du calendrier spécifiés. L’utilisateur peut spécifier le format de date abrégé, le format de date longue, le format d’année mois ou un modèle de format personnalisé.

> [!Note]  
> Cette fonction peut récupérer des données qui changent entre des mises en production, par exemple en raison de paramètres régionaux personnalisés. Si votre application doit rendre persistantes ou transmettre des données, consultez [utilisation de données de paramètres régionaux persistants](using-persistent-locale-data.md).

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL GetCalendarDateFormatEx(
  _In_        LPCWSTR       lpszLocale,
  _In_        DWORD         dwFlags,
  _In_  const LPCALDATETIME lpCalDateTime,
  _In_        LPCWSTR       lpFormat,
  _Out_       LPWSTR        lpDateStr,
  _In_        int           cchDate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpszLocale* \[ dans\]
</dt> <dd>

Pointeur vers un nom de paramètres régionaux, ou l’une des valeurs prédéfinies suivantes.

-   [nom de paramètres régionaux \_ \_ invariant](locale-name-constants.md)
-   [paramètres régionaux \_ \_ \_ par défaut du système](locale-name-constants.md)
-   [nom des paramètres régionaux \_ \_ \_ par défaut de l’utilisateur](locale-name-constants.md)

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Indicateurs spécifiant les options de format de date. Si *lpFormat* n’a pas la valeur **null**, ce paramètre doit avoir la valeur 0. Si *lpFormat* a la valeur **null**, l’application peut spécifier une combinaison des valeurs suivantes et des [paramètres régionaux \_ NOUSEROVERRIDE](locale-nouseroverride.md).



| Valeur                                                                                                                                                               | Signification                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span><dl> <dt>**DATE \_ SHORTDATE**</dt> </dl>    | Utilisez le format de date abrégé. Il s’agit de la valeur par défaut. Cette valeur ne peut pas être utilisée avec DATE \_ LONGDATE ou date \_ YEARMONTH. <br/> |
| <span id="DATE_LONGDATE"></span><span id="date_longdate"></span><dl> <dt>**DATE \_ LONGDATE**</dt> </dl>       | Utilisez le format de date longue. Cette valeur ne peut pas être utilisée avec DATE \_ SHORTDATE ou date \_ YEARMONTH. <br/>                      |
| <span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span><dl> <dt>**DATE \_ YEARMONTH**</dt> </dl>    | Utilisez le format année/mois. Cette valeur ne peut pas être utilisée avec DATE \_ SHORTDATE ou date \_ LONGDATE.<br/>                       |
| <span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span><dl> <dt>**DATE \_ LTRREADING**</dt> </dl> | Ajoutez des marques pour la lecture de gauche à droite. Cette valeur ne peut pas être utilisée avec la DATE \_ RTLREADING.<br/>                       |
| <span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span><dl> <dt>**DATE \_ RTLREADING**</dt> </dl> | Ajoutez des marques pour la lecture de droite à gauche. Cette valeur ne peut pas être utilisée avec la DATE \_ LTRREADING<br/>                        |



 

</dd> <dt>

*lpCalDateTime* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**CALDATETIME**](caldatetime.md) qui contient les informations de date et de calendrier à mettre en forme.

</dd> <dt>

*lpFormat* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne de format d’image utilisée pour former la chaîne de date. Les valeurs possibles pour la chaîne format image sont définies dans les [images de format jour, mois, année et ère](day--month--year--and-era-format-pictures.md).

La chaîne de l’image de format doit se terminer par un caractère null. La fonction utilise les paramètres régionaux uniquement pour les informations non spécifiées dans la chaîne de format image, par exemple, les noms des jours et des mois pour les paramètres régionaux. L’application affecte la **valeur null** à ce paramètre si la fonction doit utiliser le format de date des paramètres régionaux spécifiés.

</dd> <dt>

*lpDateStr* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle cette fonction reçoit la chaîne de Date mise en forme.

</dd> <dt>

*cchDate* \[ dans\]
</dt> <dd>

Taille, en caractères, de la mémoire tampon *lpDateStr* . L’application peut également affecter la valeur 0 à ce paramètre. Dans ce cas, la fonction retourne le nombre de caractères requis pour contenir la chaîne de Date mise en forme, et le paramètre *lpDateStr* n’est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de caractères écrits dans la mémoire tampon *lpDateStr* en cas de réussite. Si le paramètre *cchDate* a la valeur 0, la fonction retourne le nombre de caractères requis pour contenir la chaîne de Date mise en forme, y compris le caractère null de fin.

Cette fonction retourne 0 si elle ne fonctionne pas. Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :

-   \_date \_ d’erreur \_ hors \_ limites. La date spécifiée était hors limites.
-   ERREUR \_ de \_ mémoire tampon insuffisante. La taille de la mémoire tampon fournie n’est pas assez grande ou n’a pas été correctement définie sur **null**.
-   ERREUR \_ : indicateurs non valides \_ . Les valeurs fournies pour les indicateurs ne sont pas valides.
-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Remarques

La première Date prise en charge par cette fonction est le 1er janvier 1601.

Cette fonction n’a pas de fichier d’en-tête ou de fichier de bibliothèque associé. L’application peut appeler [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) avec le nom de la DLL (Kernel32.dll) pour obtenir un handle de module. Il peut ensuite appeler [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) avec ce handle de module et le nom de cette fonction pour recevoir l’adresse de la fonction.

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

[Images de format de jour, de mois, d’année et d’ère](day--month--year--and-era-format-pictures.md)
</dt> <dt>

[NLS : exemple d’API basées sur un nom](nls--name-based-apis-sample.md)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> <dt>

[**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> <dt>

[**GetDateFormatEx**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex)
</dt> <dt>

[**CALDATETIME**](caldatetime.md)
</dt> </dl>

 

 
