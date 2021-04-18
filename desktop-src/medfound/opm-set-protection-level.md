---
description: Définit le niveau de protection d’un mécanisme de protection de sortie.
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: OPM_SET_PROTECTION_LEVEL (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a80fb674c9347dafc3bcf1a62dc4bc909f0471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522673"
---
# <a name="opm_set_protection_level"></a><span data-ttu-id="d1d87-103">niveau de protection de l' \_ ensemble OPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="d1d87-103">OPM\_SET\_PROTECTION\_LEVEL</span></span>

<span data-ttu-id="d1d87-104">Définit le niveau de protection d’un mécanisme de protection de sortie.</span><span class="sxs-lookup"><span data-stu-id="d1d87-104">Sets the protection level for an output protection mechanism.</span></span>



| <span data-ttu-id="d1d87-105">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1d87-105">Requirement</span></span> | <span data-ttu-id="d1d87-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1d87-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d87-107">GUID de la commande</span><span class="sxs-lookup"><span data-stu-id="d1d87-107">Command GUID</span></span> | <span data-ttu-id="d1d87-108">niveau de protection de l' \_ ensemble OPM \_ \_</span><span class="sxs-lookup"><span data-stu-id="d1d87-108">OPM\_SET\_PROTECTION\_LEVEL</span></span>                                                                         |
| <span data-ttu-id="d1d87-109">Données d’entrée</span><span class="sxs-lookup"><span data-stu-id="d1d87-109">Input data</span></span>   | <span data-ttu-id="d1d87-110">Structure [**des \_ \_ paramètres de \_ niveau \_ de protection de l’ensemble OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)</span><span class="sxs-lookup"><span data-stu-id="d1d87-110">An [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d1d87-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d1d87-111">Remarks</span></span>

<span data-ttu-id="d1d87-112">Certains connecteurs peuvent prendre en charge plusieurs mécanismes de protection.</span><span class="sxs-lookup"><span data-stu-id="d1d87-112">Some connectors can support multiple protection mechanisms.</span></span> <span data-ttu-id="d1d87-113">Avec ce type de connecteur, vous pouvez appliquer plusieurs mécanismes de protection au même connecteur, avec des paramètres différents pour chacun.</span><span class="sxs-lookup"><span data-stu-id="d1d87-113">With that type of connector, you can apply several protection mechanisms to the same connector, with different settings for each.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1d87-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1d87-114">Requirements</span></span>



| <span data-ttu-id="d1d87-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1d87-115">Requirement</span></span> | <span data-ttu-id="d1d87-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1d87-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d87-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1d87-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d87-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1d87-118">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d1d87-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1d87-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d87-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1d87-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d1d87-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="d1d87-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1d87-122"><dt>Opmapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1d87-122"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1d87-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d1d87-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1d87-124">**IOPMVideoOutput :: configure**</span><span class="sxs-lookup"><span data-stu-id="d1d87-124">**IOPMVideoOutput::Configure**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[<span data-ttu-id="d1d87-125">Commandes OPM</span><span class="sxs-lookup"><span data-stu-id="d1d87-125">OPM Commands</span></span>](opm-commands.md)
</dt> </dl>

 

 




