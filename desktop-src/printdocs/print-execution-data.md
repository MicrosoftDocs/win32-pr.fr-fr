---
description: Contient le contexte d’exécution du pilote d’imprimante qui appelle GetPrintExecutionData.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: Structure PRINT_EXECUTION_DATA (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_DATA
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 0e33f77a3140c62a1f472fc27948ec26a7ecf3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204229"
---
# <a name="print_execution_data-structure"></a>Imprimer \_ la \_ structure des données d’exécution

Contient le contexte d’exécution du pilote d’imprimante qui appelle [**GetPrintExecutionData**](getprintexecutiondata.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a>Membres

<dl> <dt>

**context**
</dt> <dd>

Valeur [**du \_ \_ contexte d’exécution**](print-execution-context.md) de l’impression qui représente le contexte d’exécution actuel du pilote d’imprimante.

</dd> <dt>

**clientAppPID**
</dt> <dd>

Si la valeur de **Context** est **le \_ contexte d’exécution d’impression \_ \_ WOW64**, **clientAppPID** identifie l’application cliente au nom duquel le processus de splwow64.exe a chargé le pilote d’imprimante. Si la valeur du **contexte** n’affiche pas le **\_ contexte d’exécution \_ \_ WOW64**, **clientAppPID** est égal à zéro.

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

[**Imprimer \_ le \_ contexte d’exécution**](print-execution-context.md)
</dt> </dl>

 

 




