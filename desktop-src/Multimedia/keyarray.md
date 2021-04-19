---
title: Keyarray (mmsystem. h)
description: Keyarray spécifie un type utilisé pour définir un tableau de clés.
ms.assetid: af1a1d2f-4558-4374-93ab-5a705fc879ca
keywords:
- MIDIPATCHSIZE DE TABLEAU
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6e45e46417fb3b6653ecae605aa60f775c1d654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509925"
---
# <a name="keyarray"></a><span data-ttu-id="cdd2f-104">Tableau de la matrice</span><span class="sxs-lookup"><span data-stu-id="cdd2f-104">KEYARRAY</span></span>

<span data-ttu-id="cdd2f-105">Keyarray spécifie un type utilisé pour définir un tableau de clés.</span><span class="sxs-lookup"><span data-stu-id="cdd2f-105">KEYARRAY specifies a type used to define an array of keys.</span></span>


```C++
typedef WORD KEYARRAY[MIDIPATCHSIZE];
```



<dl> <dt>

<span data-ttu-id="cdd2f-106">**MIDIPATCHSIZE de tableau \[\]**</span><span class="sxs-lookup"><span data-stu-id="cdd2f-106">**KEYARRAY\[MIDIPATCHSIZE\]**</span></span>
</dt> <dd>

<span data-ttu-id="cdd2f-107">Chaque élément du tableau correspond à un correctif à percussion basé sur des clés avec chacun des 16 bits représentant l’un des 16 canaux MIDI.</span><span class="sxs-lookup"><span data-stu-id="cdd2f-107">Each element in the array corresponds to a key-based percussion patch with each of the 16 bits representing one of the 16 MIDI channels.</span></span> <span data-ttu-id="cdd2f-108">Les bits sont définis pour chacun des canaux qui utilisent ce correctif particulier.</span><span class="sxs-lookup"><span data-stu-id="cdd2f-108">Bits are set for each of the channels that use that particular patch.</span></span> <span data-ttu-id="cdd2f-109">Par exemple, si le correctif de percussion pour la clé numéro 60 est utilisé par les canaux MIDI physiques 9 et 15, l’élément 60 du tableau doit être défini sur 0x8200.</span><span class="sxs-lookup"><span data-stu-id="cdd2f-109">For example, if the percussion patch for key number 60 is used by physical MIDI channels 9 and 15, element 60 of the array should be set to 0x8200.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cdd2f-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cdd2f-110">Requirements</span></span>



| <span data-ttu-id="cdd2f-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cdd2f-111">Requirement</span></span> | <span data-ttu-id="cdd2f-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="cdd2f-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdd2f-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdd2f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="cdd2f-114">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdd2f-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cdd2f-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cdd2f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="cdd2f-116">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cdd2f-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cdd2f-117">Version</span><span class="sxs-lookup"><span data-stu-id="cdd2f-117">Version</span></span><br/>                  | <span data-ttu-id="cdd2f-118">MIDI (Musical Instrument Digital Interface), types MIDI</span><span class="sxs-lookup"><span data-stu-id="cdd2f-118">Musical Instrument Digital Interface (MIDI), MIDI Types</span></span><br/>                                        |
| <span data-ttu-id="cdd2f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="cdd2f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdd2f-120"><dt>MMSYSTEM. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cdd2f-120"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cdd2f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cdd2f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdd2f-122">Types MIDI</span><span class="sxs-lookup"><span data-stu-id="cdd2f-122">MIDI Types</span></span>](midi-event-types.md)
</dt> </dl>

 

 





