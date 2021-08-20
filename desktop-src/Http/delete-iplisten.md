---
title: delete iplisten
description: Spécifie une adresse IPv4 ou IPv6 à supprimer de la liste d’écoutes IP.
ms.assetid: 1d0935a5-77de-4fdf-8d3b-88c8578bd5c7
keywords:
- supprimer iplisten HTTP
topic_type:
- apiref
api_name:
- delete iplisten
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42dbe9716ae19fdbbfb8f147b0f5f7f5a592adbf7b241c2f4e4548e0ee7e6e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014867"
---
# <a name="delete-iplisten"></a>delete iplisten

Spécifie une adresse IPv4 ou IPv6 à supprimer de la liste d’écoutes IP.

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ adresse = \]** *IPAddress*
</dt> <dd>

Spécifie l’adresse IPv4 ou IPv6 à supprimer de la liste d’écoutes IP.

</dd> </dl>

## <a name="remarks"></a>Remarques

Supprime une adresse IP de la liste d’écoutes IP. Le numéro de port n’est pas inclus. La liste d’écoutes IP est utilisée pour définir l’étendue de la liste des adresses auxquelles le service HTTP est lié. « 0.0.0.0 » signifie toute adresse IPv4, tandis que « :: » signifie toute adresse IPv6.

## <a name="examples"></a>Exemples

**Supprimez iplisten Address = FE80 :: 1**

**supprimer l’adresse iplisten = 1.1.1.1**

**supprimer l’adresse iplisten = 0.0.0.0**

**supprimer iplisten Address = ::**

 

 




