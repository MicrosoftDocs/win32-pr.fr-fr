---
title: PATCHARRAY (mmsystem. h)
description: PATCHARRAY est un type utilisé pour définir un tableau de correctifs MIDI.
ms.assetid: f48ee0d2-224a-4530-ac28-ae63160316cc
keywords:
- PATCHARRAY MIDIPATCHSIZE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e07af0e878fc0d2fc79d6d17aafd48fbd991fb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844397"
---
# <a name="patcharray"></a><span data-ttu-id="a5bf0-104">PATCHARRAY</span><span class="sxs-lookup"><span data-stu-id="a5bf0-104">PATCHARRAY</span></span>

<span data-ttu-id="a5bf0-105">PATCHARRAY est un type utilisé pour définir un tableau de correctifs MIDI.</span><span class="sxs-lookup"><span data-stu-id="a5bf0-105">PATCHARRAY is a type used to define an array of MIDI patches.</span></span>


```C++
typedef WORD PATCHARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="a5bf0-106">**PATCHARRAY \[ MIDIPATCHSIZE\]**</span><span class="sxs-lookup"><span data-stu-id="a5bf0-106">**PATCHARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="a5bf0-107">Chaque élément du tableau correspond à un correctif avec chacun des 16 bits représentant l’un des 16 canaux MIDI.</span><span class="sxs-lookup"><span data-stu-id="a5bf0-107">Each element in the array corresponds to a patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="a5bf0-108">Les bits sont définis pour chacun des canaux qui utilisent ce correctif particulier.</span><span class="sxs-lookup"><span data-stu-id="a5bf0-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="a5bf0-109">Par exemple, si le correctif numéro 0 est utilisé par les canaux MIDI physiques 0 et 8, l’élément 0 du tableau doit être défini sur 0x0101.</span><span class="sxs-lookup"><span data-stu-id="a5bf0-109">For example, if patch number 0 is used by physical MIDI channels 0 and 8, element 0 of the array should be set to 0x0101.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5bf0-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a5bf0-110">Requirements</span></span>



| <span data-ttu-id="a5bf0-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a5bf0-111">Requirement</span></span> | <span data-ttu-id="a5bf0-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="a5bf0-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5bf0-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5bf0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a5bf0-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5bf0-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a5bf0-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a5bf0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a5bf0-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a5bf0-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a5bf0-117">Version</span><span class="sxs-lookup"><span data-stu-id="a5bf0-117">Version</span></span><br/>                  | <span data-ttu-id="a5bf0-118">MIDI (Musical Instrument Digital Interface), types MIDI</span><span class="sxs-lookup"><span data-stu-id="a5bf0-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="a5bf0-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="a5bf0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5bf0-120"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5bf0-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5bf0-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a5bf0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5bf0-122">Types MIDI</span><span class="sxs-lookup"><span data-stu-id="a5bf0-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 





