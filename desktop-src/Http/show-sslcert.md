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
# <a name="show-sslcert"></a><span data-ttu-id="b4b0b-104">show sslcert</span><span class="sxs-lookup"><span data-stu-id="b4b0b-104">show sslcert</span></span>

<span data-ttu-id="b4b0b-105">Répertorie les liaisons de certificat de serveur SSL et les stratégies de certificat client correspondantes pour une adresse IP et un port.</span><span class="sxs-lookup"><span data-stu-id="b4b0b-105">Lists SSL server certificate bindings and the corresponding client certificate policies for an IP address and port.</span></span>

``` syntax
show sslcert [ipport=]IP Address:port
 
```

## <a name="parameters"></a><span data-ttu-id="b4b0b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4b0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4b0b-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport = \] \* \* \* adresse IP : port*</span><span class="sxs-lookup"><span data-stu-id="b4b0b-107"><span id="_ipport__IP_Address_port"></span><span id="_ipport__ip_address_port"></span><span id="_IPPORT__IP_ADDRESS_PORT"></span>\**\[ipport=\]\*\*\*IP Address:port*</span></span>
</dt> <dd>

<span data-ttu-id="b4b0b-108">Spécifie l’adresse IPv4 ou IPv6 et le port pour lequel les liaisons de certificat SSL seront affichées.</span><span class="sxs-lookup"><span data-stu-id="b4b0b-108">Specifies the IPv4 or IPv6 address and port for which the SSL certificate bindings will be displayed.</span></span> <span data-ttu-id="b4b0b-109">Si vous ne spécifiez pas de ipport, toutes les liaisons sont répertoriées.</span><span class="sxs-lookup"><span data-stu-id="b4b0b-109">Not specifying an ipport lists all bindings.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="b4b0b-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="b4b0b-110">Examples</span></span>

<span data-ttu-id="b4b0b-111">**Show sslcert ipport = \[ FE80 :: 1 \] : 443**</span><span class="sxs-lookup"><span data-stu-id="b4b0b-111">**show sslcert ipport=\[fe80::1\]:443**</span></span>

<span data-ttu-id="b4b0b-112">**show sslcert ipport=1.1.1.1:443**</span><span class="sxs-lookup"><span data-stu-id="b4b0b-112">**show sslcert ipport=1.1.1.1:443**</span></span>

<span data-ttu-id="b4b0b-113">**show sslcert ipport=0.0.0.0:443**</span><span class="sxs-lookup"><span data-stu-id="b4b0b-113">**show sslcert ipport=0.0.0.0:443**</span></span>

<span data-ttu-id="b4b0b-114">**Show sslcert ipport = \[ ::: \] 443**</span><span class="sxs-lookup"><span data-stu-id="b4b0b-114">**show sslcert ipport=\[::\]:443**</span></span>

 

 




