---
description: La fonction FlushPrinter envoie une mémoire tampon à l’imprimante afin de l’effacer d’un état transitoire.
ms.assetid: 08e54175-da68-4ebd-91ec-8f4525f49d30
title: FlushPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FlushPrinter
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 78bd5b6ccc86651a717c29db8b938508c857f83dbd3bdf5364fb1596b8a2c956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949299"
---
# <a name="flushprinter-function"></a>FlushPrinter fonction)

La fonction **FlushPrinter** envoie une mémoire tampon à l’imprimante afin de l’effacer d’un état transitoire.

## <a name="syntax"></a>Syntaxe


```C++
BOOL FlushPrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten,
  _In_  DWORD   cSleep
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle de l’objet Printer. Il doit s’agir du même handle que celui qui a été utilisé dans un appel antérieur à [**WritePrinter**](writeprinter.md) , par le pilote d’imprimante.

</dd> <dt>

*pBuf* \[ dans\]
</dt> <dd>

Pointeur vers un tableau d’octets qui contient les données à écrire sur l’imprimante.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, du tableau pointé par *pBuf*.

</dd> <dt>

*pcWritten* \[ à\]
</dt> <dd>

Pointeur vers une valeur qui reçoit le nombre d’octets de données qui ont été écrits sur l’imprimante.

</dd> <dt>

*cSleep* \[ dans\]
</dt> <dd>

Durée, en millisecondes, pendant laquelle la ligne d’e/s du port de l’imprimante doit rester inactive.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

**FlushPrinter** doit être appelé uniquement si [**WritePrinter**](writeprinter.md) a échoué, laissant l’imprimante dans un état transitoire. Par exemple, l’imprimante peut passer à l’état transitoire lorsque le travail est abandonné et que le pilote d’imprimante a partiellement envoyé des données brutes à l’imprimante.

**FlushPrinter** peut également spécifier une période d’inactivité pendant laquelle le spouleur d’impression ne planifie aucun travail sur le port d’imprimante correspondant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




