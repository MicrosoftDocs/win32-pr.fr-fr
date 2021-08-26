---
description: Convertit un identificateur de paramètres régionaux en un nom de paramètres régionaux.
ms.assetid: 8e40d097-08a2-43e8-88e8-a4ecaddf449a
title: DownlevelLCIDToLocaleName, fonction (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLCIDToLocaleName
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b96d0c983c46c5d16007aae3a59659099a48855048194153d0c8102d26dc5bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898719"
---
# <a name="downlevellcidtolocalename-function"></a>DownlevelLCIDToLocaleName fonction)

Convertit un [identificateur de paramètres régionaux](locale-identifiers.md) en un [nom de paramètres régionaux](locale-names.md).

> [!Note]  
> cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista. Son utilisation requiert un package de téléchargement. les Applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename) pour récupérer un nom de paramètres régionaux.

 

## <a name="syntax"></a>Syntaxe


```C++
int DownlevelLCIDToLocaleName(
  _In_  LCID   Locale,
  _Out_ LPWSTR lpName,
  _In_  int    cchName,
  _In_  DWORD  dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Paramètres régionaux* \[ dans\]
</dt> <dd>

Identificateur de paramètres régionaux à convertir. Vous pouvez utiliser la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) pour créer un identificateur de paramètres régionaux. Cette fonction ne prend pas en charge les paramètres régionaux neutres ou les valeurs d’identificateur de paramètres régionaux spécifiques suivantes.

-   [paramètres régionaux \_ \_ par défaut du système](locale-system-default.md)
-   [paramètres régionaux \_ par défaut de l’utilisateur \_](locale-user-default.md)
-   [paramètres régionaux \_ personnalisés \_ par défaut](locale-custom-constants.md)
-   [paramètres régionaux \_ \_ par défaut de l’interface utilisateur personnalisée \_](locale-custom-constants.md)
-   [paramètres régionaux \_ personnalisés \_ non spécifiés](locale-custom-constants.md)

</dd> <dt>

*lpName* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon dans laquelle cette fonction récupère le nom des paramètres régionaux. La fonction récupère la **valeur null** si *cchName* a la valeur 0.

</dd> <dt>

*cchName* \[ dans\]
</dt> <dd>

Taille, en points de code UTF-16, de la mémoire tampon du nom des paramètres régionaux. L’application affecte à ce paramètre la valeur 0 pour retourner la taille requise de la mémoire tampon du nom des paramètres régionaux.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Indicateurs spécifiant le type de nom à récupérer. La valeur par défaut est le nom des paramètres régionaux de niveau inférieur \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de points de code UTF-16 dans le nom des paramètres régionaux, y compris le caractère null de fin, en cas de réussite. Si la fonction est réussie et que la valeur de *cchName* est 0, la valeur de retour est la taille requise, en caractères (y compris les caractères null), pour la mémoire tampon du nom des paramètres régionaux.

La fonction retourne 0 si elle ne fonctionne pas. Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :

-   ERREUR \_ de \_ mémoire tampon insuffisante. La taille de la mémoire tampon fournie n’est pas assez grande ou n’a pas été correctement définie sur **null**.
-   ERREUR \_ : indicateurs non valides \_ . La valeur de *dwFlags* n’est pas valide.
-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Remarques

> [!Note]  
> Cette fonction ne prend pas en charge les [paramètres régionaux personnalisés](custom-locales.md).

 

Le fichier d’en-tête et la DLL requis font partie du téléchargement des API de mappage de données Microsoft NLS, disponible dans le [Centre de téléchargement Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                |
| Composant redistribuable<br/>          | API de mappage de données de niveau inférieur Microsoft NLS onWindows XP avec SP2 et laterorWindows Vista<br/> |
| En-tête<br/>                   | <dl> <dt>Nlsdl. h</dt> </dl>                  |
| DLL<br/>                      | <dl> <dt>NlsMap.dll</dt> </dl>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des langues nationales](national-language-support.md)
</dt> <dt>

[Fonctions de prise en charge linguistique nationale](national-language-support-functions.md)
</dt> <dt>

[Mappage des données de paramètres régionaux](mapping-locale-data.md)
</dt> <dt>

[**LCIDToLocaleName**](/windows/desktop/api/Winnls/nf-winnls-lcidtolocalename)
</dt> </dl>

 

 
