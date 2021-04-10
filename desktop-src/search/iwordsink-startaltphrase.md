---
description: Indique la limite entre les expressions dans une séquence d’expressions de remplacement générées par un analyseur lexical au moment de l’indexation.
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'IWordSink :: StartAltPhrase, méthode (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201285"
---
# <a name="iwordsinkstartaltphrase-method"></a><span data-ttu-id="25be1-103">IWordSink :: StartAltPhrase, méthode</span><span class="sxs-lookup"><span data-stu-id="25be1-103">IWordSink::StartAltPhrase method</span></span>

<span data-ttu-id="25be1-104">Indique la limite entre les expressions dans une séquence d’expressions de remplacement générées par un analyseur lexical au moment de l’indexation.</span><span class="sxs-lookup"><span data-stu-id="25be1-104">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="25be1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25be1-105">Syntax</span></span>


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="25be1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25be1-106">Parameters</span></span>

<span data-ttu-id="25be1-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="25be1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25be1-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="25be1-108">Return value</span></span>

<span data-ttu-id="25be1-109">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="25be1-109">This method can return one of these values.</span></span>



| <span data-ttu-id="25be1-110">Code de retour</span><span class="sxs-lookup"><span data-stu-id="25be1-110">Return code</span></span>                                                                                           | <span data-ttu-id="25be1-111">Description</span><span class="sxs-lookup"><span data-stu-id="25be1-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25be1-112"><dt>**\_requête WBREAK \_ E \_ uniquement**</dt></span><span class="sxs-lookup"><span data-stu-id="25be1-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="25be1-113">[**StartAltPhrase**](iwordsink-startaltphrase.md) est appelé pendant la durée de la requête.</span><span class="sxs-lookup"><span data-stu-id="25be1-113">[**StartAltPhrase**](iwordsink-startaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25be1-114">Notes</span><span class="sxs-lookup"><span data-stu-id="25be1-114">Remarks</span></span>

<span data-ttu-id="25be1-115">Chaque expression de remplacement commence par un appel **StartAltPhrase** .</span><span class="sxs-lookup"><span data-stu-id="25be1-115">Each alternative phrase starts with a **StartAltPhrase** call.</span></span> <span data-ttu-id="25be1-116">L’expression est placée dans l’objet [**IWordSink**](iwordsink.md) via les appels suivants à la méthode [**IWordSink ::P utword**](iwordsink-putword.md) ou [**IWordSink ::P utaltword**](iwordsink-putaltword.md) .</span><span class="sxs-lookup"><span data-stu-id="25be1-116">The phrase is put in the [**IWordSink**](iwordsink.md) object through subsequent calls to the [**IWordSink::PutWord**](iwordsink-putword.md) or [**IWordSink::PutAltWord**](iwordsink-putaltword.md) method.</span></span> <span data-ttu-id="25be1-117">L’expression alternative finale dans une séquence d’expressions se termine par un appel à la méthode [**IWordSink :: EndAltPhrase**](iwordsink-endaltphrase.md) .</span><span class="sxs-lookup"><span data-stu-id="25be1-117">The final alternative phrase in a sequence of phrases is terminated with a call to the [**IWordSink::EndAltPhrase**](iwordsink-endaltphrase.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="25be1-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25be1-118">Requirements</span></span>



| <span data-ttu-id="25be1-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25be1-119">Requirement</span></span> | <span data-ttu-id="25be1-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="25be1-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="25be1-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25be1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="25be1-122">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25be1-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="25be1-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25be1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="25be1-124">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25be1-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="25be1-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="25be1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="25be1-126"><dt>Rechercher. h</dt></span><span class="sxs-lookup"><span data-stu-id="25be1-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25be1-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25be1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25be1-128">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="25be1-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 




