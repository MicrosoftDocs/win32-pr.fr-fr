---
description: Spécifie la qualité d’encodage pour le récepteur multimédia DLNA (Digital vivant Network Alliance).
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: Attribut MF_MP2DLNA_ENCODE_QUALITY (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c785ff12524d45d096d566014a5c0a5e24eea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034594"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a><span data-ttu-id="88cd2-103">\_Attribut de \_ qualité de codage MF MP2DLNA \_</span><span class="sxs-lookup"><span data-stu-id="88cd2-103">MF\_MP2DLNA\_ENCODE\_QUALITY attribute</span></span>

<span data-ttu-id="88cd2-104">Spécifie la qualité d’encodage pour le récepteur multimédia DLNA (Digital vivant Network Alliance).</span><span class="sxs-lookup"><span data-stu-id="88cd2-104">Specifies the encoding quality for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="88cd2-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="88cd2-105">Data type</span></span>

<span data-ttu-id="88cd2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="88cd2-106">**UINT32**</span></span>

<span data-ttu-id="88cd2-107">Plage : 0 – 18</span><span class="sxs-lookup"><span data-stu-id="88cd2-107">Range: 0–18</span></span>

## <a name="getset"></a><span data-ttu-id="88cd2-108">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="88cd2-108">Get/set</span></span>

<span data-ttu-id="88cd2-109">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="88cd2-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="88cd2-110">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="88cd2-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="88cd2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="88cd2-111">Remarks</span></span>

<span data-ttu-id="88cd2-112">Des valeurs plus élevées indiquent une meilleure qualité de codage.</span><span class="sxs-lookup"><span data-stu-id="88cd2-112">Higher numbers indicate better encoding quality.</span></span> <span data-ttu-id="88cd2-113">Les nombres inférieurs indiquent un encodage plus rapide, mais une qualité de codage inférieure.</span><span class="sxs-lookup"><span data-stu-id="88cd2-113">Lower numbers indicate faster encoding, but lower encoding quality.</span></span> <span data-ttu-id="88cd2-114">La valeur par défaut est 9.</span><span class="sxs-lookup"><span data-stu-id="88cd2-114">The default value is 9.</span></span>

<span data-ttu-id="88cd2-115">Pour définir cet attribut sur le récepteur multimédia DLNA, interrogez le récepteur multimédia pour l’interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="88cd2-115">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="88cd2-116">Définissez l’attribut avant le début de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="88cd2-116">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="88cd2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88cd2-117">Requirements</span></span>



| <span data-ttu-id="88cd2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88cd2-118">Requirement</span></span> | <span data-ttu-id="88cd2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="88cd2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88cd2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88cd2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="88cd2-121">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88cd2-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="88cd2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="88cd2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="88cd2-123">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="88cd2-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="88cd2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="88cd2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="88cd2-125"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="88cd2-125"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88cd2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88cd2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88cd2-127">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="88cd2-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




