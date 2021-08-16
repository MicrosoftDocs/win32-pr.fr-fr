---
description: Compare deux chaînes de caractères Unicode à l’aide des paramètres régionaux spécifiés.
ms.assetid: dff16c1b-d329-40de-b8d7-91edb36ce198
title: CompareStringWrapW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: 9fe05c354aaa901d87c77ba04eecd5dc4efd925d77bdeaf5387a137d85b27348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861510"
---
# <a name="comparestringwrapw-function"></a>CompareStringWrapW fonction)

\[**CompareStringWrapW** peut être utilisé dans Windows XP. Elle ne sera pas disponible dans les versions ultérieures. Vous devez utiliser [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) à la place.\]

Compare deux chaînes de caractères Unicode à l’aide des paramètres régionaux spécifiés.

> [!Note]  
> **CompareStringWrapW** est un wrapper pour la fonction **CompareStringW** . Pour plus d’informations sur les remarques d’utilisation, consultez la page [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) .

 

## <a name="syntax"></a>Syntaxe


```C++
int CompareStringWrapW(
  _In_ LCID    Locale,
  _In_ DWORD   dwCmpFlags,
  _In_ LPCWSTR lpString1,
  _In_ int     cchCount1,
  _In_ LPCWSTR lpString2,
  _In_ int     cchCount2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Paramètres régionaux* \[ dans\]
</dt> <dd>

Type : **LCID**

Identificateur de paramètres régionaux utilisé pour la comparaison. Ce paramètre peut être l’un des identificateurs de paramètres régionaux prédéfinis suivants ou un identificateur de paramètres régionaux créé par la macro [**MAKELCID**](/windows/win32/api/winnt/nf-winnt-makelcid) .

<dt>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>

<span id="LOCALE_SYSTEM_DEFAULT"></span><span id="locale_system_default"></span>**paramètres régionaux \_ \_ par défaut du système**


</dt> <dd>

Paramètres régionaux par défaut du système.

</dd> <dt>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>

<span id="LOCALE_USER_DEFAULT"></span><span id="locale_user_default"></span>**paramètres régionaux \_ par défaut de l’utilisateur \_**


</dt> <dd>

Paramètres régionaux par défaut de l’utilisateur actuel.

</dd> </dl> </dd> <dt>

*dwCmpFlags* \[ dans\]
</dt> <dd>

Type : **DWORD**

Indicateurs qui indiquent comment la fonction compare les deux chaînes. Par défaut, ces indicateurs ne sont pas définis. Affectez la valeur zéro pour accéder au comportement par défaut ou à n’importe quelle combinaison des valeurs suivantes.

<dt>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>

<span id="NORM_IGNORECASE"></span><span id="norm_ignorecase"></span>**\_IGNORECASE normal**


</dt> <dd>

Ignorer la casse.

</dd> <dt>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>

<span id="NORM_IGNOREKANATYPE"></span><span id="norm_ignorekanatype"></span>**\_IGNOREKANATYPE normale**


</dt> <dd>

Ne faites pas la distinction entre les caractères Hiragana et Katakana. Les caractères Hiragana et Katakana correspondants sont considérés comme égaux.

</dd> <dt>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>

<span id="NORM_IGNORENONSPACE"></span><span id="norm_ignorenonspace"></span>**\_IGNORENONSPACE normale**


</dt> <dd>

Ignorer les caractères sans espace.

</dd> <dt>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>

<span id="NORM_IGNORESYMBOLS"></span><span id="norm_ignoresymbols"></span>**\_IGNORESYMBOLS normale**


</dt> <dd>

Ignorer les symboles.

</dd> <dt>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>

<span id="NORM_IGNOREWIDTH"></span><span id="norm_ignorewidth"></span>**\_IGNOREWIDTH normale**


</dt> <dd>

Ne faites pas la distinction entre un caractère codé sur un octet et le même caractère qu’un caractère codé sur deux octets.

</dd> <dt>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>

<span id="SORT_STRINGSORT"></span><span id="sort_stringsort"></span>**TRIER \_ STRINGSORT**


</dt> <dd>

Traitez la ponctuation de la même façon que les symboles.

</dd> </dl> </dd> <dt>

*lpString1* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers la première chaîne Unicode à comparer.

</dd> <dt>

*cchCount1* \[ dans\]
</dt> <dd>

Type : **int**

Nombre de caractères dans la chaîne vers laquelle pointe le paramètre *lpString1* . Le nombre n’inclut pas le caractère null de fin. Si ce paramètre est une valeur négative, il est supposé que la chaîne se termine par un caractère null et que la longueur est calculée automatiquement.

</dd> <dt>

*lpString2* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers la deuxième chaîne Unicode à comparer.

</dd> <dt>

*cchCount2* \[ dans\]
</dt> <dd>

Type : **int**

Nombre de caractères dans la chaîne vers laquelle pointe le paramètre *lpString2* . Le nombre n’inclut pas le caractère null de fin. Si ce paramètre est une valeur négative, il est supposé que la chaîne se termine par un caractère null et que la longueur est calculée automatiquement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **int**

Si la fonction échoue, la valeur de retour est égale à zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). **GetLastError** peut retourner l’un des codes d’erreur suivants.

-   indicateurs d’erreur \_ non valide \_
-   paramètre d’erreur \_ non valide \_

Si la fonction est réussie, la valeur de retour est l’une des valeurs suivantes. 

| Condition requise | Valeur |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| CSTR \_ inférieur \_ à    | La chaîne vers laquelle pointe le paramètre *lpString1* est inférieure à la valeur lexicale par rapport à la chaîne vers laquelle pointe le paramètre *lpString2* . |
| CSTR \_ égal         | La chaîne vers laquelle pointe *lpString1* est égale à la valeur lexicale à la chaîne désignée par *lpString2*.                              |
| CSTR \_ supérieur \_ à | La chaîne pointée par *lpString1* est plus grande dans la valeur lexicale que la chaîne vers laquelle pointe *lpString2*                           |



 

## <a name="remarks"></a>Remarques

**Avertissement de sécurité :** L’utilisation incorrecte de cette fonction peut compromettre la sécurité de votre application. Les chaînes qui ne sont pas comparées correctement peuvent produire une entrée non valide. Testez les chaînes pour vous assurer qu’elles sont valides avant de les utiliser et fournissez des gestionnaires d’erreurs. Pour plus d’informations, consultez [Considérations sur la sécurité : fonctionnalités internationales](../intl/security-considerations--international-features.md)

La méthode recommandée consiste à utiliser [**CompareStringW**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) conjointement avec la couche Microsoft pour Unicode (MSLU).

**CompareStringWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 45.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Aucun</dt> </dl>                               |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> </dl>

 

 
