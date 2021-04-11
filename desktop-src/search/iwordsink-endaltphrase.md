---
description: Indique la fin de l’expression finale dans une séquence d’expressions de remplacement générées par un analyseur lexical au moment de l’indexation.
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'IWordSink :: EndAltPhrase, méthode (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 4056357de5e3e479124e8f9a91d9b3d906300709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201286"
---
# <a name="iwordsinkendaltphrase-method"></a><span data-ttu-id="41414-103">IWordSink :: EndAltPhrase, méthode</span><span class="sxs-lookup"><span data-stu-id="41414-103">IWordSink::EndAltPhrase method</span></span>

<span data-ttu-id="41414-104">Indique la fin de l’expression finale dans une séquence d’expressions de remplacement générées par un analyseur lexical au moment de l’indexation.</span><span class="sxs-lookup"><span data-stu-id="41414-104">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="41414-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="41414-105">Syntax</span></span>


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="41414-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41414-106">Parameters</span></span>

<span data-ttu-id="41414-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="41414-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="41414-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="41414-108">Return value</span></span>

<span data-ttu-id="41414-109">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="41414-109">This method can return one of these values.</span></span>



| <span data-ttu-id="41414-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="41414-110">Return code</span></span>                                                                                           | <span data-ttu-id="41414-111">Description</span><span class="sxs-lookup"><span data-stu-id="41414-111">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="41414-112"><dt>**\_requête WBREAK \_ E \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="41414-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="41414-113">[**EndAltPhrase**](iwordsink-endaltphrase.md) est appelé pendant la durée de la requête.</span><span class="sxs-lookup"><span data-stu-id="41414-113">[**EndAltPhrase**](iwordsink-endaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="41414-114">Notes</span><span class="sxs-lookup"><span data-stu-id="41414-114">Remarks</span></span>

<span data-ttu-id="41414-115">Les implémentations de [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) appellent **IWordSink :: EndAltPhrase** à partir de la méthode [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) pour terminer une séquence d’expressions de remplacement.</span><span class="sxs-lookup"><span data-stu-id="41414-115">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations call **IWordSink::EndAltPhrase** from the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method to terminate a sequence of alternative phrases.</span></span> <span data-ttu-id="41414-116">La méthode [**IWordSink :: StartAltPhrase**](iwordsink-startaltphrase.md) est appelée pour indiquer la fin d’une expression et le début d’une autre dans une séquence d’expressions.</span><span class="sxs-lookup"><span data-stu-id="41414-116">The [**IWordSink::StartAltPhrase**](iwordsink-startaltphrase.md) method is called to indicate the end of one phrase and the beginning of another in a sequence of phrases.</span></span> <span data-ttu-id="41414-117">Seule la dernière expression d’une séquence se termine par un appel à **EndAltPhrase**.</span><span class="sxs-lookup"><span data-stu-id="41414-117">Only the last phrase in a sequence is terminated with a call to **EndAltPhrase**.</span></span>

## <a name="requirements"></a><span data-ttu-id="41414-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41414-118">Requirements</span></span>



| <span data-ttu-id="41414-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41414-119">Requirement</span></span> | <span data-ttu-id="41414-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="41414-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41414-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41414-121">Minimum supported client</span></span><br/> | <span data-ttu-id="41414-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41414-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="41414-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41414-123">Minimum supported server</span></span><br/> | <span data-ttu-id="41414-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="41414-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="41414-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="41414-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="41414-126"><dt>Rechercher. h</dt></span><span class="sxs-lookup"><span data-stu-id="41414-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41414-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41414-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41414-128">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="41414-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
