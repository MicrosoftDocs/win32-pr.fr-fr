---
description: Met un saut après le mot précédent.
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: IWordSink ::P méthode utBreak (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318149"
---
# <a name="iwordsinkputbreak-method"></a><span data-ttu-id="6696d-103">IWordSink ::P méthode utBreak</span><span class="sxs-lookup"><span data-stu-id="6696d-103">IWordSink::PutBreak method</span></span>

<span data-ttu-id="6696d-104">Met un saut après le mot précédent.</span><span class="sxs-lookup"><span data-stu-id="6696d-104">Puts a break after the preceding word.</span></span>

## <a name="syntax"></a><span data-ttu-id="6696d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6696d-105">Syntax</span></span>


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a><span data-ttu-id="6696d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6696d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6696d-107">*breakType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6696d-107">*breakType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6696d-108">Valeur de [**\_ \_ type break WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) qui indique le type de saut que le WordSink insère après le mot précédent.</span><span class="sxs-lookup"><span data-stu-id="6696d-108">A value from [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) that indicates the type of break that the WordSink inserts after the preceding word.</span></span> <span data-ttu-id="6696d-109">Chaque saut occupe une position unique dans l’index.</span><span class="sxs-lookup"><span data-stu-id="6696d-109">Each break occupies a unique position in the index.</span></span> <span data-ttu-id="6696d-110">Par conséquent, l’insertion de séparateurs entre les mots modifie la distance relative entre les mots.</span><span class="sxs-lookup"><span data-stu-id="6696d-110">Therefore, inserting breaks between words changes the relative distance between words.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6696d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6696d-111">Return value</span></span>

<span data-ttu-id="6696d-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="6696d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="6696d-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6696d-113">Return code</span></span>                                                                          | <span data-ttu-id="6696d-114">Description</span><span class="sxs-lookup"><span data-stu-id="6696d-114">Description</span></span>                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="6696d-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6696d-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6696d-116">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="6696d-116">The operation was completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6696d-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6696d-117">Remarks</span></span>

<span data-ttu-id="6696d-118">Les méthodes [**IWordSinkPutWord**](iwordsink-putword.md) et [**IWordSink ::P utaltword**](iwordsink-putaltword.md) insèrent automatiquement une coupure de mot (EOW, indiquée par l' \_ élément WORDREP Break \_ EOW du type énuméré de [**\_ \_ type break WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) ) après chaque mot.</span><span class="sxs-lookup"><span data-stu-id="6696d-118">The [**IWordSinkPutWord**](iwordsink-putword.md) and [**IWordSink::PutAltWord**](iwordsink-putaltword.md) methods automatically insert an end-of-word break (EOW, indicated by the WORDREP\_BREAK\_EOW element of the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type) after each word.</span></span> <span data-ttu-id="6696d-119">Appelez la méthode **PutBreak** pour insérer un type d’arrêt autre que la fin du mot.</span><span class="sxs-lookup"><span data-stu-id="6696d-119">Call the **PutBreak** method to insert a break type other than end of word.</span></span> <span data-ttu-id="6696d-120">Cette méthode ne modifie pas la mémoire tampon de texte source (*pSourceText*) ou incrémente le nombre de caractères (*CWC*).</span><span class="sxs-lookup"><span data-stu-id="6696d-120">This method does not change the source text buffer (*pSourceText*) or increment the character count (*cwc*).</span></span> <span data-ttu-id="6696d-121">Toutefois, elle incrémente la position actuelle dans l’index et affecte les résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="6696d-121">However, it does increment the current position in the index and affects query results.</span></span>

## <a name="requirements"></a><span data-ttu-id="6696d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6696d-122">Requirements</span></span>



| <span data-ttu-id="6696d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6696d-123">Requirement</span></span> | <span data-ttu-id="6696d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6696d-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6696d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6696d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6696d-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6696d-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6696d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6696d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6696d-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6696d-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6696d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="6696d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6696d-130"><dt>Rechercher. h</dt></span><span class="sxs-lookup"><span data-stu-id="6696d-130"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6696d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6696d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6696d-132">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="6696d-132">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
