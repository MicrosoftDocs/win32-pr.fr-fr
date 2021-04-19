---
description: Ces constantes sont utilisées par un TSP pour identifier le type d’une demande QoS (Quality of service) qui est effectuée. À l’heure actuelle, seule une demande de niveau de service est prise en charge. Consultez \_ constantes LINEQOSSERVICELEVEL.
ms.assetid: 128fcaf8-a54d-4633-9f44-188b02e21709
title: Constantes LINEQOSREQUESTTYPE_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7795ddc70ea4fc6719578a38896a292ee1df9da3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528771"
---
# <a name="lineqosrequesttype_-constants"></a><span data-ttu-id="b6129-105">\_Constantes LINEQOSREQUESTTYPE</span><span class="sxs-lookup"><span data-stu-id="b6129-105">LINEQOSREQUESTTYPE\_ Constants</span></span>

<span data-ttu-id="b6129-106">Ces constantes sont utilisées par un TSP pour identifier le type d’une demande QoS (Quality of service) qui est effectuée.</span><span class="sxs-lookup"><span data-stu-id="b6129-106">These constants are used by a TSP to identify the type of a QoS (Quality of Service) request being made.</span></span> <span data-ttu-id="b6129-107">À l’heure actuelle, seule une demande de niveau de service est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b6129-107">Currently, only a service level request is supported.</span></span> <span data-ttu-id="b6129-108">Consultez [ \_ constantes LINEQOSSERVICELEVEL](lineqosservicelevel--constants.md).</span><span class="sxs-lookup"><span data-stu-id="b6129-108">See [LINEQOSSERVICELEVEL\_ Constants](lineqosservicelevel--constants.md).</span></span>

<dl> <dt>

<span data-ttu-id="b6129-109"><span id="LINEQOSREQUESTTYPE_SERVICELEVEL"></span><span id="lineqosrequesttype_servicelevel"></span>**LINEQOSREQUESTTYPE \_ SERVICELEVEL**</span><span class="sxs-lookup"><span data-stu-id="b6129-109"><span id="LINEQOSREQUESTTYPE_SERVICELEVEL"></span><span id="lineqosrequesttype_servicelevel"></span>**LINEQOSREQUESTTYPE\_SERVICELEVEL**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="b6129-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="b6129-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="b6129-111">La demande de qualité de service effectuée concerne un niveau de service particulier.</span><span class="sxs-lookup"><span data-stu-id="b6129-111">The QoS request being made is for a particular service level.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6129-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6129-112">Requirements</span></span>



| <span data-ttu-id="b6129-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6129-113">Requirement</span></span> | <span data-ttu-id="b6129-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6129-114">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b6129-115">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="b6129-115">TAPI version</span></span><br/> | <span data-ttu-id="b6129-116">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="b6129-116">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="b6129-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6129-117">Header</span></span><br/>       | <dl> <span data-ttu-id="b6129-118"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6129-118"><dt>Tspi.h</dt></span></span> </dl> |



 

 




