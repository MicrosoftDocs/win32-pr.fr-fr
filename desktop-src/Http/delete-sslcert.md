---
title: delete sslcert
description: Supprime les liaisons de certificat de serveur SSL et les stratégies de certificat client correspondantes pour une adresse IP et un port.
ms.assetid: 2adea7a8-f31f-4c02-8279-7d452e36cd9b
keywords:
- supprimer sslcert HTTP
topic_type:
- apiref
api_name:
- delete sslcert
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7672df5eee1634c41ff153435edcbecc58c2595
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "103678869"
---
# <a name="delete-sslcert"></a>delete sslcert

Supprime les liaisons de certificat de serveur SSL et les stratégies de certificat client correspondantes pour une adresse IP et un port.

``` syntax
delete sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>**\[ipport = \] * * * adresse IP : port*
</dt> <dd>

Spécifie l’adresse IPv4 ou IPv6 et le port pour lequel les liaisons de certificat SSL vont être supprimées.

</dd> </dl>

## <a name="examples"></a>Exemples

**delete sslcert ipport=1.1.1.1:443**

**delete sslcert ipport=0.0.0.0:443**

**Delete sslcert ipport = \[ ::: \] 443**

 

 




