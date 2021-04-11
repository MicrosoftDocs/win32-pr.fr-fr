---
description: La \_ structure doc info \_ 1 décrit un document qui sera imprimé.
ms.assetid: 142d988b-dd74-4312-8b27-331a7ec70344
title: Structure DOC_INFO_1 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_1
- _DOC_INFO_1A
- _DOC_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6f905a89163b46743a92c8616ee0fa3d0564590c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202698"
---
# <a name="doc_info_1-structure"></a><span data-ttu-id="a8d4e-103">\_Structure infos doc \_ 1</span><span class="sxs-lookup"><span data-stu-id="a8d4e-103">DOC\_INFO\_1 structure</span></span>

<span data-ttu-id="a8d4e-104">La structure **doc \_ info \_ 1** décrit un document qui sera imprimé.</span><span class="sxs-lookup"><span data-stu-id="a8d4e-104">The **DOC\_INFO\_1** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d4e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8d4e-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_1 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
} DOC_INFO_1;
```



## <a name="members"></a><span data-ttu-id="a8d4e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a8d4e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a8d4e-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="a8d4e-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="a8d4e-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du document.</span><span class="sxs-lookup"><span data-stu-id="a8d4e-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="a8d4e-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="a8d4e-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="a8d4e-110">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’un fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="a8d4e-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span> <span data-ttu-id="a8d4e-111">Pour imprimer sur une imprimante, affectez-lui la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="a8d4e-111">To print to a printer, set this to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a8d4e-112">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="a8d4e-112">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="a8d4e-113">Pointeur vers une chaîne se terminant par un caractère null qui identifie le type de données utilisé pour enregistrer le document.</span><span class="sxs-lookup"><span data-stu-id="a8d4e-113">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8d4e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8d4e-114">Requirements</span></span>



| <span data-ttu-id="a8d4e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8d4e-115">Requirement</span></span> | <span data-ttu-id="a8d4e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8d4e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d4e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8d4e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a8d4e-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8d4e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a8d4e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8d4e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a8d4e-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8d4e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a8d4e-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8d4e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8d4e-122"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8d4e-122"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a8d4e-123">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="a8d4e-123">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a8d4e-124">**\_ \_ Infos doc \_ 1s** (Unicode) et **\_ \_ infos doc \_ 1a** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a8d4e-124">**\_DOC\_INFO\_1W** (Unicode) and **\_DOC\_INFO\_1A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="a8d4e-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8d4e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8d4e-126">Impression</span><span class="sxs-lookup"><span data-stu-id="a8d4e-126">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a8d4e-127">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="a8d4e-127">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="a8d4e-128">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="a8d4e-128">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> </dl>

 

 




