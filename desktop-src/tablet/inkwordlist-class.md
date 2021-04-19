---
description: Représente une liste de mots qui peuvent être utilisés pour améliorer le résultat de la reconnaissance.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: InkWordList, classe (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526273"
---
# <a name="inkwordlist-class"></a><span data-ttu-id="372bc-103">InkWordList, classe</span><span class="sxs-lookup"><span data-stu-id="372bc-103">InkWordList class</span></span>

<span data-ttu-id="372bc-104">Représente une liste de mots qui peuvent être utilisés pour améliorer le résultat de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="372bc-104">Represents a list of words that can be used to improve the recognition result.</span></span>

<span data-ttu-id="372bc-105">**InkWordList** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="372bc-105">**InkWordList** has these types of members:</span></span>

-   [<span data-ttu-id="372bc-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="372bc-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="372bc-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="372bc-107">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="372bc-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="372bc-108">Interfaces</span></span>

<span data-ttu-id="372bc-109">La classe **InkWordList** définit ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="372bc-109">The **InkWordList** class defines these interfaces.</span></span>



| <span data-ttu-id="372bc-110">Interface</span><span class="sxs-lookup"><span data-stu-id="372bc-110">Interface</span></span>        | <span data-ttu-id="372bc-111">Description</span><span class="sxs-lookup"><span data-stu-id="372bc-111">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="372bc-112">**IInkWordList**</span><span class="sxs-lookup"><span data-stu-id="372bc-112">**IInkWordList**</span></span> | <span data-ttu-id="372bc-113">Cet objet implémente l’interface com **IInkWordList** .</span><span class="sxs-lookup"><span data-stu-id="372bc-113">This object implements the **IInkWordList** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="372bc-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="372bc-114">Methods</span></span>

<span data-ttu-id="372bc-115">La classe **InkWordList** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="372bc-115">The **InkWordList** class has these methods.</span></span>



| <span data-ttu-id="372bc-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="372bc-116">Method</span></span>                                       | <span data-ttu-id="372bc-117">Description</span><span class="sxs-lookup"><span data-stu-id="372bc-117">Description</span></span>                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="372bc-118">**AddWord**</span><span class="sxs-lookup"><span data-stu-id="372bc-118">**AddWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | <span data-ttu-id="372bc-119">Ajoute un mot unique à **InkWordList**.</span><span class="sxs-lookup"><span data-stu-id="372bc-119">Adds a single word to the **InkWordList**.</span></span><br/>                   |
| [<span data-ttu-id="372bc-120">**Fusion**</span><span class="sxs-lookup"><span data-stu-id="372bc-120">**Merge**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | <span data-ttu-id="372bc-121">Fusionne un autre **InkWordList** dans ce **InkWordList**.</span><span class="sxs-lookup"><span data-stu-id="372bc-121">Merges another **InkWordList** to into this **InkWordList**.</span></span><br/> |
| [<span data-ttu-id="372bc-122">**RemoveWord**</span><span class="sxs-lookup"><span data-stu-id="372bc-122">**RemoveWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | <span data-ttu-id="372bc-123">Supprime un mot unique d’un **InkWordList**.</span><span class="sxs-lookup"><span data-stu-id="372bc-123">Removes a single word from a **InkWordList**.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="372bc-124">Notes</span><span class="sxs-lookup"><span data-stu-id="372bc-124">Remarks</span></span>

<span data-ttu-id="372bc-125">Cet objet peut être instancié en appelant la méthode [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.</span><span class="sxs-lookup"><span data-stu-id="372bc-125">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="372bc-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="372bc-126">Requirements</span></span>



| <span data-ttu-id="372bc-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="372bc-127">Requirement</span></span> | <span data-ttu-id="372bc-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="372bc-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="372bc-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="372bc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="372bc-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="372bc-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="372bc-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="372bc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="372bc-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="372bc-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="372bc-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="372bc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="372bc-134"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="372bc-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="372bc-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="372bc-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="372bc-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="372bc-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="372bc-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="372bc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="372bc-138">**Propriété de la propriété de la propriété**</span><span class="sxs-lookup"><span data-stu-id="372bc-138">**WordList Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[<span data-ttu-id="372bc-139">Constantes Factoid</span><span class="sxs-lookup"><span data-stu-id="372bc-139">Factoid Constants</span></span>](factoid-constants.md)
</dt> <dt>

[<span data-ttu-id="372bc-140">**InkRecognizerContext, classe**</span><span class="sxs-lookup"><span data-stu-id="372bc-140">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

