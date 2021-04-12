---
description: Permet au convertisseur vidéo amélioré (EVR) d’améliorer les performances à l’aide de l’entrelacement Bob.
ms.assetid: e145e862-b987-4962-a94b-f8370bbcd5ac
title: Attribut EVRConfig_AllowDropToBob (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3940edd0945999f7300060d963806e3572a5d0fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393267"
---
# <a name="evrconfig_allowdroptobob-attribute"></a><span data-ttu-id="c755d-103">\_Attribut EVRConfig AllowDropToBob</span><span class="sxs-lookup"><span data-stu-id="c755d-103">EVRConfig\_AllowDropToBob attribute</span></span>

<span data-ttu-id="c755d-104">Permet au convertisseur vidéo amélioré (EVR) d’améliorer les performances à l’aide de l’entrelacement Bob.</span><span class="sxs-lookup"><span data-stu-id="c755d-104">Allows the Enhanced Video Renderer (EVR) to improve performance by using bob deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="c755d-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="c755d-105">Data type</span></span>

<span data-ttu-id="c755d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c755d-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c755d-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="c755d-107">Get/set</span></span>

<span data-ttu-id="c755d-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c755d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c755d-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c755d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="c755d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="c755d-110">Remarks</span></span>

<span data-ttu-id="c755d-111">Cet attribut peut être défini sur le récepteur EVRmedia.</span><span class="sxs-lookup"><span data-stu-id="c755d-111">This attribute can be set on the EVRmedia sink.</span></span> <span data-ttu-id="c755d-112">Pour définir l’attribut, **QueryInterface** pour interroger le récepteur multimédia EVR pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="c755d-112">To set the attribute, **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="c755d-113">La définition de cet attribut a le même effet que la définition de l’indicateur **MFVideoMixPrefs \_ ALLOWDROPTOBOB** sur EVR.</span><span class="sxs-lookup"><span data-stu-id="c755d-113">Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_AllowDropToBob** flag on the EVR.</span></span> <span data-ttu-id="c755d-114">Pour obtenir une description de cet indicateur, consultez [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .</span><span class="sxs-lookup"><span data-stu-id="c755d-114">See [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) for a description of this flag.</span></span>

<span data-ttu-id="c755d-115">La constante GUID de cet attribut est exportée à partir de strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="c755d-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c755d-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c755d-116">Requirements</span></span>



| <span data-ttu-id="c755d-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c755d-117">Requirement</span></span> | <span data-ttu-id="c755d-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="c755d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c755d-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c755d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c755d-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c755d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c755d-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c755d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c755d-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c755d-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c755d-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c755d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c755d-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="c755d-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c755d-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c755d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c755d-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c755d-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c755d-127">Attributs EVR</span><span class="sxs-lookup"><span data-stu-id="c755d-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="c755d-128">Gestion de la qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="c755d-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




