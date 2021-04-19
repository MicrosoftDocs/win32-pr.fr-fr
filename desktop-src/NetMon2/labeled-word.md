---
description: La structure de mot ÉTIQUETÉe \_ définit une étiquette qui s’affiche lorsqu’une valeur de propriété de mot spécifique est détectée.
ms.assetid: bfb1d34e-4a07-493f-8e43-508b77cce581
title: Structure de LABELED_WORD (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_WORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 445b24245d2e9d15c1c2b6d69de20c464cbf1724
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518801"
---
# <a name="labeled_word-structure"></a><span data-ttu-id="84529-103">Structure de mot ÉTIQUETÉe \_</span><span class="sxs-lookup"><span data-stu-id="84529-103">LABELED\_WORD structure</span></span>

<span data-ttu-id="84529-104">La structure de **\_ mot étiquetée** définit une étiquette qui s’affiche lorsqu’une valeur de propriété de mot spécifique est détectée.</span><span class="sxs-lookup"><span data-stu-id="84529-104">The **LABELED\_WORD** structure defines a label that is displayed when a specific WORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="84529-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84529-105">Syntax</span></span>


```C++
typedef struct _LABELED_WORD {
  WORD  Value;
  LPSTR Label;
} LABELED_WORD, *LPLABELED_WORD;
```



## <a name="members"></a><span data-ttu-id="84529-106">Membres</span><span class="sxs-lookup"><span data-stu-id="84529-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="84529-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="84529-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="84529-108">Valeur de mot de la propriété que vous souhaitez détecter.</span><span class="sxs-lookup"><span data-stu-id="84529-108">WORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="84529-109">**Étiquette**</span><span class="sxs-lookup"><span data-stu-id="84529-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="84529-110">Description textuelle ou étiquette qui s’affiche lorsque la valeur de mot spécifiée dans le membre de **valeur** est détectée.</span><span class="sxs-lookup"><span data-stu-id="84529-110">Textual description or label that is displayed when the WORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84529-111">Notes</span><span class="sxs-lookup"><span data-stu-id="84529-111">Remarks</span></span>

<span data-ttu-id="84529-112">Le membre **lpLabeledWordTable** de la structure [Set](set.md) pointe vers un tableau de structures Set pour définir une ou plusieurs paires valeur d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="84529-112">The **lpLabeledWordTable** member of the [SET](set.md) structure points to an array of SET structures to define one or more label value pairs.</span></span> <span data-ttu-id="84529-113">Ces paires sont utilisées lorsque vous souhaitez afficher une étiquette à la place d’une valeur de mot spécifique trouvée dans un paquet de protocole.</span><span class="sxs-lookup"><span data-stu-id="84529-113">These pairs are used when you want to display a label in place of a specific WORD value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="84529-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84529-114">Requirements</span></span>



| <span data-ttu-id="84529-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84529-115">Requirement</span></span> | <span data-ttu-id="84529-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="84529-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="84529-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84529-117">Minimum supported client</span></span><br/> | <span data-ttu-id="84529-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84529-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="84529-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="84529-119">Minimum supported server</span></span><br/> | <span data-ttu-id="84529-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="84529-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="84529-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="84529-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="84529-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="84529-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84529-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84529-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84529-124">SET</span><span class="sxs-lookup"><span data-stu-id="84529-124">SET</span></span>](set.md)
</dt> </dl>

 

 




