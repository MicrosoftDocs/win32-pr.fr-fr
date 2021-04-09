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
# <a name="delete-iplisten"></a><span data-ttu-id="64384-104">delete iplisten</span><span class="sxs-lookup"><span data-stu-id="64384-104">delete iplisten</span></span>

<span data-ttu-id="64384-105">Spécifie une adresse IPv4 ou IPv6 à supprimer de la liste d’écoutes IP.</span><span class="sxs-lookup"><span data-stu-id="64384-105">Specifies an IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

``` syntax
delete iplisten [ address=] IPAddress
 
```

## <a name="parameters"></a><span data-ttu-id="64384-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64384-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64384-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[ adresse = \]** *IPAddress*</span><span class="sxs-lookup"><span data-stu-id="64384-107"><span id="_address___IPAddress"></span><span id="_address___ipaddress"></span><span id="_ADDRESS___IPADDRESS"></span>**\[address=\]** *IPAddress*</span></span>
</dt> <dd>

<span data-ttu-id="64384-108">Spécifie l’adresse IPv4 ou IPv6 à supprimer de la liste d’écoutes IP.</span><span class="sxs-lookup"><span data-stu-id="64384-108">Specifies the IPv4 or IPv6 address to be deleted from the IP listen list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="64384-109">Notes</span><span class="sxs-lookup"><span data-stu-id="64384-109">Remarks</span></span>

<span data-ttu-id="64384-110">Supprime une adresse IP de la liste d’écoutes IP.</span><span class="sxs-lookup"><span data-stu-id="64384-110">Deletes an IP address to the IP listen list.</span></span> <span data-ttu-id="64384-111">Le numéro de port n’est pas inclus.</span><span class="sxs-lookup"><span data-stu-id="64384-111">This does not include the port number.</span></span> <span data-ttu-id="64384-112">La liste d’écoutes IP est utilisée pour définir l’étendue de la liste des adresses auxquelles le service HTTP est lié.</span><span class="sxs-lookup"><span data-stu-id="64384-112">The IP listen list is used to scope the list of addresses to which the HTTP service binds.</span></span> <span data-ttu-id="64384-113">« 0.0.0.0 » signifie toute adresse IPv4, tandis que « :: » signifie toute adresse IPv6.</span><span class="sxs-lookup"><span data-stu-id="64384-113">"0.0.0.0" means any IPv4 address and "::" means any IPv6 address.</span></span>

## <a name="examples"></a><span data-ttu-id="64384-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="64384-114">Examples</span></span>

<span data-ttu-id="64384-115">**Supprimez iplisten Address = FE80 :: 1**</span><span class="sxs-lookup"><span data-stu-id="64384-115">**delete iplisten address=fe80::1**</span></span>

<span data-ttu-id="64384-116">**supprimer l’adresse iplisten = 1.1.1.1**</span><span class="sxs-lookup"><span data-stu-id="64384-116">**delete iplisten address=1.1.1.1**</span></span>

<span data-ttu-id="64384-117">**supprimer l’adresse iplisten = 0.0.0.0**</span><span class="sxs-lookup"><span data-stu-id="64384-117">**delete iplisten address=0.0.0.0**</span></span>

<span data-ttu-id="64384-118">**supprimer iplisten Address = ::**</span><span class="sxs-lookup"><span data-stu-id="64384-118">**delete iplisten address=::**</span></span>

 

 




