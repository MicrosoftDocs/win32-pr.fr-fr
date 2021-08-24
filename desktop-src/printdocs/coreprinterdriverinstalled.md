---
description: La fonction CorePrinterDriverInstalled indique si un pilote d’imprimante principal avec un GUID, une date et une version spécifiés est installé.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: CorePrinterDriverInstalled, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 014b9932046ab6d66b64794bbe042f43a390f9f6a4b6183d36a6338eca434526
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719769"
---
# <a name="coreprinterdriverinstalled-function"></a>CorePrinterDriverInstalled fonction)

La fonction **CorePrinterDriverInstalled** indique si un pilote d’imprimante principal avec un GUID, une date et une version spécifiés est installé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszServer* \[ dans\]
</dt> <dd>

Pointeur vers une constante, chaîne terminée par le caractère null qui spécifie le nom du serveur d’impression. Utilisez la **valeur null** pour l’ordinateur local.

</dd> <dt>

*pszEnvironment* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne constante, terminée par un caractère null qui spécifie l’architecture du processeur (par exemple, Windows NT x86). Il peut s’agir de la **valeur null**.

</dd> <dt>

*CoreDriverGUID* \[ dans\]
</dt> <dd>

GUID du pilote d’imprimante principal.

</dd> <dt>

*ftDriverDate* \[ dans\]
</dt> <dd>

Date du pilote d’imprimante principal.

</dd> <dt>

*dwlDriverVersion* \[ dans\]
</dt> <dd>

Version du pilote d’imprimante principal.

</dd> <dt>

*pbDriverInstalled* \[ à\]
</dt> <dd>

Pointeur vers **true** si le pilote, ou une version plus récente, est installé ; sinon, **false** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est S \_ OK, sinon le **HRESULT** contient un code d’erreur.

Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Noms Unicode et ANSI<br/>   | **CorePrinterDriverInstalledW** (Unicode) et **CorePrinterDriverInstalledA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> </dl>

 

