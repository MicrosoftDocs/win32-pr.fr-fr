---
description: La \_ structure PROVIDOR info \_ 1 identifie un fournisseur d’impression.
ms.assetid: 0eff115a-b3d2-4c8f-b820-46e7f62dd295
title: Structure PROVIDOR_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROVIDOR_INFO_1
- _PROVIDOR_INFO_1A
- _PROVIDOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2eabc00009b76247af71b06ea877ca0bf738c1d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319970"
---
# <a name="providor_info_1-structure"></a><span data-ttu-id="4892a-103">PROVIDOR \_ information \_ 1 (structure)</span><span class="sxs-lookup"><span data-stu-id="4892a-103">PROVIDOR\_INFO\_1 structure</span></span>

<span data-ttu-id="4892a-104">La structure **PROVIDOR \_ info \_ 1** identifie un fournisseur d’impression.</span><span class="sxs-lookup"><span data-stu-id="4892a-104">The **PROVIDOR\_INFO\_1** structure identifies a print provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="4892a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4892a-105">Syntax</span></span>


```C++
typedef struct _PROVIDOR_INFO_1 {
  LPTSTR pName;
  LPTSTR pEnvironment;
  LPTSTR pDLLName;
} PROVIDOR_INFO_1, *PPROVIDOR_INFO_1;
```



## <a name="members"></a><span data-ttu-id="4892a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4892a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4892a-107">**pName**</span><span class="sxs-lookup"><span data-stu-id="4892a-107">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="4892a-108">Pointeur vers une chaîne se terminant par un caractère null qui est le nom du fournisseur d’impression.</span><span class="sxs-lookup"><span data-stu-id="4892a-108">Pointer to a null-terminated string that is the name of the print provider.</span></span>

</dd> <dt>

<span data-ttu-id="4892a-109">**pEnvironment**</span><span class="sxs-lookup"><span data-stu-id="4892a-109">**pEnvironment**</span></span>
</dt> <dd>

<span data-ttu-id="4892a-110">Pointeur vers une chaîne d’environnement se terminant par un caractère null qui spécifie l’environnement dans lequel la bibliothèque de liens dynamiques (DLL) du fournisseur est conçue pour s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="4892a-110">Pointer to a null-terminated environment string specifying the environment the provider dynamic-link library (DLL) is designed to run in.</span></span>

</dd> <dt>

<span data-ttu-id="4892a-111">**pDLLName**</span><span class="sxs-lookup"><span data-stu-id="4892a-111">**pDLLName**</span></span>
</dt> <dd>

<span data-ttu-id="4892a-112">Pointeur vers une chaîne terminée par le caractère null qui est le nom du fournisseur. dll.</span><span class="sxs-lookup"><span data-stu-id="4892a-112">Pointer to a null-terminated string that is the name of the provider .dll.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4892a-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4892a-113">Requirements</span></span>



| <span data-ttu-id="4892a-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4892a-114">Requirement</span></span> | <span data-ttu-id="4892a-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4892a-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4892a-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4892a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4892a-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4892a-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4892a-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4892a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4892a-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4892a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4892a-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="4892a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4892a-121"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4892a-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4892a-122">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="4892a-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4892a-123">**\_ PROVIDOR \_ info \_ 1s** (Unicode) et **\_ PROVIDOR \_ info \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4892a-123">**\_PROVIDOR\_INFO\_1W** (Unicode) and **\_PROVIDOR\_INFO\_1A** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="4892a-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4892a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4892a-125">Impression</span><span class="sxs-lookup"><span data-stu-id="4892a-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4892a-126">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="4892a-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="4892a-127">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="4892a-127">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




