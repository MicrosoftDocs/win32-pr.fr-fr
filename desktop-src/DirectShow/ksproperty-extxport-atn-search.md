---
description: Cette propriété envoie une commande à l’appareil pour rechercher un numéro de piste absolu (ATN). Le pilote de périphérique UVC prend en charge cette propriété.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4115c7ff1c4bc878b4ee80e284f11821c37909a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909446"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="d103b-104">\_recherche KSPROPERTY EXTXPORT \_ ATN \_</span><span class="sxs-lookup"><span data-stu-id="d103b-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="d103b-105">Cette propriété envoie une commande à l’appareil pour rechercher un numéro de piste absolu (ATN).</span><span class="sxs-lookup"><span data-stu-id="d103b-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="d103b-106">Le pilote de périphérique UVC prend en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d103b-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="d103b-107">Étiquette</span><span class="sxs-lookup"><span data-stu-id="d103b-107">Label</span></span> | <span data-ttu-id="d103b-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="d103b-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="d103b-109">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="d103b-109">Property Set GUID</span></span> | <span data-ttu-id="d103b-110">\_transport PROPSETID ext \_</span><span class="sxs-lookup"><span data-stu-id="d103b-110">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="d103b-111">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="d103b-111">Property ID</span></span>       | <span data-ttu-id="d103b-112">\_recherche KSPROPERTY EXTXPORT \_ ATN \_</span><span class="sxs-lookup"><span data-stu-id="d103b-112">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="d103b-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="d103b-113">Data Type</span></span>         | <span data-ttu-id="d103b-114">**KSPROPERTY \_ Structure EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="d103b-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="d103b-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="d103b-115">Remarks</span></span>

<span data-ttu-id="d103b-116">Définissez le membre **dwAbsTrackNumber** de la structure **KSPROPERTY \_ EXTXPORT \_ S** sur la valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="d103b-116">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="d103b-117">La spécification UVC ne définit pas la manière dont l’appareil utilise le bit de continuité.</span><span class="sxs-lookup"><span data-stu-id="d103b-117">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="d103b-118">La structure **KSPROPERTY \_ EXTXPORT \_ S** est décrite dans le DDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d103b-118">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="d103b-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d103b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d103b-120">Ensemble de propriétés de transport d’appareil externe</span><span class="sxs-lookup"><span data-stu-id="d103b-120">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



