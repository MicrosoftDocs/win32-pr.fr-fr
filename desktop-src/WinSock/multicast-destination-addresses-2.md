---
description: Lors de l’envoi à une adresse de destination de multidiffusion, le protocole IPv6 Microsoft requiert normalement que l’application ait une interface sortante spécifiée.
ms.assetid: dbfeaa1f-a7c5-4a15-90f0-4d1cdaf798e9
title: Adresses de destination de multidiffusion IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aa516713fb47f6af03d8564c464a07a19cf0f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484936"
---
# <a name="ipv6-multicast-destination-addresses"></a>Adresses de destination de multidiffusion IPv6

Lors de l’envoi à une adresse de destination de multidiffusion, le protocole IPv6 Microsoft requiert normalement que l’application ait une interface sortante spécifiée. Pour ce faire, vous pouvez utiliser l’option de socket **\_ multidiffusion \_ IPv6** ou lier le socket à une adresse source spécifique.

Vous pouvez également spécifier une interface par défaut pour une adresse de multidiffusion spécifique, une étendue d’adresse de multidiffusion complète ou toutes les adresses de multidiffusion. Cela est effectué avec un itinéraire qui place le préfixe de multidiffusion sur lien vers l’interface sortante souhaitée. Pour les exemples suivants, vous pouvez spécifier comment cela peut être spécifié :

``` syntax
ipv6 rtu ff02::5/128 3
ipv6 rtu ff0e::/16 3
ipv6 rtu ff00::/8 3
```

 

 



