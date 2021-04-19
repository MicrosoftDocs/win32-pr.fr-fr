---
description: Indique si la chaîne reconnue spécifiée provient du dictionnaire système, du dictionnaire de l’utilisateur ou de la liste de mots.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'IContextNode :: IsAlternateStringSupported, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516481"
---
# <a name="icontextnodeisalternatestringsupported-method"></a><span data-ttu-id="9912c-103">IContextNode :: IsAlternateStringSupported, méthode</span><span class="sxs-lookup"><span data-stu-id="9912c-103">IContextNode::IsAlternateStringSupported method</span></span>

<span data-ttu-id="9912c-104">Indique si la chaîne reconnue spécifiée provient du dictionnaire système, du dictionnaire de l’utilisateur ou de la liste de mots.</span><span class="sxs-lookup"><span data-stu-id="9912c-104">Indicates whether the specified recognized string came from the system dictionary, user dictionary, or word list.</span></span> <span data-ttu-id="9912c-105">Toutes les données qui restreignent, telles que les listes de mots, les repères ou les Factoids, dans n’importe quel nœud d’indication correspondant seront utilisées pour déterminer si la chaîne est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="9912c-105">Any restricting data, like wordlists, guides or factoids, in any corresponding hint node will be used to determine if the string is supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="9912c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9912c-106">Syntax</span></span>


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="9912c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9912c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9912c-108">*bstrAlternateString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9912c-108">*bstrAlternateString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9912c-109">Chaîne reconnue à vérifier.</span><span class="sxs-lookup"><span data-stu-id="9912c-109">Recognized string to verify.</span></span>

</dd> <dt>

<span data-ttu-id="9912c-110">*pfIsSupported* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9912c-110">*pfIsSupported* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9912c-111">**Variante \_ TRUE** si la chaîne spécifiée est prise en charge par le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) avec les nœuds indicateurs correspondants appliqués ; **Variante \_ FALSe** s’il n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9912c-111">**VARIANT\_TRUE** if the specified string is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; **VARIANT\_FALSE** if not supported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9912c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9912c-112">Return value</span></span>

<span data-ttu-id="9912c-113">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="9912c-113">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9912c-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9912c-114">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="9912c-115">Spécifications</span><span class="sxs-lookup"><span data-stu-id="9912c-115">Requirements</span></span>



| <span data-ttu-id="9912c-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9912c-116">Requirement</span></span> | <span data-ttu-id="9912c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="9912c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9912c-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9912c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9912c-119">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9912c-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9912c-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9912c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9912c-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="9912c-121">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="9912c-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9912c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9912c-123"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9912c-123"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9912c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="9912c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9912c-125"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9912c-125"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="9912c-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9912c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9912c-127">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="9912c-127">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




