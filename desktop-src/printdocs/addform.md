---
description: La fonction AddForm ajoute un formulaire à la liste des formulaires disponibles qui peuvent être sélectionnés pour l’imprimante spécifiée.
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: AddForm, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231665"
---
# <a name="addform-function"></a>AddForm fonction)

La fonction **AddForm** ajoute un formulaire à la liste des formulaires disponibles qui peuvent être sélectionnés pour l’imprimante spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante qui prend en charge l’impression avec le formulaire spécifié. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Niveau de la structure vers laquelle *pForm* pointe. Cette valeur doit être 1 ou 2.

</dd> <dt>

*pForm* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**d' \_ informations \_**](form-info-1.md) de formulaire 1 ou d' [**informations de formulaire \_ \_ 2**](form-info-2.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Une application peut déterminer les formulaires disponibles pour une imprimante en appelant la fonction [**EnumForms**](enumforms.md) .

Si *pForm* pointe vers une [**information de formulaire \_ \_ 2**](form-info-2.md), **AddForm** échouera s’il existe déjà un formulaire portant le nom spécifié ou si la valeur *pKeyword* de la structure existe déjà.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumForms**](enumforms.md)
</dt> <dt>

[**Informations de formulaire \_ \_ 1**](form-info-1.md)
</dt> <dt>

[**Informations de formulaire \_ \_ 2**](form-info-2.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




