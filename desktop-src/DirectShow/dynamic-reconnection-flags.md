---
description: Les indicateurs suivants spécifient le niveau de reconnexion dynamique à utiliser pendant le rendu.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Indicateurs de reconnexion dynamique (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542312"
---
# <a name="dynamic-reconnection-flags"></a><span data-ttu-id="881cc-103">Indicateurs de reconnexion dynamique</span><span class="sxs-lookup"><span data-stu-id="881cc-103">Dynamic Reconnection Flags</span></span>

<span data-ttu-id="881cc-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="881cc-104">\[Deprecated.</span></span> <span data-ttu-id="881cc-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="881cc-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="881cc-106">Les indicateurs suivants spécifient le niveau de reconnexion dynamique à utiliser pendant le rendu.</span><span class="sxs-lookup"><span data-stu-id="881cc-106">The following flags specify the level of dynamic reconnection to use during rendering.</span></span>



| <span data-ttu-id="881cc-107">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="881cc-107">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="881cc-108">Description</span><span class="sxs-lookup"><span data-stu-id="881cc-108">Description</span></span>                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <span data-ttu-id="881cc-109"><dt>**CONNECTF \_ DYNAMIQUE \_ aucun**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="881cc-109"><dt>**CONNECTF\_DYNAMIC\_NONE**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="881cc-110">Aucune reconnexion dynamique.</span><span class="sxs-lookup"><span data-stu-id="881cc-110">No dynamic reconnection.</span></span> <span data-ttu-id="881cc-111">Chargez tout avant de restituer le projet.</span><span class="sxs-lookup"><span data-stu-id="881cc-111">Load everything before rendering the project.</span></span><br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <span data-ttu-id="881cc-112"><dt>**CONNECTF \_ \_Sources dynamiques**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="881cc-112"><dt>**CONNECTF\_DYNAMIC\_SOURCES**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="881cc-113">Chargez les sources uniquement si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="881cc-113">Load sources only as needed.</span></span><br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <span data-ttu-id="881cc-114"><dt>**CONNECTF \_ \_Effets dynamiques**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="881cc-114"><dt>**CONNECTF\_DYNAMIC\_EFFECTS**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="881cc-115">Réservé.</span><span class="sxs-lookup"><span data-stu-id="881cc-115">Reserved.</span></span> <span data-ttu-id="881cc-116">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="881cc-116">Do not use.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="881cc-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="881cc-117">Requirements</span></span>



| <span data-ttu-id="881cc-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="881cc-118">Requirement</span></span> | <span data-ttu-id="881cc-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="881cc-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="881cc-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="881cc-120">Header</span></span><br/> | <dl> <span data-ttu-id="881cc-121"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="881cc-121"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="881cc-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="881cc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="881cc-123">**IRenderEngine::SetDynamicReconnectLevel**</span><span class="sxs-lookup"><span data-stu-id="881cc-123">**IRenderEngine::SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




