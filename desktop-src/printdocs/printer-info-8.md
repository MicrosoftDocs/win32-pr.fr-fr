---
description: La \_ structure d’informations sur l’imprimante \_ 8 spécifie les paramètres globaux de l’imprimante par défaut.
ms.assetid: 98f26a45-5302-4358-bed6-691d9bc37554
title: Structure PRINTER_INFO_8 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_8
- _PRINTER_INFO_8A
- _PRINTER_INFO_8W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e17780dc2f39dc3041e690de1ef7b5728c8743e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868341"
---
# <a name="printer_info_8-structure"></a><span data-ttu-id="11835-103">\_Structure des informations sur l’imprimante \_ 8</span><span class="sxs-lookup"><span data-stu-id="11835-103">PRINTER\_INFO\_8 structure</span></span>

<span data-ttu-id="11835-104">La structure d' **\_ informations sur l’imprimante \_ 8** spécifie les paramètres globaux de l’imprimante par défaut.</span><span class="sxs-lookup"><span data-stu-id="11835-104">The **PRINTER\_INFO\_8** structure specifies the global default printer settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="11835-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11835-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_8 {
  LPDEVMODE pDevMode;
} PRINTER_INFO_8, *PPRINTER_INFO_8;
```



## <a name="members"></a><span data-ttu-id="11835-106">Membres</span><span class="sxs-lookup"><span data-stu-id="11835-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="11835-107">**pDevMode**</span><span class="sxs-lookup"><span data-stu-id="11835-107">**pDevMode**</span></span>
</dt> <dd>

<span data-ttu-id="11835-108">Pointeur vers une structure [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) qui définit les données globales de l’imprimante par défaut, telles que l’orientation du papier et la résolution.</span><span class="sxs-lookup"><span data-stu-id="11835-108">A pointer to a [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) structure that defines the global default printer data such as the paper orientation and the resolution.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="11835-109">Notes</span><span class="sxs-lookup"><span data-stu-id="11835-109">Remarks</span></span>

<span data-ttu-id="11835-110">Les paramètres globaux par défaut sont définis par l’administrateur d’une imprimante qui peut être utilisée par n’importe qui.</span><span class="sxs-lookup"><span data-stu-id="11835-110">The global defaults are set by the administrator of a printer that can be used by anyone.</span></span> <span data-ttu-id="11835-111">En revanche, les valeurs par défaut par utilisateur affectent un utilisateur particulier ou toute autre personne qui utilise le profil.</span><span class="sxs-lookup"><span data-stu-id="11835-111">In contrast, the per-user defaults will affect a particular user or anyone else who uses the profile.</span></span> <span data-ttu-id="11835-112">Pour les valeurs par défaut par utilisateur, utilisez [**Printer \_ info \_ 9**](printer-info-9.md).</span><span class="sxs-lookup"><span data-stu-id="11835-112">For per-user defaults, use [**PRINTER\_INFO\_9**](printer-info-9.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11835-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11835-113">Requirements</span></span>



| <span data-ttu-id="11835-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11835-114">Requirement</span></span> | <span data-ttu-id="11835-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="11835-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11835-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11835-116">Minimum supported client</span></span><br/> | <span data-ttu-id="11835-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11835-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="11835-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11835-118">Minimum supported server</span></span><br/> | <span data-ttu-id="11835-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="11835-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="11835-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="11835-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="11835-121"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11835-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="11835-122">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="11835-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="11835-123">**\_ \_ Infos sur \_ l’imprimante 8W** (Unicode) et **\_ \_ informations sur l’imprimante \_ 8A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="11835-123">**\_PRINTER\_INFO\_8W** (Unicode) and **\_PRINTER\_INFO\_8A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="11835-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11835-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11835-125">Impression</span><span class="sxs-lookup"><span data-stu-id="11835-125">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="11835-126">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="11835-126">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="11835-127">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="11835-127">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="11835-128">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="11835-128">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="11835-129">**\_Infos sur l’imprimante \_ 9**</span><span class="sxs-lookup"><span data-stu-id="11835-129">**PRINTER\_INFO\_9**</span></span>](printer-info-9.md)
</dt> </dl>

 

 




