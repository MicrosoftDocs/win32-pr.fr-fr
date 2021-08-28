---
description: Récupère le chemin d’accès au package de pilotes d’imprimante spécifié sur un serveur d’impression.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: GetPrinterDriverPackagePath, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5058d57a0275019c5e603673d260c9969cc0b5d5641dea15e09ffe242addff10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600799"
---
# <a name="getprinterdriverpackagepath-function"></a>GetPrinterDriverPackagePath fonction)

Récupère le chemin d’accès au package de pilotes d’imprimante spécifié sur un serveur d’impression.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszServer* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le nom du serveur d’impression. Utilisez la **valeur null** pour l’ordinateur local.

</dd> <dt>

*pszEnvironment* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie l’architecture du processeur (par exemple, Windows NT x86). Il peut s’agir de la **valeur null**.

</dd> <dt>

*pszLanguage* \[ dans\]
</dt> <dd>

pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie la langue [interface utilisateur multilingue](/windows/desktop/Intl/mui-resource-management) pour le pilote en cours d’installation. Il peut s’agir de la **valeur null**.

</dd> <dt>

*pszPackageID* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie l’ID du package de pilotes.

</dd> <dt>

*pszDriverPackageCab* \[ in, out\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le chemin d’accès au fichier CAB pour le package de pilotes. Il peut s’agir de la **valeur null**. Consultez la section Notes.

</dd> <dt>

*cchDriverPackageCab* \[ dans\]
</dt> <dd>

Taille, en caractères, de la mémoire tampon *pszDriverPackageCab* . Il peut s’agir de la **valeur null**.

</dd> <dt>

*pcchRequiredSize* \[ à\]
</dt> <dd>

Pointeur vers la taille requise de la mémoire tampon *pszDriverPackageCab* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est S \_ OK, sinon le **HRESULT** contient un code d’erreur.

Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Pour obtenir une valeur pour *cchDriverPackageCab*, appelez la fonction avec **null** comme valeur de *pszDriverPackageCab*. Utilisez la valeur retournée dans *pcchRequiredSize* comme valeur de *cchDriverPackageCab* et appelez à nouveau la fonction.

Le *pszPackageID* est généralement obtenu à partir d’un appel à [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Noms Unicode et ANSI<br/>   | **GetPrinterDriverPackagePathW** (Unicode) et **GetPrinterDriverPackagePathA** (ANSI)<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> </dl>

 

