---
description: La fonction AdvancedDocumentProperties affiche une boîte de dialogue de configuration de l’imprimante pour l’imprimante spécifiée, ce qui permet à l’utilisateur de configurer cette imprimante.
ms.assetid: 29e33f34-f6ec-4989-b076-e1fef8eb5bc4
title: AdvancedDocumentProperties, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AdvancedDocumentProperties
- AdvancedDocumentPropertiesA
- AdvancedDocumentPropertiesW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: da8754add6e3f5997354c940c303c41d4588c7b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759561"
---
# <a name="advanceddocumentproperties-function"></a>AdvancedDocumentProperties fonction)

La fonction **AdvancedDocumentProperties** affiche une boîte de dialogue de configuration de l’imprimante pour l’imprimante spécifiée, ce qui permet à l’utilisateur de configurer cette imprimante.

Cette fonction est un cas particulier de la fonction [**DocumentProperties**](documentproperties.md) . Pour plus d’informations, consultez la section Notes.

## <a name="syntax"></a>Syntaxe


```C++
LONG AdvancedDocumentProperties(
  _In_  HWND     hWnd,
  _In_  HANDLE   hPrinter,
  _In_  LPTSTR   pDeviceName,
  _Out_ PDEVMODE pDevModeOutput,
  _In_  PDEVMODE pDevModeInput
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* \[ dans\]
</dt> <dd>

Handle de la fenêtre parente de la boîte de dialogue de configuration de l’imprimante.

</dd> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle d’un objet Printer. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*pDeviceName* \[ dans\]
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’appareil pour lequel une boîte de dialogue de configuration de l’imprimante doit être affichée.

</dd> <dt>

*pDevModeOutput* \[ à\]
</dt> <dd>

Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui contient les données de configuration spécifiées par l’utilisateur.

</dd> <dt>

*pDevModeInput* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui contient les données de configuration utilisées pour initialiser les contrôles de la boîte de dialogue de configuration de l’imprimante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction [**DocumentProperties**](documentproperties.md) avec ces paramètres réussit, la valeur de retour de **AdvancedDocumentProperties** est 1. Sinon, la valeur de retour est zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Cette fonction peut uniquement afficher la boîte de dialogue Configuration de l’imprimante pour permettre à un utilisateur de la configurer. Pour plus de contrôle, utilisez [**DocumentProperties**](documentproperties.md). Les paramètres d’entrée de cette fonction sont passés directement à **DocumentProperties** et la valeur *fMode* est définie sur DM \_ dans la \_ mémoire tampon \| DM dans le \_ tampon de sortie de l' \_ invite \| DM \_ \_ . Contrairement à **DocumentProperties**, cette fonction retourne uniquement 1 ou 0. Ainsi, vous ne pouvez pas déterminer la taille requise de [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) en affectant à *pDevMode* la valeur zéro.

Une application peut obtenir le nom désigné par le paramètre *pDeviceName* en appelant la fonction [**GetPrinter**](getprinter.md) , puis en examinant le membre **pPrinterName** de la structure d' [**informations d’imprimante \_ \_ 2**](printer-info-2.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **AdvancedDocumentPropertiesW** (Unicode) et **AdvancedDocumentPropertiesA** (ANSI)<br/>           |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrinter**](addprinter.md)
</dt> <dt>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**DocumentProperties**](documentproperties.md)
</dt> <dt>

[**GetPrinter**](getprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**\_Infos sur l’imprimante \_ 2**](printer-info-2.md)
</dt> </dl>

 

 




