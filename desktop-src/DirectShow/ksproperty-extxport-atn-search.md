---
description: Cette propriété envoie une commande à l’appareil pour rechercher un numéro de piste absolu (ATN). Le pilote de périphérique UVC prend en charge cette propriété.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8ff454386c444ed6b55bfbeede60196a75127c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515887"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="63ad4-104">\_recherche KSPROPERTY EXTXPORT \_ ATN \_</span><span class="sxs-lookup"><span data-stu-id="63ad4-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="63ad4-105">Cette propriété envoie une commande à l’appareil pour rechercher un numéro de piste absolu (ATN).</span><span class="sxs-lookup"><span data-stu-id="63ad4-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="63ad4-106">Le pilote de périphérique UVC prend en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="63ad4-106">The UVC device driver supports this property.</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="63ad4-107">GUID de jeu de propriétés</span><span class="sxs-lookup"><span data-stu-id="63ad4-107">Property Set GUID</span></span> | <span data-ttu-id="63ad4-108">\_transport PROPSETID ext \_</span><span class="sxs-lookup"><span data-stu-id="63ad4-108">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="63ad4-109">ID de propriété</span><span class="sxs-lookup"><span data-stu-id="63ad4-109">Property ID</span></span>       | <span data-ttu-id="63ad4-110">\_recherche KSPROPERTY EXTXPORT \_ ATN \_</span><span class="sxs-lookup"><span data-stu-id="63ad4-110">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="63ad4-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="63ad4-111">Data Type</span></span>         | <span data-ttu-id="63ad4-112">**KSPROPERTY \_ Structure EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="63ad4-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="63ad4-113">Notes</span><span class="sxs-lookup"><span data-stu-id="63ad4-113">Remarks</span></span>

<span data-ttu-id="63ad4-114">Définissez le membre **dwAbsTrackNumber** de la structure **KSPROPERTY \_ EXTXPORT \_ S** sur la valeur suivante :</span><span class="sxs-lookup"><span data-stu-id="63ad4-114">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="63ad4-115">La spécification UVC ne définit pas la manière dont l’appareil utilise le bit de continuité.</span><span class="sxs-lookup"><span data-stu-id="63ad4-115">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="63ad4-116">La structure **KSPROPERTY \_ EXTXPORT \_ S** est décrite dans le DDK Windows.</span><span class="sxs-lookup"><span data-stu-id="63ad4-116">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="63ad4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63ad4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63ad4-118">Ensemble de propriétés de transport d’appareil externe</span><span class="sxs-lookup"><span data-stu-id="63ad4-118">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



