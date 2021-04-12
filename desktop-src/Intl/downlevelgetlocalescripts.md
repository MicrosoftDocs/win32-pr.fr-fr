---
description: Fournit une liste de scripts pour les paramètres régionaux spécifiés.
ms.assetid: 0cedcf6c-bab4-4e0f-ab8f-04aa8e51602f
title: DownlevelGetLocaleScripts, fonction (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetLocaleScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: f636ab426cd4d50878df93e3e30d69de54d60ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210054"
---
# <a name="downlevelgetlocalescripts-function"></a>DownlevelGetLocaleScripts fonction)

Fournit une liste de scripts pour les paramètres régionaux spécifiés.

> [!Note]  
> Cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista. Son utilisation requiert le package de téléchargement. Les applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) avec *LCTYPE* défini sur [locale \_ SSCRIPTS](locale-sscripts.md).

 

## <a name="syntax"></a>Syntaxe


```C++
int DownlevelGetLocaleScripts(
  _In_  LPCWSTR lpLocaleName,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpLocaleName* \[ dans\]
</dt> <dd>

Pointeur vers un [nom de paramètres régionaux](locale-names.md)se terminant par null.

</dd> <dt>

*lpScripts* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle cette fonction récupère une chaîne se terminant par un caractère null qui représente une liste de scripts, à l’aide de la notation à 4 caractères utilisée dans [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Chaque nom de script se compose de quatre caractères latins, et les noms sont récupérés dans l’ordre alphabétique. Chacune d’entre elles, y compris la dernière, est suivie d’un point-virgule.

Ce paramètre peut également contenir la **valeur null** si *cchScripts* a la valeur 0. Dans ce cas, la fonction retourne la taille requise pour la mémoire tampon de script.

</dd> <dt>

*cchScripts* \[ dans\]
</dt> <dd>

Taille, en caractères, de la mémoire tampon de script indiquée par *lpScripts*.

L’application peut également affecter la valeur 0 à ce paramètre. Dans ce cas, la fonction récupère la **valeur null** dans *lpScripts* et retourne la taille requise pour la mémoire tampon de script.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de caractères récupérés dans la mémoire tampon de script, y compris le caractère null de fin. Si la fonction est réussie et que la valeur de *cchScripts* est 0, la valeur de retour est la taille requise, en caractères incluant un caractère null de fin, pour la mémoire tampon de script.

Cette fonction retourne 0 si elle ne fonctionne pas. Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :

-   ERREUR \_ BADDB. La fonction n’a pas pu accéder aux données. Cette situation ne doit normalement pas se produire, et indique généralement une installation incorrecte, un problème de disque ou similaire.
-   ERREUR \_ de \_ mémoire tampon insuffisante. La taille de la mémoire tampon fournie n’est pas assez grande ou n’a pas été correctement définie sur **null**.
-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Notes

Cette fonction est utile dans le cadre d’une stratégie visant à atténuer les problèmes de sécurité liés aux [noms de domaine internationaux (IDNs)](handling-internationalized-domain-names--idns.md).

Voici quelques exemples d’entrées et de sorties pour cette fonction, en supposant une taille de mémoire tampon suffisante :



| Paramètres régionaux                  | *lpLocaleName* | *lpScripts*     |
|-------------------------|----------------|-----------------|
| Anglais (États-Unis) | fr-FR          | LATN           |
| Hindi (Inde)           | hi-IN          | Deva           |
| Japonais (Japon)        | ja-JP          | Hani; Hira; Caractères Kana |



 

La liste ne contient pas le script latin, sauf s’il s’agit d’une partie essentielle du système d’écriture utilisé pour les paramètres régionaux. Toutefois, les caractères latins sont souvent utilisés dans le contexte des paramètres régionaux pour lesquels ils ne sont pas natifs, comme pour un nom d’entreprise étranger. Dans l’exemple ci-dessus pour l’hindi en Inde, le seul script récupéré est « Deva » (pour DÉVANÂGARÎ), bien que les caractères latins puissent également apparaître dans le texte hindi. La fonction [**DownlevelVerifyScripts**](downlevelverifyscripts.md) a un indicateur spécial pour traiter ce cas.

Le fichier d’en-tête et la DLL requis font partie du téléchargement des API d’atténuation de l' [IDN (Internationalized Domain Name) de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en) , disponible dans le [Centre de téléchargement MSDN](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                                                                                 |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                                                                        |
| Composant redistribuable<br/>          | API d’atténuation des IDN (Internationalized Domain Name) Microsoft sur Windows XP (SP2 ou version ultérieure), Windows Server 2003 (SP1 ou version ultérieure) ou Windows Vista<br/> |
| En-tête<br/>                   | <dl> <dt>Idndl. h</dt> </dl>                                                                          |
| DLL<br/>                      | <dl> <dt>Idndl.dll</dt> </dl>                                                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des langues nationales](national-language-support.md)
</dt> <dt>

[Fonctions de prise en charge linguistique nationale](national-language-support-functions.md)
</dt> <dt>

[Gestion des noms de domaine internationaux (IDNs)](handling-internationalized-domain-names--idns.md)
</dt> <dt>

[**DownlevelGetStringScripts**](downlevelgetstringscripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
