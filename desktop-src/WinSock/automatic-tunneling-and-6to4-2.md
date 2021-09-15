---
description: Le tunneling automatique avec des adresses compatibles IPv4 et 6to4 fonctionne sur un itinéraire pour un préfixe qui est sur lien vers l’interface \# 2. Les 32 bits qui suivent le préfixe sont extraits et utilisés comme adresse de destination IPv4 pour le paquet encapsulé.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: Tunneling automatique IPv6 et 6to4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede1179902a7ec3276058e078d56e069603e54a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518981"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a>Tunneling automatique IPv6 et 6to4

Le tunneling automatique avec des adresses compatibles IPv4 et 6to4 fonctionne sur un itinéraire pour un préfixe qui est sur lien vers l’interface \# 2. Les 32 bits qui suivent le préfixe sont extraits et utilisés comme adresse de destination IPv4 pour le paquet encapsulé.

Le tunneling automatique utilise le préfixe ::/96, qui est activé par défaut. Vous pouvez la désactiver en supprimant l’itinéraire pour ::/96.

6to4 utilise le préfixe 2002 ::/16, qui n’est pas activé par défaut.

 

 



