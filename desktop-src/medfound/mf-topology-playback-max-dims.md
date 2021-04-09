---
description: Spécifie la taille de la fenêtre de destination pour la lecture vidéo.
ms.assetid: 46af4c11-042c-4580-ba9d-3aee6172de56
title: Attribut MF_TOPOLOGY_PLAYBACK_MAX_DIMS (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1fc6a57c5e031bc6f35f36e688bd44986f541b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201974"
---
# <a name="mf_topology_playback_max_dims-attribute"></a><span data-ttu-id="738f2-103">\_ \_ \_ Attribut Dim Max playback de lecture de la topologie MF \_</span><span class="sxs-lookup"><span data-stu-id="738f2-103">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS attribute</span></span>

<span data-ttu-id="738f2-104">Spécifie la taille de la fenêtre de destination pour la lecture vidéo.</span><span class="sxs-lookup"><span data-stu-id="738f2-104">Specifies the size of the destination window for video playback.</span></span>

## <a name="data-type"></a><span data-ttu-id="738f2-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="738f2-105">Data type</span></span>

<span data-ttu-id="738f2-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="738f2-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="738f2-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="738f2-107">Get/set</span></span>

<span data-ttu-id="738f2-108">Pour récupérer cet attribut, appelez [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span><span class="sxs-lookup"><span data-stu-id="738f2-108">To get this attribute, call [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize).</span></span>

<span data-ttu-id="738f2-109">Pour définir cet attribut, appelez [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).</span><span class="sxs-lookup"><span data-stu-id="738f2-109">To set this attribute, call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize).</span></span>

## <a name="applies-to"></a><span data-ttu-id="738f2-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="738f2-110">Applies to</span></span>

[<span data-ttu-id="738f2-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="738f2-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="738f2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="738f2-112">Remarks</span></span>

<span data-ttu-id="738f2-113">Le chargeur de topologie utilise cet attribut pour optimiser le pipeline avant le démarrage de la lecture.</span><span class="sxs-lookup"><span data-stu-id="738f2-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="738f2-114">Si vous définissez cet attribut, affectez également à l’attribut [ \_ \_ \_ \_ optimisations de la lecture statique de la topologie MF](mf-topology-static-playback-optimizations.md) la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="738f2-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="738f2-115">Les 32 bits supérieurs de la valeur de l’attribut contiennent la largeur et les 32 bits inférieurs contiennent la hauteur, en pixels.</span><span class="sxs-lookup"><span data-stu-id="738f2-115">The upper 32 bits of the attribute value contain the width and the lower 32 bits contain the height, both in pixels.</span></span>

<span data-ttu-id="738f2-116">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="738f2-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="738f2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="738f2-117">Requirements</span></span>



| <span data-ttu-id="738f2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="738f2-118">Requirement</span></span> | <span data-ttu-id="738f2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="738f2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="738f2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="738f2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="738f2-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="738f2-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="738f2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="738f2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="738f2-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="738f2-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="738f2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="738f2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="738f2-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="738f2-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="738f2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="738f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="738f2-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="738f2-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="738f2-128">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="738f2-128">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="738f2-129">Gestion de la qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="738f2-129">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




