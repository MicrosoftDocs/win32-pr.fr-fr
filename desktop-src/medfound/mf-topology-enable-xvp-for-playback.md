---
description: Spécifie si le chargeur de topologie Active le processeur vidéo de transcodage (XVP). pour les conversions, activation de la conversion des couleurs à accélération matérielle.
title: Attribut MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK (Mfidl. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106542129"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a><span data-ttu-id="afdf0-104">\_La topologie MF \_ active \_ XVP \_ pour l' \_ attribut de lecture</span><span class="sxs-lookup"><span data-stu-id="afdf0-104">MF\_TOPOLOGY\_ENABLE\_XVP\_FOR\_PLAYBACK attribute</span></span>

<span data-ttu-id="afdf0-105">Spécifie si le chargeur de topologie Active le processeur vidéo de transcodage (XVP).</span><span class="sxs-lookup"><span data-stu-id="afdf0-105">Specifies whether the topology loader enables the Transcode Video Processor (XVP).</span></span> <span data-ttu-id="afdf0-106">pour les conversions, activation de la conversion des couleurs à accélération matérielle.</span><span class="sxs-lookup"><span data-stu-id="afdf0-106">for conversions, enabling hardware accelerated color conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="afdf0-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="afdf0-107">Data type</span></span>

<span data-ttu-id="afdf0-108">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="afdf0-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="afdf0-109">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="afdf0-109">Get/set</span></span>

<span data-ttu-id="afdf0-110">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="afdf0-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="afdf0-111">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="afdf0-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="afdf0-112">S’applique à</span><span class="sxs-lookup"><span data-stu-id="afdf0-112">Applies to</span></span>

[<span data-ttu-id="afdf0-113">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="afdf0-113">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="afdf0-114">Notes</span><span class="sxs-lookup"><span data-stu-id="afdf0-114">Remarks</span></span>

<span data-ttu-id="afdf0-115">Si cet attribut est défini, le chargeur de topologie extrait le processeur vidéo, si nécessaire, pendant la résolution de la topologie de non-transcodage.</span><span class="sxs-lookup"><span data-stu-id="afdf0-115">If this attribute is set, the topology loader will pull in the video processor, if necessary, during non-transcode topology resolution.</span></span> <span data-ttu-id="afdf0-116">Lorsque vous utilisez la topologie pour créer vos propres [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) , cet attribut indique au chargeur d’utiliser XVP pour les conversions au lieu du convertisseur de couleur hérité, ce qui permet de convertir les couleurs à accélération matérielle. le convertisseur de couleurs hérité est un logiciel uniquement.</span><span class="sxs-lookup"><span data-stu-id="afdf0-116">When you are using the topology to build your own [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) this attribute tells the loader to use XVP for conversions instead of the legacy color converter, thus enabling hardware accelerated color conversion; the legacy color converter is software-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="afdf0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afdf0-117">Requirements</span></span>



| <span data-ttu-id="afdf0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afdf0-118">Requirement</span></span> | <span data-ttu-id="afdf0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="afdf0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="afdf0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afdf0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="afdf0-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afdf0-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="afdf0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="afdf0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="afdf0-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="afdf0-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="afdf0-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="afdf0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="afdf0-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="afdf0-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afdf0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="afdf0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afdf0-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="afdf0-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="afdf0-128">Gestionnaire de périphériques Direct3D</span><span class="sxs-lookup"><span data-stu-id="afdf0-128">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="afdf0-129">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="afdf0-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




