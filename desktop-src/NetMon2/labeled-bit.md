---
description: La structure de bits ÉTIQUETÉe \_ définit une paire de bits d’étiquette.
ms.assetid: 500b5159-bf9f-49d4-8567-d8e462015eb0
title: Structure de LABELED_BIT (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BIT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 24a56e832600b551dd3ab43ea93d59c5805af630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543468"
---
# <a name="labeled_bit-structure"></a><span data-ttu-id="91de4-103">Structure de bits ÉTIQUETÉe \_</span><span class="sxs-lookup"><span data-stu-id="91de4-103">LABELED\_BIT structure</span></span>

<span data-ttu-id="91de4-104">La structure de **\_ bits étiquetée** définit une paire de bits d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="91de4-104">The **LABELED\_BIT** structure defines a label BIT pair.</span></span>

## <a name="syntax"></a><span data-ttu-id="91de4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91de4-105">Syntax</span></span>


```C++
typedef struct _LABELED_BIT {
  BYTE  BitNumber;
  LPSTR LabelOff;
  LPSTR LabelOn;
} LABELED_BIT, *LPLABELED_BIT;
```



## <a name="members"></a><span data-ttu-id="91de4-106">Membres</span><span class="sxs-lookup"><span data-stu-id="91de4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="91de4-107">**BitNumber**</span><span class="sxs-lookup"><span data-stu-id="91de4-107">**BitNumber**</span></span>
</dt> <dd>

<span data-ttu-id="91de4-108">Numéro de BIT de la paire de bits d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="91de4-108">BIT number of the label BIT pair.</span></span> <span data-ttu-id="91de4-109">Les valeurs sont comprises entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="91de4-109">Values range from 0 to 255.</span></span> <span data-ttu-id="91de4-110">Affectez le BIT utilisé dans la comparaison de la valeur de la propriété au membre **Bitnumber** .</span><span class="sxs-lookup"><span data-stu-id="91de4-110">Set the **Bitnumber** member to the BIT used in the comparison of the property value.</span></span>

</dd> <dt>

<span data-ttu-id="91de4-111">**LabelOff**</span><span class="sxs-lookup"><span data-stu-id="91de4-111">**LabelOff**</span></span>
</dt> <dd>

<span data-ttu-id="91de4-112">Chaîne ou étiquette qui s’affiche lorsque le BIT spécifié dans **BitNumber** est égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="91de4-112">String or label that is displayed when the BIT specified in **BitNumber** equals zero.</span></span> <span data-ttu-id="91de4-113">Par exemple, une étiquette possible est « bit désactivé ».</span><span class="sxs-lookup"><span data-stu-id="91de4-113">For example, a possible label is "Bit OFF".</span></span>

</dd> <dt>

<span data-ttu-id="91de4-114">**LabelOn**</span><span class="sxs-lookup"><span data-stu-id="91de4-114">**LabelOn**</span></span>
</dt> <dd>

<span data-ttu-id="91de4-115">Chaîne ou étiquette qui s’affiche lorsque le BIT spécifié dans **BitNumber** est égal à 1.</span><span class="sxs-lookup"><span data-stu-id="91de4-115">String or label that is displayed when the BIT specified in **BitNumber** equals 1.</span></span> <span data-ttu-id="91de4-116">Par exemple, une étiquette possible est « bit ON ».</span><span class="sxs-lookup"><span data-stu-id="91de4-116">For example, a possible label is "Bit ON".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91de4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="91de4-117">Remarks</span></span>

<span data-ttu-id="91de4-118">Un tableau de **structures \_ binaires étiquetées** est utilisé pour définir un ensemble de paires de bits d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="91de4-118">An array of **LABELED\_BIT** structures is used to define a set of label BIT pairs.</span></span> <span data-ttu-id="91de4-119">Un pointeur vers le tableau est spécifié dans le membre **lpLabeledBit** de la structure [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="91de4-119">A pointer to the array is specified in the **lpLabeledBit** member of the [SET](set.md) structure.</span></span> <span data-ttu-id="91de4-120">Les paires sont utilisées lorsque vous souhaitez afficher une étiquette en fonction de la valeur de chaque BIT.</span><span class="sxs-lookup"><span data-stu-id="91de4-120">The pairs are used when you want to display a label based on the setting of each BIT.</span></span> <span data-ttu-id="91de4-121">En général, ce type de jeu est utilisé pour indiquer la valeur d’activation ou de désactivation de BITs.</span><span class="sxs-lookup"><span data-stu-id="91de4-121">Typically, this type of set is used to indicate the ON or OFF value of BITs.</span></span>

<span data-ttu-id="91de4-122">Lorsqu’un jeu de bits est spécifié, Moniteur réseau affiche uniquement les BITs inclus dans le tableau de structures d' **ensemble** .</span><span class="sxs-lookup"><span data-stu-id="91de4-122">When a BIT set is specified, Network Monitor displays only the BITs included in the array of **SET** structures.</span></span> <span data-ttu-id="91de4-123">Les BITs qui ne sont pas dans la structure **Set** ne sont pas affichés.</span><span class="sxs-lookup"><span data-stu-id="91de4-123">BITs that are not in the **SET** structure are not displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="91de4-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91de4-124">Requirements</span></span>



| <span data-ttu-id="91de4-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91de4-125">Requirement</span></span> | <span data-ttu-id="91de4-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="91de4-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="91de4-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91de4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="91de4-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91de4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="91de4-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91de4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="91de4-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91de4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="91de4-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="91de4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="91de4-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="91de4-132"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91de4-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91de4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91de4-134">SET</span><span class="sxs-lookup"><span data-stu-id="91de4-134">SET</span></span>](set.md)
</dt> </dl>

 

 




