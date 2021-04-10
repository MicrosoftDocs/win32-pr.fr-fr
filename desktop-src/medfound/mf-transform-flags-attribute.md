---
description: Contient des indicateurs pour un objet d’activation de transformation Media Foundation (MFT).
ms.assetid: de377132-19b0-4c8c-882e-193c31420739
title: Attribut MF_TRANSFORM_FLAGS_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2f3e334b83bbe8ce50f8770eb33e1e7a4c799c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951392"
---
# <a name="mf_transform_flags_attribute-attribute"></a><span data-ttu-id="f823a-103">\_Attribut d' \_ attribut des indicateurs de transformation MF \_</span><span class="sxs-lookup"><span data-stu-id="f823a-103">MF\_TRANSFORM\_FLAGS\_Attribute attribute</span></span>

<span data-ttu-id="f823a-104">Contient des indicateurs pour un objet d’activation de transformation Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="f823a-104">Contains flags for a Media Foundation transform (MFT) activation object.</span></span>

## <a name="data-type"></a><span data-ttu-id="f823a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f823a-105">Data type</span></span>

<span data-ttu-id="f823a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f823a-106">**UINT32**</span></span>

<span data-ttu-id="f823a-107">La valeur est **une opération or** au niveau du bit des indicateurs de l’énumération de l' [**\_ \_ \_ indicateur d’énumération MFT**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) .</span><span class="sxs-lookup"><span data-stu-id="f823a-107">The value is a bitwise **OR** of flags from the [**\_MFT\_ENUM\_FLAG**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) enumeration.</span></span>

## <a name="getset"></a><span data-ttu-id="f823a-108">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="f823a-108">Get/set</span></span>

<span data-ttu-id="f823a-109">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f823a-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f823a-110">Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="f823a-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="f823a-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f823a-111">Remarks</span></span>

<span data-ttu-id="f823a-112">Cet attribut est défini sur les pointeurs [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) retournés par la fonction [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="f823a-112">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="f823a-113">L’attribut contient des indicateurs qui décrivent la table MFT.</span><span class="sxs-lookup"><span data-stu-id="f823a-113">The attribute contains flags that describe the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="f823a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f823a-114">Requirements</span></span>



| <span data-ttu-id="f823a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f823a-115">Requirement</span></span> | <span data-ttu-id="f823a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f823a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f823a-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f823a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f823a-118">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f823a-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f823a-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f823a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f823a-120">Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f823a-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f823a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="f823a-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f823a-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="f823a-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f823a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f823a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f823a-124">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f823a-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f823a-125">Attributs de transformation</span><span class="sxs-lookup"><span data-stu-id="f823a-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 
