---
description: Récupère l’identificateur de paramètres régionaux pour le parent des paramètres régionaux fournis.
ms.assetid: 4cfa1787-6b9e-4dd4-8466-7b737e00a4b1
title: DownlevelGetParentLocaleLCID, fonction (nlsdl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownlevelGetParentLocaleLCID
api_type:
- DllExport
api_location:
- NlsMap.dll
ms.openlocfilehash: b34f30425147057efe8039cc36514d699199c9a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320234"
---
# <a name="downlevelgetparentlocalelcid-function"></a>DownlevelGetParentLocaleLCID fonction)

Récupère l' [identificateur de paramètres régionaux](locale-identifiers.md) pour le parent des paramètres régionaux fournis.

> [!Note]  
> Cette fonction est utilisée uniquement par les applications qui s’exécutent sur des systèmes d’exploitation antérieurs à Windows Vista. Son utilisation requiert le package de téléchargement. Les applications qui s’exécutent uniquement sur Windows Vista et versions ultérieures doivent appeler [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) avec *LCTYPE* défini sur [locale \_ sParent](locale-sparent.md).

 

## <a name="syntax"></a>Syntaxe


```C++
LCID DownlevelGetParentLocaleLCID(
  _In_ LCID Locale
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Paramètres régionaux* \[ dans\]
</dt> <dd>

Identificateur de paramètres régionaux des paramètres régionaux pour lesquels récupérer l’identificateur de paramètres régionaux parent. Vous pouvez utiliser la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) pour créer un identificateur de paramètres régionaux ou utiliser l’une des valeurs prédéfinies suivantes.

-   [paramètres régionaux \_ INvariants](locale-invariant.md)
-   [paramètres régionaux \_ \_ par défaut du système](locale-system-default.md)
-   [paramètres régionaux \_ par défaut de l’utilisateur \_](locale-user-default.md)

**Windows Vista et versions ultérieures :** Les identificateurs de paramètres régionaux personnalisés suivants sont également pris en charge.

-   [paramètres régionaux \_ personnalisés \_ par défaut](locale-custom-constants.md)
-   [paramètres régionaux \_ \_ par défaut de l’interface utilisateur personnalisée \_](locale-custom-constants.md)
-   [paramètres régionaux \_ personnalisés \_ non spécifiés](locale-custom-constants.md)

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne l’identificateur de paramètres régionaux parent en cas de réussite, ou 0 dans le cas contraire. Pour obtenir des informations d’erreur étendues, l’application peut appeler [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror), qui peut retourner l’un des codes d’erreur suivants :

-   ERREUR \_ \_ : paramètre non valide. Les valeurs de paramètre ne sont pas valides.

## <a name="remarks"></a>Notes

Le fichier d’en-tête et la DLL requis font partie du téléchargement des API de mappage de données Microsoft NLS, disponible dans le [Centre de téléchargement Microsoft](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&DisplayLang=en).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | API de mappage de données de niveau inférieur Microsoft NLS onWindows XPor Windows Vista<br/>     |
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

 

 
