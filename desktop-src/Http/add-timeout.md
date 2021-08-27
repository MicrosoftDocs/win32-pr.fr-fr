---
title: add timeout
description: Ajoute un délai d’attente global au service HTTP.sys.
ms.assetid: c59a64e2-36aa-4428-b727-df21f5632d0d
keywords:
- Ajouter le délai d’expiration HTTP
topic_type:
- apiref
api_name:
- add timeout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c66a136acf65022ccc3ba8b05d070e4855a64f7abdf9b0519f7c1628d292aa0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047599"
---
# <a name="add-timeout"></a>add timeout

Ajoute un délai d’attente global au service HTTP.sys.

``` syntax
add timeout [timeouttype=]{idleconnectiontimeout|headerwaittimeout}
            [value=]u-short

 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_timeouttype___idleconnectiontimeout_headerwaittimeout_"></span><span id="_TIMEOUTTYPE___IDLECONNECTIONTIMEOUT_HEADERWAITTIMEOUT_"></span>**\[timeouttype = \] {idleconnectiontimeout, \| HeaderWaitTimeout}**
</dt> <dd>

Spécifie le type de délai d’attente pour la définition de.

</dd> <dt>

<span id="_value__u-short"></span><span id="_VALUE__U-SHORT"></span>**\[ valeur = \]**_u-Short_
</dt> <dd>

Spécifie la valeur du délai d’attente (en secondes). Si la valeur est hexadécimale, ajoutez le préfixe 0x.

</dd> </dl>

## <a name="examples"></a>Exemples

**add timeout timeouttype=idleconnectiontimeout value=120**

**add timeout timeouttype=headerwaittimeout value=0x40**

 

 




