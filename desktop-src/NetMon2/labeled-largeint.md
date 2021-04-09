---
description: La \_ structure LARGEINT nommée définit une étiquette qui s’affiche lorsqu’une valeur de propriété LARGEINT spécifique est détectée.
ms.assetid: ca565be0-96bb-4265-9422-793db0723563
title: Structure de LABELED_LARGEINT (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_LARGEINT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4de92c3e67567ef86bb3d46905e595bd9d54c194
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034577"
---
# <a name="labeled_largeint-structure"></a><span data-ttu-id="91483-103">\_Structure LARGEINT libellée</span><span class="sxs-lookup"><span data-stu-id="91483-103">LABELED\_LARGEINT structure</span></span>

<span data-ttu-id="91483-104">La **structure \_ LARGEINT nommée** définit une étiquette qui s’affiche lorsqu’une valeur de propriété LARGEINT spécifique est détectée.</span><span class="sxs-lookup"><span data-stu-id="91483-104">The **LABELED\_LARGEINT** structure defines a label that is displayed when a specific LARGEINT property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="91483-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91483-105">Syntax</span></span>


```C++
typedef struct _LABELED_LARGEINT {
  LARGE_INTEGER Value;
  LPSTR         Label;
} LABELED_LARGEINT, *LPLABELED_LARGEINT;
```



## <a name="members"></a><span data-ttu-id="91483-106">Membres</span><span class="sxs-lookup"><span data-stu-id="91483-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="91483-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="91483-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="91483-108">Valeur LARGEINT de la propriété que vous souhaitez détecter.</span><span class="sxs-lookup"><span data-stu-id="91483-108">LARGEINT value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="91483-109">**Étiquette**</span><span class="sxs-lookup"><span data-stu-id="91483-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="91483-110">Description textuelle ou étiquette qui s’affiche lorsque la valeur LARGEINT spécifiée dans le membre **value** est détectée.</span><span class="sxs-lookup"><span data-stu-id="91483-110">Textual description or label that is displayed when the LARGEINT value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91483-111">Notes</span><span class="sxs-lookup"><span data-stu-id="91483-111">Remarks</span></span>

<span data-ttu-id="91483-112">Le membre **lpLabeledLargeIntTable** de la structure [Set](set.md) pointe vers un tableau de structures d' **ensemble** qui définissent un ou plusieurs membres **label** des paires valeur LARGEINT.</span><span class="sxs-lookup"><span data-stu-id="91483-112">The **lpLabeledLargeIntTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the LARGEINT value pairs.</span></span> <span data-ttu-id="91483-113">Les paires sont utilisées lorsque vous souhaitez afficher une étiquette à la place d’une valeur LARGEINT spécifique trouvée dans un paquet de protocole.</span><span class="sxs-lookup"><span data-stu-id="91483-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in a protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="91483-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91483-114">Requirements</span></span>



| <span data-ttu-id="91483-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91483-115">Requirement</span></span> | <span data-ttu-id="91483-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="91483-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="91483-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91483-117">Minimum supported client</span></span><br/> | <span data-ttu-id="91483-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91483-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="91483-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91483-119">Minimum supported server</span></span><br/> | <span data-ttu-id="91483-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91483-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="91483-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="91483-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="91483-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="91483-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91483-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91483-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91483-124">SET</span><span class="sxs-lookup"><span data-stu-id="91483-124">SET</span></span>](set.md)
</dt> </dl>

 

 




