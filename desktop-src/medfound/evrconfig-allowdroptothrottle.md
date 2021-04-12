---
description: Autorise le convertisseur vidéo amélioré (EVR) à limiter sa sortie pour qu’il corresponde à la bande passante GPU.
ms.assetid: d591af2e-d47d-4220-a4f6-968f2ac45284
title: Attribut EVRConfig_AllowDropToThrottle (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97cbab6fae6644b3c0187d09edb59ab2538012e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033800"
---
# <a name="evrconfig_allowdroptothrottle-attribute"></a><span data-ttu-id="1aaa3-103">\_Attribut EVRConfig AllowDropToThrottle</span><span class="sxs-lookup"><span data-stu-id="1aaa3-103">EVRConfig\_AllowDropToThrottle attribute</span></span>

<span data-ttu-id="1aaa3-104">Autorise le convertisseur vidéo amélioré (EVR) à limiter sa sortie pour qu’il corresponde à la bande passante GPU.</span><span class="sxs-lookup"><span data-stu-id="1aaa3-104">Allows the Enhanced Video Renderer (EVR) to limit its output to match GPU bandwidth.</span></span>

## <a name="data-type"></a><span data-ttu-id="1aaa3-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1aaa3-105">Data type</span></span>

<span data-ttu-id="1aaa3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="1aaa3-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="1aaa3-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="1aaa3-107">Get/set</span></span>

<span data-ttu-id="1aaa3-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="1aaa3-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="1aaa3-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="1aaa3-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="1aaa3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1aaa3-110">Remarks</span></span>

<span data-ttu-id="1aaa3-111">Cet attribut peut être défini sur le récepteur multimédia EVR.</span><span class="sxs-lookup"><span data-stu-id="1aaa3-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="1aaa3-112">Pour définir l’attribut, utilisez **QueryInterface** pour interroger le récepteur multimédia EVR pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="1aaa3-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="1aaa3-113">La définition de cet attribut a le même effet que la définition de l’indicateur **MFVideoRenderPrefs \_ ALLOWOUTPUTTHROTTLING** sur EVR.</span><span class="sxs-lookup"><span data-stu-id="1aaa3-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_AllowOutputThrottling** flag on the EVR.</span></span> <span data-ttu-id="1aaa3-114">Pour obtenir une description de cet indicateur, consultez [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .</span><span class="sxs-lookup"><span data-stu-id="1aaa3-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="1aaa3-115">La constante GUID de cet attribut est exportée à partir de strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="1aaa3-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1aaa3-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1aaa3-116">Requirements</span></span>



| <span data-ttu-id="1aaa3-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1aaa3-117">Requirement</span></span> | <span data-ttu-id="1aaa3-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="1aaa3-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1aaa3-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1aaa3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1aaa3-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1aaa3-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1aaa3-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1aaa3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1aaa3-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1aaa3-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1aaa3-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="1aaa3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1aaa3-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aaa3-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aaa3-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1aaa3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aaa3-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1aaa3-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1aaa3-127">Attributs EVR</span><span class="sxs-lookup"><span data-stu-id="1aaa3-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="1aaa3-128">Gestion de la qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="1aaa3-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




