---
description: La fonction DeletePort affiche une boîte de dialogue qui permet à l’utilisateur de supprimer un nom de port.
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
title: DeletePort, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePort
- DeletePortA
- DeletePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fd1c54e6daa70ed3bfdb7c748f470da45f38445ca2588d97d2b195906b957b4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950079"
---
# <a name="deleteport-function"></a>DeletePort fonction)

La fonction **DeletePort** affiche une boîte de dialogue qui permet à l’utilisateur de supprimer un nom de port.

## <a name="syntax"></a>Syntaxe


```C++
BOOL DeletePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par zéro qui spécifie le nom du serveur pour lequel le port doit être supprimé. Si ce paramètre a la **valeur null**, un port local est supprimé.

</dd> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de la fenêtre parente de la boîte de dialogue de suppression de port.

</dd> <dt>

*pPortName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par zéro qui spécifie le nom du port qui doit être supprimé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Une application peut récupérer les noms des ports valides en appelant la fonction [**EnumPorts**](enumports.md) .

La fonction **DeletePort** renvoie une erreur si une imprimante est actuellement connectée au port spécifié.

L’appelant de la fonction **DeletePort** doit disposer d’un accès serveur \_ \_ administrer l’accès au serveur auquel le port est connecté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **DeletePortW** (Unicode) et **DeletePortA** (ANSI)<br/>                                           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPort**](addport.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




