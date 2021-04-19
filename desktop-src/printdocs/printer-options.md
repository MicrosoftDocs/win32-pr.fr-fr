---
description: Représente les options de l’imprimante.
ms.assetid: 7cc3d10c-8bc2-4899-b083-63d802ee16e7
title: Structure PRINTER_OPTIONS (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_OPTIONS
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 37c45277f0a7e30bc94b2d23ffa27de0092a7164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527532"
---
# <a name="printer_options-structure"></a><span data-ttu-id="75370-103">Structure des options de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="75370-103">PRINTER\_OPTIONS structure</span></span>

<span data-ttu-id="75370-104">Représente les options de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="75370-104">Represents printer options.</span></span>

## <a name="syntax"></a><span data-ttu-id="75370-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75370-105">Syntax</span></span>


```C++
typedef struct _PRINTER_OPTIONS {
  UINT  cbSize;
  DWORD dwFlags;
} PRINTER_OPTIONS, *PPRINTER_OPTIONS;
```



## <a name="members"></a><span data-ttu-id="75370-106">Membres</span><span class="sxs-lookup"><span data-stu-id="75370-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="75370-107">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="75370-107">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="75370-108">Taille de la structure **des \_ options** de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="75370-108">The size of the **PRINTER\_OPTIONS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="75370-109">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="75370-109">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="75370-110">Ensemble d' [**indicateurs d' \_ option \_ d’imprimante**](printer-option-flags.md) qui spécifie comment le handle d’une imprimante retournée par [**OpenPrinter2**](openprinter2.md) sera utilisé par d’autres fonctions.</span><span class="sxs-lookup"><span data-stu-id="75370-110">A set of [**PRINTER\_OPTION\_FLAGS**](printer-option-flags.md) that specifies how the handle to a printer returned by [**OpenPrinter2**](openprinter2.md) will be used by other functions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75370-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75370-111">Requirements</span></span>



| <span data-ttu-id="75370-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75370-112">Requirement</span></span> | <span data-ttu-id="75370-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="75370-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75370-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75370-114">Minimum supported client</span></span><br/> | <span data-ttu-id="75370-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75370-115">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="75370-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75370-116">Minimum supported server</span></span><br/> | <span data-ttu-id="75370-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75370-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="75370-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="75370-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="75370-119"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75370-119"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75370-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75370-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75370-121">Impression</span><span class="sxs-lookup"><span data-stu-id="75370-121">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="75370-122">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="75370-122">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="75370-123">**OpenPrinter2**</span><span class="sxs-lookup"><span data-stu-id="75370-123">**OpenPrinter2**</span></span>](openprinter2.md)
</dt> <dt>

[<span data-ttu-id="75370-124">**\_indicateurs d’option d’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="75370-124">**PRINTER\_OPTION\_FLAGS**</span></span>](printer-option-flags.md)
</dt> </dl>

 

 




