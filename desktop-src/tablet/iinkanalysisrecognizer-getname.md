---
description: Récupère le nom du module de reconnaissance.
ms.assetid: bd97fead-1e80-49dc-ada0-38eb5dc015ae
title: 'IInkAnalysisRecognizer :: GetName, méthode (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fe263878d1fd5e914cf033111997d297a20c54f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514631"
---
# <a name="iinkanalysisrecognizergetname-method"></a><span data-ttu-id="8a2f1-103">IInkAnalysisRecognizer :: GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="8a2f1-103">IInkAnalysisRecognizer::GetName method</span></span>

<span data-ttu-id="8a2f1-104">Récupère le nom du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="8a2f1-104">Retrieves the name of the recognizer.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a2f1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a2f1-105">Syntax</span></span>


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a><span data-ttu-id="8a2f1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a2f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a2f1-107">*pbstrName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8a2f1-107">*pbstrName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a2f1-108">Nom du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="8a2f1-108">The name of the recognizer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a2f1-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a2f1-109">Return value</span></span>

<span data-ttu-id="8a2f1-110">Pour obtenir une description des valeurs de retour, consultez [classes et interfaces-analyse](classes-and-interfaces---ink-analysis.md)de l’encre.</span><span class="sxs-lookup"><span data-stu-id="8a2f1-110">For a description of the return values, see [Classes and Interfaces - Ink Analysis](classes-and-interfaces---ink-analysis.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a2f1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8a2f1-111">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="8a2f1-112">Pour éviter une fuite de mémoire, appelez [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) sur \* *pbstrName* lorsque vous n’avez plus besoin d’utiliser la chaîne.</span><span class="sxs-lookup"><span data-stu-id="8a2f1-112">To avoid a memory leak, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) on \**pbstrName* when you no longer need to use the string.</span></span>

 

<span data-ttu-id="8a2f1-113">Le nom est localisé pour la langue indépendante de la région que le module de reconnaissance prend en charge.</span><span class="sxs-lookup"><span data-stu-id="8a2f1-113">The name is localized for the region-neutral language that the recognizer supports.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a2f1-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a2f1-114">Requirements</span></span>



| <span data-ttu-id="8a2f1-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a2f1-115">Requirement</span></span> | <span data-ttu-id="8a2f1-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a2f1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a2f1-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a2f1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8a2f1-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a2f1-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8a2f1-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a2f1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8a2f1-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a2f1-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="8a2f1-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a2f1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a2f1-122"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8a2f1-122"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8a2f1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8a2f1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a2f1-124"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a2f1-124"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="8a2f1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a2f1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a2f1-126">**IInkAnalysisRecognizer**</span><span class="sxs-lookup"><span data-stu-id="8a2f1-126">**IInkAnalysisRecognizer**</span></span>](iinkanalysisrecognizer.md)
</dt> <dt>

[<span data-ttu-id="8a2f1-127">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="8a2f1-127">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

