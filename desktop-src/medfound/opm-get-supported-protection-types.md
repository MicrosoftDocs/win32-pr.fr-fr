---
description: Retourne la liste des mécanismes de protection pris en charge par le connecteur.
ms.assetid: dd4cdd3c-6bb5-4427-827d-f3e909e752e5
title: OPM_GET_SUPPORTED_PROTECTION_TYPES (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc79b33673e34d00914b84165d915baa0d8f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951481"
---
# <a name="opm_get_supported_protection_types"></a><span data-ttu-id="f2951-103">\_types de \_ \_ protection compatibles \_ avec OPM</span><span class="sxs-lookup"><span data-stu-id="f2951-103">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>

<span data-ttu-id="f2951-104">Retourne la liste des mécanismes de protection pris en charge par le connecteur.</span><span class="sxs-lookup"><span data-stu-id="f2951-104">Returns the list of protection mechanisms that are supported by the connector.</span></span>



| <span data-ttu-id="f2951-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2951-105">Requirement</span></span> | <span data-ttu-id="f2951-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2951-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="f2951-107">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="f2951-107">Request GUID</span></span> | <span data-ttu-id="f2951-108">\_types de \_ \_ protection compatibles \_ avec OPM</span><span class="sxs-lookup"><span data-stu-id="f2951-108">OPM\_GET\_SUPPORTED\_PROTECTION\_TYPES</span></span>                                      |
| <span data-ttu-id="f2951-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="f2951-109">Input data</span></span>   | <span data-ttu-id="f2951-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="f2951-110">None</span></span>                                                                        |
| <span data-ttu-id="f2951-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="f2951-111">Return data</span></span>  | <span data-ttu-id="f2951-112">Structure [**d' \_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)</span><span class="sxs-lookup"><span data-stu-id="f2951-112">An [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f2951-113">Notes</span><span class="sxs-lookup"><span data-stu-id="f2951-113">Remarks</span></span>

<span data-ttu-id="f2951-114">Les mécanismes de protection sont retournés dans le membre **ulInformation** de la structure d' [**\_ \_ informations standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="f2951-114">The protection mechanisms are returned in the **ulInformation** member of the [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span> <span data-ttu-id="f2951-115">La valeur est **une opération or** au niveau du bit des indicateurs de type de [protection OPM](opm-protection-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="f2951-115">The value is a bitwise **OR** of [OPM Protection Type Flags](opm-protection-type-flags.md).</span></span>

<span data-ttu-id="f2951-116">Cette requête est équivalente à la \_ requête DXVA COPPQueryProtectionType utilisée dans le protocole Copp (Certified Output Protection Protocol).</span><span class="sxs-lookup"><span data-stu-id="f2951-116">This query is equivalent to the DXVA\_COPPQueryProtectionType query used in Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2951-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2951-117">Requirements</span></span>



| <span data-ttu-id="f2951-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2951-118">Requirement</span></span> | <span data-ttu-id="f2951-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2951-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f2951-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2951-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f2951-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2951-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f2951-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2951-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f2951-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2951-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f2951-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2951-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2951-125"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2951-125"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2951-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2951-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2951-127">**IOPMVideoOutput :: COPPCompatibleGetInformation**</span><span class="sxs-lookup"><span data-stu-id="f2951-127">**IOPMVideoOutput::COPPCompatibleGetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation)
</dt> <dt>

[<span data-ttu-id="f2951-128">**IOPMVideoOutput :: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="f2951-128">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="f2951-129">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="f2951-129">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




