---
description: spécifie un préfixe qui est en lien avec l’interface \# 4.
ms.assetid: cc3aa99d-cf45-460c-bdc1-3e9a19806fe4
title: Préfixes de site IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed8a21c59f9b6727c98ccb7fdacf4e9ec6ea5cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545785"
---
# <a name="ipv6-site-prefixes"></a>Préfixes de site IPv6

La commande IPv6 RTU autorise la configuration des préfixes on-Link publiés avec une longueur de préfixe de site. Si ce paramètre est spécifié, la longueur du préfixe de site est placée dans une option d’informations de préfixe dans les annonces de routeur. Par exemple :

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

spécifie un préfixe qui est en lien avec l’interface \# 4. Le préfixe est publié, ce qui signifie qu’il est inclus dans les annonces de routeur si l’interface \# 4 est une interface de publicité. La durée de vie dans l’option informations sur le préfixe est de 1800 secondes (30 minutes). La longueur du préfixe du site dans l’option informations sur le préfixe est 48.

La réception d’une option d’informations de préfixe spécifiant un préfixe de site entraîne la création d’une entrée dans la table de préfixe de site, qui peut être affichée à l’aide de la commande IPv6 SPT. La table de préfixe de site est utilisée pour supprimer des adresses site-local inappropriées de celles retournées par les fonctions [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et related.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Adresses IPv6 locales et de site local](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> </dl>

 

 



