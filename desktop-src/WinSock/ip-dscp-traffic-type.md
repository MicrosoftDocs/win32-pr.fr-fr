---
description: Le tableau suivant décrit les \_ options de socket de type de trafic IP DSCP \_ \_ .
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 80cbe41e58cf36cd366015d83af380f5952630ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525488"
---
# <a name="ip_dscp_traffic_type"></a><span data-ttu-id="f5fb9-103">\_type de \_ trafic \_ DSCP IP</span><span class="sxs-lookup"><span data-stu-id="f5fb9-103">IP\_DSCP\_TRAFFIC\_TYPE</span></span>

<span data-ttu-id="f5fb9-104">Le tableau suivant décrit les \_ options de socket de type de trafic IP DSCP \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f5fb9-104">The following table describes IP\_DSCP\_TRAFFIC\_TYPE Socket Options.</span></span>

<dl> <span data-ttu-id="f5fb9-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**\_type de \_ trafic \_ DSCP IP**</dt> </span><span class="sxs-lookup"><span data-stu-id="f5fb9-105"><dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**IP\_DSCP\_TRAFFIC\_TYPE**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="f5fb9-106">Option</span><span class="sxs-lookup"><span data-stu-id="f5fb9-106">Option</span></span>              | <span data-ttu-id="f5fb9-107">Obtenir</span><span class="sxs-lookup"><span data-stu-id="f5fb9-107">Get</span></span> | <span data-ttu-id="f5fb9-108">Définissez</span><span class="sxs-lookup"><span data-stu-id="f5fb9-108">Set</span></span> | <span data-ttu-id="f5fb9-109">Type Optval</span><span class="sxs-lookup"><span data-stu-id="f5fb9-109">Optval Type</span></span> | <span data-ttu-id="f5fb9-110">Description</span><span class="sxs-lookup"><span data-stu-id="f5fb9-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5fb9-111">\_type de trafic DSCP \_</span><span class="sxs-lookup"><span data-stu-id="f5fb9-111">DSCP\_TRAFFIC\_TYPE</span></span> | <span data-ttu-id="f5fb9-112">Oui</span><span class="sxs-lookup"><span data-stu-id="f5fb9-112">Yes</span></span> | <span data-ttu-id="f5fb9-113">Oui</span><span class="sxs-lookup"><span data-stu-id="f5fb9-113">Yes</span></span> | <span data-ttu-id="f5fb9-114">DWORD</span><span class="sxs-lookup"><span data-stu-id="f5fb9-114">DWORD</span></span>       | <span data-ttu-id="f5fb9-115">En définissant cette valeur sur les valeurs définies dans **\_ \_ type de trafic DSCP**, une application peut demander à ses paquets réseau d’être traités en fonction du type de service demandé.</span><span class="sxs-lookup"><span data-stu-id="f5fb9-115">By setting this value to values defined in **DSCP\_TRAFFIC\_TYPE**, an application will be able to ask its network packets to be treated according to the type of service being requested.</span></span> <span data-ttu-id="f5fb9-116">De même, les appels à [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) peuvent être utilisés pour obtenir le paramètre actuel pour le type de trafic demandé sur le socket donné.</span><span class="sxs-lookup"><span data-stu-id="f5fb9-116">Similarly calls to [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) can be used to obtain the current setting for the type of traffic requested on the given socket</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5fb9-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5fb9-117">Requirements</span></span>



| <span data-ttu-id="f5fb9-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5fb9-118">Requirement</span></span> | <span data-ttu-id="f5fb9-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5fb9-119">Value</span></span> |
|----------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f5fb9-120">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="f5fb9-120">End of client support</span></span><br/> | <span data-ttu-id="f5fb9-121">Windows 10</span><span class="sxs-lookup"><span data-stu-id="f5fb9-121">Windows 10</span></span><br/>                                                          |
| <span data-ttu-id="f5fb9-122">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="f5fb9-122">End of server support</span></span><br/> | <span data-ttu-id="f5fb9-123">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f5fb9-123">Windows Server 2016</span></span><br/>                                                 |
| <span data-ttu-id="f5fb9-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5fb9-124">Header</span></span><br/>                | <dl> <span data-ttu-id="f5fb9-125"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="f5fb9-125"><dt>N/A</dt></span></span> </dl> |



 

 




