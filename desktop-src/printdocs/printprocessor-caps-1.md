---
description: La \_ structure PRINTPROCESSOR Cap \_ 1 est le format des informations sur les fonctionnalités de l’imprimante qui est retournée par la fonction GetPrinterData dans le tampon spécifié par la variable pData.
ms.assetid: 43c568ff-ccc9-4873-b159-ede09b4a7e51
title: Structure PRINTPROCESSOR_CAPS_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_CAPS_1
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 131b5ecf874554c3642808570a53ee8b20ad0e68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536810"
---
# <a name="printprocessor_caps_1-structure"></a><span data-ttu-id="53cc0-103">\_Structure PRINTPROCESSOR Cap \_ 1</span><span class="sxs-lookup"><span data-stu-id="53cc0-103">PRINTPROCESSOR\_CAPS\_1 structure</span></span>

<span data-ttu-id="53cc0-104">La structure **PRINTPROCESSOR \_ Cap \_ 1** est le format des informations sur les fonctionnalités de l’imprimante qui est retournée par la fonction [**GetPrinterData**](getprinterdata.md) dans le tampon spécifié par la variable *pData* .</span><span class="sxs-lookup"><span data-stu-id="53cc0-104">The **PRINTPROCESSOR\_CAPS\_1** structure is the format for the printer capability information that is returned by the [**GetPrinterData**](getprinterdata.md) function in the buffer specified by the *pData* variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="53cc0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53cc0-105">Syntax</span></span>


```C++
typedef struct _PRINTPROCESSOR_CAPS_1 {
  DWORD dwLevel;
  DWORD dwNupOptions;
  DWORD dwPageOrderFlags;
  DWORD dwNumberOfCopies;
} PRINTPROCESSOR_CAPS_1, *PPRINTPROCESSOR_CAPS_1;
```



## <a name="members"></a><span data-ttu-id="53cc0-106">Membres</span><span class="sxs-lookup"><span data-stu-id="53cc0-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="53cc0-107">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="53cc0-107">**dwLevel**</span></span>
</dt> <dd>

<span data-ttu-id="53cc0-108">Numéro de version de la structure.</span><span class="sxs-lookup"><span data-stu-id="53cc0-108">The structure's version number.</span></span> <span data-ttu-id="53cc0-109">Cette valeur doit être 1.</span><span class="sxs-lookup"><span data-stu-id="53cc0-109">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="53cc0-110">**dwNupOptions**</span><span class="sxs-lookup"><span data-stu-id="53cc0-110">**dwNupOptions**</span></span>
</dt> <dd>

<span data-ttu-id="53cc0-111">Masque de bits représentant les différents nombres de pages de document que l’imprimante peut imprimer sur une page physique.</span><span class="sxs-lookup"><span data-stu-id="53cc0-111">A bit mask representing the various numbers of document pages the printer can print on a physical page.</span></span> <span data-ttu-id="53cc0-112">Le bit le moins significatif représente 1 page de document par page, le bit suivant représente 2 pages de document par page, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="53cc0-112">The least significant bit represents 1 document page per page, the next bit represents 2 document pages per page, and so on.</span></span> <span data-ttu-id="53cc0-113">Par exemple, 0x0000810B indique que l’imprimante prend en charge les pages de documents 1, 2, 4, 9 et 16 par page physique.</span><span class="sxs-lookup"><span data-stu-id="53cc0-113">For example, 0x0000810B indicates the printer supports 1, 2, 4, 9, and 16 document pages per physical page.</span></span>

</dd> <dt>

<span data-ttu-id="53cc0-114">**dwPageOrderFlags**</span><span class="sxs-lookup"><span data-stu-id="53cc0-114">**dwPageOrderFlags**</span></span>
</dt> <dd>

<span data-ttu-id="53cc0-115">Ordre dans lequel les pages seront imprimées.</span><span class="sxs-lookup"><span data-stu-id="53cc0-115">The order in which pages will be printed.</span></span> <span data-ttu-id="53cc0-116">Cette valeur peut être \_ impression normale, INverser l' \_ impression ou livret \_ imprimé.</span><span class="sxs-lookup"><span data-stu-id="53cc0-116">This value can be NORMAL\_PRINT, REVERSE\_PRINT, or BOOKLET\_PRINT.</span></span>

</dd> <dt>

<span data-ttu-id="53cc0-117">**dwNumberOfCopies**</span><span class="sxs-lookup"><span data-stu-id="53cc0-117">**dwNumberOfCopies**</span></span>
</dt> <dd>

<span data-ttu-id="53cc0-118">Nombre maximal de copies que l’imprimante peut gérer.</span><span class="sxs-lookup"><span data-stu-id="53cc0-118">The maximum number of copies the printer can handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53cc0-119">Notes</span><span class="sxs-lookup"><span data-stu-id="53cc0-119">Remarks</span></span>

<span data-ttu-id="53cc0-120">Les valeurs de tous les membres de structure sont fournies par la fonction [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) , qui est documentée dans le kit WDK (Windows Driver Kit).</span><span class="sxs-lookup"><span data-stu-id="53cc0-120">Values for all structure members are supplied by the [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function, which is documented in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="53cc0-121">Le spouleur appelle la fonction [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) d’un processeur d’impression lorsqu’une application appelle [**GetPrinterData**](getprinterdata.md), en spécifiant un nom de valeur au format PrintProcCaps \_ *DataType*, où *DataType* est le nom d’un type de données d’entrée.</span><span class="sxs-lookup"><span data-stu-id="53cc0-121">The spooler calls a print processor's [**GetPrintProcessorCapabilities**](/windows-hardware/drivers/ddi/content/winsplp/nf-winsplp-getprintprocessorcapabilities) function when an application calls [**GetPrinterData**](getprinterdata.md), specifying a value name with a format of PrintProcCaps\_*datatype*, where *datatype* is the name of an input data type.</span></span>

## <a name="requirements"></a><span data-ttu-id="53cc0-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53cc0-122">Requirements</span></span>



| <span data-ttu-id="53cc0-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53cc0-123">Requirement</span></span> | <span data-ttu-id="53cc0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="53cc0-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53cc0-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53cc0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="53cc0-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53cc0-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="53cc0-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53cc0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="53cc0-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53cc0-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="53cc0-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="53cc0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="53cc0-130"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53cc0-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53cc0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53cc0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53cc0-132">Impression</span><span class="sxs-lookup"><span data-stu-id="53cc0-132">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="53cc0-133">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="53cc0-133">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="53cc0-134">**GetPrinterData**</span><span class="sxs-lookup"><span data-stu-id="53cc0-134">**GetPrinterData**</span></span>](getprinterdata.md)
</dt> </dl>

 

