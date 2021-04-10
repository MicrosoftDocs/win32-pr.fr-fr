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
ms.openlocfilehash: 6090d3044be134035edb5f1f42a9790859d0301d
ms.sourcegitcommit: 243954e695c6ab5372b2935b095c3cd0b1202e16
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2020
ms.locfileid: "103940735"
---
# <a name="add-iplisten"></a><span data-ttu-id="9ab7e-104">add iplisten</span><span class="sxs-lookup"><span data-stu-id="9ab7e-104">add iplisten</span></span>

<span data-ttu-id="9ab7e-105">Spécifie une adresse IPv4 ou IPv6 à ajouter à la liste d’écoutes IP.</span><span class="sxs-lookup"><span data-stu-id="9ab7e-105">Specifies an IPv4 or IPv6 address to be added to the IP listen list.</span></span>

``` syntax
add iplisten [ ipaddress=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="9ab7e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9ab7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ab7e-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ IPAddress = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="9ab7e-107"><span id="__ipaddress___IPAddress"></span><span id="__ipaddress___ipaddress"></span><span id="__ipADDRESS___IPADDRESS"></span>**\[ ipaddress=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="9ab7e-108">Spécifie l’adresse IPv4 ou IPv6 à ajouter à la liste d’écoutes IP.</span><span class="sxs-lookup"><span data-stu-id="9ab7e-108">Specifies the IPv4 or IPv6 address to be added to the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ab7e-109">Notes</span><span class="sxs-lookup"><span data-stu-id="9ab7e-109">Remarks</span></span>

<span data-ttu-id="9ab7e-110">Ajoute une nouvelle adresse IP à la liste d’écoutes IP.</span><span class="sxs-lookup"><span data-stu-id="9ab7e-110">Adds a new IP address to the IP listen list.</span></span> <span data-ttu-id="9ab7e-111">Le numéro de port n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="9ab7e-111">This does not include the port number.</span></span> <span data-ttu-id="9ab7e-112">La liste d’écoutes IP est utilisée pour définir l’étendue de la liste des adresses auxquelles le service HTTP est lié.</span><span class="sxs-lookup"><span data-stu-id="9ab7e-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="9ab7e-113">« 0.0.0.0 » signifie toute adresse IPv4, tandis que « :: » signifie toute adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="9ab7e-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="9ab7e-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="9ab7e-114">Examples</span></span>

<span data-ttu-id="9ab7e-115">**add iplisten ipaddress=fe80::1**</span><span class="sxs-lookup"><span data-stu-id="9ab7e-115">**add iplisten ipaddress=fe80::1**</span></span>

<span data-ttu-id="9ab7e-116">**add iplisten ipaddress=1.1.1.1**</span><span class="sxs-lookup"><span data-stu-id="9ab7e-116">**add iplisten ipaddress=1.1.1.1**</span></span>

<span data-ttu-id="9ab7e-117">**add iplisten ipaddress=0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="9ab7e-117">**add iplisten ipaddress=0.0.0.0**</span></span>

<span data-ttu-id="9ab7e-118">**add iplisten ipaddress=::**</span><span class="sxs-lookup"><span data-stu-id="9ab7e-118">**add iplisten ipaddress=::**</span></span>

 

 




