---
description: La \_ structure doc info \_ 2 décrit un document qui sera imprimé.
ms.assetid: d62333f3-cc39-4c9b-8fb3-02a2d24bbbad
title: Structure DOC_INFO_2 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOC_INFO_2
- _DOC_INFO_2A
- _DOC_INFO_2W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76b66711883e2238e971cb26d071716bd52ca54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530175"
---
# <a name="doc_info_2-structure"></a><span data-ttu-id="9996b-103">\_Structure infos doc \_ 2</span><span class="sxs-lookup"><span data-stu-id="9996b-103">DOC\_INFO\_2 structure</span></span>

<span data-ttu-id="9996b-104">La structure **doc \_ info \_ 2** décrit un document qui sera imprimé.</span><span class="sxs-lookup"><span data-stu-id="9996b-104">The **DOC\_INFO\_2** structure describes a document that will be printed.</span></span>

## <a name="syntax"></a><span data-ttu-id="9996b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9996b-105">Syntax</span></span>


```C++
typedef struct _DOC_INFO_2 {
  LPTSTR pDocName;
  LPTSTR pOutputFile;
  LPTSTR pDatatype;
  DWORD  dwMode;
  DWORD  JobId;
} DOC_INFO_2, *PDOC_INFO_2;
```



## <a name="members"></a><span data-ttu-id="9996b-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9996b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9996b-107">**pDocName**</span><span class="sxs-lookup"><span data-stu-id="9996b-107">**pDocName**</span></span>
</dt> <dd>

<span data-ttu-id="9996b-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du document.</span><span class="sxs-lookup"><span data-stu-id="9996b-108">Pointer to a null-terminated string that specifies the name of the document.</span></span>

</dd> <dt>

<span data-ttu-id="9996b-109">**pOutputFile**</span><span class="sxs-lookup"><span data-stu-id="9996b-109">**pOutputFile**</span></span>
</dt> <dd>

<span data-ttu-id="9996b-110">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’un fichier de sortie.</span><span class="sxs-lookup"><span data-stu-id="9996b-110">Pointer to a null-terminated string that specifies the name of an output file.</span></span>

</dd> <dt>

<span data-ttu-id="9996b-111">**pDatatype**</span><span class="sxs-lookup"><span data-stu-id="9996b-111">**pDatatype**</span></span>
</dt> <dd>

<span data-ttu-id="9996b-112">Pointeur vers une chaîne se terminant par un caractère null qui identifie le type de données utilisé pour enregistrer le document.</span><span class="sxs-lookup"><span data-stu-id="9996b-112">Pointer to a null-terminated string that identifies the type of data used to record the document.</span></span>

</dd> <dt>

<span data-ttu-id="9996b-113">**dwMode**</span><span class="sxs-lookup"><span data-stu-id="9996b-113">**dwMode**</span></span>
</dt> <dd>

<span data-ttu-id="9996b-114">Informe le spouleur d’impression de la nature des données à suivre.</span><span class="sxs-lookup"><span data-stu-id="9996b-114">Informs the print spooler of the nature of the data to follow.</span></span> <span data-ttu-id="9996b-115">Si cette valeur est égale à zéro, le spouleur d’impression traite les données envoyées par les appels suivants à [**WritePrinter**](writeprinter.md) en tant que travail d’impression normal (qu’ils soient ou non mis en file d’attente dépend de la propriété Printer).</span><span class="sxs-lookup"><span data-stu-id="9996b-115">If this value is zero, the print spooler treats the data sent by subsequent calls to [**WritePrinter**](writeprinter.md) as a normal print job (whether or not it is spooled depends on the printer property).</span></span> <span data-ttu-id="9996b-116">Si cette valeur est DI \_ Channel, seul un canal de communication est ouvert.</span><span class="sxs-lookup"><span data-stu-id="9996b-116">If this value is DI\_CHANNEL, only a communications channel is opened.</span></span> <span data-ttu-id="9996b-117">Dans ce cas, les données passées dans les appels suivants à **WritePrinter** sont envoyées à l’imprimante ou les appels suivants à [**ReadPrinter**](readprinter.md) récupèrent les données de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="9996b-117">In this case, the data passed into subsequent calls to **WritePrinter** is sent to the printer or subsequent calls to [**ReadPrinter**](readprinter.md) retrieve data from the printer.</span></span> <span data-ttu-id="9996b-118">Ce mode reste effectif jusqu’à l’appel de [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) .</span><span class="sxs-lookup"><span data-stu-id="9996b-118">This mode remains effective until [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) is called.</span></span>

</dd> <dt>

<span data-ttu-id="9996b-119">**JobId**</span><span class="sxs-lookup"><span data-stu-id="9996b-119">**JobId**</span></span>
</dt> <dd>

<span data-ttu-id="9996b-120">Réservé à un usage interne ; doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="9996b-120">Reserved for internal use; should be zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9996b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9996b-121">Requirements</span></span>



| <span data-ttu-id="9996b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9996b-122">Requirement</span></span> | <span data-ttu-id="9996b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="9996b-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9996b-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9996b-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9996b-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9996b-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9996b-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9996b-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9996b-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9996b-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9996b-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="9996b-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9996b-129"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9996b-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="9996b-130">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="9996b-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9996b-131">**\_ \_ Infos doc \_ 2S** (Unicode) et **\_ \_ infos doc \_ 2A** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9996b-131">**\_DOC\_INFO\_2W** (Unicode) and **\_DOC\_INFO\_2A** (ANSI)</span></span><br/>                                   |



## <a name="see-also"></a><span data-ttu-id="9996b-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9996b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9996b-133">Impression</span><span class="sxs-lookup"><span data-stu-id="9996b-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="9996b-134">Structures de l’API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="9996b-134">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="9996b-135">**EndDoc**</span><span class="sxs-lookup"><span data-stu-id="9996b-135">**EndDoc**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-enddoc)
</dt> <dt>

[<span data-ttu-id="9996b-136">**ReadPrinter**</span><span class="sxs-lookup"><span data-stu-id="9996b-136">**ReadPrinter**</span></span>](readprinter.md)
</dt> <dt>

[<span data-ttu-id="9996b-137">**StartDocPrinter**</span><span class="sxs-lookup"><span data-stu-id="9996b-137">**StartDocPrinter**</span></span>](startdocprinter.md)
</dt> <dt>

[<span data-ttu-id="9996b-138">**WritePrinter**</span><span class="sxs-lookup"><span data-stu-id="9996b-138">**WritePrinter**</span></span>](writeprinter.md)
</dt> </dl>

 

 




