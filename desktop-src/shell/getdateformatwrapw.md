---
description: Met en forme une date sous forme de chaîne de date pour les paramètres régionaux spécifiés.
ms.assetid: e45f6d1c-2890-44f6-8406-022c99c59e02
title: GetDateFormatWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDateFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: c9c369584fd15a27d5e684452b2277104b5b1da4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202786"
---
# <a name="getdateformatwrapw-function"></a>GetDateFormatWrapW fonction)

\[**GetDateFormatWrapW** peut être utilisé dans Windows XP. Elle ne sera pas disponible dans les versions ultérieures. Vous devez utiliser [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) à la place.\]

Met en forme une date sous forme de chaîne de date pour les paramètres régionaux spécifiés. La fonction met en forme une date spécifiée ou la date du système local.

> [!Note]  
> **GetDateFormatWrapW** est un wrapper pour la fonction **GetDateFormatW** . Pour plus d’informations sur les remarques d’utilisation, consultez la page [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) .

 

## <a name="syntax"></a>Syntaxe


```C++
int GetDateFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpDate,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzDateStr,
  _In_        int        cchDate
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Paramètres régionaux* \[ dans\]
</dt> <dd>

Type : **LCID**

Paramètres régionaux pour lesquels la chaîne de date doit être mise en forme. Si *pwzFormat* a la **valeur null**, la fonction met en forme la chaîne en fonction du format de date de ces paramètres régionaux. Si *pwzFormat* n’a pas la **valeur null**, la fonction utilise les paramètres régionaux uniquement pour les informations non spécifiées dans la chaîne de format d’image (par exemple, les noms de jours et de mois des paramètres régionaux).

Ce paramètre peut être un identificateur de paramètres régionaux créé par la macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) , ou l’une des valeurs prédéfinies suivantes.

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**paramètres régionaux \_ \_ par défaut du système**


</dt> <dd>

Paramètres régionaux par défaut du système.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**paramètres régionaux \_ par défaut de l’utilisateur \_**


</dt> <dd>

Paramètres régionaux utilisateur par défaut.

</dd> </dl> </dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Type : **DWORD**

Spécifie différentes options de fonction. Si *pwzFormat* n’a pas la **valeur null**, ce paramètre doit être égal à zéro. Si *pwzFormat* a la **valeur null**, vous pouvez spécifier une combinaison des valeurs suivantes. Si vous ne spécifiez pas de DATE \_ YEARMONTH, date \_ SHORTDATE ou date \_ LONGDATE, et *pwzFormat* est **null**, alors \_ la date SHORTDATE est utilisée comme valeur par défaut.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**paramètres régionaux \_ NOUSEROVERRIDE**


</dt> <dd>

Si cette option est définie, la fonction met en forme la chaîne en utilisant le format de date système par défaut pour les paramètres régionaux spécifiés. Si la valeur n’est pas définie, la fonction met en forme la chaîne à l’aide de n’importe quelle substitution d’utilisateur au format de date par défaut de paramètres régionaux.

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**paramètres régionaux \_ use \_ CP \_ ACP**


</dt> <dd>

Utilise la page de codes système ANSI pour la conversion de chaînes à la place de la page de codes des paramètres régionaux.

</dd> <dt>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>

<span id="DATE_SHORTDATE"></span><span id="date_shortdate"></span>**DATE \_ SHORTDATE**


</dt> <dd>

Utilise le format de date abrégé. Cette valeur ne peut pas être utilisée avec DATE \_ LONGDATE ou date \_ YEARMONTH.

</dd> <dt>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>

<span id="DATE_LONGDATE"></span><span id="date_longdate"></span>**DATE \_ LONGDATE**


</dt> <dd>

Utilise le format de date longue. Cette valeur ne peut pas être utilisée avec DATE \_ SHORTDATE ou date \_ YEARMONTH.

</dd> <dt>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>

<span id="DATE_YEARMONTH"></span><span id="date_yearmonth"></span>**DATE \_ YEARMONTH**


</dt> <dd>

Utilise le format année/mois. Cette valeur ne peut pas être utilisée avec DATE \_ SHORTDATE ou date \_ LONGDATE.

</dd> <dt>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>

<span id="DATE_USE_ALT_CALENDAR"></span><span id="date_use_alt_calendar"></span>**DATE d' \_ utilisation \_ Alt \_ Calendar**


</dt> <dd>

Utilise le calendrier de remplacement, le cas échéant, pour mettre en forme la chaîne de date. Si cet indicateur est défini, la fonction utilise le format par défaut pour ce calendrier de remplacement, plutôt que d’utiliser des remplacements utilisateur. Les remplacements de l’utilisateur sont utilisés uniquement dans le cas où il n’existe pas de format par défaut pour le calendrier de remplacement spécifié.

</dd> <dt>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>

<span id="DATE_LTRREADING"></span><span id="date_ltrreading"></span>**DATE \_ LTRREADING**


</dt> <dd>

Ajoute des marques pour la lecture de gauche à droite. Cette valeur ne peut pas être utilisée avec la DATE \_ RTLREADING.

</dd> <dt>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>

<span id="DATE_RTLREADING"></span><span id="date_rtlreading"></span>**DATE \_ RTLREADING**


</dt> <dd>

Ajoute des marques pour la lecture de droite à gauche. Cette valeur ne peut pas être utilisée avec la DATE \_ LTRREADING.

</dd> </dl> </dd> <dt>

*lpDate* \[ dans\]
</dt> <dd>

Type : **const [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _

Pointeur vers une structure [_ *SystemTime* *](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) qui contient les informations de date à mettre en forme. Si ce pointeur est **null**, la fonction utilise la date système locale actuelle.

</dd> <dt>

*pwzFormat* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers une image de format à utiliser pour former la chaîne de date. Si *pwzFormat* a la **valeur null**, la fonction utilise le format de date des paramètres régionaux spécifiés. Pour plus d’informations, consultez [**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) .

</dd> <dt>

*pwzDateStr* \[ à\]
</dt> <dd>

Type : **LPWStr**

Pointeur vers une mémoire tampon qui reçoit la chaîne de Date mise en forme.

</dd> <dt>

*cchDate* \[ dans\]
</dt> <dd>

Type : **int**

Spécifie la taille, en caractères, de la mémoire tampon *pwzDateStr* . Si *cchDate* est égal à zéro, la fonction retourne le nombre de caractères requis pour contenir la chaîne de Date mise en forme, et la mémoire tampon vers laquelle pointe *pwzDateStr* n’est pas utilisée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **int**

Si la fonction a abouti, la valeur de retour est le nombre de caractères écrits dans la mémoire tampon vers laquelle pointe *pwzDateStr*. Si le paramètre *cchDate* est égal à zéro, la valeur de retour est le nombre de caractères requis pour contenir la chaîne de Date mise en forme. Le nombre comprend le caractère null de fin.

Si la fonction échoue, la valeur de retour est égale à zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** peut retourner l’un des codes d’erreur suivants.

<dl> <dt>

**ERREUR \_ de \_ mémoire tampon insuffisante**
</dt> <dt>

**indicateurs d’erreur \_ non valide \_**
</dt> <dt>

**paramètre d’erreur \_ non valide \_**
</dt> </dl>

## <a name="remarks"></a>Notes

**GetDateFormatWrapW** offre la possibilité d’utiliser des chaînes Unicode dans des systèmes d’exploitation antérieurs à Windows XP. La méthode recommandée consiste à utiliser [**GetDateFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata) conjointement avec la couche Microsoft pour Unicode (MSLU).

**GetDateFormatWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 311.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetDateFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)
</dt> </dl>

 

 
