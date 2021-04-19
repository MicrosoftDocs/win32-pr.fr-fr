---
description: La \_ structure d’informations sur le port \_ 1 identifie un port d’imprimante pris en charge.
ms.assetid: e474fe9c-e554-406a-a5bf-de07f9a72b32
title: Structure PORT_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PORT_INFO_1
- _PORT_INFO_1A
- _PORT_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d64e7dfa29cbe6b3f7efd3aaa0076851aea0311b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529824"
---
# <a name="port_info_1-structure"></a><span data-ttu-id="62f97-103">Structure des informations de PORT \_ \_ 1</span><span class="sxs-lookup"><span data-stu-id="62f97-103">PORT\_INFO\_1 structure</span></span>

<span data-ttu-id="62f97-104">La structure d' **\_ informations sur le port \_ 1** identifie un port d’imprimante pris en charge.</span><span class="sxs-lookup"><span data-stu-id="62f97-104">The **PORT\_INFO\_1** structure identifies a supported printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="62f97-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62f97-105">Syntax</span></span>


```C++
typedef struct _PORT_INFO_1 {
  LPTSTR pName;
} PORT_INFO_1, *PPORT_INFO_1;
```



## <a name="members"></a><span data-ttu-id="62f97-106">Membres</span><span class="sxs-lookup"><span data-stu-id="62f97-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="62f97-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="62f97-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="62f97-108">Pointeur vers une chaîne se terminant par un caractère null qui identifie un port imprimante pris en charge (par exemple, « LPT1 : »).</span><span class="sxs-lookup"><span data-stu-id="62f97-108">Pointer to a null-terminated string that identifies a supported printer port (for example, "LPT1:").</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="62f97-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="62f97-109">Requirements</span></span>



| <span data-ttu-id="62f97-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="62f97-110">Requirement</span></span> | <span data-ttu-id="62f97-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="62f97-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62f97-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62f97-112">Minimum supported client</span></span><br/> | <span data-ttu-id="62f97-113">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62f97-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="62f97-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="62f97-114">Minimum supported server</span></span><br/> | <span data-ttu-id="62f97-115">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="62f97-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="62f97-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="62f97-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="62f97-117"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62f97-117"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="62f97-118">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="62f97-118">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="62f97-119">**\_ \_ Informations sur \_ le port 1s** (Unicode) et **\_ \_ informations sur le port \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="62f97-119">**\_PORT\_INFO\_1W** (Unicode) and **\_PORT\_INFO\_1A** (ANSI)</span></span><br/>                                 |



## <a name="see-also"></a><span data-ttu-id="62f97-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62f97-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62f97-121">Impression</span><span class="sxs-lookup"><span data-stu-id="62f97-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="62f97-122">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="62f97-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="62f97-123">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="62f97-123">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




