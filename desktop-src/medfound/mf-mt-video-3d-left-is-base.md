---
description: Pour un format vidéo 3D, spécifie la vue qui est la vue de base.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: Attribut MF_MT_VIDEO_3D_LEFT_IS_BASE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f5ece66db7de19cd77d7e686d9665ad239c6d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536565"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a><span data-ttu-id="410e7-103">MF \_ MT \_ Video \_ 3D \_ Left \_ est l' \_ attribut de base</span><span class="sxs-lookup"><span data-stu-id="410e7-103">MF\_MT\_VIDEO\_3D\_LEFT\_IS\_BASE attribute</span></span>

<span data-ttu-id="410e7-104">Pour un format vidéo 3D, spécifie la vue qui est la vue de base.</span><span class="sxs-lookup"><span data-stu-id="410e7-104">For a 3D video format, specifies which view is the base view.</span></span>

## <a name="data-type"></a><span data-ttu-id="410e7-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="410e7-105">Data type</span></span>

<span data-ttu-id="410e7-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="410e7-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="410e7-107">Notes</span><span class="sxs-lookup"><span data-stu-id="410e7-107">Remarks</span></span>

<span data-ttu-id="410e7-108">Par défaut, la vue de gauche d’une séquence vidéo 3D est la vue de base.</span><span class="sxs-lookup"><span data-stu-id="410e7-108">By default, the left view in a 3D video sequence is the base view.</span></span> <span data-ttu-id="410e7-109">Si la vue de droite est la vue de base, affectez la valeur **false** à cet attribut.</span><span class="sxs-lookup"><span data-stu-id="410e7-109">If the right view is the base view, set this attribute to **FALSE**.</span></span>

<span data-ttu-id="410e7-110">Pour convertir une vidéo stéréoscopique en 2D, conservez la vue de base et débarrassez-vous de l’autre vue.</span><span class="sxs-lookup"><span data-stu-id="410e7-110">To convert stereoscopic video to 2D, keep the base view and discard the other view.</span></span>

## <a name="requirements"></a><span data-ttu-id="410e7-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="410e7-111">Requirements</span></span>



| <span data-ttu-id="410e7-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="410e7-112">Requirement</span></span> | <span data-ttu-id="410e7-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="410e7-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="410e7-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="410e7-114">Minimum supported client</span></span><br/> | <span data-ttu-id="410e7-115">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="410e7-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="410e7-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="410e7-116">Minimum supported server</span></span><br/> | <span data-ttu-id="410e7-117">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="410e7-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="410e7-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="410e7-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="410e7-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="410e7-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="410e7-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="410e7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="410e7-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="410e7-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




