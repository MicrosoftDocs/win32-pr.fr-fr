---
description: Spécifie si le codec doit utiliser le filtre de bruit lors de l’encodage.
ms.assetid: 9e099378-bb77-4dca-9171-7fe58e0139de
title: MFPKEY_DENOISEOPTION, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7f318e294f69095758fe300fce19043c23cf376
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519853"
---
# <a name="mfpkey_denoiseoption-property"></a><span data-ttu-id="c6e78-103">MFPKEY \_ propriété DENOISEOPTION</span><span class="sxs-lookup"><span data-stu-id="c6e78-103">MFPKEY\_DENOISEOPTION Property</span></span>

<span data-ttu-id="c6e78-104">Spécifie si le codec doit utiliser le filtre de bruit lors de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="c6e78-104">Specifies whether the codec will use the noise filter when encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="c6e78-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="c6e78-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="c6e78-106">\_wszWMVCDenoiseOption g</span><span class="sxs-lookup"><span data-stu-id="c6e78-106">g\_wszWMVCDenoiseOption</span></span>

## <a name="data-type"></a><span data-ttu-id="c6e78-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="c6e78-107">Data Type</span></span>

<span data-ttu-id="c6e78-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="c6e78-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="c6e78-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="c6e78-109">Default Value</span></span>

<span data-ttu-id="c6e78-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="c6e78-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="c6e78-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c6e78-111">Remarks</span></span>

<span data-ttu-id="c6e78-112">Le filtre de bruit peut améliorer la qualité des sources vidéo bruyantes, telles que les films contenant un grand nombre de grains ou d’images vidéo en faible luminosité.</span><span class="sxs-lookup"><span data-stu-id="c6e78-112">The noise filter can improve the quality of noisy video sources, such as film containing lots of grain or video shot in low light.</span></span> <span data-ttu-id="c6e78-113">Ce filtre peut être utilisé dans les scénarios d’encodage en temps réel où le prétraitement externe n’est pas une option.</span><span class="sxs-lookup"><span data-stu-id="c6e78-113">This filter can be used in live encoding scenarios where external preprocessing is not an option.</span></span>

<span data-ttu-id="c6e78-114">Ce filtre doit être désactivé pour les sources vidéo propres, car il peut réduire la qualité de l’image lorsque la qualité est bonne.</span><span class="sxs-lookup"><span data-stu-id="c6e78-114">This filter should be disabled for clean video sources since it can reduce image quality when the quality is good to start with.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6e78-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c6e78-115">Requirements</span></span>



| <span data-ttu-id="c6e78-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c6e78-116">Requirement</span></span> | <span data-ttu-id="c6e78-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c6e78-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e78-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6e78-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e78-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6e78-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c6e78-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c6e78-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e78-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c6e78-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6e78-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c6e78-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6e78-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6e78-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6e78-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c6e78-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e78-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6e78-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




