---
description: La fonction ScheduleJob demande que le spouleur d’impression planifie l’impression d’un travail d’impression spécifié.
ms.assetid: a103a29c-be4d-491e-9b04-84571fe969a5
title: ScheduleJob, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScheduleJob
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 9a09d3e67b4be422f10db7761f28a2aa873e9bd0d84ec2c09de23ae20c7cea4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470224"
---
# <a name="schedulejob-function"></a>ScheduleJob fonction)

La fonction **ScheduleJob** demande que le spouleur d’impression planifie l’impression d’un travail d’impression spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL ScheduleJob(
  _In_ HANDLE hPrinter,
  _In_ DWORD  dwJobID
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPrinter* \[ dans\]
</dt> <dd>

Handle vers l’imprimante pour le travail d’impression. Il doit s’agir d’une imprimante locale configurée comme imprimante spoulée. Si *hPrinter* est un handle vers une connexion d’imprimante distante, ou si l’imprimante est configurée pour l’impression directe, la fonction **ScheduleJob** échoue. Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.

*hPrinter* doit être le même handle d’imprimante que celui spécifié dans l’appel à [**AddJob**](addjob.md) qui a obtenu l’identificateur de travail d’impression *dwJobID* .

</dd> <dt>

*dwJobID* \[ dans\]
</dt> <dd>

Travail d’impression à planifier. Vous obtenez cet identificateur de travail d’impression en appelant la fonction [**AddJob**](addjob.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro.

## <a name="remarks"></a>Remarques

> [!Note]  
> Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement. La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application. L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.

 

Vous devez appeler la fonction [**AddJob**](addjob.md) avant d’appeler la fonction **ScheduleJob** . **AddJob** obtient l’identificateur du travail d’impression que vous transmettez à **ScheduleJob** en tant que *dwJobID*. Les deux appels doivent utiliser la même valeur pour *hPrinter*.

La fonction **ScheduleJob** vérifie si un fichier spouleur est valide. Si un fichier de mise en file d’attente n’est pas valide ou s’il est vide, **ScheduleJob** supprime à la fois le fichier spouleur et l’entrée correspondante dans le spouleur d’impression.

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

[**AddJob**](addjob.md)
</dt> <dt>

[**OpenPrinter**](openprinter.md)
</dt> </dl>

 

 




