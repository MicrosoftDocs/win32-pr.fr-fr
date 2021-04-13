---
description: Spécifie la quantité de contenu, en millisecondes, qui peut tenir dans la mémoire tampon du modèle.
ms.assetid: da959bef-1e87-4638-9a77-4135c31a3d27
title: MFPKEY_VIDEOWINDOW, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33d10b3a589ef3bcfc945b2c3404c7b02cb7121
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527964"
---
# <a name="mfpkey_videowindow-property"></a><span data-ttu-id="a13e8-103">MFPKEY \_ propriété VIDEOWINDOW</span><span class="sxs-lookup"><span data-stu-id="a13e8-103">MFPKEY\_VIDEOWINDOW Property</span></span>

<span data-ttu-id="a13e8-104">Spécifie la quantité de contenu, en millisecondes, qui peut tenir dans la mémoire tampon du modèle.</span><span class="sxs-lookup"><span data-stu-id="a13e8-104">Specifies the amount of content, in milliseconds, that can fit into the model buffer.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a13e8-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="a13e8-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a13e8-106">\_wszWMVCVideoWIndow g</span><span class="sxs-lookup"><span data-stu-id="a13e8-106">g\_wszWMVCVideoWIndow</span></span>

## <a name="data-type"></a><span data-ttu-id="a13e8-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="a13e8-107">Data Type</span></span>

<span data-ttu-id="a13e8-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="a13e8-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="a13e8-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="a13e8-109">Default Value</span></span>

<span data-ttu-id="a13e8-110">3000</span><span class="sxs-lookup"><span data-stu-id="a13e8-110">3000</span></span>

## <a name="remarks"></a><span data-ttu-id="a13e8-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a13e8-111">Remarks</span></span>

<span data-ttu-id="a13e8-112">La fenêtre de mémoire tampon est l’un des paramètres de modèle de « compartiment perdu » utilisés dans le contrôle du taux de codec.</span><span class="sxs-lookup"><span data-stu-id="a13e8-112">The buffer window is one of the "leaky bucket" model parameters used in the codec rate control.</span></span>

## <a name="requirements"></a><span data-ttu-id="a13e8-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a13e8-113">Requirements</span></span>



| <span data-ttu-id="a13e8-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a13e8-114">Requirement</span></span> | <span data-ttu-id="a13e8-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a13e8-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a13e8-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a13e8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a13e8-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a13e8-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a13e8-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a13e8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a13e8-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a13e8-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a13e8-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="a13e8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a13e8-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a13e8-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a13e8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a13e8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a13e8-123">Configuration de l’encodage vidéo</span><span class="sxs-lookup"><span data-stu-id="a13e8-123">Configuring Video Encoding</span></span>](configuringvideoencoding.md)
</dt> <dt>

[<span data-ttu-id="a13e8-124">Modèle de mémoire tampon de compartiment avec fuite</span><span class="sxs-lookup"><span data-stu-id="a13e8-124">The Leaky Bucket Buffer Model</span></span>](the-leaky-bucket-buffer-model.md)
</dt> <dt>

[<span data-ttu-id="a13e8-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a13e8-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




