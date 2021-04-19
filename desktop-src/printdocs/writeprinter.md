---
description: La fonction WritePrinter informe le spouleur d’impression que les données doivent être écrites sur l’imprimante spécifiée.
ms.assetid: 9411b71f-d686-44ed-9051-d410e5ab228e
title: WritePrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WritePrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 490221b15ed1e3c7dad3a4cb523c15e9ec484b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527492"
---
# <a name="writeprinter-function"></a>WritePrinter fonction)

La fonction **WritePrinter** informe le spouleur d’impression que les données doivent être écrites sur l’imprimante spécifiée.

> [!Note]  
> **WritePrinter** prend uniquement en charge l’impression GDI et ne doit pas être utilisé pour l’impression XPS. Si votre travail d’impression utilise le chemin d’impression XPS ou OpenXPS, utilisez l' [API d’impression XPS](/windows/desktop/printdocs/xps-printing). L’envoi de travaux d’impression XPS ou OpenXPS au spouleur à l’aide de **WritePrinter** n’est pas pris en charge et peut entraîner des résultats indéterminés.

 

## <a name="syntax"></a>Syntaxe


```C++
BOOL WritePrinter(
  _In_  HANDLE  hPrinter,
  _In_  LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcWritten
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*pBuf* \[ dans\]
</dt> <dd>

Pointeur vers un tableau d’octets qui contient les données qui doivent être écrites sur l’imprimante.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, du tableau.

</dd> <dt>

*pcWritten* \[ à\]
</dt> <dd>

Pointeur vers une valeur qui reçoit le nombre d’octets de données qui ont été écrits sur l’imprimante.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Notes

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

La séquence d’un travail d’impression se présente comme suit :

1.  Pour commencer un travail d’impression, appelez [**StartDocPrinter**](startdocprinter.md).
2.  Pour commencer chaque page, appelez [**StartPagePrinter**](startpageprinter.md).
3.  Pour écrire des données dans une page, appelez **WritePrinter**.
4.  Pour terminer chaque page, appelez [**EndPagePrinter**](endpageprinter.md).
5.  Répétez les étapes 2, 3 et 4 pour autant de pages que nécessaire.
6.  Pour mettre fin au travail d’impression, appelez [**EndDocPrinter**](enddocprinter.md).

Lorsqu’un document de niveau supérieur (par exemple, un fichier Adobe PDF ou Microsoft Word) ou d’autres données d’imprimante (par exemple, PCL, PS ou HPGL) sont envoyés directement à une imprimante, les paramètres d’impression définis dans le document ont priorité sur les paramètres d’impression Windows. Les documents sont générés lorsque la valeur du membre *pDatatype* de la structure [**\_ infos doc \_ 1**](doc-info-1.md) qui a été transmise dans le paramètre *PDOCINFO* de l’appel [**StartDocPrinter**](startdocprinter.md) est « RAW » doit décrire entièrement les paramètres du travail d’impression de style [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)dans la langue comprise par le matériel.

Dans les versions de Windows antérieures à Windows XP, quand une page dans un fichier mis en file d’attente dépasse environ 350 Mo, elle peut échouer et ne pas envoyer de message d’erreur. Par exemple, cela peut se produire lors de l’impression de fichiers EMF volumineux. La limite de taille de page dans les versions de Windows antérieures à Windows XP dépend de nombreux facteurs, notamment la quantité de mémoire virtuelle disponible, la quantité de mémoire allouée par les processus appelant et la quantité de fragmentation dans le segment de mémoire de processus. Dans Windows XP et les versions ultérieures de Windows, les fichiers EMF doivent avoir une taille inférieure ou égale à 2 Go. Si **WritePrinter** est utilisé pour écrire des données non EMF, telles que le PDL prêt pour l’impression, la taille du fichier est limitée uniquement par l’espace disque disponible.

## <a name="examples"></a>Exemples

Pour obtenir un exemple de programme qui utilise cette fonction, consultez [Comment : imprimer à l’aide de l’API d’impression GDI](how-to--print-using-the-gdi-print-api.md).

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

 

