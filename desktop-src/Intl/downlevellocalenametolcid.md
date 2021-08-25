---
description: Convertit un nom de paramètres régionaux en un identificateur de paramètres régionaux qui peut être utilisé pour obtenir des informations à partir du système d’exploitation.
ms.assetid: dc776c41-0376-4222-bebf-86be7e4be122
title: DownlevelLocaleNameToLCID, fonction (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelLocaleNameToLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: 39a0a6b274ba141553d2ddda927f71754cc9639ff5fc3a0d3870a974e46526a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898729"
---
# <a name="downlevellocalenametolcid-function"></a>DownlevelLocaleNameToLCID fonction)

Convertit un [nom de paramètres régionaux](locale-names.md) en un [identificateur de paramètres régionaux](locale-identifiers.md) qui peut être utilisé pour obtenir des informations à partir du système d’exploitation.

> [!Note]  
> cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista. Son utilisation requiert un package de téléchargement. les Applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) pour récupérer un identificateur de paramètres régionaux.

 

## <a name="syntax"></a>Syntaxe


```C++
LCID DownlevelLocaleNameToLCID(
  _In_ LPWSTR lpName,
  _In_ DWORD  dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui représente un [nom de paramètres régionaux](locale-names.md).

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Indicateurs spécifiant le type de nom. La valeur par défaut est le nom des paramètres régionaux de niveau inférieur \_ \_ .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’identificateur de paramètres régionaux qui correspond au nom des paramètres régionaux en cas de réussite.

La fonction retourne 0 si elle ne fonctionne pas. Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :

-   ERREUR \_ : indicateurs non valides \_ . Les valeurs fournies pour les indicateurs ne sont pas valides.
-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Remarques

> [!Note]  
> Cette fonction ne prend pas en charge les paramètres régionaux neutres. la fonction [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) équivalente prend en charge les [paramètres régionaux personnalisés](custom-locales.md), mais uniquement pour Windows Vista et versions ultérieures.

 

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

[**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
</dt> </dl>

 

 
