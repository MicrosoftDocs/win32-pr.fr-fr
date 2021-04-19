---
description: Représente des informations sur les fonctionnalités de l’imprimante.
ms.assetid: 70120739-a4e0-4b87-ac7a-40a42fb509ee
title: Structure PRINTPROCESSOR_CAPS_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_2
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 1847ffa1912a8638476ce80dfbdb71c40fc376d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530677"
---
# <a name="printprocessor_caps_2-structure"></a><span data-ttu-id="e3e1d-103">\_Structure PRINTPROCESSOR Cap \_ 2</span><span class="sxs-lookup"><span data-stu-id="e3e1d-103">PRINTPROCESSOR\_CAPS\_2 structure</span></span>

<span data-ttu-id="e3e1d-104">Représente des informations sur les fonctionnalités de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-104">Represents printer capability information.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e1d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3e1d-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_2 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
  DWORD dwNupDirectionCaps;
  DWORD dwNupBorderCaps;
  DWORD dwBookletHandlingCaps;
  DWORD dwDuplexHandlingCaps;
  DWORD dwScalingCaps;
} PRINTPROCESSOR_CAPS_2, *PPRINTPROCESSOR_CAPS_2;
```



## <a name="members"></a><span data-ttu-id="e3e1d-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e3e1d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e3e1d-107">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="e3e1d-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="e3e1d-108">Valeur qui indique le numéro de version de la structure.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-108">A value that indicates the structure's version number.</span></span>

</dd> <dt>

<span data-ttu-id="e3e1d-109">**dwNupOptions**</span><span class="sxs-lookup"><span data-stu-id="e3e1d-109">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="e3e1d-110">Masque de bits représentant les différents nombres de pages de document que l’imprimante peut imprimer sur un seul côté d’une feuille physique.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-110">A bit mask representing the various numbers of document pages the printer can print on a single side of a physical sheet.</span></span> <span data-ttu-id="e3e1d-111">Le bit le moins significatif représente une page de document par côté, le bit suivant représente 2 pages de document par côté, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-111">The least significant bit represents one document page per side, the next bit represents 2 document pages per side, and so on.</span></span> <span data-ttu-id="e3e1d-112">Par exemple, 0x0000810B indique que l’imprimante prend en charge les pages de documents 1, 2, 4, 9 et 16 par côté physique.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-112">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical side.</span></span>

</dd> <dt>

<span data-ttu-id="e3e1d-113">**dwPageOrderFlags**</span><span class="sxs-lookup"><span data-stu-id="e3e1d-113">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="e3e1d-114">Valeur d’indicateur qui indique l’ordre dans lequel les pages seront imprimées.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-114">A flag value that indicates the order in which pages will be printed.</span></span> <span data-ttu-id="e3e1d-115">Il peut s’agir d’une **\_ impression normale**, d’une **\_ impression inversée** ou d’un **livret \_ imprimé**.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-115">It can be **NORMAL\_PRINT**, **REVERSE\_PRINT**, or **BOOKLET\_PRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="e3e1d-116">**dwNumberOfCopies**</span><span class="sxs-lookup"><span data-stu-id="e3e1d-116">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="e3e1d-117">Nombre maximal de copies que l’imprimante peut gérer.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-117">The maximum number of copies the printer can handle.</span></span>

</dd> <dt>

<span data-ttu-id="e3e1d-118">**dwNupDirectionCaps**</span><span class="sxs-lookup"><span data-stu-id="e3e1d-118">**dwNupDirectionCaps**</span></span>
</dt> <dd>

<span data-ttu-id="e3e1d-119">Les modèles disponibles lorsque plusieurs pages de document sont imprimées sur le même côté d’une feuille de papier.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-119">The available patterns when multiple document pages are printed on the same side of a sheet of paper.</span></span> <span data-ttu-id="e3e1d-120">Les indicateurs possibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e3e1d-120">The possible flags are the following:</span></span>



| <span data-ttu-id="e3e1d-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3e1d-121">Value</span></span>                     | <span data-ttu-id="e3e1d-122">Signification</span><span class="sxs-lookup"><span data-stu-id="e3e1d-122">Meaning</span></span>                                                                                             |
|---------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e1d-123">PPCAPS \_ \_ vers la droite, puis \_ vers le PG.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-123">PPCAPS\_RIGHT\_THEN\_DOWN</span></span> | <span data-ttu-id="e3e1d-124">Les pages apparaissent dans des lignes de droite à gauche, chaque ligne suivante sous son prédécesseur.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-124">Pages appear in rows from right to left, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="e3e1d-125">PPCAPS \_ vers le \_ droite, puis vers la \_ droite</span><span class="sxs-lookup"><span data-stu-id="e3e1d-125">PPCAPS\_DOWN\_THEN\_RIGHT</span></span> | <span data-ttu-id="e3e1d-126">Les pages apparaissent dans des colonnes de haut en bas, chaque colonne suivante à droite de son prédécesseur.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-126">Pages appear in columns from top to bottom, each subsequent column to the right of its predecessor.</span></span> |
| <span data-ttu-id="e3e1d-127">PPCAPS à gauche et à \_ droite \_ \_</span><span class="sxs-lookup"><span data-stu-id="e3e1d-127">PPCAPS\_LEFT\_THEN\_DOWN</span></span>  | <span data-ttu-id="e3e1d-128">Les pages apparaissent dans des lignes de gauche à droite, chaque ligne suivante sous son prédécesseur.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-128">Pages appear in rows from left to right, each subsequent row below its predecessor.</span></span>                 |
| <span data-ttu-id="e3e1d-129">PPCAPS \_ \_ , puis \_ gauche</span><span class="sxs-lookup"><span data-stu-id="e3e1d-129">PPCAPS\_DOWN\_THEN\_LEFT</span></span>  | <span data-ttu-id="e3e1d-130">Les pages apparaissent dans des colonnes de haut en bas, chaque colonne suivante à gauche de son prédécesseur.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-130">Pages appear in columns from top to bottom, each subsequent column to the left of its predecessor.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="e3e1d-131">**dwNupBorderCaps**</span><span class="sxs-lookup"><span data-stu-id="e3e1d-131">**dwNupBorderCaps**</span></span>
</dt> <dd>

<span data-ttu-id="e3e1d-132">Peut être uniquement imprimé PPCAPS \_ Border \_ , ce qui indique que lorsque plusieurs pages de document sont imprimées sur un seul côté d’une feuille physique, l’imprimante peut être informée de l’impression ou non d’une bordure autour de la zone imageable de chaque page de document.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-132">Can be only PPCAPS\_BORDER\_PRINT, indicating that, when multiple document pages are being printed on a single side of a physical sheet, the printer can be told whether or not to print a border around the imageable area of each document page.</span></span>

</dd> <dt>

<span data-ttu-id="e3e1d-133">**dwBookletHandlingCaps**</span><span class="sxs-lookup"><span data-stu-id="e3e1d-133">**dwBookletHandlingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="e3e1d-134">Peut uniquement être \_ un bord de livret PPCAPS \_ , indiquant que l’imprimante peut imprimer le style de livret.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-134">Can only be PPCAPS\_BOOKLET\_EDGE, indicating that the printer can print booklet style.</span></span>

<span data-ttu-id="e3e1d-135"></dd> <dt>**dwDuplexHandlingCaps**</dt> </span><span class="sxs-lookup"><span data-stu-id="e3e1d-135"></dd> <dt>**dwDuplexHandlingCaps**</dt> </span></span><dd> 

| <span data-ttu-id="e3e1d-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3e1d-136">Value</span></span>                                         | <span data-ttu-id="e3e1d-137">Signification</span><span class="sxs-lookup"><span data-stu-id="e3e1d-137">Meaning</span></span>                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e1d-138">PPCAPS \_ les pages inversées \_ \_ pour le \_ \_ duplex inversé</span><span class="sxs-lookup"><span data-stu-id="e3e1d-138">PPCAPS\_REVERSE\_PAGES\_FOR\_REVERSE\_DUPLEX</span></span>  | <span data-ttu-id="e3e1d-139">Lors de l’impression dans l’ordre inverse et le duplexage, le processeur peut imprimer l’ordre de chaque paire de pages. par conséquent, au lieu d’imprimer dans l’ordre 4, 3, 2, 1, il s’imprimera dans l’ordre 3, 4, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-139">When printing in reverse order and duplexing, the processor can print swap the order of each pair of pages, so instead of printing in order 4,3,2,1, they will print in the order 3,4,1,2.</span></span>                                                                                                       |
| <span data-ttu-id="e3e1d-140">PPCAPS ne pas \_ \_ Envoyer \_ \_ de pages supplémentaires \_ pour le \_ duplex</span><span class="sxs-lookup"><span data-stu-id="e3e1d-140">PPCAPS\_DONT\_SEND\_EXTRA\_PAGES\_FOR\_DUPLEX</span></span> | <span data-ttu-id="e3e1d-141">Lors du duplexage, le processeur d’impression peut être invité à ne pas envoyer de page supplémentaire lorsqu’il existe un nombre impair de pages de document.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-141">When duplexing, the Print Processor can be told not to send an extra page when there is an odd number of document pages.</span></span> <span data-ttu-id="e3e1d-142">Le processeur honorera la valeur le mieux possible, mais dans les cas où la prévention d’une page vierge supplémentaire entraînerait une sortie incorrecte, les pages supplémentaires seront peut-être encore envoyées.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-142">The processor will honor the value as best as it can, but in cases where preventing an extra blank page would cause improper output, the extra pages may still be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e3e1d-143">**dwScalingCaps**</span><span class="sxs-lookup"><span data-stu-id="e3e1d-143">**dwScalingCaps**</span></span>
</dt> <dd>

<span data-ttu-id="e3e1d-144">Peut uniquement être PPCAPS de mise à l’échelle \_ carrée \_ , ce qui indique que l’imprimante peut mettre à l’échelle l’image de page.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-144">Can only be PPCAPS\_SQUARE\_SCALING, indicating that the printer can scale the page image.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3e1d-145">Notes</span><span class="sxs-lookup"><span data-stu-id="e3e1d-145">Remarks</span></span>

<span data-ttu-id="e3e1d-146">Les valeurs de tous les membres de structure sont fournies par la fonction **GetPrintProcessorCapabilities** , qui est documentée dans le kit de pilotes Windows.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-146">Values for all structure members are supplied by the **GetPrintProcessorCapabilities** function which is documented in the Windows Driver Kit.</span></span>

<span data-ttu-id="e3e1d-147">Quand une application appelle [**GetPrinterData**](getprinterdata.md), le spouleur appelle la fonction **GetPrintProcessorCapabilities** d’un processeur d’impression et spécifie un nom de valeur qui a un format _de type de_ données **PrintProcCaps \_**, où *DataType* est le nom d’un type de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e3e1d-147">When an application calls [**GetPrinterData**](getprinterdata.md), the spooler calls a print processor's **GetPrintProcessorCapabilities** function and specifies a value name that has a format of **PrintProcCaps\_**_datatype_, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3e1d-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3e1d-148">Requirements</span></span>



| <span data-ttu-id="e3e1d-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3e1d-149">Requirement</span></span> | <span data-ttu-id="e3e1d-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3e1d-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3e1d-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3e1d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="e3e1d-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3e1d-152">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="e3e1d-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e3e1d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="e3e1d-154">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e3e1d-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e3e1d-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3e1d-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3e1d-156"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3e1d-156"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3e1d-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3e1d-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3e1d-158">Impression</span><span class="sxs-lookup"><span data-stu-id="e3e1d-158">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e3e1d-159">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="e3e1d-159">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="e3e1d-160">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="e3e1d-160">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

 




