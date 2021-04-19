---
description: Spécifie si le chargeur de topologie Active l’accélération vidéo Microsoft DirectX (DXVA) dans la topologie.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: Attribut MF_TOPOLOGY_DXVA_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad75b37a2ca2e971077b05d1bbeb92748530614
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514814"
---
# <a name="mf_topology_dxva_mode-attribute"></a><span data-ttu-id="d01e2-103">\_ \_ Attribut de mode DXVA de topologie MF \_</span><span class="sxs-lookup"><span data-stu-id="d01e2-103">MF\_TOPOLOGY\_DXVA\_MODE attribute</span></span>

<span data-ttu-id="d01e2-104">Spécifie si le chargeur de topologie Active l’accélération vidéo Microsoft DirectX (DXVA) dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="d01e2-104">Specifies whether the topology loader enables Microsoft DirectX Video Acceleration (DXVA) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="d01e2-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d01e2-105">Data type</span></span>

<span data-ttu-id="d01e2-106">**[**MFTOPOLOGY \_ \_Mode DXVA**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d01e2-106">**[**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="d01e2-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="d01e2-107">Get/set</span></span>

<span data-ttu-id="d01e2-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="d01e2-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d01e2-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="d01e2-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d01e2-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="d01e2-110">Applies to</span></span>

[<span data-ttu-id="d01e2-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="d01e2-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="d01e2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d01e2-112">Remarks</span></span>

<span data-ttu-id="d01e2-113">La valeur de cet attribut est une constante d’énumération du [**\_ \_ mode DXVA MFTOPOLOGY**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) .</span><span class="sxs-lookup"><span data-stu-id="d01e2-113">The value of this attribute is an [**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) enumeration constant.</span></span> <span data-ttu-id="d01e2-114">La valeur par défaut est **MFTOPOLOGY \_ DXVA \_ par défaut**.</span><span class="sxs-lookup"><span data-stu-id="d01e2-114">The default value is **MFTOPOLOGY\_DXVA\_DEFAULT**.</span></span>

<span data-ttu-id="d01e2-115">Cet attribut contrôle les MFTs qui reçoivent un pointeur vers le gestionnaire de périphériques Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d01e2-115">This attribute controls which MFTs receive a pointer to the Direct3D device manager.</span></span> <span data-ttu-id="d01e2-116">Pour activer l’accélération vidéo complète, définissez la valeur sur **MFTOPOLOGY \_ DXVA \_ Full**.</span><span class="sxs-lookup"><span data-stu-id="d01e2-116">To enable full video acceleration, set the value to **MFTOPOLOGY\_DXVA\_FULL**.</span></span> <span data-ttu-id="d01e2-117">La valeur **MFTOPOLOGY \_ DXVA \_ default** est définie pour la compatibilité descendante. elle correspond au comportement de toutes les versions antérieures de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="d01e2-117">The value **MFTOPOLOGY\_DXVA\_DEFAULT** is defined for backward compatibility; it matches the behavior of all earlier versions of Microsoft Media Foundation.</span></span>

<span data-ttu-id="d01e2-118">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d01e2-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d01e2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d01e2-119">Requirements</span></span>



| <span data-ttu-id="d01e2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d01e2-120">Requirement</span></span> | <span data-ttu-id="d01e2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d01e2-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d01e2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d01e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d01e2-123">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d01e2-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d01e2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d01e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d01e2-125">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d01e2-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d01e2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d01e2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d01e2-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d01e2-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d01e2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d01e2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d01e2-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d01e2-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d01e2-130">Gestionnaire de périphériques Direct3D</span><span class="sxs-lookup"><span data-stu-id="d01e2-130">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="d01e2-131">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="d01e2-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




