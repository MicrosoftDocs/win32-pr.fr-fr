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
ms.openlocfilehash: 9ed7356d8dea3b4313a46c7d7906de15b7389edc
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104030465"
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

## <a name="remarks"></a>Notes

Supprime une adresse IP de la liste d’écoutes IP. Le numéro de port n’est pas inclus. La liste d’écoutes IP est utilisée pour définir l’étendue de la liste des adresses auxquelles le service HTTP est lié. « 0.0.0.0 » signifie toute adresse IPv4, tandis que « :: » signifie toute adresse IPv6.

## <a name="examples"></a>Exemples

**Supprimez iplisten Address = FE80 :: 1**

**supprimer l’adresse iplisten = 1.1.1.1**

**supprimer l’adresse iplisten = 0.0.0.0**

**supprimer iplisten Address = ::**

 

 




