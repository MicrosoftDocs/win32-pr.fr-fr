---
description: Spécifie s’il faut charger des transformations de Microsoft Media Foundation matérielles (MFTs) dans la topologie.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: Attribut MF_TOPOLOGY_HARDWARE_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec7933e9a380bbf5e66f4030a214f3f4aa93abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531642"
---
# <a name="mf_topology_hardware_mode-attribute"></a><span data-ttu-id="c4b27-103">\_ \_ Attribut de mode matériel \_ de la topologie MF</span><span class="sxs-lookup"><span data-stu-id="c4b27-103">MF\_TOPOLOGY\_HARDWARE\_MODE attribute</span></span>

<span data-ttu-id="c4b27-104">Spécifie s’il faut charger des transformations de Microsoft Media Foundation matérielles (MFTs) dans la topologie.</span><span class="sxs-lookup"><span data-stu-id="c4b27-104">Specifies whether to load hardware-based Microsoft Media Foundation transforms (MFTs) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="c4b27-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="c4b27-105">Data type</span></span>

<span data-ttu-id="c4b27-106">**[**MFTOPOLOGY \_ \_Mode matériel**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c4b27-106">**[**MFTOPOLOGY\_HARDWARE\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c4b27-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="c4b27-107">Get/set</span></span>

<span data-ttu-id="c4b27-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c4b27-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c4b27-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c4b27-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c4b27-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="c4b27-110">Applies to</span></span>

[<span data-ttu-id="c4b27-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="c4b27-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="c4b27-112">Notes</span><span class="sxs-lookup"><span data-stu-id="c4b27-112">Remarks</span></span>

<span data-ttu-id="c4b27-113">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="c4b27-113">This attribute is optional.</span></span> <span data-ttu-id="c4b27-114">Définissez l’attribut avant de résoudre la topologie.</span><span class="sxs-lookup"><span data-stu-id="c4b27-114">Set the attribute before resolving the topology.</span></span>



| <span data-ttu-id="c4b27-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4b27-115">Value</span></span>                                  | <span data-ttu-id="c4b27-116">Description</span><span class="sxs-lookup"><span data-stu-id="c4b27-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4b27-117">**MFTOPOLOGY \_ HWMODE \_ use \_ Hardware**</span><span class="sxs-lookup"><span data-stu-id="c4b27-117">**MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**</span></span>  | <span data-ttu-id="c4b27-118">Le chargeur de topologie chargera les MFTs matériels, tels que les décodeurs matériels, lorsqu’ils sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="c4b27-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="c4b27-119">Le chargeur de topologie revient automatiquement au décodage logiciel si aucun décodeur matériel n’est trouvé, ou si un décodeur matériel ne parvient pas à se connecter pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="c4b27-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="c4b27-120">**MFTOPOLOGY \_ HWMODE \_ Software \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="c4b27-120">**MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**</span></span> | <span data-ttu-id="c4b27-121">Le chargeur de topologie chargera uniquement les MFTss logicielles, y compris les décodeurs logiciels.</span><span class="sxs-lookup"><span data-stu-id="c4b27-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="c4b27-122">La valeur par défaut est **MFTOPOLOGY \_ HWMODE \_ Software \_ uniquement**, pour la compatibilité avec les applications existantes.</span><span class="sxs-lookup"><span data-stu-id="c4b27-122">The default value is **MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**, for compatibility with existing applications.</span></span> <span data-ttu-id="c4b27-123">La valeur recommandée est **MFTOPOLOGY \_ HWMODE \_ use \_ Hardware**.</span><span class="sxs-lookup"><span data-stu-id="c4b27-123">The recommended value is **MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**.</span></span>

<span data-ttu-id="c4b27-124">Si le chargeur de topologie insère une table MFT matérielle dans la topologie, il définit l’attribut d' [ \_ attribut d' \_ \_ URL matériel \_ de l’énumération MFT](mft-enum-hardware-url-attribute.md) sur le nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="c4b27-124">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="c4b27-125">Pour vérifier si une table MFT matérielle est présente, énumérez les nœuds dans la topologie résolue et vérifiez si cet attribut est présent.</span><span class="sxs-lookup"><span data-stu-id="c4b27-125">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="c4b27-126">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c4b27-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4b27-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4b27-127">Requirements</span></span>



| <span data-ttu-id="c4b27-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4b27-128">Requirement</span></span> | <span data-ttu-id="c4b27-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4b27-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c4b27-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4b27-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c4b27-131">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4b27-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c4b27-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4b27-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c4b27-133">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4b27-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c4b27-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4b27-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4b27-135"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4b27-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4b27-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4b27-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4b27-137">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c4b27-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c4b27-138">Attributs de topologie</span><span class="sxs-lookup"><span data-stu-id="c4b27-138">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




