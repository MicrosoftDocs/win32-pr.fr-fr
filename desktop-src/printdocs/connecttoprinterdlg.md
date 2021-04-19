---
description: La fonction ConnectToPrinterDlg affiche une boîte de dialogue qui permet aux utilisateurs de parcourir les imprimantes et de s’y connecter sur un réseau.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: ConnectToPrinterDlg, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521962"
---
# <a name="connecttoprinterdlg-function"></a>ConnectToPrinterDlg fonction)

La fonction **ConnectToPrinterDlg** affiche une boîte de dialogue qui permet aux utilisateurs de parcourir les imprimantes et de s’y connecter sur un réseau. Si l’utilisateur sélectionne une imprimante, la fonction tente de créer une connexion à celle-ci ; Si aucun pilote approprié n’est installé sur le serveur, l’utilisateur a la possibilité de créer une imprimante localement.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Spécifie la fenêtre parente de la boîte de dialogue.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Ce paramètre est réservé et doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction s’exécute correctement et que l’utilisateur sélectionne une imprimante, la valeur de retour est un handle vers l’imprimante sélectionnée.

Si la fonction échoue, ou si l’utilisateur annule la boîte de dialogue sans sélectionner d’imprimante, la valeur de retour est **null**.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

La fonction **ConnectToPrinterDlg** tente de créer une connexion à l’imprimante sélectionnée. Toutefois, si le serveur sur lequel l’imprimante réside n’a pas de pilote approprié installé, la fonction offre à l’utilisateur la possibilité de créer une imprimante localement. Une application appelante peut déterminer si la fonction a créé une imprimante localement en appelant [**GetPrinter**](getprinter.md) avec une structure [**Printer \_ info \_ 2**](printer-info-2.md) , puis en examinant le membre des **attributs** de cette structure.

Une application doit appeler [**DeletePrinter**](deleteprinter.md) pour supprimer une imprimante locale. Une application doit appeler [**DeletePrinterConnection**](deleteprinterconnection.md) pour supprimer une connexion à une imprimante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>WinSpool. drv</dt> </dl>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinterConnection**](addprinterconnection.md)
</dt> <dt>

[**ClosePrinter**](closeprinter.md)
</dt> <dt>

[**DeletePrinter**](deleteprinter.md)
</dt> <dt>

[**DeletePrinterConnection**](deleteprinterconnection.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




