---
description: Retourne le type de connecteur physique de la sortie vidéo.
ms.assetid: c5862758-0125-4dbe-af72-5ed4a85bd702
title: OPM_GET_CONNECTOR_TYPE (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a95ca88b079aa93b4c2665fe7aa954eb58cfc1a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201865"
---
# <a name="opm_get_connector_type"></a><span data-ttu-id="0ff81-103">\_type de \_ connecteur d’extraction OPM \_</span><span class="sxs-lookup"><span data-stu-id="0ff81-103">OPM\_GET\_CONNECTOR\_TYPE</span></span>

<span data-ttu-id="0ff81-104">Retourne le type de connecteur physique de la sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="0ff81-104">Returns the physical connector type of the video output.</span></span>



| <span data-ttu-id="0ff81-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ff81-105">Requirement</span></span> | <span data-ttu-id="0ff81-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ff81-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="0ff81-107">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="0ff81-107">Request GUID</span></span> | <span data-ttu-id="0ff81-108">\_type de \_ connecteur d’extraction OPM \_</span><span class="sxs-lookup"><span data-stu-id="0ff81-108">OPM\_GET\_CONNECTOR\_TYPE</span></span>                                                   |
| <span data-ttu-id="0ff81-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="0ff81-109">Input data</span></span>   | <span data-ttu-id="0ff81-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="0ff81-110">None</span></span>                                                                        |
| <span data-ttu-id="0ff81-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="0ff81-111">Return data</span></span>  | <span data-ttu-id="0ff81-112">Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="0ff81-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0ff81-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0ff81-113">Remarks</span></span>

<span data-ttu-id="0ff81-114">Le type de connecteur est retourné dans le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="0ff81-114">The connector type is returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="0ff81-115">La valeur de **ulInformation** est égale à l’un des types de connecteur listés dans les [**indicateurs de type de connecteur OPM**](opm-connector-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0ff81-115">The value of **ulInformation** is equal to one of the connector types listed in [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="0ff81-116">En mode d’émulation COPP, le type de connecteur peut être combiné avec l’indicateur **\_ interne de \_ \_ \_ type \_ de connecteur compatible de OPM** .</span><span class="sxs-lookup"><span data-stu-id="0ff81-116">In COPP emulation mode, the connector type might be combined with the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="0ff81-117">Utilisez une opération de bits **and** pour extraire le type de connecteur :</span><span class="sxs-lookup"><span data-stu-id="0ff81-117">Use a bitwise **AND** to extract the connector type:</span></span>

`ulInformation & ~OPM_COPP_COMPATIBLE_CONNECTOR_TYPE_INTERNAL`

<span data-ttu-id="0ff81-118">Les applications doivent ignorer l’indicateur **\_ interne du \_ \_ \_ type \_ de connecteur compatible avec OPM Copp** .</span><span class="sxs-lookup"><span data-stu-id="0ff81-118">Applications should ignore the **OPM\_COPP\_COMPATIBLE\_CONNECTOR\_TYPE\_INTERNAL** flag.</span></span> <span data-ttu-id="0ff81-119">Pour plus d’informations, consultez la section Notes des [**indicateurs de type de connecteur OPM**](opm-connector-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0ff81-119">For more information, see the Remarks section of [**OPM Connector Type Flags**](opm-connector-type-flags.md).</span></span>

<span data-ttu-id="0ff81-120">Cette requête est équivalente à la \_ requête DXVA COPPQueryConnectorType utilisée dans le protocole Copp (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="0ff81-120">This query is equivalent to the DXVA\_COPPQueryConnectorType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff81-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ff81-121">Requirements</span></span>



| <span data-ttu-id="0ff81-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ff81-122">Requirement</span></span> | <span data-ttu-id="0ff81-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ff81-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff81-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ff81-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0ff81-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ff81-125">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0ff81-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0ff81-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0ff81-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0ff81-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0ff81-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ff81-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ff81-129"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ff81-129"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ff81-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ff81-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff81-131">**IOPMVideoOutput :: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="0ff81-131">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="0ff81-132">**IOPMVideoOutput :: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="0ff81-132">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="0ff81-133">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="0ff81-133">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




