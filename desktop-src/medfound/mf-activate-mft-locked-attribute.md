---
description: Spécifie si le chargeur de topologie doit modifier les types de médias sur une Media Foundation transformation (MFT). En général, les applications n’utilisent pas cet attribut.
ms.assetid: 96a99f35-f9db-407e-a4e3-7adc3caccb19
title: Attribut MF_ACTIVATE_MFT_LOCKED (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d6dcb6cb60f760d87761a18b2b83545937878c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114610"
---
# <a name="mf_activate_mft_locked-attribute"></a><span data-ttu-id="82079-104">\_Attribut de \_ verrouillage MFT d’activation MF \_</span><span class="sxs-lookup"><span data-stu-id="82079-104">MF\_ACTIVATE\_MFT\_LOCKED attribute</span></span>

<span data-ttu-id="82079-105">Spécifie si le chargeur de topologie doit modifier les types de médias sur une Media Foundation transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="82079-105">Specifies whether the Topology Loader will change the media types on a Media Foundation transform (MFT).</span></span> <span data-ttu-id="82079-106">En général, les applications n’utilisent pas cet attribut.</span><span class="sxs-lookup"><span data-stu-id="82079-106">Applications typically do not use this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="82079-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="82079-107">Data type</span></span>

<span data-ttu-id="82079-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="82079-108">**UINT32**</span></span>

<span data-ttu-id="82079-109">Traiter en tant que valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="82079-109">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82079-110">Notes</span><span class="sxs-lookup"><span data-stu-id="82079-110">Remarks</span></span>

<span data-ttu-id="82079-111">Si la valeur de cet attribut est différente de zéro, le chargeur de topologie ne modifiera pas les types de média sur la MFT.</span><span class="sxs-lookup"><span data-stu-id="82079-111">If value of this attribute is nonzero, the topology loader will not change the media types on the MFT.</span></span> <span data-ttu-id="82079-112">Le chargeur de topologie définit cet attribut après le chargement de la topologie.</span><span class="sxs-lookup"><span data-stu-id="82079-112">The topology loader sets this attribute after it loads the topology.</span></span>

<span data-ttu-id="82079-113">La constante GUID de cet attribut est exportée à partir de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="82079-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="82079-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82079-114">Requirements</span></span>



| <span data-ttu-id="82079-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82079-115">Requirement</span></span> | <span data-ttu-id="82079-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="82079-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82079-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82079-117">Minimum supported client</span></span><br/> | <span data-ttu-id="82079-118">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82079-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="82079-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="82079-119">Minimum supported server</span></span><br/> | <span data-ttu-id="82079-120">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="82079-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="82079-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="82079-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="82079-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="82079-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82079-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82079-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82079-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="82079-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="82079-125">**IMFAttributes::GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="82079-125">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="82079-126">**IMFAttributes::SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="82079-126">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="82079-127">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="82079-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




