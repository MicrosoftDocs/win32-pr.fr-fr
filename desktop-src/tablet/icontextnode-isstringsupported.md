---
description: Indique si la chaîne reconnue de ce IContextNode provient du dictionnaire système, du dictionnaire de l’utilisateur ou de la liste de mots.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'IContextNode :: IsStringSupported, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 853b244cdd6f9e61d4474876190daeccaa2c8779
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515470"
---
# <a name="icontextnodeisstringsupported-method"></a><span data-ttu-id="d8ead-103">IContextNode :: IsStringSupported, méthode</span><span class="sxs-lookup"><span data-stu-id="d8ead-103">IContextNode::IsStringSupported method</span></span>

<span data-ttu-id="d8ead-104">Indique si la chaîne reconnue de ce [**IContextNode**](icontextnode.md) provient du dictionnaire système, du dictionnaire de l’utilisateur ou de la liste de mots.</span><span class="sxs-lookup"><span data-stu-id="d8ead-104">Indicates whether recognized string of this [**IContextNode**](icontextnode.md) came from the system dictionary, user dictionary, or word list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8ead-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8ead-105">Syntax</span></span>


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a><span data-ttu-id="d8ead-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8ead-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8ead-107">*pfIsSupported* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d8ead-107">*pfIsSupported* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d8ead-108">**Variante \_ TRUE** si la valeur de chaîne reconnue de ce [**IContextNode**](icontextnode.md) est prise en charge par le [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) avec les nœuds indicateurs correspondants appliqués ; Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="d8ead-108">**VARIANT\_TRUE** if the recognized string value of this [**IContextNode**](icontextnode.md) is supported by the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) with any corresponding hint nodes applied; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8ead-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8ead-109">Return value</span></span>

<span data-ttu-id="d8ead-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="d8ead-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8ead-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8ead-111">Requirements</span></span>



| <span data-ttu-id="d8ead-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8ead-112">Requirement</span></span> | <span data-ttu-id="d8ead-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8ead-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8ead-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8ead-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d8ead-115">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8ead-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d8ead-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8ead-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d8ead-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8ead-117">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="d8ead-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8ead-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8ead-119"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d8ead-119"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d8ead-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d8ead-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8ead-121"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8ead-121"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="d8ead-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8ead-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8ead-123">**IContextNode**</span><span class="sxs-lookup"><span data-stu-id="d8ead-123">**IContextNode**</span></span>](icontextnode.md)
</dt> </dl>

 

 




