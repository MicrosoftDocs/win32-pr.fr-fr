---
description: La fonction GetDefaultPrinter récupère le nom de l’imprimante par défaut de l’utilisateur actuel sur l’ordinateur local.
ms.assetid: 8ec06743-43ce-4fac-83c4-f09eac7ee333
title: GetDefaultPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetDefaultPrinter
- GetDefaultPrinterA
- GetDefaultPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 8db5b2aef859ea5d8247fc203611af74c8daddd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517839"
---
# <a name="getdefaultprinter-function"></a>GetDefaultPrinter fonction)

La fonction **GetDefaultPrinter** récupère le nom de l’imprimante par défaut de l’utilisateur actuel sur l’ordinateur local.

## <a name="syntax"></a>Syntaxe


```C++
BOOL GetDefaultPrinter(
  _In_    LPTSTR  pszBuffer,
  _Inout_ LPDWORD pcchBuffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pszBuffer* \[ dans\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit une chaîne de caractères se terminant par null et contenant le nom par défaut de l’imprimante. Si ce paramètre a la **valeur null**, la fonction échoue et la variable vers laquelle pointe *pcchBuffer* retourne la taille de mémoire tampon requise, en caractères.

</dd> <dt>

*pcchBuffer* \[ in, out\]
</dt> <dd>

En entrée, spécifie la taille, en caractères, de la mémoire tampon *pszBuffer* . Lors de la sortie, reçoit la taille, en caractères, de la chaîne du nom de l’imprimante, y compris le caractère null de fin.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro et la variable vers laquelle pointe *pcchBuffer* contient le nombre de caractères copiés dans la mémoire tampon *pszBuffer* , y compris le caractère null de fin.

Si la fonction échoue, la valeur de retour est égale à zéro.



| Valeur                       | Signification                                                                                                                        |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| ERREUR \_ de \_ mémoire tampon insuffisante | La mémoire tampon *pszBuffer* est trop petite. La variable vers laquelle pointe *pcchBuffer* contient la taille de mémoire tampon requise, en caractères. |
| \_fichier d' \_ erreur \_ introuvable     | Il n’y a pas d’imprimante par défaut.                                                                                                   |



 

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
| Noms Unicode et ANSI<br/>   | **GetDefaultPrinterW** (Unicode) et **GetDefaultPrinterA** (ANSI)<br/>                             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**SetDefaultPrinter**](setdefaultprinter.md)
</dt> </dl>

 

 




