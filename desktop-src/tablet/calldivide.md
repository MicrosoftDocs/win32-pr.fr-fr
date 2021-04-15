---
description: Récupère des informations d’analyse à partir de l’objet InkDivider.
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: CallDivide fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524404"
---
# <a name="calldivide-function"></a><span data-ttu-id="04757-103">CallDivide fonction)</span><span class="sxs-lookup"><span data-stu-id="04757-103">CallDivide function</span></span>

<span data-ttu-id="04757-104">Récupère des informations d’analyse à partir de l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="04757-104">Retrieves analysis information from the [**InkDivider**](inkdivider-class.md) object.</span></span>

<span data-ttu-id="04757-105">Cette fonction n’est pas destinée à être utilisée par le code d’application.</span><span class="sxs-lookup"><span data-stu-id="04757-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="04757-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04757-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a><span data-ttu-id="04757-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04757-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04757-108">*hDivider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04757-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04757-109">Handle de l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="04757-109">A handle to the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="04757-110">*pWordSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04757-110">*pWordSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04757-111">Taille du mot retourné par l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="04757-111">The size of the word returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="04757-112">*pLineSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04757-112">*pLineSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04757-113">Taille de la ligne retournée par l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="04757-113">The size of the line returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="04757-114">*pParagraphSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04757-114">*pParagraphSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04757-115">Taille du paragraphe retourné par l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="04757-115">The size of the paragraph returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="04757-116">*pDrawingSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="04757-116">*pDrawingSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04757-117">Taille du dessin retourné par l’objet [**InkDivider**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="04757-117">The size of the drawing returned by the [**InkDivider**](inkdivider-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="04757-118">*pWordCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="04757-118">*pWordCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04757-119">Nombre de mots retournés par l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="04757-119">The number of words returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="04757-120">*pLineCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="04757-120">*pLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04757-121">Nombre de lignes retournées par l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="04757-121">The number of lines returned by ink analysis.</span></span>

</dd> <dt>

<span data-ttu-id="04757-122">*pParagraphCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="04757-122">*pParagraphCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="04757-123">Nombre de paragraphes renvoyés par l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="04757-123">The number of paragraphs returned by ink analysis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04757-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="04757-124">Return value</span></span>

<span data-ttu-id="04757-125">Cette fonction peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="04757-125">This function can return one of these values.</span></span>



| <span data-ttu-id="04757-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="04757-126">Return code</span></span>                                                                                  | <span data-ttu-id="04757-127">Description</span><span class="sxs-lookup"><span data-stu-id="04757-127">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="04757-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="04757-128"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="04757-129">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="04757-129">The function suceeded.</span></span><br/>              |
| <dl> <span data-ttu-id="04757-130"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="04757-130"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="04757-131">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="04757-131">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="04757-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="04757-132">Requirements</span></span>



| <span data-ttu-id="04757-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="04757-133">Requirement</span></span> | <span data-ttu-id="04757-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="04757-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04757-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04757-135">Minimum supported client</span></span><br/> | <span data-ttu-id="04757-136">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="04757-136">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="04757-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="04757-137">Minimum supported server</span></span><br/> | <span data-ttu-id="04757-138">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="04757-138">None supported</span></span><br/>                                                             |
| <span data-ttu-id="04757-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="04757-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="04757-140"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04757-140"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




