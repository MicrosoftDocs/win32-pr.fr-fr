---
description: La fonction AddPort ajoute le nom d’un port à la liste des ports pris en charge. La fonction AddPort est exportée par le moniteur de port.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: AddPort, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 00e589b59b15c898887090b12348f23fac57fda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868345"
---
# <a name="addport-function"></a>AddPort fonction)

La fonction **addport** ajoute le nom d’un port à la liste des ports pris en charge. La fonction **addport** est exportée par le moniteur de port.

## <a name="syntax"></a>Syntaxe


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par zéro qui spécifie le nom du serveur auquel le port est connecté. Si ce paramètre a la **valeur null**, le port est local.

</dd> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de la fenêtre parente de la boîte de dialogue **addport** .

</dd> <dt>

*pMonitorName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par zéro qui spécifie l’analyse associée au port.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

La fonction **addport** parcourt le réseau pour rechercher les ports existants et affiche une boîte de dialogue pour l’utilisateur. La fonction **addport** doit valider le nom de port entré par l’utilisateur en appelant [**EnumPorts**](enumports.md) pour s’assurer qu’il n’existe aucun nom en double.

L’appelant de la fonction **addport** doit disposer d’un accès serveur \_ \_ administrer l’accès au serveur auquel le port est connecté.

Pour ajouter un port sans afficher de boîte de dialogue, appelez la fonction **XcvData** à la place de **addport**. Pour plus d’informations sur **XcvData**, consultez le kit de développement de pilotes (DDK) Microsoft Windows.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Noms Unicode et ANSI<br/>   | **AddPortW** (Unicode) et **AddPortA** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePort**](deleteport.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




