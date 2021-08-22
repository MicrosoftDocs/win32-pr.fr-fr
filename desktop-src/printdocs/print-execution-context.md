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
ms.openlocfilehash: 78e4afb29b75c0a73799302ddb76e270b18ca2c38cb6325b59ebae5041d5f99e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033957"
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
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Winspool. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**Imprimer \_ les \_ données d’exécution**](print-execution-data.md)
</dt> </dl>

 

 




