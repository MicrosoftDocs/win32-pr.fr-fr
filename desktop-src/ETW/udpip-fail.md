---
description: Cette classe est la classe de type d’événement pour les événements de défaillance TCP/IP. La syntaxe suivante est simplifiée à partir du code MOF.
ms.assetid: 552e63ef-70e4-4bc4-be33-bd77bd5acd61
title: Classe UdpIp_Fail
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UdpIp_Fail
- UdpIp_Fail.Proto
- UdpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: aef0194d296395501500022bf4cae8b9c8a8f188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973823"
---
# <a name="udpip_fail-class"></a><span data-ttu-id="e665e-104">\_Classe d’échec UdpIp</span><span class="sxs-lookup"><span data-stu-id="e665e-104">UdpIp\_Fail class</span></span>

<span data-ttu-id="e665e-105">Cette classe est la classe de type d’événement pour les événements de défaillance TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="e665e-105">This class is the event type class for TCP/IP failure events.</span></span>

<span data-ttu-id="e665e-106">La syntaxe suivante est simplifiée à partir du code MOF.</span><span class="sxs-lookup"><span data-stu-id="e665e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e665e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e665e-107">Syntax</span></span>

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class UdpIp_Fail : UdpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a><span data-ttu-id="e665e-108">Membres</span><span class="sxs-lookup"><span data-stu-id="e665e-108">Members</span></span>

<span data-ttu-id="e665e-109">La classe d' **\_ échec UdpIp** a les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e665e-109">The **UdpIp\_Fail** class has these types of members:</span></span>

-   [<span data-ttu-id="e665e-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e665e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e665e-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e665e-111">Properties</span></span>

<span data-ttu-id="e665e-112">La classe d' **\_ échec UdpIp** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="e665e-112">The **UdpIp\_Fail** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e665e-113">**FailureCode**</span><span class="sxs-lookup"><span data-stu-id="e665e-113">**FailureCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e665e-114">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e665e-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e665e-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e665e-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e665e-116">Motif de l’échec.</span><span class="sxs-lookup"><span data-stu-id="e665e-116">Reason for the failure.</span></span> <span data-ttu-id="e665e-117">Il peut s’agir de l’un des codes suivants :</span><span class="sxs-lookup"><span data-stu-id="e665e-117">Can be one of the following codes:</span></span>

<dl> <dt>

<span data-ttu-id="e665e-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**Erreur \_ \_Ressources INsuffisantes** (1)</span><span class="sxs-lookup"><span data-stu-id="e665e-118"><span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**ERROR\_INSUFFICIENT\_RESOURCES** (1)</span></span>
</dt> <dt>

<span data-ttu-id="e665e-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**Erreur \_ TROP \_ d' \_ adresses** (2)</span><span class="sxs-lookup"><span data-stu-id="e665e-119"><span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**ERROR\_TOO\_MANY\_ADDRESSES** (2)</span></span>
</dt> <dt>

<span data-ttu-id="e665e-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**Erreur \_ L’adresse \_ existe** (3)</span><span class="sxs-lookup"><span data-stu-id="e665e-120"><span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**ERROR\_ADDRESS\_EXISTS** (3)</span></span>
</dt> <dt>

<span data-ttu-id="e665e-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**Erreur \_ \_Adresse non valide** (4)</span><span class="sxs-lookup"><span data-stu-id="e665e-121"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS** (4)</span></span>
</dt> <dt>

<span data-ttu-id="e665e-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**Erreur \_ AUTRE** (5)</span><span class="sxs-lookup"><span data-stu-id="e665e-122"><span id="ERROR_OTHER"></span><span id="error_other"></span>**ERROR\_OTHER** (5)</span></span>
</dt> <dt>

<span data-ttu-id="e665e-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**Erreur \_ L' \_ adresse TIMEWAIT \_ existe** (6)</span><span class="sxs-lookup"><span data-stu-id="e665e-123"><span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**ERROR\_TIMEWAIT\_ADDRESS\_EXIST** (6)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e665e-124">**Proto**</span><span class="sxs-lookup"><span data-stu-id="e665e-124">**Proto**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e665e-125">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e665e-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e665e-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="e665e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e665e-127">Identifie le protocole.</span><span class="sxs-lookup"><span data-stu-id="e665e-127">Identifies the protocol.</span></span> <span data-ttu-id="e665e-128">Peut avoir l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e665e-128">Can be one of the following values:</span></span>



| <span data-ttu-id="e665e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e665e-129">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="e665e-130">Signification</span><span class="sxs-lookup"><span data-stu-id="e665e-130">Meaning</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <span data-ttu-id="e665e-131"><dt>**AF \_ INET**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e665e-131"><dt>**AF\_INET**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="e665e-132">Famille d’adresses IPv4 (Internet Protocol version 4).</span><span class="sxs-lookup"><span data-stu-id="e665e-132">The Internet Protocol version 4 (IPv4) address family.</span></span><br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <span data-ttu-id="e665e-133"><dt>**AF \_ INET6**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="e665e-133"><dt>**AF\_INET6**</dt> <dt>23</dt></span></span> </dl> | <span data-ttu-id="e665e-134">Famille d’adresses IPv6 (Internet Protocol version 6).</span><span class="sxs-lookup"><span data-stu-id="e665e-134">The Internet Protocol version 6 (IPv6) address family..</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e665e-135">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e665e-135">Requirements</span></span>



| <span data-ttu-id="e665e-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e665e-136">Requirement</span></span> | <span data-ttu-id="e665e-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="e665e-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e665e-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e665e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e665e-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e665e-139">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e665e-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e665e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e665e-141">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e665e-141">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e665e-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e665e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e665e-143">**UdpIp**</span><span class="sxs-lookup"><span data-stu-id="e665e-143">**UdpIp**</span></span>](udpip.md)
</dt> </dl>

 

 




