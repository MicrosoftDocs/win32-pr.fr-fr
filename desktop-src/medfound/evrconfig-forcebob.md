---
description: Force le convertisseur de vidéo amélioré (EVR) à utiliser la désentrelacement de Bob.
ms.assetid: 56f808b3-c2eb-46e4-84a1-c478a5db78e7
title: Attribut EVRConfig_ForceBob (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afeeb1e7fb57f956d378e71ac4452ea2e4f168be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545773"
---
# <a name="evrconfig_forcebob-attribute"></a><span data-ttu-id="904b1-103">\_Attribut EVRConfig ForceBob</span><span class="sxs-lookup"><span data-stu-id="904b1-103">EVRConfig\_ForceBob attribute</span></span>

<span data-ttu-id="904b1-104">Force le convertisseur de vidéo amélioré (EVR) à utiliser la désentrelacement de Bob.</span><span class="sxs-lookup"><span data-stu-id="904b1-104">Forces the Enhanced Video Renderer (EVR) to use bob deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="904b1-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="904b1-105">Data type</span></span>

<span data-ttu-id="904b1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="904b1-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="904b1-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="904b1-107">Get/set</span></span>

<span data-ttu-id="904b1-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="904b1-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="904b1-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="904b1-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="904b1-110">Notes</span><span class="sxs-lookup"><span data-stu-id="904b1-110">Remarks</span></span>

<span data-ttu-id="904b1-111">Cet attribut peut être défini sur le récepteur multimédia EVR.</span><span class="sxs-lookup"><span data-stu-id="904b1-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="904b1-112">Pour définir l’attribut, utilisez **QueryInterface** pour interroger le récepteur multimédia EVR pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="904b1-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="904b1-113">La définition de cet attribut a le même effet que la définition de l’indicateur **MFVideoMixPrefs \_ FORCEBOB** sur EVR.</span><span class="sxs-lookup"><span data-stu-id="904b1-113">Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_ForceBob** flag on the EVR.</span></span> <span data-ttu-id="904b1-114">Pour obtenir une description de cet indicateur, consultez [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .</span><span class="sxs-lookup"><span data-stu-id="904b1-114">See [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) for a description of this flag.</span></span>

<span data-ttu-id="904b1-115">La constante GUID de cet attribut est exportée à partir de strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="904b1-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="904b1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="904b1-116">Requirements</span></span>



| <span data-ttu-id="904b1-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="904b1-117">Requirement</span></span> | <span data-ttu-id="904b1-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="904b1-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="904b1-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="904b1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="904b1-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="904b1-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="904b1-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="904b1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="904b1-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="904b1-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="904b1-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="904b1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="904b1-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="904b1-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="904b1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="904b1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904b1-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="904b1-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="904b1-127">Attributs EVR</span><span class="sxs-lookup"><span data-stu-id="904b1-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="904b1-128">Gestion de la qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="904b1-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




