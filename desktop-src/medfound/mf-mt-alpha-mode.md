---
description: Spécifie si le mode Alpha pour les types de vidéo multimédias couleur est prémultiplié ou droit.
ms.assetid: A263C3F7-357B-426D-B38C-533F9F6A1262
title: Attribut MF_MT_ALPHA_MODE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06b81da14bc0a9e089a5af4815e5bf97359a9cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034591"
---
# <a name="mf_mt_alpha_mode-attribute"></a><span data-ttu-id="1ef4c-103">MF \_ - \_ attribut de mode Alpha MT \_</span><span class="sxs-lookup"><span data-stu-id="1ef4c-103">MF\_MT\_ALPHA\_MODE attribute</span></span>

<span data-ttu-id="1ef4c-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="1ef4c-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1ef4c-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="1ef4c-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1ef4c-106">Spécifie si le mode Alpha pour les types de vidéo multimédias couleur est prémultiplié ou droit.</span><span class="sxs-lookup"><span data-stu-id="1ef4c-106">Specifies whether the alpha mode for color media video types is premultiplied or straight.</span></span>

## <a name="data-type"></a><span data-ttu-id="1ef4c-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="1ef4c-107">Data type</span></span>

<span data-ttu-id="1ef4c-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1ef4c-108">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="1ef4c-109">Notes</span><span class="sxs-lookup"><span data-stu-id="1ef4c-109">Remarks</span></span>

<span data-ttu-id="1ef4c-110">Cette valeur peut être convertie en valeur de [**\_ \_ mode Alpha dxgi**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) .</span><span class="sxs-lookup"><span data-stu-id="1ef4c-110">This value can be cast to a [**DXGI\_ALPHA\_MODE**](/windows/win32/api/dxgi1_2/ne-dxgi1_2-dxgi_alpha_mode) value.</span></span> <span data-ttu-id="1ef4c-111">Si cet attribut n’est pas présent, pour des raisons de compatibilité descendante, la valeur est **dxgi \_ \_ mode Alpha \_ directement** pour le format vidéo prenant en charge le canal alpha, tel que ARGB32 ou le **\_ mode Alpha dxgi \_ \_ ignore** pour le format vidéo sans canal alpha, tel que RGB32.</span><span class="sxs-lookup"><span data-stu-id="1ef4c-111">If this attribute isn’t present, for backward compatibility, the value is **DXGI\_ALPHA\_MODE\_STRAIGHT** for video format supporting alpha channel, such as ARGB32, or **DXGI\_ALPHA\_MODE\_IGNORE** for video format without alpha channel, such as RGB32.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ef4c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ef4c-112">Requirements</span></span>



| <span data-ttu-id="1ef4c-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ef4c-113">Requirement</span></span> | <span data-ttu-id="1ef4c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ef4c-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ef4c-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ef4c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1ef4c-116">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ef4c-116">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1ef4c-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ef4c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1ef4c-118">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1ef4c-118">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="1ef4c-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ef4c-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ef4c-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ef4c-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
