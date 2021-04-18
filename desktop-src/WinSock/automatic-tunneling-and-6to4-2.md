---
description: Le tunneling automatique avec des adresses compatibles IPv4 et 6to4 fonctionne sur un itinéraire pour un préfixe qui est sur lien vers l’interface \# 2. Les 32 bits qui suivent le préfixe sont extraits et utilisés comme adresse de destination IPv4 pour le paquet encapsulé.
ms.assetid: 92261a1b-2b7f-4a76-b98a-2631dc303618
title: Tunneling automatique IPv6 et 6to4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede1179902a7ec3276058e078d56e069603e54a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516006"
---
# <a name="ipv6-automatic-tunneling-and-6to4"></a><span data-ttu-id="8c1c9-104">Tunneling automatique IPv6 et 6to4</span><span class="sxs-lookup"><span data-stu-id="8c1c9-104">IPv6 Automatic Tunneling and 6to4</span></span>

<span data-ttu-id="8c1c9-105">Le tunneling automatique avec des adresses compatibles IPv4 et 6to4 fonctionne sur un itinéraire pour un préfixe qui est sur lien vers l’interface \# 2.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-105">Automatic tunneling with IPv4-compatible addresses and 6to4 both work through a route for a prefix that is on-link to interface \#2.</span></span> <span data-ttu-id="8c1c9-106">Les 32 bits qui suivent le préfixe sont extraits et utilisés comme adresse de destination IPv4 pour le paquet encapsulé.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-106">The 32 bits following the prefix are extracted and used as an IPv4 destination address for the encapsulated packet.</span></span>

<span data-ttu-id="8c1c9-107">Le tunneling automatique utilise le préfixe ::/96, qui est activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-107">Automatic tunneling uses the ::/96 prefix, which is enabled by default.</span></span> <span data-ttu-id="8c1c9-108">Vous pouvez la désactiver en supprimant l’itinéraire pour ::/96.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-108">It can be disabled by removing the route for ::/96.</span></span>

<span data-ttu-id="8c1c9-109">6to4 utilise le préfixe 2002 ::/16, qui n’est pas activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="8c1c9-109">6to4 uses the 2002::/16 prefix, which is not enabled by default.</span></span>

 

 



