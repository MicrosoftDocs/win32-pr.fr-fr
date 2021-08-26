---
description: La fonction AddJob ajoute un travail d’impression à la liste des travaux d’impression qui peuvent être planifiés par le spouleur d’impression. La fonction récupère le nom du fichier que vous pouvez utiliser pour stocker le travail.
ms.assetid: cfafa874-6022-4bf4-bf3d-096213eb0c98
title: AddJob, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddJob
- AddJobA
- AddJobW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de99b0866e8cd7ec8486d2a3f15f95194b4350008a43fe4db8ae82d970684c39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950749"
---
# <a name="addjob-function"></a>AddJob fonction)

La fonction **AddJob** ajoute un travail d’impression à la liste des travaux d’impression qui peuvent être planifiés par le spouleur d’impression. La fonction récupère le nom du fichier que vous pouvez utiliser pour stocker le travail.

> [!NOTE]
> dans Windows 8 et les systèmes d’exploitation ultérieurs, nous ne recommandons pas l’utilisation directe de **AddJob** , car il existe des cas (par exemple l’impression dans une file d’attente à l’aide de file : ou PORTPROMPT :) où **AddJob** échouera. Au lieu de cela, il est recommandé d’utiliser l' [API d’impression GDI](gdi-printing.md), l' [API d’impression XPS](xps-printing.md), [**StartDocPrinter**](startdocprinter.md)ou la méthode appropriée à partir du [**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing) , selon le scénario d’impression.
>
> Si vous essayez d’imprimer dans une file d’attente à l’aide de **file :** ou **PORTPROMPT :**, **AddJob** retourne l' \_ erreur non prise en charge.

## <a name="syntax"></a>Syntaxe

```C++
BOOL AddJob(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pData,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle qui spécifie l’imprimante pour le travail d’impression. Il doit s’agir d’une imprimante locale configurée comme imprimante spoulée. Si *hPrinter* est un handle vers une connexion d’imprimante distante, ou si l’imprimante est configurée pour l’impression directe, la fonction **AddJob** échoue. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

De *niveau* \[ dans\]
</dt> <dd>

Version de la structure de données d’informations du travail d’impression que la fonction stocke dans la mémoire tampon vers laquelle pointe *pData*. Définissez ce paramètre sur un.

</dd> <dt>

*pData* \[ à\]
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit une structure de données [**ADDJOB \_ information \_ 1**](addjob-info-1.md) et une chaîne de chemin d’accès.

</dd> <dt>

*cbBuf* \[ dans\]
</dt> <dd>

Taille, en octets, de la mémoire tampon vers laquelle pointe *pData*. La mémoire tampon doit être suffisamment grande pour contenir une structure [**ADDJOB \_ information \_ 1**](addjob-info-1.md) et une chaîne de chemin d’accès.

</dd> <dt>

*pcbNeeded* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille totale, en octets, de la structure de données [**ADDJOB \_ info \_ 1**](addjob-info-1.md) plus la chaîne du chemin d’accès. Si cette valeur est inférieure ou égale à *cbBuf* et que la fonction est réussie, il s’agit du nombre réel d’octets écrits dans la mémoire tampon pointée par *pData*. Si ce nombre est supérieur à *cbBuf*, la mémoire tampon est insuffisante et vous devez appeler à nouveau la fonction avec une taille de mémoire tampon au moins aussi grande que \* *pcbNeeded*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Vous pouvez appeler la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) pour ouvrir le fichier de mise en file d’attente spécifié par le membre **path** de la structure [**ADDJOB \_ info \_ 1**](addjob-info-1.md) , puis appeler la fonction [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) pour y écrire des données de travail d’impression. Après cela, appelez la fonction [**ScheduleJob**](schedulejob.md) pour notifier au spouleur d’impression que le travail d’impression peut désormais être planifié par le spouleur pour l’impression.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Noms Unicode et ANSI<br/>   | **AddJobW** (Unicode) et **AddJobA** (ANSI)<br/>                                                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Informations ADDJOB \_ 1**](addjob-info-1.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[API d’impression GDI](gdi-printing.md)
</dt> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> <dt>

[**ScheduleJob**](schedulejob.md)
</dt> <dt>

[**StartDocPrinter**](startdocprinter.md)
</dt> <dt>

[**Windows. Graphics. Printing**](/uwp/api/Windows.Graphics.Printing)
</dt> <dt>

[**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)
</dt> <dt>

[API d’impression XPS](xps-printing.md)
</dt> </dl>

 

