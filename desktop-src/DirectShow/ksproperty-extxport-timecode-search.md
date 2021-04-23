---
description: Cette propriété envoie une commande à l’appareil pour rechercher un code d’heure spécifié. Le pilote de périphérique UVC prend en charge cette propriété.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6852dc44e6ef10eebb59721f16a276ac5d4306a3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909437"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="a4c09-104">\_recherche de \_ code temporel KSPROPERTY EXTXPORT \_</span><span class="sxs-lookup"><span data-stu-id="a4c09-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="a4c09-105">Cette propriété envoie une commande à l’appareil pour rechercher un code d’heure spécifié.</span><span class="sxs-lookup"><span data-stu-id="a4c09-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="a4c09-106">Le pilote de périphérique UVC prend en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="a4c09-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="a4c09-107">Étiquette</span><span class="sxs-lookup"><span data-stu-id="a4c09-107">Label</span></span> | <span data-ttu-id="a4c09-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4c09-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="a4c09-109">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="a4c09-109">Property Set GUID</span></span> | <span data-ttu-id="a4c09-110">\_transport PROPSETID ext \_</span><span class="sxs-lookup"><span data-stu-id="a4c09-110">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="a4c09-111">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="a4c09-111">Property ID</span></span>       | <span data-ttu-id="a4c09-112">\_recherche de \_ code temporel KSPROPERTY EXTXPORT \_</span><span class="sxs-lookup"><span data-stu-id="a4c09-112">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="a4c09-113">Type de données</span><span class="sxs-lookup"><span data-stu-id="a4c09-113">Data Type</span></span>         | <span data-ttu-id="a4c09-114">**KSPROPERTY \_ Structure EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="a4c09-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="a4c09-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="a4c09-115">Remarks</span></span>

<span data-ttu-id="a4c09-116">Renseignez le membre du **code temporel** de la structure **KSPROPERTY \_ EXTXPORT \_ S** avec l’image, la seconde, la minute et l’heure souhaitées.</span><span class="sxs-lookup"><span data-stu-id="a4c09-116">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="a4c09-117">La structure **KSPROPERTY \_ EXTXPORT \_ S** est décrite dans le DDK Windows.</span><span class="sxs-lookup"><span data-stu-id="a4c09-117">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4c09-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a4c09-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c09-119">Ensemble de propriétés de transport d’appareil externe</span><span class="sxs-lookup"><span data-stu-id="a4c09-119">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



