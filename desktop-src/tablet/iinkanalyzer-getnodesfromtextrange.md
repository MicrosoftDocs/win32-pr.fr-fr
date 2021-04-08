---
description: Récupère une collection d’objets IContextNode qui sont pertinents pour la plage de texte spécifiée pour les nœuds de contexte spécifiés.
ms.assetid: 39a5dd52-7007-4395-8668-261eca78a090
title: 'IInkAnalyzer :: GetNodesFromTextRange, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetNodesFromTextRange
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ada60a64bb4e7d8b4604b18982630dabd7e44256
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751812"
---
# <a name="iinkanalyzergetnodesfromtextrange-method"></a><span data-ttu-id="85732-103">IInkAnalyzer :: GetNodesFromTextRange, méthode</span><span class="sxs-lookup"><span data-stu-id="85732-103">IInkAnalyzer::GetNodesFromTextRange method</span></span>

<span data-ttu-id="85732-104">Récupère une collection d’objets [**IContextNode**](icontextnode.md) qui sont pertinents pour la plage de texte spécifiée pour les nœuds de contexte spécifiés.</span><span class="sxs-lookup"><span data-stu-id="85732-104">Retrieves a collection of [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

## <a name="syntax"></a><span data-ttu-id="85732-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85732-105">Syntax</span></span>


```C++
HRESULT GetNodesFromTextRange(
  [in, out] LONG          *plStart,
  [in, out] LONG          *plLength,
  [out]     IContextNodes **ppContextNodes,
  [in]      IContextNodes *pNodesToSearch = defaultvalue
);
```



## <a name="parameters"></a><span data-ttu-id="85732-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85732-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85732-107">*plStart* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="85732-107">*plStart* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85732-108">Référence au début de la plage de texte dans la partie *pNodesToSearch* de la chaîne reconnue.</span><span class="sxs-lookup"><span data-stu-id="85732-108">A reference to the start of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="85732-109">*plLength* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="85732-109">*plLength* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85732-110">Référence à la longueur de la plage de texte dans la partie *pNodesToSearch* de la chaîne reconnue.</span><span class="sxs-lookup"><span data-stu-id="85732-110">A reference to the length of the text range in the *pNodesToSearch* portion of the recognized string.</span></span>

</dd> <dt>

<span data-ttu-id="85732-111">*ppContextNodes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="85732-111">*ppContextNodes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85732-112">Pointeur vers les objets [**IContextNode**](icontextnode.md) qui sont pertinents pour la plage de texte spécifiée pour les nœuds de contexte spécifiés.</span><span class="sxs-lookup"><span data-stu-id="85732-112">A pointer to the [**IContextNode**](icontextnode.md) objects that are relevant to the specified text range for the specified context nodes.</span></span>

</dd> <dt>

<span data-ttu-id="85732-113">*pNodesToSearch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85732-113">*pNodesToSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85732-114">Objets [**IContextNode**](icontextnode.md) auxquels limiter la recherche.</span><span class="sxs-lookup"><span data-stu-id="85732-114">The [**IContextNode**](icontextnode.md) objects to which to limit the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85732-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85732-115">Return value</span></span>

<span data-ttu-id="85732-116">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="85732-116">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="85732-117">Notes</span><span class="sxs-lookup"><span data-stu-id="85732-117">Remarks</span></span>

<span data-ttu-id="85732-118">La plage de texte spécifiée doit être relative à la partie *pNodesToSearch* de la chaîne reconnue du [**IInkAnalyzer**](iinkanalyzer.md), plutôt qu’à la chaîne reconnue du **IInkAnalyzer** entier.</span><span class="sxs-lookup"><span data-stu-id="85732-118">The specified text range should be relative to the *pNodesToSearch* portion of the recognized string of the [**IInkAnalyzer**](iinkanalyzer.md), rather than to the recognized string of the entire **IInkAnalyzer**.</span></span>

<span data-ttu-id="85732-119">Cette méthode modifie les valeurs des paramètres *plStart* et *plLength* en développant la plage de texte aux limites de mot les plus proches.</span><span class="sxs-lookup"><span data-stu-id="85732-119">This method modifies the values of the *plStart* and *plLength* parameters by expanding the text range to the nearest word boundaries.</span></span>

<span data-ttu-id="85732-120">Par exemple, si la chaîne reconnue est « je suis tardif » et que vous appelez cette méthode à l’aide des valeurs de paramètre de 6 pour *plStart* et 1 pour *plLength*, qui correspond à la lettre « a » dans « Late », cette méthode retourne une collection contenant un [**IContextNode**](icontextnode.md)unique, InkWord ou TextWord qui correspond au mot « Late ».</span><span class="sxs-lookup"><span data-stu-id="85732-120">For example, if the recognized string is "I am late" and you call this method using the parameter values of 6 for *plStart* and 1 for *plLength*, which corresponds to the letter "a" in "late", this method returns a collection containing a single [**IContextNode**](icontextnode.md), the InkWord or TextWord that corresponds to the word "late".</span></span> <span data-ttu-id="85732-121">Pour cet exemple, cette méthode modifie également la valeur de *plStart* à 5 et la valeur de *plLength* à 4, ce qui correspond au mot « Late ».</span><span class="sxs-lookup"><span data-stu-id="85732-121">For this example, this method also modifies the value of *plStart* to 5 and the value of *plLength* to 4, which corresponds to the word "late".</span></span>

> [!Note]  
> <span data-ttu-id="85732-122">Le paramètre *plStart* est relatif à la chaîne reconnue du paramètre *pNodesToSearch* .</span><span class="sxs-lookup"><span data-stu-id="85732-122">The *plStart* parameter is relative to the recognized string of the *pNodesToSearch* parameter.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="85732-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85732-123">Requirements</span></span>



| <span data-ttu-id="85732-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85732-124">Requirement</span></span> | <span data-ttu-id="85732-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="85732-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85732-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85732-126">Minimum supported client</span></span><br/> | <span data-ttu-id="85732-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="85732-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="85732-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="85732-128">Minimum supported server</span></span><br/> | <span data-ttu-id="85732-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="85732-129">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="85732-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="85732-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="85732-131"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="85732-131"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="85732-132">DLL</span><span class="sxs-lookup"><span data-stu-id="85732-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85732-133"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85732-133"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="85732-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85732-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85732-135">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="85732-135">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> </dl>

 

 




