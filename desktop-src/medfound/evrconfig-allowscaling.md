---
description: Alllows le convertisseur vidéo amélioré (EVR) pour mélanger la vidéo dans un rectangle plus petit que le rectangle de sortie, puis mettre à l’échelle le résultat.
ms.assetid: 7e3b8fe1-959b-4391-a715-5d5a7a7dda39
title: Attribut EVRConfig_AllowScaling (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1d0662c7145d9f5c5484df81c2483305402850
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861797"
---
# <a name="evrconfig_allowscaling-attribute"></a><span data-ttu-id="7f047-103">\_Attribut EVRConfig AllowScaling</span><span class="sxs-lookup"><span data-stu-id="7f047-103">EVRConfig\_AllowScaling attribute</span></span>

<span data-ttu-id="7f047-104">Alllows le convertisseur vidéo amélioré (EVR) pour mélanger la vidéo dans un rectangle plus petit que le rectangle de sortie, puis mettre à l’échelle le résultat.</span><span class="sxs-lookup"><span data-stu-id="7f047-104">Alllows the Enhanced Video Renderer (EVR) to mix the video within a rectangle that is smaller than the output rectangle, and then scale the result.</span></span>

## <a name="data-type"></a><span data-ttu-id="7f047-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="7f047-105">Data type</span></span>

<span data-ttu-id="7f047-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7f047-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7f047-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="7f047-107">Get/set</span></span>

<span data-ttu-id="7f047-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7f047-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7f047-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7f047-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7f047-110">Notes</span><span class="sxs-lookup"><span data-stu-id="7f047-110">Remarks</span></span>

<span data-ttu-id="7f047-111">Cet attribut peut être défini sur le récepteur multimédia EVR.</span><span class="sxs-lookup"><span data-stu-id="7f047-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="7f047-112">Pour définir l’attribut, utilisez **QueryInterface** pour interroger le récepteur multimédia EVR pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="7f047-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="7f047-113">La définition de cet attribut a le même effet que la définition de l’indicateur **MFVideoRenderPrefs \_ ALLOWSCALING** sur EVR.</span><span class="sxs-lookup"><span data-stu-id="7f047-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_AllowScaling** flag on the EVR.</span></span> <span data-ttu-id="7f047-114">Pour obtenir une description de cet indicateur, consultez [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .</span><span class="sxs-lookup"><span data-stu-id="7f047-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="7f047-115">La constante GUID de cet attribut est exportée à partir de strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="7f047-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f047-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7f047-116">Requirements</span></span>



| <span data-ttu-id="7f047-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7f047-117">Requirement</span></span> | <span data-ttu-id="7f047-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="7f047-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7f047-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f047-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f047-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f047-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7f047-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7f047-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f047-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7f047-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7f047-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="7f047-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f047-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f047-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f047-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f047-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f047-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7f047-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f047-127">Attributs EVR</span><span class="sxs-lookup"><span data-stu-id="7f047-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="7f047-128">Gestion de la qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="7f047-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




