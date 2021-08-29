---
description: La fonction DeletePrinter supprime l’objet Printer spécifié.
ms.assetid: 04d9c073-b795-4307-ba89-d4984bc5b354
title: DeletePrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 08ba5a38214e2d6fb7c9a0eedef7949551b66fd275d9a00c2d09eeab12a79bf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112569"
---
# <a name="deleteprinter-function"></a>DeletePrinter fonction)

La fonction **DeletePrinter** supprime l’objet Printer spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL DeletePrinter(
  _Inout_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ in, out\]
</dt> <dd>

Handle vers un objet Printer qui sera supprimé. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

S’il reste des travaux d’impression à traiter pour l’imprimante spécifiée, **DeletePrinter** marque l’imprimante comme étant en attente de suppression, puis la supprime une fois que tous les travaux d’impression ont été imprimés. Aucun travail d’impression ne peut être ajouté à une imprimante marquée pour une suppression en attente.

Une imprimante marquée pour une suppression en attente ne peut pas être maintenue, mais ses travaux d’impression peuvent être conservés, repris et redémarrés. Si l’imprimante est maintenue et qu’il y a des travaux pour l’imprimante, **DeletePrinter** échoue avec l’erreur \_ accès \_ refusé.

Notez que **DeletePrinter** ne ferme pas le handle qui lui est passé. Ainsi, l’application doit toujours appeler [**ClosePrinter**](closeprinter.md).

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

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**EnumPrinters**](enumprinters.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




