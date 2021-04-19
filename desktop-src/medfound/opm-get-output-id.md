---
description: Retourne l’identificateur unique de l’analyseur associé à cette sortie vidéo.
ms.assetid: d34d68ff-c513-483e-8619-4a9baa2a40ba
title: OPM_GET_OUTPUT_ID (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6146c07be3467e513b33f636bde78e699f3e0d6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534399"
---
# <a name="opm_get_output_id"></a><span data-ttu-id="d9a37-103">ID de sortie de l' \_ extraction OPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="d9a37-103">OPM\_GET\_OUTPUT\_ID</span></span>

<span data-ttu-id="d9a37-104">Retourne l’identificateur unique de l’analyseur associé à cette sortie vidéo.</span><span class="sxs-lookup"><span data-stu-id="d9a37-104">Returns the unique identifier of the monitor associated with this video output.</span></span>



| <span data-ttu-id="d9a37-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9a37-105">Requirement</span></span> | <span data-ttu-id="d9a37-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9a37-106">Value</span></span> |
|--------------|------------------------------------------------------------------|
| <span data-ttu-id="d9a37-107">GUID de la demande</span><span class="sxs-lookup"><span data-stu-id="d9a37-107">Request GUID</span></span> | <span data-ttu-id="d9a37-108">ID de sortie de l' \_ extraction OPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="d9a37-108">OPM\_GET\_OUTPUT\_ID</span></span>                                             |
| <span data-ttu-id="d9a37-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="d9a37-109">Input data</span></span>   | <span data-ttu-id="d9a37-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="d9a37-110">None</span></span>                                                             |
| <span data-ttu-id="d9a37-111">Retourner les données</span><span class="sxs-lookup"><span data-stu-id="d9a37-111">Return data</span></span>  | <span data-ttu-id="d9a37-112">Structure de données de l' [**\_ ID de sortie \_ \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)</span><span class="sxs-lookup"><span data-stu-id="d9a37-112">An [**OPM\_OUTPUT\_ID\_DATA**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d9a37-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d9a37-113">Remarks</span></span>

<span data-ttu-id="d9a37-114">Le pilote vidéo attribue un identificateur unique à chaque analyse.</span><span class="sxs-lookup"><span data-stu-id="d9a37-114">The video driver assigns a unique identifier to each monitor.</span></span> <span data-ttu-id="d9a37-115">Cette requête retourne l’identificateur pour l’analyse associée au pointeur [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) actuel.</span><span class="sxs-lookup"><span data-stu-id="d9a37-115">This query returns the identifier for the monitor that is associated with the current [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9a37-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9a37-116">Requirements</span></span>



| <span data-ttu-id="d9a37-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9a37-117">Requirement</span></span> | <span data-ttu-id="d9a37-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9a37-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d9a37-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9a37-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d9a37-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9a37-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d9a37-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9a37-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d9a37-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9a37-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d9a37-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d9a37-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9a37-124"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9a37-124"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9a37-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9a37-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a37-126">**IOPMVideoOutput :: GetInformation**</span><span class="sxs-lookup"><span data-stu-id="d9a37-126">**IOPMVideoOutput::GetInformation**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation)
</dt> <dt>

[<span data-ttu-id="d9a37-127">Demandes d’État OPM</span><span class="sxs-lookup"><span data-stu-id="d9a37-127">OPM Status Requests</span></span>](opm-status-requests.md)
</dt> </dl>

 

 




