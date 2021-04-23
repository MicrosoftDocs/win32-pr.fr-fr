---
description: Le navigateur DVD utilise cette propriété pour informer le décodeur que le navigateur définit les horodatages corrects sur les exemples qu’il remet au décodeur.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: AM_RATE_CorrectTS, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c65b613f892708dc210af2ca2a05efb74785fb
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910297"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="63eba-103">\_ \_ Propriété CORRECTTS rate AM</span><span class="sxs-lookup"><span data-stu-id="63eba-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="63eba-104">Le navigateur DVD utilise cette propriété pour informer le décodeur que le navigateur définit les horodatages corrects sur les exemples qu’il remet au décodeur.</span><span class="sxs-lookup"><span data-stu-id="63eba-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



| <span data-ttu-id="63eba-105">Étiquette</span><span class="sxs-lookup"><span data-stu-id="63eba-105">Label</span></span> | <span data-ttu-id="63eba-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="63eba-106">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="63eba-107">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="63eba-107">Property Set GUID</span></span> | <span data-ttu-id="63eba-108">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="63eba-108">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="63eba-109">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="63eba-109">Property ID</span></span>       | <span data-ttu-id="63eba-110">\_Taux am \_ CorrectTS</span><span class="sxs-lookup"><span data-stu-id="63eba-110">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="63eba-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="63eba-111">Data Type</span></span>         | <span data-ttu-id="63eba-112">**LONG**</span><span class="sxs-lookup"><span data-stu-id="63eba-112">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="63eba-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="63eba-113">Remarks</span></span>

<span data-ttu-id="63eba-114">Les versions antérieures du navigateur DVD n’ont pas défini les horodatages corrects lorsque la vitesse de lecture était différente de 1,0.</span><span class="sxs-lookup"><span data-stu-id="63eba-114">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="63eba-115">De nombreux décodeurs contournent ce problème en ignorant les horodatages pendant le rembobinage ou l’avance rapide, et en estimant les durées de présentation appropriées.</span><span class="sxs-lookup"><span data-stu-id="63eba-115">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="63eba-116">Ces problèmes ont été corrigés dans la version actuelle du navigateur DVD.</span><span class="sxs-lookup"><span data-stu-id="63eba-116">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="63eba-117">Pour assurer la compatibilité descendante avec les décodeurs existants, le navigateur DVD indique que les horodatages sont corrects en définissant la \_ \_ propriété CorrectTS rate sur le décodeur avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="63eba-117">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="63eba-118">Quand cette propriété est définie, le décodeur doit utiliser les horodatages réels au lieu d’estimer les temps de présentation.</span><span class="sxs-lookup"><span data-stu-id="63eba-118">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="63eba-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63eba-119">Requirements</span></span>



| <span data-ttu-id="63eba-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63eba-120">Requirement</span></span> | <span data-ttu-id="63eba-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="63eba-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63eba-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="63eba-122">Header</span></span><br/> | <dl> <span data-ttu-id="63eba-123"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="63eba-123"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63eba-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63eba-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63eba-125">**Définition de la propriété change rate**</span><span class="sxs-lookup"><span data-stu-id="63eba-125">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




