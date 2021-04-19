---
description: La \_ structure Printer info \_ 3 spécifie les informations de sécurité de l’imprimante.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: Structure PRINTER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aad24e56d43f6fadd3da3f627b2399249a7ff8a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521887"
---
# <a name="printer_info_3-structure"></a><span data-ttu-id="c84e1-103">Structure de l’imprimante \_ info \_ 3</span><span class="sxs-lookup"><span data-stu-id="c84e1-103">PRINTER\_INFO\_3 structure</span></span>

<span data-ttu-id="c84e1-104">La structure **Printer \_ info \_ 3** spécifie les informations de sécurité de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c84e1-104">The **PRINTER\_INFO\_3** structure specifies printer security information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c84e1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c84e1-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="c84e1-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c84e1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c84e1-107">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c84e1-107">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="c84e1-108">Pointeur vers une structure de [**\_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) qui spécifie les informations de sécurité d’une imprimante.</span><span class="sxs-lookup"><span data-stu-id="c84e1-108">Pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that specifies a printer's security information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c84e1-109">Notes</span><span class="sxs-lookup"><span data-stu-id="c84e1-109">Remarks</span></span>

<span data-ttu-id="c84e1-110">La structure **Printer \_ info \_ 3** permet à une application d’obtenir et de définir le descripteur de sécurité d’une imprimante.</span><span class="sxs-lookup"><span data-stu-id="c84e1-110">The **PRINTER\_INFO\_3** structure lets an application get and set a printer's security descriptor.</span></span> <span data-ttu-id="c84e1-111">L’appelant peut le faire même s’il ne dispose pas d’autorisations d’imprimante spécifiques, à condition qu’il dispose des droits standard décrits dans [**SetPrinter**](setprinter.md) et [**GetPrinter**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="c84e1-111">The caller may do so even if it lacks specific printer permissions, as long as it has the standard rights described in [**SetPrinter**](setprinter.md) and [**GetPrinter**](getprinter.md).</span></span> <span data-ttu-id="c84e1-112">Par conséquent, une application peut refuser temporairement tout accès à une imprimante, tout en autorisant le propriétaire de l’imprimante à accéder à la liste de contrôle d’accès discrétionnaire de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c84e1-112">Thus, an application may temporarily deny all access to a printer, while allowing the owner of the printer to have access to the printer's discretionary ACL.</span></span>

## <a name="requirements"></a><span data-ttu-id="c84e1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c84e1-113">Requirements</span></span>



| <span data-ttu-id="c84e1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c84e1-114">Requirement</span></span> | <span data-ttu-id="c84e1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c84e1-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c84e1-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c84e1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c84e1-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c84e1-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c84e1-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c84e1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c84e1-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c84e1-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c84e1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="c84e1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="c84e1-121"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c84e1-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c84e1-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c84e1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84e1-123">Impression</span><span class="sxs-lookup"><span data-stu-id="c84e1-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c84e1-124">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="c84e1-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="c84e1-125">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="c84e1-125">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="c84e1-126">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="c84e1-126">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="c84e1-127">**\_Infos sur l’imprimante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c84e1-127">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="c84e1-128">**\_Infos sur l’imprimante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c84e1-128">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="c84e1-129">**\_Infos sur l’imprimante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="c84e1-129">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="c84e1-130">**descripteur de sécurité \_**</span><span class="sxs-lookup"><span data-stu-id="c84e1-130">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

