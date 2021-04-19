---
description: La \_ structure d’octets étiquetée définit une paire de bits étiquetée. L’étiquette de la paire de bits étiquetée s’affiche lorsqu’une valeur de propriété d’octet spécifique est détectée.
ms.assetid: 6dc6a773-da75-4ffe-878f-b30ceef2acb1
title: Structure de LABELED_BYTE (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LABELED_BYTE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 4768e605892b9bfe2a3df67fbdea862f67dc1a16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530653"
---
# <a name="labeled_byte-structure"></a><span data-ttu-id="3105a-104">Structure d’octets ÉTIQUETÉe \_</span><span class="sxs-lookup"><span data-stu-id="3105a-104">LABELED\_BYTE structure</span></span>

<span data-ttu-id="3105a-105">La structure d' **\_ octets étiquetée** définit une paire de bits étiquetée.</span><span class="sxs-lookup"><span data-stu-id="3105a-105">The **LABELED\_BYTE** structure defines a labeled BIT pair.</span></span> <span data-ttu-id="3105a-106">L' **étiquette** de la paire de bits étiquetée s’affiche lorsqu’une valeur de propriété d’octet spécifique est détectée.</span><span class="sxs-lookup"><span data-stu-id="3105a-106">The **Label** of the labeled BIT pair is displayed when a specific byte property value is detected.</span></span>

## <a name="syntax"></a><span data-ttu-id="3105a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3105a-107">Syntax</span></span>


```C++
typedef struct _LABELED_BYTE {
  BYTE  Value;
  LPSTR Label;
} LABELED_BYTE, *LPLABELED_BYTE;
```



## <a name="members"></a><span data-ttu-id="3105a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3105a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3105a-109">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="3105a-109">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="3105a-110">Valeur d’octet de la propriété que vous souhaitez détecter.</span><span class="sxs-lookup"><span data-stu-id="3105a-110">BYTE value of the property that you want to detect.</span></span>

</dd> <dt>

<span data-ttu-id="3105a-111">**Étiquette**</span><span class="sxs-lookup"><span data-stu-id="3105a-111">**Label**</span></span>
</dt> <dd>

<span data-ttu-id="3105a-112">Description textuelle ou étiquette qui s’affiche lorsque la valeur spécifiée dans le membre de **valeur** est détectée.</span><span class="sxs-lookup"><span data-stu-id="3105a-112">Textual description or label that is displayed when the value specified in the **Value** member is detected.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3105a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3105a-113">Remarks</span></span>

<span data-ttu-id="3105a-114">Le membre **lpLabeledByteTable** de la structure [Set](set.md) pointe vers un tableau de structures d' **ensemble** qui définissent un ou plusieurs membres **étiquette** des paires valeur octet.</span><span class="sxs-lookup"><span data-stu-id="3105a-114">The **lpLabeledByteTable** member of the [SET](set.md) structure points to an array of **SET** structures that define one or more **Label** members of the BYTE value pairs.</span></span> <span data-ttu-id="3105a-115">Ces paires sont utilisées lorsque vous souhaitez afficher une étiquette à la place d’une valeur d’octet spécifique trouvée dans le paquet de protocole.</span><span class="sxs-lookup"><span data-stu-id="3105a-115">These pairs are used when you want to display a label in place of a specific BYTE value that is found in the protocol packet.</span></span>

## <a name="requirements"></a><span data-ttu-id="3105a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3105a-116">Requirements</span></span>



| <span data-ttu-id="3105a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3105a-117">Requirement</span></span> | <span data-ttu-id="3105a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="3105a-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3105a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3105a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3105a-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3105a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3105a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3105a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3105a-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3105a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3105a-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="3105a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3105a-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3105a-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3105a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3105a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3105a-126">SET</span><span class="sxs-lookup"><span data-stu-id="3105a-126">SET</span></span>](set.md)
</dt> </dl>

 

 




