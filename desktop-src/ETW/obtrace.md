---
description: Représente la classe parente à partir de laquelle toutes les classes de trace d’événements du gestionnaire d’objets sont dérivées.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: ObTrace, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8cf30fe0c7b028c819477bcf0c66c2b674fc588286916be1cd1fd1a6b207770d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328749"
---
# <a name="obtrace-class"></a>ObTrace, classe

Représente la classe parente à partir de laquelle toutes les classes de trace d’événements du gestionnaire d’objets sont dérivées.

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Membres

La classe **ObTrace** ne définit aucun membre.

## <a name="remarks"></a>Remarques

Pour activer le suivi d’événements du gestionnaire d’objets, appelez la fonction [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) avec le paramètre *InformationClass* égal à la valeur d’énumération de la [**\_ \_ classe informations de trace**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) **TraceSystemTraceEnableFlagsInfo** et le membre **EnableFlags** de la structure des [**\_ \_ Propriétés de trace d’événements**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) égal au **\_ \_ handle de perf ob** (0x80000040).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |



 

 
