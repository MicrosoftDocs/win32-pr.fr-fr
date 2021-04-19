---
description: Spécifie si un flux s’exclut mutuellement avec d’autres flux du même type.
ms.assetid: 00a426ae-297c-4fcb-8132-d9c538bc9f1a
title: Attribut MF_SD_MUTUALLY_EXCLUSIVE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e3604eb9424bb646766f57261f745c57e18f3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541875"
---
# <a name="mf_sd_mutually_exclusive-attribute"></a><span data-ttu-id="81006-103">\_ \_ Attribut mutuelle exclusif MF \_ SD</span><span class="sxs-lookup"><span data-stu-id="81006-103">MF\_SD\_MUTUALLY\_EXCLUSIVE attribute</span></span>

<span data-ttu-id="81006-104">Spécifie si un flux s’exclut mutuellement avec d’autres flux du même type.</span><span class="sxs-lookup"><span data-stu-id="81006-104">Specifies whether a stream is mutually exclusive with other streams of the same type.</span></span>

## <a name="data-type"></a><span data-ttu-id="81006-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="81006-105">Data type</span></span>

<span data-ttu-id="81006-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="81006-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="81006-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="81006-107">Get/set</span></span>

<span data-ttu-id="81006-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="81006-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="81006-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="81006-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="81006-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="81006-110">Applies to</span></span>

[<span data-ttu-id="81006-111">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="81006-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="81006-112">Notes</span><span class="sxs-lookup"><span data-stu-id="81006-112">Remarks</span></span>

<span data-ttu-id="81006-113">Si cet attribut a la **valeur true** (différent de zéro), le flux s’exclut mutuellement avec d’autres flux du même type, tels que des données audio ou vidéo, au sein de la même présentation.</span><span class="sxs-lookup"><span data-stu-id="81006-113">If this attribute is **TRUE** (nonzero), the stream is mutually exclusive with other streams of the same type, such as audio or video, within the same presentation.</span></span> <span data-ttu-id="81006-114">Par exemple, si un fichier AVI contient plusieurs flux audio, ceux-ci sont marqués comme s’excluant mutuellement, car un seul flux audio doit être lu en même temps.</span><span class="sxs-lookup"><span data-stu-id="81006-114">For example, if an AVI file contains multiple audio streams, they are marked as mutually exclusive, because only one audio stream should be played at one time.</span></span>

<span data-ttu-id="81006-115">La valeur par défaut est **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="81006-115">The default value is **FALSE**.</span></span>

> [!Note]  
> <span data-ttu-id="81006-116">Cet attribut n’est pas utilisé pour les fichiers ASF (Advanced Systems Format), qui offrent un moyen plus sophistiqué de représenter des critères d’exclusion mutuelle.</span><span class="sxs-lookup"><span data-stu-id="81006-116">This attribute is not used for Advanced Systems Format (ASF) files, which have a more sophisticated way to represent mutual exclusion criteria.</span></span> <span data-ttu-id="81006-117">Pour plus d’informations, consultez [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="81006-117">For more information, see [**IMFASFMutualExclusion**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmutualexclusion).</span></span>

 

<span data-ttu-id="81006-118">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="81006-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="81006-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81006-119">Requirements</span></span>



| <span data-ttu-id="81006-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81006-120">Requirement</span></span> | <span data-ttu-id="81006-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="81006-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="81006-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81006-122">Minimum supported client</span></span><br/> | <span data-ttu-id="81006-123">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="81006-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="81006-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81006-124">Minimum supported server</span></span><br/> | <span data-ttu-id="81006-125">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="81006-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="81006-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="81006-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="81006-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="81006-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81006-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81006-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81006-129">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="81006-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="81006-130">Attributs du descripteur de flux</span><span class="sxs-lookup"><span data-stu-id="81006-130">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




