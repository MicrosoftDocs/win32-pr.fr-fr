---
description: La fonction EndDocPrinter met fin à un travail d’impression pour l’imprimante spécifiée.
ms.assetid: 13c713e8-cc24-4191-8b1e-967b9e20e541
title: EndDocPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndDocPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 8d3e2bc110e5ee9412bb1edb89779f896edb015a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519737"
---
# <a name="enddocprinter-function"></a>EndDocPrinter fonction)

La fonction **EndDocPrinter** met fin à un travail d’impression pour l’imprimante spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
BOOL EndDocPrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers une imprimante pour laquelle le travail d’impression doit être terminé. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

La fonction **EndDocPrinter** retourne une erreur si le travail d’impression n’a pas été démarré en appelant la fonction [**StartDocPrinter**](startdocprinter.md) .

La séquence d’un travail d’impression se présente comme suit :

1.  Pour commencer un travail d’impression, appelez [**StartDocPrinter**](startdocprinter.md).
2.  Pour commencer chaque page, appelez [**StartPagePrinter**](startpageprinter.md).
3.  Pour écrire des données dans une page, appelez [**WritePrinter**](writeprinter.md).
4.  Pour terminer chaque page, appelez [**EndPagePrinter**](endpageprinter.md).
5.  Répétez les étapes 2, 3 et 4 pour autant de pages que nécessaire.
6.  Pour mettre fin au travail d’impression, appelez **EndDocPrinter**.

Quand une page dans un fichier mis en file d’attente dépasse environ 350 Mo, elle risque de ne pas s’imprimer et d’envoyer un message d’erreur. Par exemple, cela peut se produire lors de l’impression de fichiers EMF volumineux. La limite de taille de page dépend de nombreux facteurs, notamment de la quantité de mémoire virtuelle disponible, de la quantité de mémoire allouée par les processus d’appel et de la quantité de fragmentation dans le segment de mémoire de processus.

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

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




