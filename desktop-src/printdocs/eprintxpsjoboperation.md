---
description: Spécifie si un travail d’impression XPS est dans la phase de mise en file d’attente ou de rendu.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: EPrintXPSJobOperation, énumération (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 44f1f7ed80cd1de071633de37c5f0e91e913841388754a65c0194665bd3084de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971538"
---
# <a name="eprintxpsjoboperation-enumeration"></a>Énumération EPrintXPSJobOperation

Spécifie si un travail d’impression XPS est dans la phase de mise en file d’attente ou de rendu.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**
</dt> <dd>

La tâche XPS est en attente.

</dd> <dt>

<span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**
</dt> <dd>

Le travail XPS est en rendu.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette énumération est principalement utilisée comme paramètre pour la fonction [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



 

 




