---
description: Place un mot et sa position dans l’objet IWordSink.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: IWordSink ::P méthode utWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 5f622e09c2b82bc8de986dafcc83247617caec75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513367"
---
# <a name="iwordsinkputword-method"></a><span data-ttu-id="61423-103">IWordSink ::P méthode utWord</span><span class="sxs-lookup"><span data-stu-id="61423-103">IWordSink::PutWord method</span></span>

<span data-ttu-id="61423-104">Place un mot et sa position dans l’objet [**IWordSink**](iwordsink.md) .</span><span class="sxs-lookup"><span data-stu-id="61423-104">Puts a word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="61423-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61423-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="61423-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61423-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61423-107">*CWC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61423-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61423-108">Nombre de caractères dans *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="61423-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="61423-109">*pwcInBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61423-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61423-110">Pointeur vers une mémoire tampon qui contient une autre forme d’un mot du texte source.</span><span class="sxs-lookup"><span data-stu-id="61423-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="61423-111">Ce paramètre n’est pas modifié par **PutWord**.</span><span class="sxs-lookup"><span data-stu-id="61423-111">This parameter is not modified by **PutWord**.</span></span> <span data-ttu-id="61423-112">Vous pouvez transmettre le paramètre *pTextSource* à partir de [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="61423-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="61423-113">*cwcSrcLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61423-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61423-114">Nombre de caractères dans la mémoire tampon de texte source (indiqué par le paramètre *pTextSource* à [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) qui correspond au mot contenu dans *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="61423-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="61423-115">*cwcSrcPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="61423-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61423-116">Position de départ du mot dans *pwcInBuf* dans la mémoire tampon de texte source (indiquée par le paramètre *pTextSource* à [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="61423-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61423-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="61423-117">Return value</span></span>

<span data-ttu-id="61423-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="61423-118">This method can return one of these values.</span></span>



| <span data-ttu-id="61423-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="61423-119">Return code</span></span>                                                                                              | <span data-ttu-id="61423-120">Description</span><span class="sxs-lookup"><span data-stu-id="61423-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="61423-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="61423-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="61423-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="61423-122">The operation was completed successfully.</span></span> <span data-ttu-id="61423-123">Indique également qu’il n’y a plus de texte disponible pour remplir la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="61423-123">Also indicates that no more text is available to refill the buffer.</span></span><br/>                                  |
| <dl> <span data-ttu-id="61423-124"><dt>**Langue \_ \_ \_ mot S grand**</dt></span><span class="sxs-lookup"><span data-stu-id="61423-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="61423-125">La valeur de *CWC* est supérieure à la valeur de *UlMaxTokenSize* spécifiée dans [**IWordBreaker :: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span><span class="sxs-lookup"><span data-stu-id="61423-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="61423-126">Notes</span><span class="sxs-lookup"><span data-stu-id="61423-126">Remarks</span></span>

<span data-ttu-id="61423-127">Nous recommandons que la méthode **IWordSink ::P utword** contienne toujours le mot d’origine tel qu’il figure dans *pTextSource*.</span><span class="sxs-lookup"><span data-stu-id="61423-127">We recommend that the **IWordSink::PutWord** method always contain the original word as found in *pTextSource*.</span></span> <span data-ttu-id="61423-128">Les autres formes du mot sont passées à WordSink à l’aide de [**IWordSink ::P utaltword**](iwordsink-putaltword.md).</span><span class="sxs-lookup"><span data-stu-id="61423-128">Alternative forms of the word are passed to WordSink by using [**IWordSink::PutAltWord**](iwordsink-putaltword.md).</span></span> <span data-ttu-id="61423-129">Nous vous recommandons également de faire en sorte que les mots de *pwcInBuf* correspondent le mieux possible au texte source.</span><span class="sxs-lookup"><span data-stu-id="61423-129">We also recommend that the words in *pwcInBuf* match the source text as closely as possible.</span></span> <span data-ttu-id="61423-130">Par exemple, conservez les majuscules et les accents lorsque cela est possible.</span><span class="sxs-lookup"><span data-stu-id="61423-130">For example, retain capitalization and accents where possible.</span></span>

<span data-ttu-id="61423-131">Cet appel doit être effectué pour chaque mot récupéré à partir de *pTextSource* , à l’exception de ceux pour lesquels l’appel [**IWordSink ::P utaltword**](iwordsink-putaltword.md) a été effectué.</span><span class="sxs-lookup"><span data-stu-id="61423-131">This call must be made for every word retrieved from *pTextSource* except those for which the [**IWordSink::PutAltWord**](iwordsink-putaltword.md) call was made.</span></span> <span data-ttu-id="61423-132">Le mot se termine par un caractère EOW lorsqu’il est enregistré dans le WordSink.</span><span class="sxs-lookup"><span data-stu-id="61423-132">The word is terminated with an EOW character when it is saved to the WordSink.</span></span>

## <a name="requirements"></a><span data-ttu-id="61423-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61423-133">Requirements</span></span>



| <span data-ttu-id="61423-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="61423-134">Requirement</span></span> | <span data-ttu-id="61423-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="61423-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="61423-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61423-136">Minimum supported client</span></span><br/> | <span data-ttu-id="61423-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61423-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="61423-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="61423-138">Minimum supported server</span></span><br/> | <span data-ttu-id="61423-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="61423-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="61423-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="61423-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="61423-141"><dt>Rechercher. h</dt></span><span class="sxs-lookup"><span data-stu-id="61423-141"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61423-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61423-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61423-143">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="61423-143">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
