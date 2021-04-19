---
description: La \_ structure info 9 de l’imprimante \_ spécifie les paramètres par défaut de l’imprimante par utilisateur.
ms.assetid: 8bafb995-f31c-46e3-a950-45e240c678aa
title: Structure PRINTER_INFO_9 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_9
- _PRINTER_INFO_9A
- _PRINTER_INFO_9W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c0ae3c099da17d7fc437a67035d8da2cd00136bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545855"
---
# <a name="printer_info_9-structure"></a><span data-ttu-id="89749-103">\_Structure info 9 de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="89749-103">PRINTER\_INFO\_9 structure</span></span>

<span data-ttu-id="89749-104">La **structure \_ info \_ 9** de l’imprimante spécifie les paramètres par défaut de l’imprimante par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="89749-104">The **PRINTER\_INFO\_9** structure specifies the per-user default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="89749-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89749-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_9 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_9, *PPRINTER_INFO_9;
```



## <a name="members"></a><span data-ttu-id="89749-106">Membres</span><span class="sxs-lookup"><span data-stu-id="89749-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="89749-107">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="89749-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="89749-108">Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui définit les données d’imprimante par défaut par utilisateur, telles que l’orientation du papier et la résolution.</span><span class="sxs-lookup"><span data-stu-id="89749-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the per-user default printer data such as the paper orientation and the resolution.</span></span> <span data-ttu-id="89749-109">Le **DEVMODE** est stocké dans le registre de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="89749-109">The **DEVMODE** is stored in the user's registry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89749-110">Notes</span><span class="sxs-lookup"><span data-stu-id="89749-110">Remarks</span></span>

<span data-ttu-id="89749-111">Les valeurs par défaut par utilisateur affectent uniquement un utilisateur particulier ou toute personne qui utilise le profil.</span><span class="sxs-lookup"><span data-stu-id="89749-111">The per-user defaults will affect only a particular user or anyone who uses the profile.</span></span> <span data-ttu-id="89749-112">En revanche, les valeurs par défaut globales sont définies par l’administrateur d’une imprimante qui peut être utilisée par n’importe qui.</span><span class="sxs-lookup"><span data-stu-id="89749-112">In contrast, the global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="89749-113">Pour les valeurs par défaut globales, utilisez [**Printer \_ info \_ 8**](printer-info-8.md).</span><span class="sxs-lookup"><span data-stu-id="89749-113">For global defaults, use [**PRINTER\_INFO\_8**](printer-info-8.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="89749-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89749-114">Requirements</span></span>



| <span data-ttu-id="89749-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89749-115">Requirement</span></span> | <span data-ttu-id="89749-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="89749-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89749-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89749-117">Minimum supported client</span></span><br/> | <span data-ttu-id="89749-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89749-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="89749-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="89749-119">Minimum supported server</span></span><br/> | <span data-ttu-id="89749-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="89749-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="89749-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="89749-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="89749-122"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89749-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="89749-123">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="89749-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="89749-124">**\_ \_ Infos sur \_ l’imprimante 9W** (Unicode) et **\_ \_ informations sur l’imprimante \_ 9A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="89749-124">**\_PRINTER\_INFO\_9W** (Unicode) and **\_PRINTER\_INFO\_9A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="89749-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89749-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89749-126">Impression</span><span class="sxs-lookup"><span data-stu-id="89749-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="89749-127">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="89749-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="89749-128">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="89749-128">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="89749-129">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="89749-129">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="89749-130">**\_Infos sur l’imprimante \_ 8**</span><span class="sxs-lookup"><span data-stu-id="89749-130">**PRINTER\_INFO\_8**</span></span>](printer-info-8.md)
</dt> </dl>

 

 




