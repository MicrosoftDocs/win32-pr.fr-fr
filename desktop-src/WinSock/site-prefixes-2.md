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
# <a name="ipv6-site-prefixes"></a><span data-ttu-id="353a3-103">Préfixes de site IPv6</span><span class="sxs-lookup"><span data-stu-id="353a3-103">IPv6 Site Prefixes</span></span>

<span data-ttu-id="353a3-104">La commande IPv6 RTU autorise la configuration des préfixes on-Link publiés avec une longueur de préfixe de site.</span><span class="sxs-lookup"><span data-stu-id="353a3-104">The ipv6 rtu command allows published on-link prefixes to be configured with a site prefix length.</span></span> <span data-ttu-id="353a3-105">Si ce paramètre est spécifié, la longueur du préfixe de site est placée dans une option d’informations de préfixe dans les annonces de routeur.</span><span class="sxs-lookup"><span data-stu-id="353a3-105">If specified, the site prefix length is put into a prefix information option in router advertisements.</span></span> <span data-ttu-id="353a3-106">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="353a3-106">For example:</span></span>

``` syntax
ipv6 rtu 2002:836b:9820:2::/64 4 pub life 1800 spl 48
```

<span data-ttu-id="353a3-107">spécifie un préfixe qui est en lien avec l’interface \# 4.</span><span class="sxs-lookup"><span data-stu-id="353a3-107">specifies a prefix that is on-link to interface \#4.</span></span> <span data-ttu-id="353a3-108">Le préfixe est publié, ce qui signifie qu’il est inclus dans les annonces de routeur si l’interface \# 4 est une interface de publicité.</span><span class="sxs-lookup"><span data-stu-id="353a3-108">The prefix is published, meaning that it is included in router advertisements if interface \#4 is an advertising interface.</span></span> <span data-ttu-id="353a3-109">La durée de vie dans l’option informations sur le préfixe est de 1800 secondes (30 minutes).</span><span class="sxs-lookup"><span data-stu-id="353a3-109">The lifetime in the prefix information option is 1800 seconds (30 minutes).</span></span> <span data-ttu-id="353a3-110">La longueur du préfixe du site dans l’option informations sur le préfixe est 48.</span><span class="sxs-lookup"><span data-stu-id="353a3-110">The site prefix length in the prefix information option is 48.</span></span>

<span data-ttu-id="353a3-111">La réception d’une option d’informations de préfixe spécifiant un préfixe de site entraîne la création d’une entrée dans la table de préfixe de site, qui peut être affichée à l’aide de la commande IPv6 SPT.</span><span class="sxs-lookup"><span data-stu-id="353a3-111">The receipt of a prefix information option that specifies a site prefix causes an entry to be created in the site prefix table, which can be displayed by using the ipv6 spt command.</span></span> <span data-ttu-id="353a3-112">La table de préfixe de site est utilisée pour supprimer des adresses site-local inappropriées de celles retournées par les fonctions [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et related.</span><span class="sxs-lookup"><span data-stu-id="353a3-112">The site prefix table is used to remove inappropriate site-local addresses from those returned by the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and related functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="353a3-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="353a3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="353a3-114">Adresses IPv6 locales et de site local</span><span class="sxs-lookup"><span data-stu-id="353a3-114">IPv6 Link-local and Site-local Addresses</span></span>](link-local-and-site-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="353a3-115">Netsh.exe</span><span class="sxs-lookup"><span data-stu-id="353a3-115">Netsh.exe</span></span>](netsh-exe.md)
</dt> </dl>

 

 



