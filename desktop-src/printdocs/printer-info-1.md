---
description: La \_ structure infos imprimante \_ 1 spécifie des informations générales sur l’imprimante.
ms.assetid: 0b0e2d0e-2625-4cab-a8f9-536185479443
title: Structure PRINTER_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_1
- _PRINTER_INFO_1A
- _PRINTER_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: cbeff42a9125331c45ffd8bbbee5758fd864648c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519372"
---
# <a name="printer_info_1-structure"></a><span data-ttu-id="9ff95-103">\_Structure infos imprimante \_ 1</span><span class="sxs-lookup"><span data-stu-id="9ff95-103">PRINTER\_INFO\_1 structure</span></span>

<span data-ttu-id="9ff95-104">La **structure \_ infos imprimante \_ 1** spécifie des informations générales sur l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="9ff95-104">The **PRINTER\_INFO\_1** structure specifies general printer information.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ff95-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9ff95-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_1 {
  DWORD  Flags;
  LPTSTR pDescription;
  LPTSTR pName;
  LPTSTR pComment;
} PRINTER_INFO_1, *PPRINTER_INFO_1;
```



## <a name="members"></a><span data-ttu-id="9ff95-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9ff95-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9ff95-107">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="9ff95-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="9ff95-108">Spécifie des informations sur les données retournées.</span><span class="sxs-lookup"><span data-stu-id="9ff95-108">Specifies information about the returned data.</span></span> <span data-ttu-id="9ff95-109">Voici les valeurs de ce membre.</span><span class="sxs-lookup"><span data-stu-id="9ff95-109">Following are the values for this member.</span></span>



| <span data-ttu-id="9ff95-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ff95-110">Value</span></span>                    | <span data-ttu-id="9ff95-111">Signification</span><span class="sxs-lookup"><span data-stu-id="9ff95-111">Meaning</span></span>                                                                                                                                                                                                                                                   |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff95-112">\_étendre l’énumération de l’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="9ff95-112">PRINTER\_ENUM\_EXPAND</span></span>    | <span data-ttu-id="9ff95-113">Un fournisseur d’impression peut définir cet indicateur comme indicateur pour une application appelante afin d’énumérer plus précisément cet objet si l’extension par défaut est activée.</span><span class="sxs-lookup"><span data-stu-id="9ff95-113">A print provider can set this flag as a hint to a calling application to enumerate this object further if default expansion is enabled.</span></span> <span data-ttu-id="9ff95-114">Par exemple, lorsque des domaines sont énumérés, un fournisseur d’impression peut indiquer le domaine de l’utilisateur en définissant cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="9ff95-114">For example, when domains are enumerated, a print provider might indicate the user's domain by setting this flag.</span></span> |
| <span data-ttu-id="9ff95-115">\_conteneur d’énumération d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="9ff95-115">PRINTER\_ENUM\_CONTAINER</span></span> | <span data-ttu-id="9ff95-116">Si cet indicateur est défini, l’objet Printer peut contenir des objets énumérables.</span><span class="sxs-lookup"><span data-stu-id="9ff95-116">If this flag is set, the printer object may contain enumerable objects.</span></span> <span data-ttu-id="9ff95-117">Par exemple, l’objet peut être un serveur d’impression qui contient des imprimantes.</span><span class="sxs-lookup"><span data-stu-id="9ff95-117">For example, the object may be a print server that contains printers.</span></span>                                                                                                             |
| <span data-ttu-id="9ff95-118">\_ICON1 d’énumération d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="9ff95-118">PRINTER\_ENUM\_ICON1</span></span>     | <span data-ttu-id="9ff95-119">Indique que, le cas échéant, une application doit afficher une icône identifiant l’objet comme un nom de réseau de niveau supérieur, tel que réseau Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9ff95-119">Indicates that, where appropriate, an application should display an icon identifying the object as a top-level network name, such as Microsoft Windows Network.</span></span>                                                                                           |
| <span data-ttu-id="9ff95-120">\_ICON2 d’énumération d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="9ff95-120">PRINTER\_ENUM\_ICON2</span></span>     | <span data-ttu-id="9ff95-121">Indique que, le cas échéant, une application doit afficher une icône qui identifie l’objet en tant que domaine réseau.</span><span class="sxs-lookup"><span data-stu-id="9ff95-121">Indicates that, where appropriate, an application should display an icon that identifies the object as a network domain.</span></span>                                                                                                                                  |
| <span data-ttu-id="9ff95-122">\_ICON3 d’énumération d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="9ff95-122">PRINTER\_ENUM\_ICON3</span></span>     | <span data-ttu-id="9ff95-123">Indique que, le cas échéant, une application doit afficher une icône qui identifie l’objet en tant que serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="9ff95-123">Indicates that, where appropriate, an application should display an icon that identifies the object as a print server.</span></span>                                                                                                                                    |
| <span data-ttu-id="9ff95-124">\_ICON4 d’énumération d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="9ff95-124">PRINTER\_ENUM\_ICON4</span></span>     | <span data-ttu-id="9ff95-125">Réservé.</span><span class="sxs-lookup"><span data-stu-id="9ff95-125">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9ff95-126">\_ICON5 d’énumération d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="9ff95-126">PRINTER\_ENUM\_ICON5</span></span>     | <span data-ttu-id="9ff95-127">Réservé.</span><span class="sxs-lookup"><span data-stu-id="9ff95-127">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9ff95-128">\_ICON6 d’énumération d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="9ff95-128">PRINTER\_ENUM\_ICON6</span></span>     | <span data-ttu-id="9ff95-129">Réservé.</span><span class="sxs-lookup"><span data-stu-id="9ff95-129">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9ff95-130">\_ICON7 d’énumération d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="9ff95-130">PRINTER\_ENUM\_ICON7</span></span>     | <span data-ttu-id="9ff95-131">Réservé.</span><span class="sxs-lookup"><span data-stu-id="9ff95-131">Reserved.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="9ff95-132">\_ICON8 d’énumération d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="9ff95-132">PRINTER\_ENUM\_ICON8</span></span>     | <span data-ttu-id="9ff95-133">Indique que, le cas échéant, une application doit afficher une icône qui identifie l’objet en tant qu’imprimante.</span><span class="sxs-lookup"><span data-stu-id="9ff95-133">Indicates that, where appropriate, an application should display an icon that identifies the object as a printer.</span></span>                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="9ff95-134">**pDescription**</span><span class="sxs-lookup"><span data-stu-id="9ff95-134">**pDescription**</span></span>
</dt> <dd>

<span data-ttu-id="9ff95-135">Pointeur vers une chaîne terminée par le caractère null qui décrit le contenu de la structure.</span><span class="sxs-lookup"><span data-stu-id="9ff95-135">Pointer to a null-terminated string that describes the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="9ff95-136">**pName**</span><span class="sxs-lookup"><span data-stu-id="9ff95-136">**pName**</span></span>
</dt> <dd>

<span data-ttu-id="9ff95-137">Pointeur vers une chaîne se terminant par un caractère null qui nomme le contenu de la structure.</span><span class="sxs-lookup"><span data-stu-id="9ff95-137">Pointer to a null-terminated string that names the contents of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="9ff95-138">**pComment**</span><span class="sxs-lookup"><span data-stu-id="9ff95-138">**pComment**</span></span>
</dt> <dd>

<span data-ttu-id="9ff95-139">Pointeur vers une chaîne terminée par le caractère null qui contient des données supplémentaires qui décrivent la structure.</span><span class="sxs-lookup"><span data-stu-id="9ff95-139">Pointer to a null-terminated string that contains additional data describing the structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9ff95-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ff95-140">Requirements</span></span>



| <span data-ttu-id="9ff95-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ff95-141">Requirement</span></span> | <span data-ttu-id="9ff95-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ff95-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ff95-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ff95-143">Minimum supported client</span></span><br/> | <span data-ttu-id="9ff95-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ff95-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9ff95-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9ff95-145">Minimum supported server</span></span><br/> | <span data-ttu-id="9ff95-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9ff95-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9ff95-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="9ff95-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ff95-148"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9ff95-148"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9ff95-149">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="9ff95-149">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9ff95-150">**\_ \_ Infos imprimante \_ 1s** (Unicode) et **\_ \_ infos imprimante \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9ff95-150">**\_PRINTER\_INFO\_1W** (Unicode) and **\_PRINTER\_INFO\_1A** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="9ff95-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ff95-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ff95-152">Impression</span><span class="sxs-lookup"><span data-stu-id="9ff95-152">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9ff95-153">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="9ff95-153">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9ff95-154">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="9ff95-154">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="9ff95-155">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="9ff95-155">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="9ff95-156">**\_Infos sur l’imprimante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="9ff95-156">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="9ff95-157">**\_Infos sur l’imprimante \_ 3**</span><span class="sxs-lookup"><span data-stu-id="9ff95-157">**PRINTER\_INFO\_3**</span></span>](printer-info-3.md)
</dt> <dt>

[<span data-ttu-id="9ff95-158">**\_Infos sur l’imprimante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="9ff95-158">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> </dl>

 

 




