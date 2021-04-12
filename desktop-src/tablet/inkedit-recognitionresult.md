---
description: 'Se produit lorsque le contrôle InkEdit obtient les résultats manuellement à partir d’un appel à la méthode InkEdit :: Recognize ou automatiquement après le déclenchement du délai d’attente de reconnaissance.'
ms.assetid: 09618be0-fe49-494f-940f-79ff8352097e
title: Événement InkEdit. RecognitionResult (. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d6206293b604e5540b5e6d0271e1ebe984a987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210301"
---
# <a name="inkeditrecognitionresult-event"></a><span data-ttu-id="a30f5-103">Événement InkEdit. RecognitionResult</span><span class="sxs-lookup"><span data-stu-id="a30f5-103">InkEdit.RecognitionResult event</span></span>

<span data-ttu-id="a30f5-104">Se produit lorsque le contrôle [InkEdit](inkedit-control-reference.md) obtient les résultats manuellement à partir d’un appel à la méthode [**InkEdit :: Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) ou automatiquement après le déclenchement du délai d’attente de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a30f5-104">Occurs when the [InkEdit](inkedit-control-reference.md) control gets results manually from a call to the [**InkEdit::Recognize**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize) method or automatically after the recognition timeout fires.</span></span>

## <a name="syntax"></a><span data-ttu-id="a30f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a30f5-105">Syntax</span></span>


```C++
void RecognitionResult(
  [in] IInkRecognitionResult *RecognitionResult
);
```



## <a name="parameters"></a><span data-ttu-id="a30f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a30f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a30f5-107">*RecognitionResult* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a30f5-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a30f5-108">Objet [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) qui contient le résultat de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="a30f5-108">An [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object that contains the result of the recognition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a30f5-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a30f5-109">Return value</span></span>

<span data-ttu-id="a30f5-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a30f5-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a30f5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="a30f5-111">Remarks</span></span>

<span data-ttu-id="a30f5-112">Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="a30f5-112">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="a30f5-113">L’interface **\_ IInkEditEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IeeRecognitionResult.</span><span class="sxs-lookup"><span data-stu-id="a30f5-113">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeRecognitionResult.</span></span>

## <a name="requirements"></a><span data-ttu-id="a30f5-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a30f5-114">Requirements</span></span>



| <span data-ttu-id="a30f5-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a30f5-115">Requirement</span></span> | <span data-ttu-id="a30f5-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a30f5-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a30f5-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a30f5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a30f5-118">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a30f5-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="a30f5-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a30f5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a30f5-120">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a30f5-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="a30f5-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a30f5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a30f5-122"><dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="a30f5-122"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a30f5-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a30f5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="a30f5-124"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a30f5-124"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="a30f5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a30f5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30f5-126">InkEdit</span><span class="sxs-lookup"><span data-stu-id="a30f5-126">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="a30f5-127">[**Recognize, méthode \[ contrôle InkEdit\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span><span class="sxs-lookup"><span data-stu-id="a30f5-127">[**Recognize Method \[InkEdit Control\]**](/windows/desktop/api/inked/nf-inked-iinkedit-recognize)</span></span>
</dt> </dl>

 

