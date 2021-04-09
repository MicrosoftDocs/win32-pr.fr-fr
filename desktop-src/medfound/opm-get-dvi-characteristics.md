---
description: Demande si un connecteur DVI (Digital Video Interface) prend en charge DVI version 1,1 ou ultérieure.
ms.assetid: b6c450c0-e97f-472d-ae09-fa1e062aeb9e
title: OPM_GET_DVI_CHARACTERISTICS (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a6f996b0397db509a45af6e243359c581df333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034153"
---
# <a name="opm_get_dvi_characteristics"></a><span data-ttu-id="b5d06-103">\_ \_ caractéristiques DVI de l’offre OPM \_</span><span class="sxs-lookup"><span data-stu-id="b5d06-103">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>

<span data-ttu-id="b5d06-104">Demande si un connecteur DVI (Digital Video Interface) prend en charge DVI version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b5d06-104">Queries whether a digital video interface (DVI) connector supports DVI version 1.1 or later.</span></span>



| <span data-ttu-id="b5d06-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5d06-105">Requirement</span></span> | <span data-ttu-id="b5d06-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5d06-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="b5d06-107">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="b5d06-107">Request GUID</span></span> | <span data-ttu-id="b5d06-108">\_ \_ caractéristiques DVI de l’offre OPM \_</span><span class="sxs-lookup"><span data-stu-id="b5d06-108">OPM\_GET\_DVI\_CHARACTERISTICS</span></span>                                              |
| <span data-ttu-id="b5d06-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="b5d06-109">Input data</span></span>   | <span data-ttu-id="b5d06-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="b5d06-110">None</span></span>                                                                        |
| <span data-ttu-id="b5d06-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="b5d06-111">Return data</span></span>  | <span data-ttu-id="b5d06-112">Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="b5d06-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b5d06-113">Notes</span><span class="sxs-lookup"><span data-stu-id="b5d06-113">Remarks</span></span>

<span data-ttu-id="b5d06-114">Si cette requête est réussie, le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) contient l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b5d06-114">If this query succeeds, the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure contains one of the following values.</span></span>



| <span data-ttu-id="b5d06-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5d06-115">Value</span></span>                                     | <span data-ttu-id="b5d06-116">Description</span><span class="sxs-lookup"><span data-stu-id="b5d06-116">Description</span></span>               |
|-------------------------------------------|---------------------------|
| <span data-ttu-id="b5d06-117">\_Caractéristique DVI \_ OPM \_ 1 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b5d06-117">OPM\_DVI\_CHARACTERISTIC\_1\_0</span></span>            | <span data-ttu-id="b5d06-118">Version DVI 1,0.</span><span class="sxs-lookup"><span data-stu-id="b5d06-118">DVI version 1.0.</span></span>          |
| <span data-ttu-id="b5d06-119">\_Caractéristique DVI \_ OPM \_ 1 \_ 1 \_ ou \_ supérieure</span><span class="sxs-lookup"><span data-stu-id="b5d06-119">OPM\_DVI\_CHARACTERISTIC\_1\_1\_OR\_ABOVE</span></span> | <span data-ttu-id="b5d06-120">DVI version 1,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b5d06-120">DVI version 1.1 or later.</span></span> |



 

<span data-ttu-id="b5d06-121">Cette requête est prise en charge uniquement lorsque le type de connecteur physique est le type de \_ connecteur OPM \_ \_ DVI.</span><span class="sxs-lookup"><span data-stu-id="b5d06-121">This query is supported only when the physical connector type is OPM\_CONNECTOR\_TYPE\_DVI.</span></span> <span data-ttu-id="b5d06-122">Pour obtenir le type de connecteur, envoyez la requête de [**\_ \_ \_ type obtenir le connecteur OPM**](opm-get-connector-type.md) .</span><span class="sxs-lookup"><span data-stu-id="b5d06-122">To get the connector type, send the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) query.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5d06-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b5d06-123">Requirements</span></span>



| <span data-ttu-id="b5d06-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b5d06-124">Requirement</span></span> | <span data-ttu-id="b5d06-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b5d06-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b5d06-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5d06-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b5d06-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5d06-127">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b5d06-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b5d06-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b5d06-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b5d06-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b5d06-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="b5d06-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5d06-131"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5d06-131"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5d06-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b5d06-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5d06-133">**IOPMVideoOutput :: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="b5d06-133">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="b5d06-134">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="b5d06-134">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




