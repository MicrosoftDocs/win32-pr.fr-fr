---
description: La \_ structure doc info \_ 3 décrit un document qui sera imprimé.
ms.assetid: 6e7b6727-da04-4f67-af77-6b51c68a4eb3
title: Structure DOC_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_3
- _DOC_INFO_3A
- _DOC_INFO_3W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 85d1d0f6af2eece8f9bd58112347478ec384642a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524629"
---
# <a name="doc_info_3-structure"></a><span data-ttu-id="b0115-103">\_Structure infos doc \_ 3</span><span class="sxs-lookup"><span data-stu-id="b0115-103">DOC\_INFO\_3 structure</span></span>

<span data-ttu-id="b0115-104">La structure **doc \_ info \_ 3** décrit un document qui sera imprimé.</span><span class="sxs-lookup"><span data-stu-id="b0115-104">The **DOC\_INFO\_3** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0115-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0115-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_3 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwFlags;
} DOC_INFO_3, *PDOC_INFO_3;
```



## <a name="members"></a><span data-ttu-id="b0115-106">Membres</span><span class="sxs-lookup"><span data-stu-id="b0115-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b0115-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="b0115-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="b0115-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du document.</span><span class="sxs-lookup"><span data-stu-id="b0115-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="b0115-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="b0115-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="b0115-110">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’un fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="b0115-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="b0115-111">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="b0115-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="b0115-112">Pointeur vers une chaîne se terminant par un caractère null qui identifie le type de données utilisé pour enregistrer le document.</span><span class="sxs-lookup"><span data-stu-id="b0115-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="b0115-113">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="b0115-113">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b0115-114">Père.</span><span class="sxs-lookup"><span data-stu-id="b0115-114">Flags.</span></span> <span data-ttu-id="b0115-115">Actuellement, il peut s’agir de la **valeur null** ou de ce qui suit.</span><span class="sxs-lookup"><span data-stu-id="b0115-115">Currently, it can be **NULL** or the following.</span></span>



| <span data-ttu-id="b0115-116">Indicateur</span><span class="sxs-lookup"><span data-stu-id="b0115-116">Flag</span></span>                 | <span data-ttu-id="b0115-117">Signification</span><span class="sxs-lookup"><span data-stu-id="b0115-117">Meaning</span></span>                                                                                                                                          |
|----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0115-118">\_écriture di MEMORYMAP \_</span><span class="sxs-lookup"><span data-stu-id="b0115-118">DI\_MEMORYMAP\_WRITE</span></span> | <span data-ttu-id="b0115-119">Force [**StartDocPrinter**](startdocprinter.md) à ne pas utiliser [**AddJob**](addjob.md) et [**ScheduleJob**](schedulejob.md) pour l’impression locale.</span><span class="sxs-lookup"><span data-stu-id="b0115-119">Causes [**StartDocPrinter**](startdocprinter.md) to not use [**AddJob**](addjob.md) and [**ScheduleJob**](schedulejob.md) for local printing.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0115-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b0115-120">Remarks</span></span>

<span data-ttu-id="b0115-121">Le \_ \_ paramètre d’écriture di MEMORYMAP dans **doc \_ info \_ 3** est une optimisation.</span><span class="sxs-lookup"><span data-stu-id="b0115-121">The DI\_MEMORYMAP\_WRITE setting in **DOC\_INFO\_3** is an optimization.</span></span> <span data-ttu-id="b0115-122">Cela permet à GDI de mapper les fichiers de mise en file d’attente dans l’application et d’accélérer l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b0115-122">This allows GDI to map spool files in the application and speed up the recording.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0115-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0115-123">Requirements</span></span>



| <span data-ttu-id="b0115-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0115-124">Requirement</span></span> | <span data-ttu-id="b0115-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0115-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0115-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0115-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b0115-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0115-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b0115-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0115-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b0115-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0115-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b0115-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0115-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0115-131"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0115-131"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b0115-132">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="b0115-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b0115-133">**\_ Informations de document \_ \_ 3W** (Unicode) et **\_ \_ infos doc \_ 3A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b0115-133">**\_DOC\_INFO\_3W** (Unicode) and **\_DOC\_INFO\_3A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="b0115-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0115-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0115-135">Impression</span><span class="sxs-lookup"><span data-stu-id="b0115-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b0115-136">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="b0115-136">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="b0115-137">**AddJob**</span><span class="sxs-lookup"><span data-stu-id="b0115-137">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="b0115-138">**ScheduleJob**</span><span class="sxs-lookup"><span data-stu-id="b0115-138">**ScheduleJob**</span></span>](schedulejob.md)
</dt> <dt>

[<span data-ttu-id="b0115-139">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="b0115-139">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




