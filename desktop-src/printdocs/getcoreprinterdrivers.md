---
description: Récupère le GUID, la version et la date des pilotes d’imprimante principaux spécifiés et le chemin d’accès à leurs packages.
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: GetCorePrinterDrivers, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319090"
---
# <a name="getcoreprinterdrivers-function"></a>GetCorePrinterDrivers fonction)

Récupère le GUID, la version et la date des pilotes d’imprimante principaux spécifiés et le chemin d’accès à leurs packages.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
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

*pszzCoreDriverDependencies* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne multiple se terminant par un caractère null qui spécifie les GUID des pilotes d’imprimante principaux.

</dd> <dt>

*cCorePrinterDrivers* \[ dans\]
</dt> <dd>

Nombre de chaînes dans *pszzCoreDriverDependencies*.

</dd> <dt>

*pCorePrinterDrivers* \[ à\]
</dt> <dd>

Pointeur vers un tableau d’une ou de plusieurs structures de [**\_ \_ pilote d’imprimante principale**](core-printer-driver.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est S \_ OK, sinon le **HRESULT** contient un code d’erreur.

Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).

## <a name="remarks"></a>Notes

Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Noms Unicode et ANSI<br/>   | **GetCorePrinterDriversW** (Unicode) et **GetCorePrinterDriversA** (ANSI)<br/>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> </dl>

 

