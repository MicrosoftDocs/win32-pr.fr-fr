---
description: La fonction ReadPrinter récupère les données de l’imprimante spécifiée.
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
title: ReadPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 63683e421441fb15ec299f3077088bd8f9cffb65644550be912ee39b5c530371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824019"
---
# <a name="readprinter-function"></a>ReadPrinter fonction)

La fonction **ReadPrinter** récupère les données de l’imprimante spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL ReadPrinter(
  _In_  HANDLE  hPrinter,
  _Out_ LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pNoBytesRead
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle de l’objet Printer pour lequel récupérer des données. Utilisez la fonction [**OpenPrinter**](openprinter.md) pour récupérer un handle d’objet Printer. Utilisez le format : nom_imprimante, Job xxxx.

</dd> <dt>

*pBuf* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit les données de l’imprimante.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle *pBuf* pointe.

</dd> <dt>

*pNoBytesRead* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit le nombre d’octets de données copiés dans le tableau vers lequel *pBuf* pointe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

**ReadPrinter** renvoie une erreur si l’appareil ou l’imprimante n’est pas bidirectionnel.

## <a name="requirements"></a>Configuration requise



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

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




