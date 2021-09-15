---
description: La fonction SetForm définit les informations de formulaire pour l’imprimante spécifiée.
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
title: SetForm, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetForm
- SetFormA
- SetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 93848afa0f36032bb972f8f4a7c6c3d5eb8c42ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127519449"
---
# <a name="setform-function"></a>SetForm fonction)

La fonction **SetForm** définit les informations de formulaire pour l’imprimante spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL SetForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName,
  _In_ DWORD  Level,
  _In_ LPTSTR pForm
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante pour laquelle les informations de formulaire sont définies. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*pFormName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du formulaire pour lequel les informations de formulaire sont définies.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Version de la structure vers laquelle *pForm* pointe. Cette valeur doit être 1 ou 2.

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

 

**SetForm** peut être appelé plusieurs fois pour une [**information de formulaire existante \_ \_ 2**](form-info-2.md), chaque appel ajoutant des paires de valeurs **pDisplayName** et **wLangId** supplémentaires. Toutes les versions linguistiques du formulaire obtiendront les valeurs **Size** et **ImageableArea** des **informations de \_ formulaire \_ 2** dans l’appel le plus récent à **SetForm**.

Si l’appelant est distant et que le *niveau* est 2, la valeur **StringType** des [**informations de formulaire \_ \_ 2**](form-info-2.md) ne peut pas être de type chaîne \_ MUIDLL.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **SetFormW** (Unicode) et **SetFormA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**Informations de formulaire \_ \_ 1**](form-info-1.md)
</dt> <dt>

[**Informations de formulaire \_ \_ 2**](form-info-2.md)
</dt> </dl>

 

 




