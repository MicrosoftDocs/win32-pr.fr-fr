---
description: Spécifie si le récepteur multimédia DLNA (Digital vivant Network Alliance) utilise le service Planificateur de classes multimédias (MMCSS).
ms.assetid: 4c27e2ec-624a-4b1f-bea9-3aaad1534c9b
title: Attribut MF_MP2DLNA_USE_MMCSS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfdaf36ce51f1158e110dcb3682a5b072c060dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034592"
---
# <a name="mf_mp2dlna_use_mmcss-attribute"></a><span data-ttu-id="e9f80-103">MF \_ MP2DLNA \_ utiliser l' \_ attribut mmcss</span><span class="sxs-lookup"><span data-stu-id="e9f80-103">MF\_MP2DLNA\_USE\_MMCSS attribute</span></span>

<span data-ttu-id="e9f80-104">Spécifie si le récepteur multimédia DLNA (Digital vivant Network Alliance) utilise le service Planificateur de classes multimédias (MMCSS).</span><span class="sxs-lookup"><span data-stu-id="e9f80-104">Specifies whether the Digital Living Network Alliance (DLNA) media sink uses the Multimedia Class Scheduler Service (MMCSS).</span></span>

## <a name="data-type"></a><span data-ttu-id="e9f80-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e9f80-105">Data type</span></span>

<span data-ttu-id="e9f80-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e9f80-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e9f80-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="e9f80-107">Get/set</span></span>

<span data-ttu-id="e9f80-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e9f80-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e9f80-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e9f80-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="e9f80-110">Notes</span><span class="sxs-lookup"><span data-stu-id="e9f80-110">Remarks</span></span>

<span data-ttu-id="e9f80-111">Pour définir cet attribut sur le récepteur multimédia DLNA, interrogez le récepteur multimédia pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="e9f80-111">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="e9f80-112">Définissez l’attribut avant le début de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="e9f80-112">Set the attribute before streaming begins.</span></span>

<span data-ttu-id="e9f80-113">Si cet attribut a la **valeur true**, le récepteur multimédia DLNA s’inscrit lui-même auprès de mmcss.</span><span class="sxs-lookup"><span data-stu-id="e9f80-113">If this attribute is **TRUE**, the DLNA media sink registers itself with MMCSS.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9f80-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9f80-114">Requirements</span></span>



| <span data-ttu-id="e9f80-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9f80-115">Requirement</span></span> | <span data-ttu-id="e9f80-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9f80-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f80-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9f80-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f80-118">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9f80-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e9f80-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9f80-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f80-120">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9f80-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e9f80-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9f80-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9f80-122"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9f80-122"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9f80-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9f80-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f80-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e9f80-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




