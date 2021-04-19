---
description: Spécifie le type de bus d’e/s utilisé par la carte graphique.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: Énumération D3DBUSTYPE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 807e5a57c4abbf57c241643a3e7fea47606fbf75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544601"
---
# <a name="d3dbustype-enumeration"></a><span data-ttu-id="f525a-103">Énumération D3DBUSTYPE</span><span class="sxs-lookup"><span data-stu-id="f525a-103">D3DBUSTYPE enumeration</span></span>

<span data-ttu-id="f525a-104">Spécifie le type de bus d’e/s utilisé par la carte graphique.</span><span class="sxs-lookup"><span data-stu-id="f525a-104">Specifies the type of I/O bus used by the graphics adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f525a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f525a-105">Syntax</span></span>


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a><span data-ttu-id="f525a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="f525a-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f525a-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ autre**</span><span class="sxs-lookup"><span data-stu-id="f525a-107"><span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE\_OTHER**</span></span>
</dt> <dd>

<span data-ttu-id="f525a-108">Indique un type de bus autre que les types répertoriés ici.</span><span class="sxs-lookup"><span data-stu-id="f525a-108">Indicates a type of bus other than the types listed here.</span></span>

</dd> <dt>

<span data-ttu-id="f525a-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**</span><span class="sxs-lookup"><span data-stu-id="f525a-109"><span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE\_PCI**</span></span>
</dt> <dd>

<span data-ttu-id="f525a-110">Bus PCI.</span><span class="sxs-lookup"><span data-stu-id="f525a-110">PCI bus.</span></span>

</dd> <dt>

<span data-ttu-id="f525a-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ PCIx**</span><span class="sxs-lookup"><span data-stu-id="f525a-111"><span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE\_PCIX**</span></span>
</dt> <dd>

<span data-ttu-id="f525a-112">Bus PCI-X.</span><span class="sxs-lookup"><span data-stu-id="f525a-112">PCI-X bus.</span></span>

</dd> <dt>

<span data-ttu-id="f525a-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ PCIEXPRESS**</span><span class="sxs-lookup"><span data-stu-id="f525a-113"><span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE\_PCIEXPRESS**</span></span>
</dt> <dd>

<span data-ttu-id="f525a-114">Bus PCI Express.</span><span class="sxs-lookup"><span data-stu-id="f525a-114">PCI Express bus.</span></span>

</dd> <dt>

<span data-ttu-id="f525a-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**</span><span class="sxs-lookup"><span data-stu-id="f525a-115"><span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE\_AGP**</span></span>
</dt> <dd>

<span data-ttu-id="f525a-116">Bus AGP (Accelerated Graphics Port).</span><span class="sxs-lookup"><span data-stu-id="f525a-116">Accelerated Graphics Port (AGP) bus.</span></span>

</dd> <dt>

<span data-ttu-id="f525a-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**\_Modificateur D3DBUSIMPL \_ à l’intérieur \_ du \_ Chipset**</span><span class="sxs-lookup"><span data-stu-id="f525a-117"><span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**D3DBUSIMPL\_MODIFIER\_INSIDE\_OF\_CHIPSET**</span></span>
</dt> <dd>

<span data-ttu-id="f525a-118">L’implémentation de la carte graphique se trouve dans le pont nord d’un chipset de carte mère.</span><span class="sxs-lookup"><span data-stu-id="f525a-118">The implementation for the graphics adapter is in a motherboard chipset's north bridge.</span></span> <span data-ttu-id="f525a-119">Cet indicateur implique que les données ne sont jamais placées sur un bus d’expansion (comme PCI ou AGP) lorsqu’elles sont transférées de la mémoire principale vers la carte graphique.</span><span class="sxs-lookup"><span data-stu-id="f525a-119">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f525a-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**\_Le modificateur D3DBUSIMPL \_ effectue \_ le suivi de la \_ carte mère \_ \_ \_ sur la puce**</span><span class="sxs-lookup"><span data-stu-id="f525a-120"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_CHIP**</span></span>
</dt> <dd>

<span data-ttu-id="f525a-121">Indique que la carte graphique est connectée au pont nord d’un chipset de carte mère par des pistes sur la carte mère et que toutes les puces de la carte graphique sont soudées à la carte mère.</span><span class="sxs-lookup"><span data-stu-id="f525a-121">Indicates that the graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard and all of the graphics adapter's chips are soldered to the motherboard.</span></span> <span data-ttu-id="f525a-122">Cet indicateur implique que les données ne sont jamais placées sur un bus d’expansion (comme PCI ou AGP) lorsqu’elles sont transférées de la mémoire principale vers la carte graphique.</span><span class="sxs-lookup"><span data-stu-id="f525a-122">This flag implies that data never goes over an expansion bus (such as PCI or AGP) when it is transferred from main memory to the graphics adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f525a-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**\_Le modificateur D3DBUSIMPL \_ effectue \_ le suivi de la \_ \_ carte mère \_ au \_ Socket**</span><span class="sxs-lookup"><span data-stu-id="f525a-123"><span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL\_MODIFIER\_TRACKS\_ON\_MOTHER\_BOARD\_TO\_SOCKET**</span></span>
</dt> <dd>

<span data-ttu-id="f525a-124">La carte graphique est connectée au pont nord d’un chipset de carte mère par des pistes sur la carte mère, et toutes les puces de la carte graphique sont connectées via des sockets à la carte mère.</span><span class="sxs-lookup"><span data-stu-id="f525a-124">The graphics adapter is connected to a motherboard chipset's north bridge by tracks on the motherboard, and all of the graphics adapter's chips are connected through sockets to the motherboard.</span></span>

</dd> <dt>

<span data-ttu-id="f525a-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**\_ \_ Connecteur de carte fille de MODIFICATeur D3DBUSIMPL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f525a-125"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR**</span></span>
</dt> <dd>

<span data-ttu-id="f525a-126">La carte graphique est connectée à la carte mère via un connecteur en fille.</span><span class="sxs-lookup"><span data-stu-id="f525a-126">The graphics adapter is connected to the motherboard through a daughterboard connector.</span></span>

</dd> <dt>

<span data-ttu-id="f525a-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**\_ \_ \_ Connecteur de carte fille de modificateur D3DBUSIMPL \_ \_ dans \_ \_ NUAE**</span><span class="sxs-lookup"><span data-stu-id="f525a-127"><span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**D3DBUSIMPL\_MODIFIER\_DAUGHTER\_BOARD\_CONNECTOR\_INSIDE\_OF\_NUAE**</span></span>
</dt> <dd>

<span data-ttu-id="f525a-128">La carte graphique est connectée à la carte mère via un connecteur à fille et la carte graphique est à l’intérieur d’un boîtier qui n’est pas accessible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f525a-128">The graphics adapter is connected to the motherboard through a daughterboard connector, and the graphics adapter is inside an enclosure that is not user accessible.</span></span>

</dd> <dt>

<span data-ttu-id="f525a-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**\_Modificateur D3DBUSIMPL \_ non \_ standard**</span><span class="sxs-lookup"><span data-stu-id="f525a-129"><span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**D3DBUSIMPL\_MODIFIER\_NON\_STANDARD**</span></span>
</dt> <dd>

<span data-ttu-id="f525a-130">L’un des indicateurs modificateur de \_ modificateur D3DBUSIMPL \_ \_ xxx est défini.</span><span class="sxs-lookup"><span data-stu-id="f525a-130">One of the D3DBUSIMPL\_MODIFIER\_MODIFIER\_Xxx flags is set.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f525a-131">Notes</span><span class="sxs-lookup"><span data-stu-id="f525a-131">Remarks</span></span>

<span data-ttu-id="f525a-132">Jusqu’à trois indicateurs peuvent être définis.</span><span class="sxs-lookup"><span data-stu-id="f525a-132">As many as three flags can be set.</span></span> <span data-ttu-id="f525a-133">Les indicateurs dans la plage 0x00 à 0x04 (**D3DBUSTYPE \_ xxx**) fournissent le type de bus de base.</span><span class="sxs-lookup"><span data-stu-id="f525a-133">Flags in the range 0x00 through 0x04 (**D3DBUSTYPE\_Xxx**) provide the basic bus type.</span></span> <span data-ttu-id="f525a-134">Les indicateurs dans la plage 0x10000 à 0x50000 **( \_ modificateur D3DBUSIMPL \_ xxx**) modifient la description de base.</span><span class="sxs-lookup"><span data-stu-id="f525a-134">Flags in the range 0x10000 through 0x50000 (**D3DBUSIMPL\_MODIFIER\_Xxx**) modify the basic description.</span></span> <span data-ttu-id="f525a-135">Le pilote définit un indicateur de type bus et peut définir zéro ou un indicateur de modificateur.</span><span class="sxs-lookup"><span data-stu-id="f525a-135">The driver sets one bus-type flag, and can set zero or one modifier flag.</span></span> <span data-ttu-id="f525a-136">Si le pilote définit un indicateur de modificateur, il définit également l’indicateur **D3DBUSIMPL \_ modificateur \_ non \_ standard** .</span><span class="sxs-lookup"><span data-stu-id="f525a-136">If the driver sets a modifier flag, it also sets the **D3DBUSIMPL\_MODIFIER\_NON\_STANDARD** flag.</span></span> <span data-ttu-id="f525a-137">Les indicateurs sont combinés avec une **opération or** au niveau du bit.</span><span class="sxs-lookup"><span data-stu-id="f525a-137">Flags are combined with a bitwise **OR**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f525a-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f525a-138">Requirements</span></span>



| <span data-ttu-id="f525a-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f525a-139">Requirement</span></span> | <span data-ttu-id="f525a-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="f525a-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f525a-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f525a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f525a-142">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f525a-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f525a-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f525a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f525a-144">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f525a-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f525a-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="f525a-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="f525a-146"><dt>D3d9types. h (inclure d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f525a-146"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f525a-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f525a-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f525a-148">Énumérations de vidéos Direct3D</span><span class="sxs-lookup"><span data-stu-id="f525a-148">Direct3D Video Enumerations</span></span>](direct3d-video-enumerations.md)
</dt> </dl>

 

 




