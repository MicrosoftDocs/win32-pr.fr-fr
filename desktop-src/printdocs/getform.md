---
description: La fonction GetForm récupère des informations sur un formulaire spécifié.
ms.assetid: 10b25748-6d7c-46ab-bd2c-9b6126a1d7d1
title: GetForm, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetForm
- GetFormA
- GetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: bf5263d0de24d86053f8293f2fc9f6c410519ddef568cec9f4692223166e6ab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971438"
---
# <a name="getform-function"></a>GetForm fonction)

La fonction **GetForm** récupère des informations sur un formulaire spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL GetForm(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pFormName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*pFormName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du formulaire. Pour récupérer les noms des formulaires pris en charge par l’imprimante, appelez la fonction [**EnumForms**](enumforms.md) .

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Version de la structure vers laquelle *pForm* pointe. Cette valeur doit être 1 ou 2.

</dd> <dt>

*pForm* \[ à\]
</dt> <dd>

Pointeur vers un tableau d’octets qui reçoit la structure d' [**informations de \_ formulaire \_ 1**](form-info-1.md) ou [**d' \_ informations \_ de formulaire 2**](form-info-2.md) initialisée.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, du tableau *pForm* .

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une valeur qui spécifie le nombre d’octets copiés si la fonction est réussie ou le nombre d’octets requis si *cbBuf* est trop petit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Si l’appelant est distant et que le *niveau* est 2, la valeur **StringType** des informations de [**formulaire \_ \_ 2**](form-info-2.md) retournées est toujours la chaîne \_ LANGPAIR.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **GetFormW** (Unicode) et **GetFormA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**DeleteForm**](deleteform.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

 




