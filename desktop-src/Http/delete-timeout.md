---
title: delete timeout
description: Supprime un délai d’attente global et rend le service HTTP.sys rétabli aux valeurs par défaut.
ms.assetid: 5fcd5df4-023e-486d-b41a-639e210a128f
keywords:
- supprimer le délai d’expiration HTTP
topic_type:
- apiref
api_name:
- delete timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6ee436e1eb7f545a74aa56f6c146afbd1c57066
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "106511057"
---
# <a name="delete-timeout"></a>delete timeout

Supprime un délai d’attente global et rend le service HTTP.sys rétabli aux valeurs par défaut.

``` syntax
delete timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleconnectiontimeout, \| HeaderWaitTimeout}**
</dt> <dd>

Spécifie le type de paramètre de délai d’attente.

</dd> </dl>

## <a name="examples"></a>Exemples

**delete timeout timeouttype=idleconnectiontimeout**

**delete timeout timeouttype=headerwaittimeout**

 

 




