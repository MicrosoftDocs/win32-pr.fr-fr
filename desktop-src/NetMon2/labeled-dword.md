---
description: La \_ structure DWORD étiquetée définit une étiquette qui s’affiche lorsqu’une valeur de propriété DWORD spécifique est détectée.
ms.assetid: 1aed3226-6d69-41b0-860b-4ffb5b905f1a
title: Structure de LABELED_DWORD (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_DWORD
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 0bec068622683172116bf8c4f6e88450d5752920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204009"
---
# <a name="labeled_dword-structure"></a><span data-ttu-id="acee4-103">\_Structure DWORD étiquetée</span><span class="sxs-lookup"><span data-stu-id="acee4-103">LABELED\_DWORD structure</span></span>

<span data-ttu-id="acee4-104">La **structure \_ DWORD étiquetée** définit une étiquette qui s’affiche lorsqu’une valeur de propriété DWORD spécifique est détectée.</span><span class="sxs-lookup"><span data-stu-id="acee4-104">The **LABELED\_DWORD** structure defines a label that is displayed when a specific DWORD property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="acee4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="acee4-105">Syntax</span></span>


```C++
typedef struct _LABELED_DWORD {
  DWORD Value;
  LPSTR Label;
} LABELED_DWORD, *LPLABELED_DWORD;
```



## <a name="members"></a><span data-ttu-id="acee4-106">Membres</span><span class="sxs-lookup"><span data-stu-id="acee4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="acee4-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="acee4-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="acee4-108">Valeur DWORD de la propriété que vous souhaitez détecter.</span><span class="sxs-lookup"><span data-stu-id="acee4-108">DWORD value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="acee4-109">**Étiquette**</span><span class="sxs-lookup"><span data-stu-id="acee4-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="acee4-110">Description textuelle ou étiquette qui s’affiche lorsque la valeur DWORD spécifiée dans le membre **value** est détectée.</span><span class="sxs-lookup"><span data-stu-id="acee4-110">Textual description or label that is displayed when the DWORD value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="acee4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="acee4-111">Remarks</span></span>

<span data-ttu-id="acee4-112">Le membre **lpLabeledDwordTable** de la structure [Set](set.md) pointe vers un tableau de structures d' **ensemble** qui définissent un ou plusieurs membres **étiquette** des paires valeur DWORD.</span><span class="sxs-lookup"><span data-stu-id="acee4-112">The **lpLabeledDwordTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the DWORD value pairs.</span></span> <span data-ttu-id="acee4-113">Les paires sont utilisées lorsque vous souhaitez afficher une étiquette à la place d’une valeur DWORD spécifique trouvée dans le paquet de protocole.</span><span class="sxs-lookup"><span data-stu-id="acee4-113">The pairs are used when you want to display a label in place of a specific DWORD value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="acee4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="acee4-114">Requirements</span></span>



| <span data-ttu-id="acee4-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="acee4-115">Requirement</span></span> | <span data-ttu-id="acee4-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="acee4-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="acee4-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acee4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="acee4-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acee4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="acee4-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="acee4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="acee4-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="acee4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="acee4-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="acee4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="acee4-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="acee4-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acee4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="acee4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acee4-124">SET</span><span class="sxs-lookup"><span data-stu-id="acee4-124">SET</span></span>](set.md)
</dt> </dl>

 

 




