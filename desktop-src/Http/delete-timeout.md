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
ms.openlocfilehash: b95571f3cfb0ff1b77b6da0106cb734af342dcb68689f15dbfdc35f6cb5e7339
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014877"
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

 

 




