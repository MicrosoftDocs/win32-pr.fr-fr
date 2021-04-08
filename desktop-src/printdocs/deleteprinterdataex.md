---
description: La fonction DeletePrinterDataEx supprime une valeur spécifiée des données de configuration pour une imprimante.
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: DeletePrinterDataEx, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDataEx
- DeletePrinterDataExA
- DeletePrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 07cf6262db0a1e3a3c4c098ee26e03b3fdad4002
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757389"
---
# <a name="deleteprinterdataex-function"></a>DeletePrinterDataEx fonction)

La fonction **DeletePrinterDataEx** supprime une valeur spécifiée des données de configuration pour une imprimante. Les données de configuration d’une imprimante consistent en un ensemble de valeurs nommées et typées stockées dans une hiérarchie de clés de registre. La fonction supprime une valeur spécifiée sous une clé spécifiée.

À l’instar de la fonction [**DeletePrinterData**](deleteprinterdata.md) , **DeletePrinterDataEx** peut supprimer des valeurs stockées par la fonction [**SetPrinterData**](setprinterdata.md) . En outre, **DeletePrinterDataEx** peut supprimer des valeurs stockées sous une clé spécifiée par la fonction [**SetPrinterDataEx**](setprinterdataex.md) .

## <a name="syntax"></a>Syntaxe


```C++
DWORD DeletePrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante pour laquelle la fonction supprime une valeur. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*pKeyName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie la clé contenant la valeur à supprimer. Utilisez la barre oblique inverse ( \\ ) comme séparateur pour spécifier un chemin d’accès qui a une ou plusieurs sous-clés.

Si *pKeyName* a la **valeur null** ou est une chaîne vide, **DELETEPRINTERDATAEX** retourne un paramètre d’erreur \_ non valide \_ .

</dd> <dt>

*pValueName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de la valeur à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour est un code d’erreur système.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **DeletePrinterDataExW** (Unicode) et **DeletePrinterDataExA** (ANSI)<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePrinterKey**](deleteprinterkey.md)
</dt> <dt>

[**EnumPrinterDataEx**](enumprinterdataex.md)
</dt> <dt>

[**EnumPrinterKey**](enumprinterkey.md)
</dt> <dt>

[**GetPrinterDataEx**](getprinterdataex.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetPrinterDataEx**](setprinterdataex.md)
</dt> </dl>

 

 




