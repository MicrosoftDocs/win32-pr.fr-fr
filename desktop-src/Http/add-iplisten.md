---
title: add iplisten
description: Spécifie une adresse IPv4 ou IPv6 à ajouter à la liste d’écoutes IP.
ms.assetid: 38253818-c029-4a46-ab52-095cbfdeeaf4
keywords:
- Ajouter iplisten HTTP
topic_type:
- apiref
api_name:
- add iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2133a3f590c46c9e27b518d7621c158b86895961acb07670f6603e03513d1cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014977"
---
# <a name="add-iplisten"></a>add iplisten

Spécifie une adresse IPv4 ou IPv6 à ajouter à la liste d’écoutes IP.

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ IPAddress = \]** *IPAddress*
</dt> <dd>

Spécifie l’adresse IPv4 ou IPv6 à ajouter à la liste d’écoutes IP.

</dd> </dl>

## <a name="remarks"></a>Remarques

Ajoute une nouvelle adresse IP à la liste d’écoutes IP. Le numéro de port n’est pas inclus. La liste d’écoutes IP est utilisée pour définir l’étendue de la liste des adresses auxquelles le service HTTP est lié. « 0.0.0.0 » signifie toute adresse IPv4, tandis que « :: » signifie toute adresse IPv6.

## <a name="examples"></a>Exemples

**add iplisten ipaddress=fe80::1**

**add iplisten ipaddress=1.1.1.1**

**add iplisten ipaddress=0.0.0.0**

**add iplisten ipaddress=::**

 

 




