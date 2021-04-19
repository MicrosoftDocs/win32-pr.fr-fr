---
description: Le navigateur DVD utilise cette propriété pour informer le décodeur que le navigateur définit les horodatages corrects sur les exemples qu’il remet au décodeur.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: AM_RATE_CorrectTS, propriété (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa410b079d3de63de364662c7d5465c82814d24a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539967"
---
# <a name="am_rate_correctts-property"></a><span data-ttu-id="723af-103">\_ \_ Propriété CORRECTTS rate AM</span><span class="sxs-lookup"><span data-stu-id="723af-103">AM\_RATE\_CorrectTS Property</span></span>

<span data-ttu-id="723af-104">Le navigateur DVD utilise cette propriété pour informer le décodeur que le navigateur définit les horodatages corrects sur les exemples qu’il remet au décodeur.</span><span class="sxs-lookup"><span data-stu-id="723af-104">The DVD Navigator uses this property to inform the decoder that the Navigator is setting the correct time stamps on the samples it delivers to the decoder.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="723af-105">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="723af-105">Property Set GUID</span></span> | <span data-ttu-id="723af-106">AM \_ KSPROPSETID \_ TSRateChange</span><span class="sxs-lookup"><span data-stu-id="723af-106">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="723af-107">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="723af-107">Property ID</span></span>       | <span data-ttu-id="723af-108">\_Taux am \_ CorrectTS</span><span class="sxs-lookup"><span data-stu-id="723af-108">AM\_RATE\_CorrectTS</span></span>           |
| <span data-ttu-id="723af-109">Type de données</span><span class="sxs-lookup"><span data-stu-id="723af-109">Data Type</span></span>         | <span data-ttu-id="723af-110">**LONG**</span><span class="sxs-lookup"><span data-stu-id="723af-110">**LONG**</span></span>                      |



 

## <a name="remarks"></a><span data-ttu-id="723af-111">Notes</span><span class="sxs-lookup"><span data-stu-id="723af-111">Remarks</span></span>

<span data-ttu-id="723af-112">Les versions antérieures du navigateur DVD n’ont pas défini les horodatages corrects lorsque la vitesse de lecture était différente de 1,0.</span><span class="sxs-lookup"><span data-stu-id="723af-112">Earlier versions of the DVD Navigator did not set the correct time stamps when the playback rate was something other than 1.0.</span></span> <span data-ttu-id="723af-113">De nombreux décodeurs contournent ce problème en ignorant les horodatages pendant le rembobinage ou l’avance rapide, et en estimant les durées de présentation appropriées.</span><span class="sxs-lookup"><span data-stu-id="723af-113">Many decoders work around this problem by ignoring the time stamps during rewind or fast forward, and estimating the correct presentation times.</span></span>

<span data-ttu-id="723af-114">Ces problèmes ont été corrigés dans la version actuelle du navigateur DVD.</span><span class="sxs-lookup"><span data-stu-id="723af-114">These problems have been corrected in the current version of the DVD Navigator.</span></span> <span data-ttu-id="723af-115">Pour assurer la compatibilité descendante avec les décodeurs existants, le navigateur DVD indique que les horodatages sont corrects en définissant la \_ \_ propriété CorrectTS rate sur le décodeur avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="723af-115">For backward compatibility with existing decoders, the DVD Navigator indicates that the time stamps are correct by setting the AM\_RATE\_CorrectTS property on the decoder with the value **TRUE**.</span></span> <span data-ttu-id="723af-116">Quand cette propriété est définie, le décodeur doit utiliser les horodatages réels au lieu d’estimer les temps de présentation.</span><span class="sxs-lookup"><span data-stu-id="723af-116">When this property is set, the decoder should use the actual time stamps, instead of estimating the presentation times.</span></span>

## <a name="requirements"></a><span data-ttu-id="723af-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="723af-117">Requirements</span></span>



| <span data-ttu-id="723af-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="723af-118">Requirement</span></span> | <span data-ttu-id="723af-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="723af-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="723af-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="723af-120">Header</span></span><br/> | <dl> <span data-ttu-id="723af-121"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="723af-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="723af-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="723af-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="723af-123">**Définition de la propriété change rate**</span><span class="sxs-lookup"><span data-stu-id="723af-123">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




