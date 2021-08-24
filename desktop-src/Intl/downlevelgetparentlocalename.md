---
description: Récupère le nom des paramètres régionaux pour le parent des paramètres régionaux fournis.
ms.assetid: a8db8107-822c-4bbc-acb8-40b25d2b41c4
title: DownlevelGetParentLocaleName, fonction (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: af7580188c7ded31c80476509aef8a10ee83b1cb1f9767ca5819eed053f1ce87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898739"
---
# <a name="downlevelgetparentlocalename-function"></a>DownlevelGetParentLocaleName fonction)

Récupère le [nom des paramètres régionaux](locale-names.md) pour le parent des paramètres régionaux fournis.

> [!Note]  
> cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista. Son utilisation requiert le package de téléchargement. les Applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) avec *LCType* défini sur [locale \_ SPARENT](locale-sparent.md).

 

## <a name="syntax"></a>Syntaxe


```C++
int DownlevelGetParentLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Paramètres régionaux* \[ dans\]
</dt> <dd>

[Identificateur de paramètres régionaux](locale-identifiers.md) des paramètres régionaux. Vous pouvez utiliser la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) pour créer un identificateur de paramètres régionaux ou utiliser l’une des valeurs prédéfinies suivantes.

-   [paramètres régionaux \_ INvariants](locale-invariant.md)
-   [paramètres régionaux \_ \_ par défaut du système](locale-system-default.md)
-   [paramètres régionaux \_ par défaut de l’utilisateur \_](locale-user-default.md)

**Windows Vista et versions ultérieures :** Les identificateurs de paramètres régionaux personnalisés suivants sont également pris en charge.

-   [paramètres régionaux \_ personnalisés \_ par défaut](locale-custom-constants.md)
-   [paramètres régionaux \_ \_ par défaut de l’interface utilisateur personnalisée \_](locale-custom-constants.md)
-   [paramètres régionaux \_ personnalisés \_ non spécifiés](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle la fonction récupère le nom de paramètres régionaux parent, ou l’une des valeurs prédéfinies suivantes. Ce paramètre a la valeur **null** si *cchName* a la valeur 0.

-   [nom de paramètres régionaux \_ \_ invariant](locale-name-constants.md)
-   [paramètres régionaux \_ \_ \_ par défaut du système](locale-name-constants.md)
-   [nom des paramètres régionaux \_ \_ \_ par défaut de l’utilisateur](locale-name-constants.md)

</dd> <dt>

*cchName* \[ dans\]
</dt> <dd>

Taille de la mémoire tampon indiquée par *lpName*, en points de code UTF-16. La valeur 0 pour ce paramètre fait en sorte que la fonction ignore la mémoire tampon *lpName* et retourne la taille de la mémoire tampon, en caractères (caractères null inclus), requis pour contenir le nom des paramètres régionaux parents.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de points de code UTF-16 dans le nom des paramètres régionaux, y compris le caractère null de fin, en cas de réussite.

Cette fonction retourne 0 si elle ne fonctionne pas. Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :

-   ERREUR \_ de \_ mémoire tampon insuffisante. La taille de la mémoire tampon fournie n’est pas assez grande ou n’a pas été correctement définie sur **null**.
-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Remarques

Le fichier d’en-tête et la DLL requis font partie du téléchargement des API de mappage de données Microsoft NLS, disponible dans le [Centre de téléchargement Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | API de mappage de données Microsoft NLS onWindows XP avec SP2 et versions ultérieures<br/>  |
| En-tête<br/>                   | <dl> <dt>Nlsdl. h</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des langues nationales](national-language-support.md)
</dt> <dt>

[Fonctions de prise en charge linguistique nationale](national-language-support-functions.md)
</dt> <dt>

[Mappage des données de paramètres régionaux](mapping-locale-data.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> </dl>

 

 
