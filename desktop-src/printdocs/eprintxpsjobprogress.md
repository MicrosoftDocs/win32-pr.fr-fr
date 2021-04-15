---
description: Spécifie ce que le spouleur effectue actuellement lors du traitement d’un travail d’impression XPS.
ms.assetid: 4fa5b749-e4f9-4f08-97b5-e58f82d0b485
title: EPrintXPSJobProgress, énumération (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobProgress
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 2a09b55ed72a6276a1a9d224cc08e03546f887d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529542"
---
# <a name="eprintxpsjobprogress-enumeration"></a><span data-ttu-id="1f103-103">Énumération EPrintXPSJobProgress</span><span class="sxs-lookup"><span data-stu-id="1f103-103">EPrintXPSJobProgress enumeration</span></span>

<span data-ttu-id="1f103-104">Spécifie ce que le spouleur effectue actuellement lors du traitement d’un travail d’impression XPS.</span><span class="sxs-lookup"><span data-stu-id="1f103-104">Specifies what the spooler is currently doing as it processes an XPS print job.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f103-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1f103-105">Syntax</span></span>


```C++
typedef enum tagEPrintXPSJobProgress { 
  kAddingDocumentSequence,
  kDocumentSequenceAdded,
  kAddingFixedDocument,
  kFixedDocumentAdded,
  kAddingFixedPage,
  kFixedPageAdded,
  kResourceAdded,
  kFontAdded,
  kImageAdded,
  kXpsDocumentCommitted
} EPrintXPSJobProgress;
```



## <a name="constants"></a><span data-ttu-id="1f103-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1f103-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1f103-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**</span><span class="sxs-lookup"><span data-stu-id="1f103-107"><span id="kAddingDocumentSequence"></span><span id="kaddingdocumentsequence"></span><span id="KADDINGDOCUMENTSEQUENCE"></span>**kAddingDocumentSequence**</span></span>
</dt> <dd>

<span data-ttu-id="1f103-108">Une séquence de documents va être ajoutée à la tâche XPS.</span><span class="sxs-lookup"><span data-stu-id="1f103-108">A document sequence is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="1f103-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**</span><span class="sxs-lookup"><span data-stu-id="1f103-109"><span id="kDocumentSequenceAdded"></span><span id="kdocumentsequenceadded"></span><span id="KDOCUMENTSEQUENCEADDED"></span>**kDocumentSequenceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="1f103-110">Une séquence de documents a été ajoutée à la tâche XPS.</span><span class="sxs-lookup"><span data-stu-id="1f103-110">A document sequence has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="1f103-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**</span><span class="sxs-lookup"><span data-stu-id="1f103-111"><span id="kAddingFixedDocument"></span><span id="kaddingfixeddocument"></span><span id="KADDINGFIXEDDOCUMENT"></span>**kAddingFixedDocument**</span></span>
</dt> <dd>

<span data-ttu-id="1f103-112">Un document fixe va être ajouté à la tâche XPS.</span><span class="sxs-lookup"><span data-stu-id="1f103-112">A fixed document is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="1f103-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**</span><span class="sxs-lookup"><span data-stu-id="1f103-113"><span id="kFixedDocumentAdded"></span><span id="kfixeddocumentadded"></span><span id="KFIXEDDOCUMENTADDED"></span>**kFixedDocumentAdded**</span></span>
</dt> <dd>

<span data-ttu-id="1f103-114">Un document fixe a été ajouté à la tâche XPS.</span><span class="sxs-lookup"><span data-stu-id="1f103-114">A fixed document has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="1f103-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**</span><span class="sxs-lookup"><span data-stu-id="1f103-115"><span id="kAddingFixedPage"></span><span id="kaddingfixedpage"></span><span id="KADDINGFIXEDPAGE"></span>**kAddingFixedPage**</span></span>
</dt> <dd>

<span data-ttu-id="1f103-116">Une page va être ajoutée au travail XPS.</span><span class="sxs-lookup"><span data-stu-id="1f103-116">A page is about to be added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="1f103-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**</span><span class="sxs-lookup"><span data-stu-id="1f103-117"><span id="kFixedPageAdded"></span><span id="kfixedpageadded"></span><span id="KFIXEDPAGEADDED"></span>**kFixedPageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="1f103-118">Une page a été ajoutée à la tâche XPS.</span><span class="sxs-lookup"><span data-stu-id="1f103-118">A page has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="1f103-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**</span><span class="sxs-lookup"><span data-stu-id="1f103-119"><span id="kResourceAdded"></span><span id="kresourceadded"></span><span id="KRESOURCEADDED"></span>**kResourceAdded**</span></span>
</dt> <dd>

<span data-ttu-id="1f103-120">Une ressource a été ajoutée à la tâche XPS.</span><span class="sxs-lookup"><span data-stu-id="1f103-120">A resource had been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="1f103-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**</span><span class="sxs-lookup"><span data-stu-id="1f103-121"><span id="kFontAdded"></span><span id="kfontadded"></span><span id="KFONTADDED"></span>**kFontAdded**</span></span>
</dt> <dd>

<span data-ttu-id="1f103-122">Une police a été ajoutée à la tâche XPS.</span><span class="sxs-lookup"><span data-stu-id="1f103-122">A font has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="1f103-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**</span><span class="sxs-lookup"><span data-stu-id="1f103-123"><span id="kImageAdded"></span><span id="kimageadded"></span><span id="KIMAGEADDED"></span>**kImageAdded**</span></span>
</dt> <dd>

<span data-ttu-id="1f103-124">Une image a été ajoutée à la tâche XPS.</span><span class="sxs-lookup"><span data-stu-id="1f103-124">An image has been added to the XPS job.</span></span>

</dd> <dt>

<span data-ttu-id="1f103-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**</span><span class="sxs-lookup"><span data-stu-id="1f103-125"><span id="kXpsDocumentCommitted"></span><span id="kxpsdocumentcommitted"></span><span id="KXPSDOCUMENTCOMMITTED"></span>**kXpsDocumentCommitted**</span></span>
</dt> <dd>

<span data-ttu-id="1f103-126">Les données de la tâche XPS ont été validées.</span><span class="sxs-lookup"><span data-stu-id="1f103-126">The data for the XPS job has been committed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f103-127">Notes</span><span class="sxs-lookup"><span data-stu-id="1f103-127">Remarks</span></span>

<span data-ttu-id="1f103-128">Cette énumération est principalement utilisée comme paramètre pour la fonction [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .</span><span class="sxs-lookup"><span data-stu-id="1f103-128">This enumeration is primarily used as a parameter for the [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) function.</span></span>

<span data-ttu-id="1f103-129">Ces valeurs peuvent faire référence à la phase de mise en file d’attente ou de rendu d’un travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="1f103-129">These values can refer to either the spooling or the rendering phase of a print job.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f103-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1f103-130">Requirements</span></span>



| <span data-ttu-id="1f103-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1f103-131">Requirement</span></span> | <span data-ttu-id="1f103-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="1f103-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f103-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f103-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1f103-134">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f103-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1f103-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1f103-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1f103-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1f103-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1f103-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="1f103-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f103-138"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f103-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



 

 




