---
description: La \_ structure PROVIDOR info \_ 2 ajoute un fournisseur d’impression à la liste ordre des fournisseurs d’impression.
ms.assetid: 840523ca-22d0-460f-81fb-e0a9e2d4f5d6
title: Structure PROVIDOR_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_2
- _PROVIDOR_INFO_2A
- _PROVIDOR_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: d40f5843bf68254b92e3d814d9f308ba4f058889
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521335"
---
# <a name="providor_info_2-structure"></a><span data-ttu-id="7153b-103">\_Structure PROVIDOR info \_ 2</span><span class="sxs-lookup"><span data-stu-id="7153b-103">PROVIDOR\_INFO\_2 structure</span></span>

<span data-ttu-id="7153b-104">La structure **PROVIDOR \_ info \_ 2** ajoute un fournisseur d’impression à la liste ordre des fournisseurs d’impression.</span><span class="sxs-lookup"><span data-stu-id="7153b-104">The **PROVIDOR\_INFO\_2** structure appends a print provider to the print provider order list.</span></span>

## <a name="syntax"></a><span data-ttu-id="7153b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7153b-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_2 {
  LPTSTR pOrder;
} PROVIDOR_INFO_2, *PPROVIDOR_INFO_2;
```



## <a name="members"></a><span data-ttu-id="7153b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="7153b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7153b-107">**pOrder**</span><span class="sxs-lookup"><span data-stu-id="7153b-107">**pOrder**</span></span>
</dt> <dd>

<span data-ttu-id="7153b-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fournisseur d’impression.</span><span class="sxs-lookup"><span data-stu-id="7153b-108">Pointer to a null-terminated string that specifies the name of the print provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7153b-109">Notes</span><span class="sxs-lookup"><span data-stu-id="7153b-109">Remarks</span></span>

<span data-ttu-id="7153b-110">Cette structure est utilisée lors de l’appel de [**AddPrintProvidor**](addprintprovidor.md), niveau 2, pour ajouter le fournisseur d’impression spécifié à la fin de la liste des commandes du fournisseur d’impression.</span><span class="sxs-lookup"><span data-stu-id="7153b-110">This structure is used when calling [**AddPrintProvidor**](addprintprovidor.md), level 2, to add the specified print provider to the end of the print provider order list.</span></span> <span data-ttu-id="7153b-111">Le fournisseur est immédiatement utilisé pour le routage si l’appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="7153b-111">The provider is immediately used for routing if the call succeeds.</span></span>

## <a name="requirements"></a><span data-ttu-id="7153b-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7153b-112">Requirements</span></span>



| <span data-ttu-id="7153b-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7153b-113">Requirement</span></span> | <span data-ttu-id="7153b-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="7153b-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7153b-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7153b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7153b-116">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7153b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7153b-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7153b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7153b-118">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7153b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7153b-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="7153b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7153b-120"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7153b-120"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="7153b-121">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="7153b-121">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7153b-122">**\_ PROVIDOR \_ info \_ 2S** (Unicode) et **\_ PROVIDOR \_ info \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="7153b-122">**\_PROVIDOR\_INFO\_2W** (Unicode) and **\_PROVIDOR\_INFO\_2A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="7153b-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7153b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7153b-124">Impression</span><span class="sxs-lookup"><span data-stu-id="7153b-124">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7153b-125">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="7153b-125">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="7153b-126">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="7153b-126">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




