---
description: La fonction EndPagePrinter informe le spouleur d’impression que l’application se trouve à la fin d’une page dans un travail d’impression.
ms.assetid: aceb88b9-375b-4cd2-996a-c369f590154e
title: EndPagePrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndPagePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 9a152716a295650575fce0fefe5299ca4a214c322afa6570760c988182f9ba65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119711859"
---
# <a name="endpageprinter-function"></a>EndPagePrinter fonction)

La fonction **EndPagePrinter** informe le spouleur d’impression que l’application se trouve à la fin d’une page dans un travail d’impression.

## <a name="syntax"></a>Syntaxe


```C++
BOOL EndPagePrinter(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante pour laquelle la page sera concluante. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

La séquence d’un travail d’impression se présente comme suit :

1.  Pour commencer un travail d’impression, appelez [**StartDocPrinter**](startdocprinter.md).
2.  Pour commencer chaque page, appelez [**StartPagePrinter**](startpageprinter.md).
3.  Pour écrire des données dans une page, appelez [**WritePrinter**](writeprinter.md).
4.  Pour terminer chaque page, appelez **EndPagePrinter**.
5.  Répétez les étapes 2, 3 et 4 pour autant de pages que nécessaire.
6.  Pour mettre fin au travail d’impression, appelez [**EndDocPrinter**](enddocprinter.md).

Quand une page dans un fichier mis en file d’attente dépasse environ 350 Mo, elle peut échouer et ne pas envoyer de message d’erreur. Par exemple, cela peut se produire lors de l’impression de fichiers EMF volumineux. La limite de taille de page dépend de nombreux facteurs, notamment de la quantité de mémoire virtuelle disponible, de la quantité de mémoire allouée par les processus d’appel et de la quantité de fragmentation dans le segment de mémoire de processus.

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

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**StartPagePrinter**](startpageprinter.md)
</dt> <dt>

[**WritePrinter**](writeprinter.md)
</dt> </dl>

 

 




