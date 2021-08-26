---
description: La fonction DeletePrinterConnection supprime une connexion à une imprimante qui a été établie par un appel à AddPrinterConnection ou ConnectToPrinterDlg.
ms.assetid: 7b056eea-fbd9-4a08-a2dc-7326caeec387
title: DeletePrinterConnection, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterConnection
- DeletePrinterConnectionA
- DeletePrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e8a00b8b29ff5da4fb9b75af435c36f6313bd46d287408731eb3171d2e3b5001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950059"
---
# <a name="deleteprinterconnection-function"></a>DeletePrinterConnection fonction)

La fonction **DeletePrinterConnection** supprime une connexion à une imprimante qui a été établie par un appel à [**AddPrinterConnection**](addprinterconnection.md) ou [**ConnectToPrinterDlg**](connecttoprinterdlg.md).

## <a name="syntax"></a>Syntaxe


```C++
BOOL DeletePrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pname* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de la connexion d’imprimante à supprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

La fonction **DeletePrinterConnection** ne supprime pas les fichiers de pilote d’imprimante qui ont été copiés sur le serveur auquel l’imprimante est attachée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **DeletePrinterConnectionW** (Unicode) et **DeletePrinterConnectionA** (ANSI)<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterConnection**](addprinterconnection.md)
</dt> <dt>

[**AddPrinterConnection2**](addprinterconnection2.md)
</dt> <dt>

[**ConnectToPrinterDlg**](connecttoprinterdlg.md)
</dt> </dl>

 

 




