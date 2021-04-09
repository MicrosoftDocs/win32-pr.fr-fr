---
description: Cette propriété envoie une commande à l’appareil pour rechercher un code d’heure spécifié. Le pilote de périphérique UVC prend en charge cette propriété.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52125f0c2e7ddd292cc1f93577a212d5c78a76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033418"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="12391-104">\_recherche de \_ code temporel KSPROPERTY EXTXPORT \_</span><span class="sxs-lookup"><span data-stu-id="12391-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="12391-105">Cette propriété envoie une commande à l’appareil pour rechercher un code d’heure spécifié.</span><span class="sxs-lookup"><span data-stu-id="12391-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="12391-106">Le pilote de périphérique UVC prend en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="12391-106">The UVC device driver supports this property.</span></span>



|                   |                                        |
|-------------------|----------------------------------------|
| <span data-ttu-id="12391-107">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="12391-107">Property Set GUID</span></span> | <span data-ttu-id="12391-108">\_transport PROPSETID ext \_</span><span class="sxs-lookup"><span data-stu-id="12391-108">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="12391-109">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="12391-109">Property ID</span></span>       | <span data-ttu-id="12391-110">\_recherche de \_ code temporel KSPROPERTY EXTXPORT \_</span><span class="sxs-lookup"><span data-stu-id="12391-110">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="12391-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="12391-111">Data Type</span></span>         | <span data-ttu-id="12391-112">**KSPROPERTY \_ Structure EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="12391-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="12391-113">Notes</span><span class="sxs-lookup"><span data-stu-id="12391-113">Remarks</span></span>

<span data-ttu-id="12391-114">Renseignez le membre du **code temporel** de la structure **KSPROPERTY \_ EXTXPORT \_ S** avec l’image, la seconde, la minute et l’heure souhaitées.</span><span class="sxs-lookup"><span data-stu-id="12391-114">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="12391-115">La structure **KSPROPERTY \_ EXTXPORT \_ S** est décrite dans le DDK Windows.</span><span class="sxs-lookup"><span data-stu-id="12391-115">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="12391-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="12391-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12391-117">Ensemble de propriétés de transport d’appareil externe</span><span class="sxs-lookup"><span data-stu-id="12391-117">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



