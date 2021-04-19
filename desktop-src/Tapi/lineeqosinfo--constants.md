---
description: Ces constantes sont utilisées par un TSP pour identifier le résultat d’une demande QoS (Quality of service).
ms.assetid: 617ddbf4-212f-4990-93c2-f38f04b035ab
title: Constantes LINEEQOSINFO_ (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423cc6172a1c6c87c1f3bb38929f727a15dad5c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535336"
---
# <a name="lineeqosinfo_-constants"></a><span data-ttu-id="dd0c8-103">\_Constantes LINEEQOSINFO</span><span class="sxs-lookup"><span data-stu-id="dd0c8-103">LINEEQOSINFO\_ Constants</span></span>

<span data-ttu-id="dd0c8-104">Ces constantes sont utilisées par un TSP pour identifier le résultat d’une demande QoS (Quality of service).</span><span class="sxs-lookup"><span data-stu-id="dd0c8-104">These constants are used by a TSP to identify the result of a QoS (Quality of Service) request.</span></span>

<dl> <dt>

<span data-ttu-id="dd0c8-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO \_ NOQOS**</span><span class="sxs-lookup"><span data-stu-id="dd0c8-105"><span id="LINEEQOSINFO_NOQOS"></span><span id="lineeqosinfo_noqos"></span>**LINEEQOSINFO\_NOQOS**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="dd0c8-106">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dd0c8-106">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="dd0c8-107">QoS n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="dd0c8-107">QoS is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd0c8-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO \_ ADMISSIONFAILURE**</span><span class="sxs-lookup"><span data-stu-id="dd0c8-108"><span id="LINEEQOSINFO_ADMISSIONFAILURE"></span><span id="lineeqosinfo_admissionfailure"></span>**LINEEQOSINFO\_ADMISSIONFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="dd0c8-109">0x00000002</span><span class="sxs-lookup"><span data-stu-id="dd0c8-109">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="dd0c8-110">La demande QoS n’a pas pu être satisfaite.</span><span class="sxs-lookup"><span data-stu-id="dd0c8-110">The QoS request could not be met.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd0c8-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO \_ POLICYFAILURE**</span><span class="sxs-lookup"><span data-stu-id="dd0c8-111"><span id="LINEEQOSINFO_POLICYFAILURE"></span><span id="lineeqosinfo_policyfailure"></span>**LINEEQOSINFO\_POLICYFAILURE**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="dd0c8-112">0x00000003</span><span class="sxs-lookup"><span data-stu-id="dd0c8-112">0x00000003</span></span>
</dt> <dt>



<span data-ttu-id="dd0c8-113">Le type de QoS demandé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="dd0c8-113">The type of QoS requested is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="dd0c8-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO \_ erreur générique**</span><span class="sxs-lookup"><span data-stu-id="dd0c8-114"><span id="LINEEQOSINFO_GENERICERROR"></span><span id="lineeqosinfo_genericerror"></span>**LINEEQOSINFO\_GENERICERROR**</span></span>
</dt> <dd> <dl> <dt>

 <span data-ttu-id="dd0c8-115">0x00000004</span><span class="sxs-lookup"><span data-stu-id="dd0c8-115">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="dd0c8-116">Erreur QoS non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dd0c8-116">Unspecified QoS error.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd0c8-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd0c8-117">Requirements</span></span>



| <span data-ttu-id="dd0c8-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd0c8-118">Requirement</span></span> | <span data-ttu-id="dd0c8-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd0c8-119">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="dd0c8-120">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="dd0c8-120">TAPI version</span></span><br/> | <span data-ttu-id="dd0c8-121">Nécessite TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="dd0c8-121">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="dd0c8-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd0c8-122">Header</span></span><br/>       | <dl> <span data-ttu-id="dd0c8-123"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd0c8-123"><dt>Tspi.h</dt></span></span> </dl> |



 

 




