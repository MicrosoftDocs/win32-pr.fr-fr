---
description: Signale au service spouleur d’impression si un travail d’impression XPS se trouve dans la phase de mise en file d’attente ou de rendu et quelle partie du traitement est actuellement en cours.
ms.assetid: 66f7483d-be98-410d-b0c7-430743397de2
title: ReportJobProcessingProgress, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReportJobProcessingProgress
api_type:
- DllExport
api_location:
- Spoolss.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- WinSpool.Drv
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: a560c584568dac251ae529255958c9a26fb159631f17d1534949aba38674ccd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823989"
---
# <a name="reportjobprocessingprogress-function"></a>ReportJobProcessingProgress fonction)

Signale au service spouleur d’impression si un travail d’impression XPS se trouve dans la phase de mise en file d’attente ou de rendu et quelle partie du traitement est actuellement en cours.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ReportJobProcessingProgress(
  _In_ HANDLE                printerHandle,
  _In_ ULONG                 jobId,
       EPrintXPSJobOperation jobOperation,
       EPrintXPSJobProgress  jobProgress
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*printerHandle* \[ dans\]
</dt> <dd>

Handle d’imprimante pour lequel la fonction doit récupérer des informations. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

</dd> <dt>

*JobID* \[ dans\]
</dt> <dd>

Identifie le travail d’impression dont les données doivent être récupérées. Utilisez la fonction [**AddJob**](addjob.md) ou la fonction [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) pour obtenir un identificateur de travail d’impression.

</dd> <dt>

*jobOperation* 
</dt> <dd>

Spécifie si le travail se trouve dans la phase de mise en file d’attente ou dans la phase de rendu.

</dd> <dt>

*jobProgress* 
</dt> <dd>

Spécifie quelle partie du traitement est en cours d’exécution. Cette valeur fait référence aux événements de la phase de mise en file d’attente ou de rendu en fonction de la valeur de *jobOperation*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est S \_ OK, sinon le **HRESULT** contient un code d’erreur.

Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

> [!Note]  
> **ReportJobProcessingProgress** indique uniquement la progression du travail d’impression XPS si le travail d’impression est en phase de mise en file d’attente ou de rendu. **ReportJobProcessingProgress** échoue si elle est appelée lorsque le travail d’impression XPS n’est pas dans la phase de mise en file d’attente ou de rendu.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression](printdocs-printing.md)
</dt> <dt>

[Fonctions API du spouleur d’impression](printing-and-print-spooler-functions.md)
</dt> <dt>

[**EPrintXPSJobOperation**](eprintxpsjoboperation.md)
</dt> <dt>

[**EPrintXPSJobProgress**](eprintxpsjobprogress.md)
</dt> </dl>

 

