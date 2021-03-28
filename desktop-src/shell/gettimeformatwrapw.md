---
description: Met en forme l’heure sous la forme d’une chaîne d’heure pour les paramètres régionaux spécifiés.
ms.assetid: 048b209c-f757-4b65-9ce7-282a5c21021f
title: GetTimeFormatWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTimeFormatWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 53f1bb88c2b3a79b58f3025daec31a7b1340b642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973195"
---
# <a name="gettimeformatwrapw-function"></a>GetTimeFormatWrapW fonction)

\[**GetTimeFormatWrapW** peut être utilisé dans Windows XP. Elle n’est peut-être pas disponible dans les versions ultérieures. Vous devez utiliser [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) à la place.\]

Met en forme l’heure sous la forme d’une chaîne d’heure pour les paramètres régionaux spécifiés. La fonction met en forme une heure spécifiée ou l’heure système locale.

> [!Note]  
> **GetTimeFormatWrapW** est un wrapper pour la fonction **GetTimeFormatW** . Pour plus d’informations sur les remarques d’utilisation, consultez la page [**getTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .

 

## <a name="syntax"></a>Syntaxe


```C++
int GetTimeFormatWrapW(
  _In_        LCID       Locale,
  _In_        DWORD      dwFlags,
  _In_  const SYSTEMTIME *lpTime,
  _In_        LPCWSTR    pwzFormat,
  _Out_       LPWSTR     pwzTimeStr,
  _In_        int        cchTime
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Paramètres régionaux* \[ dans\]
</dt> <dd>

Type : **LCID**

Spécifie les paramètres régionaux pour lesquels la chaîne d’heure doit être mise en forme. Si *pwzFormat* a la **valeur null**, la fonction met en forme la chaîne en fonction du format d’heure de ces paramètres régionaux. Si *pwzFormat* n’a pas la **valeur null**, la fonction utilise les paramètres régionaux uniquement pour les informations non spécifiées dans la chaîne de format d’image (par exemple, les marqueurs d’heure de la région).

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

Spécifie différentes options de fonction. Vous pouvez spécifier une combinaison des valeurs suivantes.

<dt>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>

<span id="LOCALE_NOUSEROVERRIDE"></span><span id="locale_nouseroverride"></span>**paramètres régionaux \_ NOUSEROVERRIDE**


</dt> <dd>

Si cette option est définie, la fonction met en forme la chaîne en utilisant le format d’heure par défaut du système pour les paramètres régionaux spécifiés. S’il n’est pas défini, la fonction met en forme la chaîne à l’aide de n’importe quel remplacement de l’utilisateur au format d’heure par défaut de la région. Cet indicateur ne peut être défini que si *pwzFormat* a la **valeur null**.

</dd> <dt>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>

<span id="LOCALE_USE_CP_ACP"></span><span id="locale_use_cp_acp"></span>**paramètres régionaux \_ use \_ CP \_ ACP**


</dt> <dd>

Utilise la page de codes système ANSI pour la conversion de chaînes à la place de la page de codes des paramètres régionaux.

</dd> <dt>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>

<span id="TIME_NOMINUTESORSECONDS"></span><span id="time_nominutesorseconds"></span>**TEMPS \_ NOMINUTESORSECONDS**


</dt> <dd>

N’utilise pas de minutes ou de secondes.

</dd> <dt>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>

<span id="TIME_NOSECONDS"></span><span id="time_noseconds"></span>**intervalle de temps (en \_ secondes)**


</dt> <dd>

N’utilise pas de secondes.

</dd> <dt>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>

<span id="TIME_NOTIMEMARKER"></span><span id="time_notimemarker"></span>**TEMPS \_ NOTIMEMARKER**


</dt> <dd>

N’utilise pas de marqueur d’heure.

</dd> <dt>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>

<span id="TIME_FORCE24HOURFORMAT"></span><span id="time_force24hourformat"></span>**TEMPS \_ FORCE24HOURFORMAT**


</dt> <dd>

Utilise toujours un format horaire de 24 heures.

</dd> </dl> </dd> <dt>

*lpTime* \[ dans\]
</dt> <dd>

Type : **const [**SystemTime**](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) \** _

Pointeur vers une structure [_ *SystemTime* *](/windows/win32/api/minwinbase/ns-minwinbase-systemtime) qui contient les informations d’heure à mettre en forme. Si ce pointeur est **null**, la fonction utilise l’heure système locale actuelle.

</dd> <dt>

*pwzFormat* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers un format à utiliser pour former la chaîne d’heure. Si *pwzFormat* a la **valeur null**, la fonction utilise le format d’heure des paramètres régionaux spécifiés. Pour plus d’informations, consultez [**getTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) .

</dd> <dt>

*pwzTimeStr* \[ à\]
</dt> <dd>

Type : **LPWStr**

Pointeur vers une mémoire tampon qui reçoit la chaîne d’heure mise en forme.

</dd> <dt>

*cchTime* \[ dans\]
</dt> <dd>

Type : **int**

Taille, en caractères, de la mémoire tampon *pwzTimeStr* . Si *cchTime* est égal à zéro, la fonction retourne le nombre de caractères requis pour contenir la chaîne de temps mise en forme, et la mémoire tampon vers laquelle pointe *pwzTimeStr* n’est pas utilisée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **int**

Si la fonction a abouti, la valeur de retour est le nombre de caractères écrits dans la mémoire tampon vers laquelle pointe *pwzTimeStr*. Si le paramètre *cchTime* est égal à zéro, la valeur de retour est le nombre de caractères requis pour contenir la chaîne de temps mise en forme. Le nombre comprend le caractère null de fin.

Si la fonction échoue, la valeur de retour est égale à zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** peut retourner l’un des codes d’erreur suivants.

<dl> <dt>

**ERREUR \_ de \_ mémoire tampon insuffisante**
</dt> <dt>

**indicateurs d’erreur \_ non valide \_**
</dt> <dt>

**paramètre d’erreur \_ non valide \_**
</dt> </dl>

## <a name="remarks"></a>Notes

**GetTimeFormatWrapW** offre la possibilité d’utiliser des chaînes Unicode dans des systèmes d’exploitation antérieurs à Windows XP. La méthode recommandée consiste à utiliser [**GetTimeFormatW**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata) conjointement avec la couche Microsoft pour Unicode (MSLU).

**GetTimeFormatWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 310.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetTimeFormat**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)
</dt> </dl>

 

 
