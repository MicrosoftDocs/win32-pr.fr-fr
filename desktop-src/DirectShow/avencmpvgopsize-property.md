---
description: Spécifie le nombre maximal d’images d’un en-tête de groupe d’images (GOP) à l’en-tête de GOP suivant.
ms.assetid: 90433df4-5a96-4bc2-a780-93306abcb0a4
title: Propriété AVEncMPVGOPSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c8907d0992153039b1af9a9a0e82ee5782b525d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033518"
---
# <a name="avencmpvgopsize-property"></a><span data-ttu-id="91724-103">Propriété AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="91724-103">AVEncMPVGOPSize property</span></span>

<span data-ttu-id="91724-104">Spécifie le nombre maximal d’images d’un en-tête de groupe d’images (GOP) à l’en-tête de GOP suivant.</span><span class="sxs-lookup"><span data-stu-id="91724-104">Specifies the maximum number of pictures from one group-of-pictures (GOP) header to the next GOP header.</span></span>

<span data-ttu-id="91724-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="91724-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="91724-106">Type de données</span><span class="sxs-lookup"><span data-stu-id="91724-106">Data type</span></span>

<span data-ttu-id="91724-107">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="91724-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="91724-108">Guid de propriété</span><span class="sxs-lookup"><span data-stu-id="91724-108">Property GUID</span></span>

<span data-ttu-id="91724-109">**CODECAPI \_ AVEncMPVGOPSize**</span><span class="sxs-lookup"><span data-stu-id="91724-109">**CODECAPI\_AVEncMPVGOPSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="91724-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="91724-110">Property value</span></span>

<span data-ttu-id="91724-111">Les encodeurs peuvent implémenter cette propriété en tant que jeu énuméré ou en tant que plage linéaire.</span><span class="sxs-lookup"><span data-stu-id="91724-111">Encoders can implement this property as an enumerated set or as a linear range.</span></span>

## <a name="remarks"></a><span data-ttu-id="91724-112">Notes</span><span class="sxs-lookup"><span data-stu-id="91724-112">Remarks</span></span>

<span data-ttu-id="91724-113">Définissez cette propriété avant de démarrer un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="91724-113">Set this property before starting a recording.</span></span>

<span data-ttu-id="91724-114">**S’applique à Windows 8 :** La taille de groupe d’images encodée doit être inférieure ou égale au nombre spécifié par le biais de cette propriété, afin de conserver le même modèle de frame B défini par [CODECAPI \_ AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) dans le groupe d’images ou en raison de la modification de la scène.</span><span class="sxs-lookup"><span data-stu-id="91724-114">**Applies to Windows 8:** The encoded GOP size shall be smaller than or equal to the specified number through this property, in order to keep the same B frame pattern set by [CODECAPI\_AVEncMPVDefaultBPictureCount](avencmpvdefaultbpicturecount-property.md) throughout the GOP or due to scene change.</span></span> <span data-ttu-id="91724-115">Par exemple, lorsque le nombre de frames B dans un groupe d’images est spécifié sur 2, et que la taille du groupe d’images est de 11, l’encodeur produit une taille de groupe d’images de 10 images ou moins.</span><span class="sxs-lookup"><span data-stu-id="91724-115">For example, when the number of B frames in a GOP is specified to be 2, and GOP size is 11, then encoder shall produce GOP size of 10 frames or less.</span></span> <span data-ttu-id="91724-116">Lorsque la modification de la scène se produit au milieu d’un groupe d’images, l’encodeur peut également insérer une image clé et produire un groupe d’images plus petit.</span><span class="sxs-lookup"><span data-stu-id="91724-116">When scene change happens in the middle of a GOP, encoder might also insert key frame and produce smaller GOP.</span></span>

<span data-ttu-id="91724-117">La taille de GOP 0 est dépendante de l’encodeur et les encodeurs peuvent choisir différentes tailles de groupe d’images en fonction de leur implémentation/qualité/performance.</span><span class="sxs-lookup"><span data-stu-id="91724-117">GOP size 0 is encoder dependent and encoders can choose different GOP sizes based on their implementation/quality/performance.</span></span> <span data-ttu-id="91724-118">Les encodeurs doivent honorer la taille de groupe d’images et tronquer les frames B dans ce cas.</span><span class="sxs-lookup"><span data-stu-id="91724-118">Encoders should honor the GOP size and truncate B frames in this case.</span></span>

## <a name="requirements"></a><span data-ttu-id="91724-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91724-119">Requirements</span></span>



| <span data-ttu-id="91724-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91724-120">Requirement</span></span> | <span data-ttu-id="91724-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="91724-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91724-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91724-122">Minimum supported client</span></span><br/> | <span data-ttu-id="91724-123">Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="91724-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="91724-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91724-124">Minimum supported server</span></span><br/> | <span data-ttu-id="91724-125">Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="91724-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="91724-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="91724-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="91724-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="91724-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91724-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91724-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91724-129">Propriétés de l’API codec</span><span class="sxs-lookup"><span data-stu-id="91724-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="91724-130">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="91724-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




