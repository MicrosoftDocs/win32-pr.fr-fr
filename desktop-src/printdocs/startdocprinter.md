---
description: La fonction StartDocPrinter informe le spouleur d’impression qu’un document doit être mis en file d’attente pour l’impression.
ms.assetid: caa2bd80-4af3-4968-a5b9-d12f16cac6fc
title: StartDocPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StartDocPrinter
- StartDocPrinterA
- StartDocPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: f8bdb0ae08c88e553dad3a91f0f1a578bed4ad39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868025"
---
# <a name="startdocprinter-function"></a>StartDocPrinter fonction)

La fonction **StartDocPrinter** informe le spouleur d’impression qu’un document doit être mis en file d’attente pour l’impression.

## <a name="syntax"></a>Syntaxe


```C++
DWORD StartDocPrinter(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pDocInfo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Version de la structure vers laquelle *pDocInfo* pointe. Cette valeur doit être 1.

</dd> <dt>

*pDocInfo* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**\_ infos doc \_ 1**](doc-info-1.md) qui décrit le document à imprimer.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour identifie le travail d’impression.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

La séquence classique d’un travail d’impression est la suivante :

1.  Pour commencer un travail d’impression, appelez **StartDocPrinter**.
2.  Pour commencer chaque page, appelez [**StartPagePrinter**](startpageprinter.md).
3.  Pour écrire des données dans une page, appelez [**WritePrinter**](writeprinter.md).
4.  Pour terminer chaque page, appelez [**EndPagePrinter**](endpageprinter.md).
5.  Répétez les étapes 2, 3 et 4 pour autant de pages que nécessaire.
6.  Pour mettre fin au travail d’impression, appelez [**EndDocPrinter**](enddocprinter.md).

Notez que l’appel de [**StartPagePrinter**](startpageprinter.md) et de [**EndPagePrinter**](endpageprinter.md) peut ne pas être nécessaire, par exemple si le type de données d’impression comprend les informations de page.

Quand une page dans un fichier mis en file d’attente dépasse environ 350 Mo, elle peut échouer et ne pas envoyer de message d’erreur. Par exemple, cela peut se produire lors de l’impression de fichiers EMF volumineux. La limite de taille de page dépend de nombreux facteurs, notamment de la quantité de mémoire virtuelle disponible, de la quantité de mémoire allouée par les processus d’appel et de la quantité de fragmentation dans le segment de mémoire de processus.

## <a name="examples"></a>Exemples

Pour obtenir un exemple de programme qui utilise cette fonction, consultez [Comment : imprimer à l’aide de l’API d’impression GDI](how-to--print-using-the-gdi-print-api.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **StartDocPrinterW** (Unicode) et **StartDocPrinterA** (ANSI)<br/>                                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AddJob**](addjob.md)
</dt> <dt>

[**\_Infos doc \_ 1**](doc-info-1.md)
</dt> <dt>

[**\_Infos doc \_ 2**](doc-info-2.md)
</dt> <dt>

[**EndDocPrinter**](enddocprinter.md)
</dt> <dt>

[**EndPagePrinter**](endpageprinter.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




