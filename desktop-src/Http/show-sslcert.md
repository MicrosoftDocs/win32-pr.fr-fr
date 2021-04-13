---
title: show sslcert
description: Répertorie les liaisons de certificat de serveur SSL et les stratégies de certificat client correspondantes pour une adresse IP et un port.
ms.assetid: 8e20f55e-a357-4f9c-a24e-e234607c3196
keywords:
- afficher sslcert HTTP
topic_type:
- apiref
api_name:
- show sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b71c2faf370066f5ce8d5ce6a20b173a74d0f645
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313324"
---
# <a name="show-sslcert"></a>show sslcert

Répertorie les liaisons de certificat de serveur SSL et les stratégies de certificat client correspondantes pour une adresse IP et un port.

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = \] * * * adresse IP : port*
</dt> <dd>

Spécifie l’adresse IPv4 ou IPv6 et le port pour lequel les liaisons de certificat SSL seront affichées. Si vous ne spécifiez pas de ipport, toutes les liaisons sont répertoriées.

</dd> </dl>

## <a name="examples"></a>Exemples

**Show sslcert ipport = \[ FE80 :: 1 \] : 443**

**show sslcert ipport=1.1.1.1:443**

**show sslcert ipport=0.0.0.0:443**

**Show sslcert ipport = \[ ::: \] 443**

 

 




