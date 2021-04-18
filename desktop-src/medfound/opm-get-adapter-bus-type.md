---
description: Retourne le type de bus d’e/s utilisé par la sortie vidéo.
ms.assetid: 1aff4c81-ffa0-4116-b7ea-60b1b83042df
title: OPM_GET_ADAPTER_BUS_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acde3611eb00977670c59c4326f793c1cb9037fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519583"
---
# <a name="opm_get_adapter_bus_type"></a><span data-ttu-id="9d9e3-103">TYPE de bus d’accès de l' \_ \_ adaptateur OPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="9d9e3-103">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>

<span data-ttu-id="9d9e3-104">Retourne le type de bus d’e/s utilisé par la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="9d9e3-104">Returns the type of I/O bus used by the video output.</span></span>



| <span data-ttu-id="9d9e3-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d9e3-105">Requirement</span></span> | <span data-ttu-id="9d9e3-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d9e3-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="9d9e3-107">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="9d9e3-107">Request GUID</span></span> | <span data-ttu-id="9d9e3-108">TYPE de bus d’accès de l' \_ \_ adaptateur OPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="9d9e3-108">OPM\_GET\_ADAPTER\_BUS\_TYPE</span></span>                                                |
| <span data-ttu-id="9d9e3-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="9d9e3-109">Input data</span></span>   | <span data-ttu-id="9d9e3-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="9d9e3-110">None</span></span>                                                                        |
| <span data-ttu-id="9d9e3-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="9d9e3-111">Return data</span></span>  | <span data-ttu-id="9d9e3-112">Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="9d9e3-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="9d9e3-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9d9e3-113">Remarks</span></span>

<span data-ttu-id="9d9e3-114">Le type de bus est retourné dans le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="9d9e3-114">The bus type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="9d9e3-115">La valeur est **un or au niveau du** bit des indicateurs de type de [**bus OPM**](opm-bus-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9d9e3-115">The value is a bitwise **OR** of [**OPM Bus Type Flags**](opm-bus-type-flags.md).</span></span>

<span data-ttu-id="9d9e3-116">Cette requête est équivalente à la \_ requête DXVA COPPQueryBusData utilisée dans le protocole Copp (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="9d9e3-116">This query is equivalent to the DXVA\_COPPQueryBusData query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d9e3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d9e3-117">Requirements</span></span>



| <span data-ttu-id="9d9e3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d9e3-118">Requirement</span></span> | <span data-ttu-id="9d9e3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d9e3-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9d9e3-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d9e3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9d9e3-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d9e3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9d9e3-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d9e3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9d9e3-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d9e3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9d9e3-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d9e3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d9e3-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d9e3-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d9e3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d9e3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d9e3-127">**IOPMVideoOutput :: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="9d9e3-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="9d9e3-128">**IOPMVideoOutput :: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="9d9e3-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="9d9e3-129">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="9d9e3-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




