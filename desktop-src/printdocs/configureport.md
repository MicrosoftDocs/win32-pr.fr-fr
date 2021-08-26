---
description: La fonction ConfigurePort affiche la boîte de dialogue de configuration du port pour un port sur le serveur spécifié.
ms.assetid: a65e9876-d6af-48c2-9e6b-8bd8695db130
title: ConfigurePort, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurePort
- ConfigurePortA
- ConfigurePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dbc31de341c137e8baf729a468e8576684ccef8b0a860be898c9cb5a6af34217
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950439"
---
# <a name="configureport-function"></a>ConfigurePort fonction)

La fonction **ConfigurePort** affiche la boîte de dialogue de configuration du port pour un port sur le serveur spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL ConfigurePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le port spécifié existe. Si ce paramètre a la **valeur null**, le port est local.

</dd> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle vers la fenêtre parente de la boîte de dialogue Configuration du port.

</dd> <dt>

*pPortName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du port à configurer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Avant d’appeler la fonction **ConfigurePort** , une application doit appeler la fonction [**EnumPorts**](enumports.md) pour déterminer les noms de ports valides.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **ConfigurePortW** (Unicode) et **ConfigurePortA** (ANSI)<br/>                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




