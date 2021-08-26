---
description: La fonction DeletePrintProcessor supprime un processeur d’impression ajouté par la fonction AddPrintProcessor.
ms.assetid: 65c77874-aa2c-4b4c-b218-fad361270a3e
title: DeletePrintProcessor, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProcessor
- DeletePrintProcessorA
- DeletePrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: be88839ae51fc52d453e1171a8ed0489df7827dda9476bf5e27d9f3d6a16ee1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949989"
---
# <a name="deleteprintprocessor-function"></a>DeletePrintProcessor fonction)

La fonction **DeletePrintProcessor** supprime un processeur d’impression ajouté par la fonction [**AddPrintProcessor**](addprintprocessor.md) .

## <a name="syntax"></a>Syntaxe


```C++
BOOL DeletePrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur à partir duquel le processeur doit être supprimé. Si ce paramètre a la **valeur null**, le processeur de l’imprimante est supprimé localement.

</dd> <dt>

*pEnvironment* \[ dans\]
</dt> <dd>

pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement à partir duquel le processeur doit être supprimé (par exemple, Windows NT x86, Windows IA64 ou Windows x64). Si ce paramètre a la **valeur null**, le processeur est supprimé de l’environnement actuel de l’application appelante et de l’ordinateur client (pas du serveur d’impression et de l’application de destination). La valeur **null** est recommandée, car elle offre une portabilité maximale.

</dd> <dt>

*pPrintProcessorName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **DeletePrintProcessorW** (Unicode) et **DeletePrintProcessorA** (ANSI)<br/>                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> </dl>

 

