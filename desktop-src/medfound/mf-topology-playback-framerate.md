---
description: Spécifie la fréquence d’actualisation du moniteur.
ms.assetid: deeb780c-2dc2-4a9a-926a-23b9ae3bedd5
title: Attribut MF_TOPOLOGY_PLAYBACK_FRAMERATE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 620d7ff7dbc893065ebb378557f0731cd8826582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201975"
---
# <a name="mf_topology_playback_framerate-attribute"></a><span data-ttu-id="f3291-103">\_ \_ Attribut de fréquence de lecture de la topologie MF \_</span><span class="sxs-lookup"><span data-stu-id="f3291-103">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE attribute</span></span>

<span data-ttu-id="f3291-104">Spécifie la fréquence d’actualisation du moniteur.</span><span class="sxs-lookup"><span data-stu-id="f3291-104">Specifies the monitor refresh rate.</span></span>

## <a name="data-type"></a><span data-ttu-id="f3291-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f3291-105">Data type</span></span>

<span data-ttu-id="f3291-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f3291-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="f3291-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="f3291-107">Get/set</span></span>

<span data-ttu-id="f3291-108">Pour récupérer cet attribut, appelez [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="f3291-108">To get this attribute, call [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).</span></span>

<span data-ttu-id="f3291-109">Pour définir cet attribut, appelez [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span><span class="sxs-lookup"><span data-stu-id="f3291-109">To set this attribute, call [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).</span></span>

## <a name="applies-to"></a><span data-ttu-id="f3291-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="f3291-110">Applies to</span></span>

[<span data-ttu-id="f3291-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="f3291-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="f3291-112">Notes</span><span class="sxs-lookup"><span data-stu-id="f3291-112">Remarks</span></span>

<span data-ttu-id="f3291-113">Le chargeur de topologie utilise cet attribut pour optimiser le pipeline avant le démarrage de la lecture.</span><span class="sxs-lookup"><span data-stu-id="f3291-113">The topology loader uses this attribute to optimize the pipeline before playback starts.</span></span> <span data-ttu-id="f3291-114">Si vous définissez cet attribut, affectez également à l’attribut [ \_ \_ \_ \_ optimisations de la lecture statique de la topologie MF](mf-topology-static-playback-optimizations.md) la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="f3291-114">If you set this attribute, also set the [MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS](mf-topology-static-playback-optimizations.md) attribute to **TRUE**.</span></span>

<span data-ttu-id="f3291-115">La fréquence d’images est exprimée sous la forme d’un rapport.</span><span class="sxs-lookup"><span data-stu-id="f3291-115">The frame rate is expressed as a ratio.</span></span> <span data-ttu-id="f3291-116">Les 32 bits supérieurs de la valeur d’attribut contiennent le numérateur, et les 32 de bits inférieurs contiennent le dénominateur.</span><span class="sxs-lookup"><span data-stu-id="f3291-116">The upper 32 bits of the attribute value contain the numerator, and the lower 32 bits contain the denominator.</span></span>

<span data-ttu-id="f3291-117">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="f3291-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3291-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3291-118">Requirements</span></span>



| <span data-ttu-id="f3291-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3291-119">Requirement</span></span> | <span data-ttu-id="f3291-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3291-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f3291-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3291-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f3291-122">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3291-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f3291-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3291-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f3291-124">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3291-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="f3291-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3291-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3291-126"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3291-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3291-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3291-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3291-128">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f3291-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3291-129">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="f3291-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="f3291-130">Gestion de la qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="f3291-130">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




