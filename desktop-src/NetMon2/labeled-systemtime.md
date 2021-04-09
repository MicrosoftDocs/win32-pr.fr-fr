---
description: La \_ structure SYSTEMTIME nommée définit une étiquette qui s’affiche lorsqu’une valeur de propriété SYSTEMTIME spécifique est détectée.
ms.assetid: 307b490a-af8e-4f2a-a45a-33a84fcb4d5c
title: Structure de LABELED_SYSTEMTIME (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_SYSTEMTIME
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4484d5ec55f700410eb80d11d2249cceceef43ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868826"
---
# <a name="labeled_systemtime-structure"></a><span data-ttu-id="07699-103">\_Structure SYSTEMTIME étiquetée</span><span class="sxs-lookup"><span data-stu-id="07699-103">LABELED\_SYSTEMTIME structure</span></span>

<span data-ttu-id="07699-104">La **structure \_ SystemTime nommée** définit une étiquette qui s’affiche lorsqu’une valeur de propriété SYSTEMTIME spécifique est détectée.</span><span class="sxs-lookup"><span data-stu-id="07699-104">The **LABELED\_SYSTEMTIME** structure defines a label that is displayed when a specific SYSTEMTIME property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="07699-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07699-105">Syntax</span></span>


```C++
typedef struct _LABELED_SYSTEMTIME {
  SYSTEMTIME Value;
  LPSTR      Label;
} LABELED_SYSTEMTIME, *LPLABELED_SYSTEMTIME;
```



## <a name="members"></a><span data-ttu-id="07699-106">Membres</span><span class="sxs-lookup"><span data-stu-id="07699-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="07699-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="07699-107">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="07699-108">Valeur SYSTEMTIME d’une propriété que vous souhaitez détecter.</span><span class="sxs-lookup"><span data-stu-id="07699-108">SYSTEMTIME value of a property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="07699-109">**Étiquette**</span><span class="sxs-lookup"><span data-stu-id="07699-109">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="07699-110">Description textuelle ou étiquette qui s’affiche lorsque la valeur SYSTEMTIME spécifiée dans le membre de **valeur** est détectée.</span><span class="sxs-lookup"><span data-stu-id="07699-110">Textual description or label that is displayed when the SYSTEMTIME value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07699-111">Notes</span><span class="sxs-lookup"><span data-stu-id="07699-111">Remarks</span></span>

<span data-ttu-id="07699-112">Le membre **lpLabeledSystemTimeTable** de la structure [Set](set.md) pointe vers un tableau de structures d' **ensemble** qui définissent une ou plusieurs paires de valeurs d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="07699-112">The **lpLabeledSystemTimeTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more label value pairs.</span></span> <span data-ttu-id="07699-113">Les paires sont utilisées lorsque vous souhaitez afficher une étiquette à la place d’une valeur LARGEINT spécifique trouvée dans le paquet de protocole.</span><span class="sxs-lookup"><span data-stu-id="07699-113">The pairs are used when you want to display a label in place of a specific LARGEINT value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="07699-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07699-114">Requirements</span></span>



| <span data-ttu-id="07699-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07699-115">Requirement</span></span> | <span data-ttu-id="07699-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="07699-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="07699-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07699-117">Minimum supported client</span></span><br/> | <span data-ttu-id="07699-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07699-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="07699-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07699-119">Minimum supported server</span></span><br/> | <span data-ttu-id="07699-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07699-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="07699-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="07699-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="07699-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="07699-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07699-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07699-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07699-124">SET</span><span class="sxs-lookup"><span data-stu-id="07699-124">SET</span></span>](set.md)
</dt> </dl>

 

 




