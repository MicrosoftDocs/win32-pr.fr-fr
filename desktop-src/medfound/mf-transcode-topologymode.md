---
description: Spécifie pour une topologie de transcodage si le chargeur de topologie charge des transformations matérielles.
ms.assetid: 33db8621-114a-4531-908f-f30034441973
title: Attribut MF_TRANSCODE_TOPOLOGYMODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f700397914faf7fee35e7f82027d8f8771e8b099
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863170"
---
# <a name="mf_transcode_topologymode-attribute"></a><span data-ttu-id="0c453-103">\_Attribut TOPOLOGYMODE de transcodage MF \_</span><span class="sxs-lookup"><span data-stu-id="0c453-103">MF\_TRANSCODE\_TOPOLOGYMODE attribute</span></span>

<span data-ttu-id="0c453-104">Spécifie pour une topologie de transcodage si le chargeur de topologie charge des transformations matérielles.</span><span class="sxs-lookup"><span data-stu-id="0c453-104">Specifies for a transcode topology whether the topology loader will load hardware-based transforms.</span></span>

<span data-ttu-id="0c453-105">Le mode de topologie spécifie si les transformations matérielles (telles que les codecs matériels) peuvent être utilisées dans la topologie de transcodage.</span><span class="sxs-lookup"><span data-stu-id="0c453-105">The topology mode specifies whether hardware transforms (such as hardware codecs) may be used in the transcode topology.</span></span> <span data-ttu-id="0c453-106">L’application peut stocker cet attribut dans un profil de transcodage en appelant [**IMFTranscodeProfile :: SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span><span class="sxs-lookup"><span data-stu-id="0c453-106">The application can store this attribute in a transcode profile by calling [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span>

## <a name="data-type"></a><span data-ttu-id="0c453-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="0c453-107">Data type</span></span>

<span data-ttu-id="0c453-108">**[**MF \_ Transcodage \_ TOPOLOGYMODE \_ indicateurs**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0c453-108">**[**MF\_TRANSCODE\_TOPOLOGYMODE\_FLAGS**](/windows/desktop/api/mfidl/ne-mfidl-mf_transcode_topologymode_flags)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="0c453-109">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="0c453-109">Get/set</span></span>

<span data-ttu-id="0c453-110">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="0c453-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="0c453-111">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="0c453-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="0c453-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0c453-112">Remarks</span></span>

<span data-ttu-id="0c453-113">Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="0c453-113">This attribute is optional.</span></span> <span data-ttu-id="0c453-114">Elle doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="0c453-114">It must have one of the following values.</span></span>



| <span data-ttu-id="0c453-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c453-115">Value</span></span>                                              | <span data-ttu-id="0c453-116">Description</span><span class="sxs-lookup"><span data-stu-id="0c453-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c453-117">**\_matériel TOPOLOGYMODE de transcodage MF \_ \_ \_ autorisé**</span><span class="sxs-lookup"><span data-stu-id="0c453-117">**MF\_TRANSCODE\_TOPOLOGYMODE\_HARDWARE\_ALLOWED**</span></span> | <span data-ttu-id="0c453-118">Le chargeur de topologie chargera les MFTs matériels, tels que les décodeurs matériels, lorsqu’ils sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="0c453-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="0c453-119">Le chargeur de topologie revient automatiquement au décodage logiciel si aucun décodeur matériel n’est trouvé, ou si un décodeur matériel ne parvient pas à se connecter pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="0c453-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="0c453-120">**MF \_ transcodage \_ TOPOLOGYMODE \_ logiciel \_ uniquement**</span><span class="sxs-lookup"><span data-stu-id="0c453-120">**MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**</span></span>    | <span data-ttu-id="0c453-121">Le chargeur de topologie chargera uniquement les MFTss logicielles, y compris les décodeurs logiciels.</span><span class="sxs-lookup"><span data-stu-id="0c453-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="0c453-122">La valeur par défaut est **MF \_ transcodage \_ TOPOLOGYMODE \_ Software \_ uniquement**.</span><span class="sxs-lookup"><span data-stu-id="0c453-122">The default value is **MF\_TRANSCODE\_TOPOLOGYMODE\_SOFTWARE\_ONLY**.</span></span>

<span data-ttu-id="0c453-123">Si le chargeur de topologie insère une table MFT matérielle dans la topologie, il définit l’attribut d' [ \_ attribut d' \_ \_ URL matériel \_ de l’énumération MFT](mft-enum-hardware-url-attribute.md) sur le nœud de topologie.</span><span class="sxs-lookup"><span data-stu-id="0c453-123">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="0c453-124">Pour vérifier si une table MFT matérielle est présente, énumérez les nœuds dans la topologie résolue et vérifiez si cet attribut est présent.</span><span class="sxs-lookup"><span data-stu-id="0c453-124">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="0c453-125">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="0c453-125">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c453-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c453-126">Requirements</span></span>



| <span data-ttu-id="0c453-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c453-127">Requirement</span></span> | <span data-ttu-id="0c453-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c453-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0c453-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c453-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0c453-130">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c453-130">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0c453-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c453-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0c453-132">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c453-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="0c453-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c453-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c453-134"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c453-134"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c453-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c453-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c453-136">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c453-136">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0c453-137">API de transcodage</span><span class="sxs-lookup"><span data-stu-id="0c453-137">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="0c453-138">**IMFTranscodeProfile::GetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="0c453-138">**IMFTranscodeProfile::GetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-getcontainerattributes)
</dt> <dt>

[<span data-ttu-id="0c453-139">**IMFTranscodeProfile::SetContainerAttributes**</span><span class="sxs-lookup"><span data-stu-id="0c453-139">**IMFTranscodeProfile::SetContainerAttributes**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes)
</dt> </dl>

 

 




