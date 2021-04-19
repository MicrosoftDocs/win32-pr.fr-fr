---
description: Le type d’adresse identifie le format d’adresse, par exemple le numéro de téléphone standard ou l’adresse de messagerie. Seules les applications qui négocient TAPI version 3,0 ou ultérieure peuvent utiliser des types d’adresse.
ms.assetid: 2c32eda1-e510-40eb-ae75-fc7b9e9953cd
title: Constantes LINEADDRESSTYPE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d0a46eff2a7a0c38fa17aed4b831ef8701c565
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520916"
---
# <a name="lineaddresstype_-constants"></a><span data-ttu-id="6f4b5-104">\_Constantes LINEADDRESSTYPE</span><span class="sxs-lookup"><span data-stu-id="6f4b5-104">LINEADDRESSTYPE\_ Constants</span></span>

<span data-ttu-id="6f4b5-105">Le type d’adresse identifie le format d’adresse, par exemple le numéro de téléphone standard ou l’adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="6f4b5-105">The address type identifies address format, such as standard phone number or e-mail address.</span></span> <span data-ttu-id="6f4b5-106">Seules les applications qui négocient TAPI version 3,0 ou ultérieure peuvent utiliser des types d’adresse.</span><span class="sxs-lookup"><span data-stu-id="6f4b5-106">Only applications that negotiate TAPI version 3.0 or higher can use address types.</span></span>

<dl> <dt>

<span data-ttu-id="6f4b5-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE \_ PHONENUMBER**</span><span class="sxs-lookup"><span data-stu-id="6f4b5-107"><span id="LINEADDRESSTYPE_PHONENUMBER"></span><span id="lineaddresstype_phonenumber"></span>**LINEADDRESSTYPE\_PHONENUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f4b5-108">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6f4b5-108">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="6f4b5-109">Le type d’adresse est un numéro de téléphone standard.</span><span class="sxs-lookup"><span data-stu-id="6f4b5-109">Address type is a standard phone number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f4b5-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**\_SDP LINEADDRESSTYPE**</span><span class="sxs-lookup"><span data-stu-id="6f4b5-110"><span id="LINEADDRESSTYPE_SDP"></span><span id="lineaddresstype_sdp"></span>**LINEADDRESSTYPE\_SDP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f4b5-111">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6f4b5-111">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="6f4b5-112">Le type d’adresse est Conférence SDP (session Description Protocol).</span><span class="sxs-lookup"><span data-stu-id="6f4b5-112">Address type is Session Description Protocol (SDP) conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f4b5-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE \_ EMAILNAME**</span><span class="sxs-lookup"><span data-stu-id="6f4b5-113"><span id="LINEADDRESSTYPE_EMAILNAME"></span><span id="lineaddresstype_emailname"></span>**LINEADDRESSTYPE\_EMAILNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f4b5-114">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6f4b5-114">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="6f4b5-115">Le type d’adresse est un nom de messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="6f4b5-115">Address type is an e-mail name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f4b5-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE \_ nomdomaine**</span><span class="sxs-lookup"><span data-stu-id="6f4b5-116"><span id="LINEADDRESSTYPE_DOMAINNAME"></span><span id="lineaddresstype_domainname"></span>**LINEADDRESSTYPE\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f4b5-117">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6f4b5-117">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="6f4b5-118">Le type d’adresse est un nom de domaine.</span><span class="sxs-lookup"><span data-stu-id="6f4b5-118">Address type is a domain name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6f4b5-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**\_adresse IP LINEADDRESSTYPE**</span><span class="sxs-lookup"><span data-stu-id="6f4b5-119"><span id="LINEADDRESSTYPE_IPADDRESS"></span><span id="lineaddresstype_ipaddress"></span>**LINEADDRESSTYPE\_IPADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6f4b5-120">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6f4b5-120">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="6f4b5-121">Le type d’adresse est une adresse IP.</span><span class="sxs-lookup"><span data-stu-id="6f4b5-121">Address type is an IP address.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6f4b5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f4b5-122">Requirements</span></span>



| <span data-ttu-id="6f4b5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f4b5-123">Requirement</span></span> | <span data-ttu-id="6f4b5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f4b5-124">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6f4b5-125">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="6f4b5-125">TAPI version</span></span><br/> | <span data-ttu-id="6f4b5-126">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6f4b5-126">Requires TAPI 3.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6f4b5-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f4b5-127">Header</span></span><br/>       | <dl> <span data-ttu-id="6f4b5-128"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f4b5-128"><dt>Tapi.h</dt></span></span> </dl> |



 

 




