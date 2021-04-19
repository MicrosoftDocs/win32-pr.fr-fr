---
description: Gère les mots identifiés par des césures de mots pendant la durée de l’index et la durée de la requête.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: Interface IWordSink (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 2eab8eee4f7b07b0f712e68d7ad05b970506b00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517238"
---
# <a name="iwordsink-interface"></a><span data-ttu-id="b1ce5-103">Interface IWordSink</span><span class="sxs-lookup"><span data-stu-id="b1ce5-103">IWordSink interface</span></span>

<span data-ttu-id="b1ce5-104">Gère les mots identifiés par des césures de mots pendant la durée de l’index et la durée de la requête.</span><span class="sxs-lookup"><span data-stu-id="b1ce5-104">Handles words identified by word breaks during both index time and query time.</span></span>

## <a name="members"></a><span data-ttu-id="b1ce5-105">Membres</span><span class="sxs-lookup"><span data-stu-id="b1ce5-105">Members</span></span>

<span data-ttu-id="b1ce5-106">L’interface **IWordSink** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b1ce5-106">The **IWordSink** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b1ce5-107">**IWordSink** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b1ce5-107">**IWordSink** also has these types of members:</span></span>

-   [<span data-ttu-id="b1ce5-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b1ce5-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b1ce5-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b1ce5-109">Methods</span></span>

<span data-ttu-id="b1ce5-110">L’interface **IWordSink** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="b1ce5-110">The **IWordSink** interface has these methods.</span></span>



| <span data-ttu-id="b1ce5-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="b1ce5-111">Method</span></span>                                             | <span data-ttu-id="b1ce5-112">Description</span><span class="sxs-lookup"><span data-stu-id="b1ce5-112">Description</span></span>                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1ce5-113">**EndAltPhrase**</span><span class="sxs-lookup"><span data-stu-id="b1ce5-113">**EndAltPhrase**</span></span>](iwordsink-endaltphrase.md)     | <span data-ttu-id="b1ce5-114">Indique la fin de l’expression finale dans une séquence d’expressions de remplacement générées par un analyseur lexical au moment de l’indexation.</span><span class="sxs-lookup"><span data-stu-id="b1ce5-114">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/>  |
| [<span data-ttu-id="b1ce5-115">**PutAltWord**</span><span class="sxs-lookup"><span data-stu-id="b1ce5-115">**PutAltWord**</span></span>](iwordsink-putaltword.md)         | <span data-ttu-id="b1ce5-116">Place un autre mot et sa position dans l’objet **IWordSink** .</span><span class="sxs-lookup"><span data-stu-id="b1ce5-116">Puts an alternative word and its position in the **IWordSink** object.</span></span><br/>                                                       |
| [<span data-ttu-id="b1ce5-117">**PutBreak**</span><span class="sxs-lookup"><span data-stu-id="b1ce5-117">**PutBreak**</span></span>](iwordsink-putbreak.md)             | <span data-ttu-id="b1ce5-118">Met un saut après le mot précédent.</span><span class="sxs-lookup"><span data-stu-id="b1ce5-118">Puts a break after the preceding word.</span></span><br/>                                                                                       |
| [<span data-ttu-id="b1ce5-119">**PutWord**</span><span class="sxs-lookup"><span data-stu-id="b1ce5-119">**PutWord**</span></span>](iwordsink-putword.md)               | <span data-ttu-id="b1ce5-120">Place un mot et sa position dans l’objet **IWordSink** .</span><span class="sxs-lookup"><span data-stu-id="b1ce5-120">Puts a word and its position in the **IWordSink** object.</span></span><br/>                                                                    |
| [<span data-ttu-id="b1ce5-121">**StartAltPhrase**</span><span class="sxs-lookup"><span data-stu-id="b1ce5-121">**StartAltPhrase**</span></span>](iwordsink-startaltphrase.md) | <span data-ttu-id="b1ce5-122">Indique la limite entre les expressions dans une séquence d’expressions de remplacement générées par un analyseur lexical au moment de l’indexation.</span><span class="sxs-lookup"><span data-stu-id="b1ce5-122">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b1ce5-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b1ce5-123">Remarks</span></span>

<span data-ttu-id="b1ce5-124">Windows Search crée et initialise des instances de l’objet **IWordSink** .</span><span class="sxs-lookup"><span data-stu-id="b1ce5-124">Windows Search creates and initializes instances of the **IWordSink** object.</span></span> <span data-ttu-id="b1ce5-125">L’objet **IWordSink** reçoit le paramètre *fQuery* pendant l’initialisation et utilise ce paramètre pour déterminer le contexte de césure des mots dans lequel l’objet est utilisé.</span><span class="sxs-lookup"><span data-stu-id="b1ce5-125">The **IWordSink** object receives the *fQuery* parameter during initialization and uses this parameter to determine the word-breaking context in which the object is used.</span></span>

<span data-ttu-id="b1ce5-126">Les implémentations de [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) reçoivent un pointeur vers l’objet **IWordSink** dans la méthode [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) .</span><span class="sxs-lookup"><span data-stu-id="b1ce5-126">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations receive a pointer to the **IWordSink** object in the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1ce5-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1ce5-127">Requirements</span></span>



| <span data-ttu-id="b1ce5-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1ce5-128">Requirement</span></span> | <span data-ttu-id="b1ce5-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1ce5-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b1ce5-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1ce5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b1ce5-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1ce5-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b1ce5-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1ce5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b1ce5-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b1ce5-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b1ce5-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1ce5-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1ce5-135"><dt>Rechercher. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1ce5-135"><dt>Search.h</dt></span></span> </dl> |



 

 
