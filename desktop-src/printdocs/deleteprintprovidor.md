---
description: La fonction DeletePrintProvidor supprime un fournisseur d’impression ajouté par la fonction AddPrintProvidor.
ms.assetid: b7104f9a-111c-4904-a355-063bb4cc81f1
title: DeletePrintProvidor, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProvidor
- DeletePrintProvidorA
- DeletePrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e68e56f115bac8abb1d0999990f57067f791d76d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203710"
---
# <a name="deleteprintprovidor-function"></a>DeletePrintProvidor fonction)

La fonction **DeletePrintProvidor** supprime un fournisseur d’impression ajouté par la fonction [**AddPrintProvidor**](addprintprovidor.md) .

## <a name="syntax"></a>Syntaxe


```C++
BOOL DeletePrintProvidor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProviderName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Réservé doit avoir la **valeur null**.

</dd> <dt>

*pEnvironment* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement à partir duquel le fournisseur doit être supprimé (par exemple, Windows NT x86, Windows IA64 ou Windows x64). Si ce paramètre a la **valeur null**, le fournisseur est supprimé de l’environnement actuel de l’application appelante et de l’ordinateur client (et non de l’application de destination et du serveur d’impression). La valeur **null** est recommandée, car elle offre une portabilité maximale.

</dd> <dt>

*pPrintProviderName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fournisseur à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

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
| Noms Unicode et ANSI<br/>   | **DeletePrintProvidorW** (Unicode) et **DeletePrintProvidorA** (ANSI)<br/>                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProvidor**](addprintprovidor.md)
</dt> </dl>

 

 




