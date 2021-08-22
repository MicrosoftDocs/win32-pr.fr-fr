---
description: Compare deux listes énumérées de scripts.
ms.assetid: 3500ce36-75e4-4d61-8449-a65c99532326
title: DownlevelVerifyScripts, fonction (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelVerifyScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: df0bdb1e8968d6bb044a3f270eb9200adf1ecaa54137fe3cface0e0898a9b5be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068239"
---
# <a name="downlevelverifyscripts-function"></a>DownlevelVerifyScripts fonction)

Compare deux listes énumérées de scripts.

> [!Note]  
> cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista. Son utilisation requiert le package de téléchargement. les Applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts).

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL DownlevelVerifyScripts(
  _In_ DWORD   dwFlags,
  _In_ LPCWSTR lpLocaleScripts,
  _In_ int     cchLocaleScripts,
  _In_ LPCWSTR lpTestScripts,
  _In_ int     cchTestScripts
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Indicateurs spécifiant les options de vérification de script.



| Valeur                                                                                                                                                             | Signification                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="VS_ALLOW_LATIN"></span><span id="vs_allow_latin"></span><dl> <dt>**VS \_ \_ latin**</dt> </dl> | Autorisez « LATN » (script latin) dans la liste de tests, même s’il ne figure pas dans la liste des paramètres régionaux.<br/> |



 

</dd> <dt>

*lpLocaleScripts* \[ dans\]
</dt> <dd>

Pointeur vers la liste des paramètres régionaux, liste énumérée des scripts pour des paramètres régionaux donnés. Cette liste est généralement remplie en appelant [**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md).

</dd> <dt>

*cchLocaleScripts* \[ dans\]
</dt> <dd>

Taille, en caractères, de la chaîne indiquée par *lpLocaleScripts*. L’application affecte à ce paramètre la valeur-1 si la chaîne se termine par un caractère null. Si ce paramètre a la valeur 0, la fonction échoue.

</dd> <dt>

*lpTestScripts* \[ dans\]
</dt> <dd>

Pointeur vers la liste de tests, une deuxième liste énumérée de scripts. Cette liste est généralement remplie en appelant [**DownlevelGetStringScripts**](downlevelgetstringscripts.md).

</dd> <dt>

*cchTestScripts* \[ dans\]
</dt> <dd>

Taille, en caractères, de la chaîne indiquée par *lpTestScripts*. L’application affecte à ce paramètre la valeur-1 si la chaîne se termine par un caractère null. Si ce paramètre a la valeur 0, la fonction échoue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si la liste de tests n’est pas vide et si tous les éléments de la liste sont également inclus dans la liste des paramètres régionaux. Dans le cas contraire, la fonction retourne **false**.

Une valeur de retour **false** peut indiquer que la liste de tests contient un élément qui n’est pas dans la liste des paramètres régionaux ou qu’elle peut indiquer une erreur. Pour faire la distinction entre ces deux cas, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror). Si **DownlevelVerifyScripts** a déterminé qu’il existe un élément dans la liste de tests qui ne figure pas dans la liste des paramètres régionaux, **GetLastError** retourne la réussite de l’erreur \_ . Dans le cas contraire, **GetLastError** peut retourner l’un des codes d’erreur suivants :

-   ERREUR \_ : indicateurs non valides \_ . Les valeurs fournies pour les indicateurs ne sont pas valides.
-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Remarques

Cette fonction compare des chaînes, telles que « Latn ». Cyrl ;», qui se compose d’une série de noms de script de 4 caractères, chaque nom de script suivi d’un point-virgule. Il a également un cas particulier de tenir compte du fait que le script latin est souvent utilisé dans les langages et les paramètres régionaux pour lesquels il n’est pas natif.

Cette fonction est utile dans le cadre d’une stratégie visant à atténuer les problèmes de sécurité liés aux [noms de domaine internationaux (IDNs)](handling-internationalized-domain-names--idns.md).

Voici des exemples de retour de cette fonction et d’un appel ultérieur à [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) dans différents scénarios. Les deux derniers exemples illustrent, respectivement, un cas dans lequel la liste de tests n’a pas de point-virgule de fin (chaîne incorrecte) et un cas dans lequel la liste de tests est vide.



| Chaîne « locale » | Chaîne « test » | *dwFlags*        | Valeur retournée | Retour de GetLastError       |
|-----------------|---------------|------------------|--------------|---------------------------|
| Hani; Hira; Caractères Kana | Hani;         | N/A              | **TRUE**     | N/A                       |
| Hani; Hira; Caractères Kana | Hani; LATN    | 0                | **FALSE**    | ERREUR de \_ réussite            |
| Hani; Hira; Caractères Kana | Hani; LATN    | VS \_ \_ latin | **TRUE**     | N/A                       |
| Hani; Hira; Caractères Kana | Cyrl         | N/A              | **FALSE**    | ERREUR de \_ réussite            |
| Hani; Hira; Caractères Kana | Cyrl         | N/A              | **FALSE**    | paramètre d’erreur \_ non valide \_ |
| Hani; Hira; Caractères Kana |               | N/A              | **FALSE**    | ERREUR de \_ réussite            |



 

Le fichier d’en-tête et la DLL requis font partie du téléchargement des API d’atténuation de l' [IDN (Internationalized Domain Name) de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponible dans le [Centre de téléchargement MSDN](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                                                         |
| Composant redistribuable<br/>          | api d’atténuation des IDN (internationalized domain Name) Microsoft onWindows XP avec SP2, Windows Server 2003 avec SP1, intégral Vista<br/> |
| En-tête<br/>                   | <dl> <dt>Idndl. h</dt> </dl>                                                           |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des langues nationales](national-language-support.md)
</dt> <dt>

[Fonctions de prise en charge linguistique nationale](national-language-support-functions.md)
</dt> <dt>

[Gestion des noms de domaine internationaux (IDNs)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**VerifyScripts**](/windows/desktop/api/Winnls/nf-winnls-verifyscripts)
</dt> </dl>

 

 
