---
description: Force le convertisseur de vidéo amélioré (EVR) à appeler par lots la méthode IDirect3D9Device ::P renouvely.
ms.assetid: d7523000-baa0-4011-97e1-d1ffe7263d01
title: Attribut EVRConfig_ForceBatching (UUID. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c6dff5d7a5e90377c8749519033b6a66ef7663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524519"
---
# <a name="evrconfig_forcebatching-attribute"></a><span data-ttu-id="43c4c-103">\_Attribut EVRConfig ForceBatching</span><span class="sxs-lookup"><span data-stu-id="43c4c-103">EVRConfig\_ForceBatching attribute</span></span>

<span data-ttu-id="43c4c-104">Force le convertisseur de vidéo amélioré (EVR) à appeler par lots la méthode [**IDirect3D9Device ::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) renouvely.</span><span class="sxs-lookup"><span data-stu-id="43c4c-104">Forces the Enhanced Video Renderer (EVR) to batch calls to the [**IDirect3D9Device::Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method.</span></span>

## <a name="data-type"></a><span data-ttu-id="43c4c-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="43c4c-105">Data type</span></span>

<span data-ttu-id="43c4c-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="43c4c-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="43c4c-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="43c4c-107">Get/set</span></span>

<span data-ttu-id="43c4c-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="43c4c-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="43c4c-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="43c4c-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="43c4c-110">Notes</span><span class="sxs-lookup"><span data-stu-id="43c4c-110">Remarks</span></span>

<span data-ttu-id="43c4c-111">Cet attribut peut être défini sur le récepteur multimédia EVR.</span><span class="sxs-lookup"><span data-stu-id="43c4c-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="43c4c-112">Pour définir l’attribut, utilisez **QueryInterface** pour interroger le récepteur multimédia EVR pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="43c4c-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="43c4c-113">La définition de cet attribut a le même effet que la définition de l’indicateur **MFVideoRenderPrefs \_ FORCEBATCHING** sur EVR.</span><span class="sxs-lookup"><span data-stu-id="43c4c-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_ForceBatching** flag on the EVR.</span></span> <span data-ttu-id="43c4c-114">Pour obtenir une description de cet indicateur, consultez [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .</span><span class="sxs-lookup"><span data-stu-id="43c4c-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="43c4c-115">La constante GUID de cet attribut est exportée à partir de strmiids. lib.</span><span class="sxs-lookup"><span data-stu-id="43c4c-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="43c4c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43c4c-116">Requirements</span></span>



| <span data-ttu-id="43c4c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43c4c-117">Requirement</span></span> | <span data-ttu-id="43c4c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="43c4c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43c4c-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43c4c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="43c4c-120">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43c4c-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="43c4c-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43c4c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="43c4c-122">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43c4c-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="43c4c-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="43c4c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="43c4c-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="43c4c-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43c4c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43c4c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c4c-126">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="43c4c-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="43c4c-127">Attributs EVR</span><span class="sxs-lookup"><span data-stu-id="43c4c-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="43c4c-128">Gestion de la qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="43c4c-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 
