---
description: Met une autre forme d’un mot dans l’objet IWordFormSink.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: IWordFormSink ::P méthode utAltWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 43539bbf67e23bc37ca92f6a961b945ae581e746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750357"
---
# <a name="iwordformsinkputaltword-method"></a><span data-ttu-id="414cc-103">IWordFormSink ::P méthode utAltWord</span><span class="sxs-lookup"><span data-stu-id="414cc-103">IWordFormSink::PutAltWord method</span></span>

<span data-ttu-id="414cc-104">Met une autre forme d’un mot dans l’objet [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .</span><span class="sxs-lookup"><span data-stu-id="414cc-104">Puts an alternative form of a word in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="414cc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="414cc-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="414cc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="414cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="414cc-107">*pwcInBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="414cc-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="414cc-108">Pointeur vers une mémoire tampon qui contient une autre forme d’un mot.</span><span class="sxs-lookup"><span data-stu-id="414cc-108">A pointer to a buffer that contains an alternative form of a word.</span></span>

</dd> <dt>

<span data-ttu-id="414cc-109">*CWC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="414cc-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="414cc-110">Nombre de caractères dans *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="414cc-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="414cc-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="414cc-111">Return value</span></span>

<span data-ttu-id="414cc-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="414cc-112">This method can return one of these values.</span></span>



| <span data-ttu-id="414cc-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="414cc-113">Return code</span></span>                                                                                              | <span data-ttu-id="414cc-114">Description</span><span class="sxs-lookup"><span data-stu-id="414cc-114">Description</span></span>                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="414cc-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="414cc-115"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="414cc-116">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="414cc-116">The operation was completed successfully.</span></span> <br/>                                                                                             |
| <dl> <span data-ttu-id="414cc-117"><dt>**Langue \_ \_ \_ mot S grand**</dt></span><span class="sxs-lookup"><span data-stu-id="414cc-117"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="414cc-118">La valeur de *CWC* est supérieure à la valeur de *UlMaxTokenSize* spécifiée dans [**IStemmer :: init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init).</span><span class="sxs-lookup"><span data-stu-id="414cc-118">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IStemmer::Init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="414cc-119">Notes</span><span class="sxs-lookup"><span data-stu-id="414cc-119">Remarks</span></span>

<span data-ttu-id="414cc-120">Cette méthode est appelée à partir de la méthode [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) de l’implémentation [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) .</span><span class="sxs-lookup"><span data-stu-id="414cc-120">This method is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="414cc-121">Toutes les autres formes d’un mot, à l’exception de la dernière, sont placées dans l’objet [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) en appelant **IWordFormSink ::P utaltword**.</span><span class="sxs-lookup"><span data-stu-id="414cc-121">All alternative forms for a word, except the last, are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling **IWordFormSink::PutAltWord**.</span></span> <span data-ttu-id="414cc-122">La forme alternative finale d’un mot, qui est toujours la forme d’origine du mot, est gérée en appelant [**IWordFormSink ::P utword**](iwordformsink-putword.md).</span><span class="sxs-lookup"><span data-stu-id="414cc-122">The final alternative form of a word, which is always the original form of the word, is handled by calling [**IWordFormSink::PutWord**](iwordformsink-putword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="414cc-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="414cc-123">Requirements</span></span>



| <span data-ttu-id="414cc-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="414cc-124">Requirement</span></span> | <span data-ttu-id="414cc-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="414cc-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="414cc-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="414cc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="414cc-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="414cc-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="414cc-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="414cc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="414cc-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="414cc-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="414cc-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="414cc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="414cc-131"><dt>Rechercher. h</dt></span><span class="sxs-lookup"><span data-stu-id="414cc-131"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="414cc-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="414cc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="414cc-133">**IWordFormSink**</span><span class="sxs-lookup"><span data-stu-id="414cc-133">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
