---
description: La fonction SetDefaultPrinter définit le nom de l’imprimante par défaut de l’utilisateur actuel sur l’ordinateur local.
ms.assetid: 55eec548-577f-422b-80e3-8b23aa4d2159
title: SetDefaultPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDefaultPrinter
- SetDefaultPrinterA
- SetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 346d356aea3d806284823541aa219699e51c2187
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519452"
---
# <a name="setdefaultprinter-function"></a>SetDefaultPrinter fonction)

La fonction **SetDefaultPrinter** définit le nom de l’imprimante par défaut de l’utilisateur actuel sur l’ordinateur local.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SetDefaultPrinter(
  _In_ LPCTSTR pszPrinter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszPrinter* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par null et contenant le nom par défaut de l’imprimante. Pour une connexion d’imprimante distante, le format du nom est **\\\\** _serveur_ *_\\_* _nom_imprimante_. Pour une imprimante locale, le format du nom est *nom_imprimante*.

Si ce paramètre a la **valeur null** ou est une chaîne vide, autrement dit, «», **SetDefaultPrinter** sélectionne une imprimante par défaut à partir de l’une des imprimantes installées. Si une imprimante par défaut existe déjà, l’appel de **SetDefaultPrinter** avec une chaîne **null** ou vide dans ce paramètre peut modifier l’imprimante par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

Lorsque vous utilisez cette méthode, vous devez spécifier une imprimante, un pilote et un port valides. Si elles ne sont pas valides, les API n’échouent pas, mais le résultat n’est pas défini. Cela peut permettre à d’autres programmes de remettre l’imprimante à l’imprimante valide précédente. Vous pouvez utiliser [**EnumPrinters**](enumprinters.md) pour récupérer le nom de l’imprimante, le nom du pilote et le nom de port de toutes les imprimantes disponibles.

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **SetDefaultPrinterW** (Unicode) et **SetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**GetDefaultPrinter**](getdefaultprinter.md)
</dt> </dl>

 

 




