---
description: Récupère le nom du fournisseur du IInkAnalysisRecognizer.
ms.assetid: 62ff209e-2a34-4c04-90a0-661d06898298
title: 'IInkAnalysisRecognizer :: GetVendor, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetVendor
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a48bec62ed4a6a9d94d54ea3a1ba4a53eddd4b7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113358"
---
# <a name="iinkanalysisrecognizergetvendor-method"></a><span data-ttu-id="3ad19-103">IInkAnalysisRecognizer :: GetVendor, méthode</span><span class="sxs-lookup"><span data-stu-id="3ad19-103">IInkAnalysisRecognizer::GetVendor method</span></span>

<span data-ttu-id="3ad19-104">Récupère le nom du fournisseur du [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span><span class="sxs-lookup"><span data-stu-id="3ad19-104">Retrieves the vendor name of the [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3ad19-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ad19-105">Syntax</span></span>


```C++
HRESULT GetVendor(
  [out] BSTR *pbstrVendor
);
```



## <a name="parameters"></a><span data-ttu-id="3ad19-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ad19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ad19-107">*pbstrVendor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3ad19-107">*pbstrVendor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad19-108">Nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3ad19-108">The name of the vendor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ad19-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ad19-109">Return value</span></span>

<span data-ttu-id="3ad19-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="3ad19-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3ad19-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3ad19-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="3ad19-112">Pour éviter une fuite de mémoire, appelez [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) sur \* *pbstrVendor* lorsque vous n’avez plus besoin d’utiliser la chaîne.</span><span class="sxs-lookup"><span data-stu-id="3ad19-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrVendor* when you no longer need to use the string.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3ad19-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ad19-113">Requirements</span></span>



| <span data-ttu-id="3ad19-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ad19-114">Requirement</span></span> | <span data-ttu-id="3ad19-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ad19-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad19-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ad19-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad19-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ad19-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3ad19-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ad19-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad19-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ad19-119">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="3ad19-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ad19-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ad19-121"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3ad19-121"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3ad19-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3ad19-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ad19-123"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ad19-123"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="3ad19-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ad19-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ad19-125">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="3ad19-125">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="3ad19-126">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="3ad19-126">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

