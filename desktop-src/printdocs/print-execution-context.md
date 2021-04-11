---
description: Représente le contexte d’exécution lorsque GetPrintExecutionData est appelé.
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: Énumération PRINT_EXECUTION_CONTEXT (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_CONTEXT
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 20b1050edc0088fb629ee10cf63dc9cffa07228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202806"
---
# <a name="print_execution_context-enumeration"></a>\_Énumération du contexte d’exécution d’impression \_

Représente le contexte d’exécution lorsque [**GetPrintExecutionData**](getprintexecutiondata.md) est appelé.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**Imprimer \_ le \_ contexte d’exécution \_ application**
</dt> <dd>

L’appelant est en cours d’exécution dans une application.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**\_ \_ \_ service spouleur du contexte d’exécution d’impression \_**
</dt> <dd>

L’appelant est en cours d’exécution dans le service de spouleur (spoolsv.exe).

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**\_ \_ \_ hôte d’isolation du spouleur du contexte \_ d’exécution d' \_ impression**
</dt> <dd>

L’appelant est en cours d’exécution dans l’hôte d’isolation d’impression (PrintIsolationHost.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**Imprimer \_ le \_ \_ pipeline du filtre du contexte d’exécution \_**
</dt> <dd>

L’appelant est en cours d’exécution dans le pipeline de filtre d’impression (printfilterpipelinesvc.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**Contexte d’exécution d’impression \_ \_ \_ WOW64**
</dt> <dd>

L’appelant est en cours d’exécution dans splwow64.exe

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                                                |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**Imprimer \_ les \_ données d’exécution**](print-execution-data.md)
</dt> </dl>

 

 




