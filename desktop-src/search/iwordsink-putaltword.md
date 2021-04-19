---
description: Place un autre mot et sa position dans l’objet IWordSink.
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: IWordSink ::P méthode utAltWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515416"
---
# <a name="iwordsinkputaltword-method"></a><span data-ttu-id="b21fc-103">IWordSink ::P méthode utAltWord</span><span class="sxs-lookup"><span data-stu-id="b21fc-103">IWordSink::PutAltWord method</span></span>

<span data-ttu-id="b21fc-104">Place un autre mot et sa position dans l’objet [**IWordSink**](iwordsink.md) .</span><span class="sxs-lookup"><span data-stu-id="b21fc-104">Puts an alternative word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b21fc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b21fc-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="b21fc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b21fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b21fc-107">*CWC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b21fc-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b21fc-108">Nombre de caractères dans *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="b21fc-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="b21fc-109">*pwcInBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b21fc-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b21fc-110">Pointeur vers une mémoire tampon qui contient une autre forme d’un mot du texte source.</span><span class="sxs-lookup"><span data-stu-id="b21fc-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="b21fc-111">Ce paramètre n’est pas modifié par **PutAltWord**.</span><span class="sxs-lookup"><span data-stu-id="b21fc-111">This parameter is not modified by **PutAltWord**.</span></span> <span data-ttu-id="b21fc-112">Vous pouvez transmettre le paramètre *pTextSource* à partir de [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b21fc-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="b21fc-113">*cwcSrcLen* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b21fc-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b21fc-114">Nombre de caractères dans la mémoire tampon de texte source (indiqué par le paramètre *pTextSource* à [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) qui correspond au mot contenu dans *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="b21fc-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="b21fc-115">*cwcSrcPos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b21fc-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b21fc-116">Position de départ du mot dans *pwcInBuf* dans la mémoire tampon de texte source (indiquée par le paramètre *pTextSource* à [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="b21fc-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b21fc-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b21fc-117">Return value</span></span>

<span data-ttu-id="b21fc-118">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b21fc-118">This method can return one of these values.</span></span>



| <span data-ttu-id="b21fc-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b21fc-119">Return code</span></span>                                                                                              | <span data-ttu-id="b21fc-120">Description</span><span class="sxs-lookup"><span data-stu-id="b21fc-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b21fc-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b21fc-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="b21fc-122">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="b21fc-122">The operation was completed successfully.</span></span> <span data-ttu-id="b21fc-123">Indique également qu’il ne reste plus de texte à traiter.</span><span class="sxs-lookup"><span data-stu-id="b21fc-123">Also indicates that no more text remains to be processed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="b21fc-124"><dt>**Langue \_ \_ \_ mot S grand**</dt></span><span class="sxs-lookup"><span data-stu-id="b21fc-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="b21fc-125">La valeur de *CWC* est supérieure à la valeur de *UlMaxTokenSize* spécifiée dans [**IWordBreaker :: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span><span class="sxs-lookup"><span data-stu-id="b21fc-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="b21fc-126">Notes</span><span class="sxs-lookup"><span data-stu-id="b21fc-126">Remarks</span></span>

<span data-ttu-id="b21fc-127">**PutAltWord** place une autre forme de mot dans le [**IWordSink**](iwordsink.md).</span><span class="sxs-lookup"><span data-stu-id="b21fc-127">**PutAltWord** puts an alternative form of a word in the [**IWordSink**](iwordsink.md).</span></span> <span data-ttu-id="b21fc-128">Le mot est placé à la même position que le mot d’origine dans la source de texte (*pTextSource* dans [**IWordBreaker :: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="b21fc-128">The word is put in the same position as the original word in the text source (*pTextSource* in [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span> <span data-ttu-id="b21fc-129">Par défaut, **PutAltWord** met fin à des mots avec un type d’arrêt **WORDREP \_ break \_ EOW** à partir du type énuméré de [**\_ \_ type break WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b21fc-129">By default, **PutAltWord** terminates words with a **WORDREP\_BREAK\_EOW** break type from the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="b21fc-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b21fc-130">Requirements</span></span>



| <span data-ttu-id="b21fc-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b21fc-131">Requirement</span></span> | <span data-ttu-id="b21fc-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="b21fc-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b21fc-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b21fc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b21fc-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b21fc-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b21fc-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b21fc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b21fc-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b21fc-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b21fc-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="b21fc-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b21fc-138"><dt>Rechercher. h</dt></span><span class="sxs-lookup"><span data-stu-id="b21fc-138"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b21fc-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b21fc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b21fc-140">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="b21fc-140">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
