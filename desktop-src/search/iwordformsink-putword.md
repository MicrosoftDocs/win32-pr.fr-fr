---
description: Place le formulaire Word d’origine dans l’objet IWordFormSink.
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: IWordFormSink ::P méthode utWord (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514791"
---
# <a name="iwordformsinkputword-method"></a><span data-ttu-id="69a02-103">IWordFormSink ::P méthode utWord</span><span class="sxs-lookup"><span data-stu-id="69a02-103">IWordFormSink::PutWord method</span></span>

<span data-ttu-id="69a02-104">Place le formulaire Word d’origine dans l’objet [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .</span><span class="sxs-lookup"><span data-stu-id="69a02-104">Puts the original word form in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="69a02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69a02-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="69a02-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69a02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69a02-107">*pwcInBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69a02-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69a02-108">Pointeur vers une mémoire tampon qui contient la forme alternative finale d’un mot, qui est toujours le mot d’origine.</span><span class="sxs-lookup"><span data-stu-id="69a02-108">A pointer to a buffer that contains the final alternative form of a word, which is always the original word.</span></span>

</dd> <dt>

<span data-ttu-id="69a02-109">*CWC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="69a02-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69a02-110">Nombre de caractères dans *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="69a02-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69a02-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="69a02-111">Return value</span></span>

<span data-ttu-id="69a02-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="69a02-112">This method can return one of these values.</span></span>



| <span data-ttu-id="69a02-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="69a02-113">Return code</span></span>                                                                          | <span data-ttu-id="69a02-114">Description</span><span class="sxs-lookup"><span data-stu-id="69a02-114">Description</span></span>                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="69a02-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="69a02-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="69a02-116">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="69a02-116">The operation was completed successfully.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="69a02-117">Notes</span><span class="sxs-lookup"><span data-stu-id="69a02-117">Remarks</span></span>

<span data-ttu-id="69a02-118">**PutWord** est appelé à partir de la méthode [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) de l’implémentation [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) .</span><span class="sxs-lookup"><span data-stu-id="69a02-118">**PutWord** is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="69a02-119">Cette méthode gère la forme d’origine d’un mot et est appelée en dernier.</span><span class="sxs-lookup"><span data-stu-id="69a02-119">This method handles the original form of a word and is called last.</span></span> <span data-ttu-id="69a02-120">Toutes les autres formes précédentes pour un mot sont placées dans l’objet [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) en appelant [**IWordFormSink ::P utaltword**](iwordformsink-putphrase.md).</span><span class="sxs-lookup"><span data-stu-id="69a02-120">All preceding alternative forms for a word are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling [**IWordFormSink::PutAltWord**](iwordformsink-putphrase.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="69a02-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="69a02-121">Requirements</span></span>



| <span data-ttu-id="69a02-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="69a02-122">Requirement</span></span> | <span data-ttu-id="69a02-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="69a02-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="69a02-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69a02-124">Minimum supported client</span></span><br/> | <span data-ttu-id="69a02-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69a02-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="69a02-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="69a02-126">Minimum supported server</span></span><br/> | <span data-ttu-id="69a02-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="69a02-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="69a02-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="69a02-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="69a02-129"><dt>Rechercher. h</dt></span><span class="sxs-lookup"><span data-stu-id="69a02-129"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69a02-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="69a02-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69a02-131">**IWordFormSink**</span><span class="sxs-lookup"><span data-stu-id="69a02-131">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
