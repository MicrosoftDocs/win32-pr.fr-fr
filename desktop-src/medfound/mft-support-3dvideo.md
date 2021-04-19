---
description: Spécifie si une Media Foundation transformation (MFT) prend en charge la vidéo stéréoscopique 3D.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: Attribut MFT_SUPPORT_3DVIDEO (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbc7208f9bbcf2c638ae83e988c6e541a4be2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517740"
---
# <a name="mft_support_3dvideo-attribute"></a><span data-ttu-id="f09fb-103">\_Attribut 3DVIDEO de la prise en charge de MFT \_</span><span class="sxs-lookup"><span data-stu-id="f09fb-103">MFT\_SUPPORT\_3DVIDEO attribute</span></span>

<span data-ttu-id="f09fb-104">Spécifie si une Media Foundation transformation (MFT) prend en charge la vidéo stéréoscopique 3D.</span><span class="sxs-lookup"><span data-stu-id="f09fb-104">Specifies whether a Media Foundation transform (MFT) supports 3D stereoscopic video.</span></span>

## <a name="data-type"></a><span data-ttu-id="f09fb-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="f09fb-105">Data type</span></span>

<span data-ttu-id="f09fb-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f09fb-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f09fb-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f09fb-107">Remarks</span></span>

<span data-ttu-id="f09fb-108">Pour interroger cet attribut, appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour obtenir le magasin d’attributs global de la table MFT.</span><span class="sxs-lookup"><span data-stu-id="f09fb-108">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="f09fb-109">Si la condition **GetAttributes** est établie, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="f09fb-109">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="f09fb-110">La valeur par défaut de cet attribut est **false**.</span><span class="sxs-lookup"><span data-stu-id="f09fb-110">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="f09fb-111">Traiter cet attribut comme étant en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="f09fb-111">Treat this attribute as read-only.</span></span> <span data-ttu-id="f09fb-112">Ne modifiez pas la valeur ; la table MFT ignore toute modification apportée à la valeur.</span><span class="sxs-lookup"><span data-stu-id="f09fb-112">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f09fb-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f09fb-113">Requirements</span></span>



| <span data-ttu-id="f09fb-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f09fb-114">Requirement</span></span> | <span data-ttu-id="f09fb-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="f09fb-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f09fb-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f09fb-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f09fb-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f09fb-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f09fb-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f09fb-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f09fb-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="f09fb-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f09fb-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="f09fb-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f09fb-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="f09fb-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f09fb-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f09fb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f09fb-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f09fb-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




