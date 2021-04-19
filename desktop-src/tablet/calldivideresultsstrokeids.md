---
description: Récupère les propriétés d’ID pour les objets IInkStrokeDisp du mot, de la ligne, du paragraphe ou du dessin correspondants, déterminés par l’analyse de l’encre.
ms.assetid: f05ffa3b-2a47-46fe-bb8f-e682aa094b69
title: CallDivideResultsStrokeIds fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivideResultsStrokeIds
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: ee690c9564df3b8c75eca6eec8eeb88b7531f4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514761"
---
# <a name="calldivideresultsstrokeids-function"></a><span data-ttu-id="c497c-103">CallDivideResultsStrokeIds fonction)</span><span class="sxs-lookup"><span data-stu-id="c497c-103">CallDivideResultsStrokeIds function</span></span>

<span data-ttu-id="c497c-104">Récupère les propriétés d' [**ID**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) pour les objets [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) du mot, de la ligne, du paragraphe ou du dessin correspondants, déterminés par l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="c497c-104">Retrieves the [**Id**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokedisp-get_id) properties for the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects of the corresponding word, line, paragraph, or drawing determined by ink analysis.</span></span>

<span data-ttu-id="c497c-105">Cette fonction n’est pas destinée à être utilisée par le code d’application.</span><span class="sxs-lookup"><span data-stu-id="c497c-105">This function is not intended to be used by application code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c497c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c497c-106">Syntax</span></span>


```C++
HRESULT WINAPI CallDivideResultsStrokeIds(
  _In_  INT_PTR hDivider,
  _Out_ int     aWordStrokeIds[],
  _Out_ int     aLineStrokeIds[],
  _Out_ int     aParagraphStrokeIds[],
  _Out_ int     aDrawingStrokeIds[]
);
```



## <a name="parameters"></a><span data-ttu-id="c497c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c497c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c497c-108">*hDivider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c497c-108">*hDivider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c497c-109">Handle de l’objet de [séparateur](the-divider-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c497c-109">A handle to the [Divider](the-divider-object.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="c497c-110">*\[ aWordStrokeIds \]* en \[ sortie\]</span><span class="sxs-lookup"><span data-stu-id="c497c-110">*aWordStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c497c-111">Tableau des ID de trait de l’encre dans le mot.</span><span class="sxs-lookup"><span data-stu-id="c497c-111">An array of the stroke IDs of the ink in the word.</span></span>

</dd> <dt>

<span data-ttu-id="c497c-112">*\[ aLineStrokeIds \]* en \[ sortie\]</span><span class="sxs-lookup"><span data-stu-id="c497c-112">*aLineStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c497c-113">Tableau des ID de trait de l’encre dans la ligne.</span><span class="sxs-lookup"><span data-stu-id="c497c-113">An array of the stroke IDs of the ink in the line.</span></span>

</dd> <dt>

<span data-ttu-id="c497c-114">*\[ aParagraphStrokeIds \]* en \[ sortie\]</span><span class="sxs-lookup"><span data-stu-id="c497c-114">*aParagraphStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c497c-115">Tableau des ID de trait de l’encre dans le paragraphe.</span><span class="sxs-lookup"><span data-stu-id="c497c-115">An array of the stroke IDs of the ink in the paragraph.</span></span>

</dd> <dt>

<span data-ttu-id="c497c-116">*\[ aDrawingStrokeIds \]* en \[ sortie\]</span><span class="sxs-lookup"><span data-stu-id="c497c-116">*aDrawingStrokeIds\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c497c-117">Tableau des ID de trait de l’encre dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="c497c-117">An array of the stroke IDs of the ink in the drawing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c497c-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c497c-118">Return value</span></span>

<span data-ttu-id="c497c-119">Cette fonction peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="c497c-119">This function can return one of these values.</span></span>



| <span data-ttu-id="c497c-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c497c-120">Return code</span></span>                                                                                  | <span data-ttu-id="c497c-121">Description</span><span class="sxs-lookup"><span data-stu-id="c497c-121">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="c497c-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c497c-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c497c-123">La fonction a réussi.</span><span class="sxs-lookup"><span data-stu-id="c497c-123">The function succeeded.</span></span><br/>              |
| <dl> <span data-ttu-id="c497c-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c497c-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c497c-125">Le paramètre *hDivider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c497c-125">The *hDivider* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c497c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c497c-126">Requirements</span></span>



| <span data-ttu-id="c497c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c497c-127">Requirement</span></span> | <span data-ttu-id="c497c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c497c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c497c-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c497c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c497c-130">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c497c-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="c497c-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c497c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c497c-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c497c-132">None supported</span></span><br/>                                                             |
| <span data-ttu-id="c497c-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c497c-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="c497c-134"><dt>InkDiv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c497c-134"><dt>InkDiv.dll</dt></span></span> </dl> |



 

 




