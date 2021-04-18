---
description: Valeur qui indique le type de capteur fourni par une source de frame, telle que la couleur, l’infrarouge ou la profondeur.
ms.assetid: F327B9E9-C01C-4F5B-9A26-6404ECD7F27F
title: Attribut MF_MT_FRAMESOURCE_TYPES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4475d66aea245ac9295a7996da2c37cabdb9627
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106522675"
---
# <a name="mf_mt_framesource_types-attribute"></a><span data-ttu-id="03921-103">\_Attribut des \_ types FRAMESOURCE MF MT \_</span><span class="sxs-lookup"><span data-stu-id="03921-103">MF\_MT\_FRAMESOURCE\_TYPES attribute</span></span>

<span data-ttu-id="03921-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="03921-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="03921-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="03921-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="03921-106">Valeur qui indique le type de capteur fourni par une source de frame, telle que la couleur, l’infrarouge ou la profondeur.</span><span class="sxs-lookup"><span data-stu-id="03921-106">A value that indicates the type of sensor provided by a frame source, such as color, infrared, or depth.</span></span>

## <a name="data-type"></a><span data-ttu-id="03921-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="03921-107">Data type</span></span>

<span data-ttu-id="03921-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="03921-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="03921-109">Notes</span><span class="sxs-lookup"><span data-stu-id="03921-109">Remarks</span></span>

<span data-ttu-id="03921-110">Cette valeur doit être un membre de l’énumération [**\_ MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="03921-110">This value should be a member of the [**\_MFFrameSourceTypes**](/previous-versions/windows/desktop/legacy/mt846679(v=vs.85)) enumeration.</span></span> <span data-ttu-id="03921-111">Pour la compatibilité descendante, lorsque cet attribut n’est pas défini sur un type de média, il est supposé être **\_ MFFrameSourceTyes :: Color**.</span><span class="sxs-lookup"><span data-stu-id="03921-111">For backward compatibility, when this attribute is not defined on a media type, it's assumed to be **\_MFFrameSourceTyes::Color**.</span></span>

## <a name="requirements"></a><span data-ttu-id="03921-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03921-112">Requirements</span></span>



| <span data-ttu-id="03921-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03921-113">Requirement</span></span> | <span data-ttu-id="03921-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="03921-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03921-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03921-115">Minimum supported client</span></span><br/> | <span data-ttu-id="03921-116">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03921-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="03921-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="03921-117">Minimum supported server</span></span><br/> | <span data-ttu-id="03921-118">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="03921-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="03921-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="03921-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="03921-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="03921-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
