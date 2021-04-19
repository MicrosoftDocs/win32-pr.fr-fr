---
description: Fournit la liste des scripts utilisés dans la chaîne Unicode spécifiée.
ms.assetid: 3ad23613-8d0c-432a-b352-637c373a0980
title: DownlevelGetStringScripts, fonction (idndl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetStringScripts
api_type:
- DllExport
api_location:
- Idndl.dll
ms.openlocfilehash: bc5a9fdaf3beb9e1c401943f923fa48bd9d4b44c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534718"
---
# <a name="downlevelgetstringscripts-function"></a>DownlevelGetStringScripts fonction)

Fournit la liste des scripts utilisés dans la chaîne Unicode spécifiée.

> [!Note]  
> Cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista. Son utilisation requiert le package de téléchargement. Les applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts).

 

## <a name="syntax"></a>Syntaxe


```C++
int DownlevelGetStringScripts(
  _In_  DWORD   dwFlags,
  _In_  LPCWSTR lpString,
  _In_  int     cchString,
  _Out_ LPWSTR  lpScripts,
  _In_  int     cchScripts
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Indicateurs spécifiant des options pour la récupération de script.



| Valeur                                                                                                                                                                                                  | Signification                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GSS_ALLOW_INHERITED_COMMON"></span><span id="gss_allow_inherited_common"></span><dl> <dt>**GSS \_ autoriser l' \_ héritage \_ commun**</dt> </dl> | Récupérez les informations de script « Qaii » (hérité) et « ZYYY » (communes). Cette valeur n’affecte pas le traitement des caractères non assignés. Ces caractères dans la chaîne d’entrée provoquent toujours l’affichage d’un « zzzz » (script non assigné) dans la chaîne de script.<br/> |



 

> [!Note]  
> Par défaut, cette fonction ignore les caractères hérités ou communs dans la chaîne Unicode d’entrée. Si GSS \_ allow \_ \_ Common Common n’est pas défini, « Qaii » et « ZYYY » ne s’affichent pas dans la chaîne de script, même si la chaîne d’entrée contient des caractères de ce type. Si GSS \_ autorise \_ \_ l’héritage commun est défini et si la chaîne d’entrée contient des caractères hérités et/ou communs, « Qaii » et/ou « ZYYY » apparaissent dans la chaîne de script. Consultez la section Notes.

 

</dd> <dt>

*lpString* \[ dans\]
</dt> <dd>

Pointeur vers la chaîne Unicode à analyser.

</dd> <dt>

*cchString* \[ dans\]
</dt> <dd>

Taille, en caractères, de la chaîne Unicode indiquée par *lpString*. L’application affecte à ce paramètre la valeur-1 si la chaîne se termine par un caractère null. Si l’application définit ce paramètre sur 0, la fonction récupère une chaîne Unicode null (L " \\ 0") dans *lpScripts* et retourne 1.

</dd> <dt>

*lpScripts* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle cette fonction récupère une chaîne se terminant par un caractère null qui représente une liste de scripts, à l’aide de la notation à 4 caractères utilisée dans [ISO 15924](https://www.unicode.org/iso15924/iso15924-codes.html). Chaque nom de script se compose de quatre caractères latins, et les noms sont récupérés dans l’ordre alphabétique. Chaque nom, y compris le dernier, est suivi d’un point-virgule.

Ce paramètre peut également contenir la **valeur null** si *cchScripts* a la valeur 0. Dans ce cas, la fonction retourne la taille requise pour la mémoire tampon de script.

</dd> <dt>

*cchScripts* \[ dans\]
</dt> <dd>

Taille, en caractères, de la mémoire tampon de script indiquée par *lpScripts*.

L’application peut également affecter la valeur 0 à ce paramètre. Dans ce cas, la fonction récupère la **valeur null** dans *lpScripts* et retourne la taille requise pour la mémoire tampon de script.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de caractères récupérés dans la mémoire tampon de sortie, y compris un caractère null de fin, en cas de réussite et *cchScripts* est défini sur une valeur différente de zéro. La fonction retourne 1 pour indiquer qu’aucun script n’a été trouvé, par exemple, quand la chaîne d’entrée contient uniquement des caractères communs ou HÉRITÉs et que GSS \_ allow \_ \_ Common Common n’est pas défini. Étant donné que chaque script trouvé ajoute cinq caractères (quatre caractères + délimiteur), une opération mathématique simple fournit le nombre de scripts sous la forme ( \_ Code de retour-1)/5.

Si la fonction est réussie et que la valeur de *cchScripts* est 0, la valeur de retour est la taille requise, en caractères incluant un caractère null de fin, pour la mémoire tampon de script. Le nombre de scripts est décrit ci-dessus.

La fonction retourne 0 si elle ne fonctionne pas. Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :

-   ERREUR \_ BADDB. La fonction n’a pas pu accéder aux données. Cette situation ne doit normalement pas se produire, et indique généralement une installation incorrecte, un problème de disque ou similaire.
-   ERREUR \_ de \_ mémoire tampon insuffisante. La taille de la mémoire tampon fournie n’est pas assez grande ou n’a pas été correctement définie sur **null**.
-   ERREUR \_ : indicateurs non valides \_ . Les valeurs fournies pour les indicateurs ne sont pas valides.
-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Notes

Cette fonction est utile dans le cadre d’une stratégie visant à atténuer les problèmes de sécurité liés aux [noms de domaine internationaux (IDNs)](handling-internationalized-domain-names--idns.md).

La détermination du script est basée sur les valeurs de script publiées par le consortium Unicode dans <https://www.unicode.org/Public/4.1.0/ucd/Scripts.txt> , sauf que les caractères non assignés ont la valeur « zzzz » (non assigné) au lieu de « ZYYY » (commun).

Voici quelques exemples du comportement de cette fonction :



Chaîne d’entrée

*dwFlags*

*lpScripts*

Scripts

Microsoft.com

0

LATN

Latin

Microsoft.com

GSS \_ autoriser l' \_ héritage \_ commun

LATN Zyyy;

Latin + courant

$ {ROWSPAN2} $Ni ÑO $ {REMOVE} $  

004E 0069 0241 006F

$ {ROWSPAN2} $GSS \_ autoriser l' \_ héritage \_ $ {Remove} $  

$ {ROWSPAN2} $Latn ; $ {REMOVE} $  

$ {ROWSPAN2} $Latin $ {REMOVE} $  

Utilise la lettre minuscule latine N avec TILDE

$ {ROWSPAN2} $Ni ÑO $ {REMOVE} $  

004E 0069 006E 0303 006F

$ {ROWSPAN2} $GSS \_ autoriser l' \_ héritage \_ $ {Remove} $  

$Latn $ {ROWSPAN2}; Qaii ; $ {REMOVE} $  

$ {ROWSPAN2} $Latin + + hérité $ {REMOVE} $  

Utilise la combinaison TILDE

$ {ROWSPAN2} $Sp ооf $ {REMOVE} $  

0053 0070 043e 043e 0066

$ {ROWSPAN2} $0 $ {REMOVE} $  

$Latn $ {ROWSPAN2}; Cyrl ; $ {REMOVE} $  

$ {ROWSPAN2} $Latin + cyrillique $ {REMOVE} $  

Utilise la lettre minuscule cyrillique O



U + F000

0

Zzzz

Non affecté



U + F000

GSS \_ autoriser l' \_ héritage \_ commun

Zzzz

Non affecté



 

Le fichier d’en-tête et la DLL requis font partie du téléchargement des API d’atténuation de l' [IDN (Internationalized Domain Name) de Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=AD6158D7-DDBA-416A-9109-07607425A815&displaylang=en%0A) , disponible dans le [Centre de téléchargement MSDN](https://www.microsoft.com/?ref=go).

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

[**DownlevelGetLocaleScripts**](downlevelgetlocalescripts.md)
</dt> <dt>

[**DownlevelVerifyScripts**](downlevelverifyscripts.md)
</dt> <dt>

[**GetStringScripts**](/windows/desktop/api/Winnls/nf-winnls-getstringscripts)
</dt> </dl>

 

 
