---
description: Se produit lorsque la classe InkRecognizerContext a généré des résultats après l’appel de la méthode de méthode BackgroundRecognizeWithAlternates.
ms.assetid: 5e86a4d5-c0a7-4283-81cc-ec3a26f74880
title: Événement InkRecognizerContext. RecognitionWithAlternates (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a7d35d8281305b0cb5f84114bb2f2fa0e718c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203817"
---
# <a name="inkrecognizercontextrecognitionwithalternates-event"></a><span data-ttu-id="fa8e6-103">Événement InkRecognizerContext. RecognitionWithAlternates</span><span class="sxs-lookup"><span data-stu-id="fa8e6-103">InkRecognizerContext.RecognitionWithAlternates event</span></span>

<span data-ttu-id="fa8e6-104">Se produit lorsque la [**classe InkRecognizerContext**](inkrecognizercontext-class.md) a généré des résultats après l’appel de la méthode de [**méthode BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) .</span><span class="sxs-lookup"><span data-stu-id="fa8e6-104">Occurs when the [**InkRecognizerContext Class**](inkrecognizercontext-class.md) has generated results after calling the [**BackgroundRecognizeWithAlternates Method**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa8e6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa8e6-105">Syntax</span></span>


```C++
void RecognitionWithAlternates(
  [in] IInkRecognitionResult *RecognitionResult,
  [in] VARIANT               CustomData,
  [in] InkRecognitionStatus  RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="fa8e6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa8e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa8e6-107">*RecognitionResult* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa8e6-107">*RecognitionResult* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa8e6-108">Résultat de la reconnaissance de l’événement.</span><span class="sxs-lookup"><span data-stu-id="fa8e6-108">The recognition result from the event.</span></span>

</dd> <dt>

<span data-ttu-id="fa8e6-109">*CustomData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa8e6-109">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa8e6-110">Données personnalisées pour le résultat de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="fa8e6-110">The custom data for the recognition result.</span></span>

<span data-ttu-id="fa8e6-111">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="fa8e6-111">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="fa8e6-112">*RecognitionStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa8e6-112">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa8e6-113">État de reconnaissance en tant que résultat de reconnaissance le plus récent.</span><span class="sxs-lookup"><span data-stu-id="fa8e6-113">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa8e6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa8e6-114">Return value</span></span>

<span data-ttu-id="fa8e6-115">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fa8e6-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa8e6-116">Notes</span><span class="sxs-lookup"><span data-stu-id="fa8e6-116">Remarks</span></span>

<span data-ttu-id="fa8e6-117">Le comportement de l’interface de programmation d’applications (API) est imprévisible si vous essayez d’accéder à l’objet [**InkRecognizerContext**](inkrecognizercontext-class.md) d’origine à partir du gestionnaire d’événements de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="fa8e6-117">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="fa8e6-118">N’essayez pas de le faire.</span><span class="sxs-lookup"><span data-stu-id="fa8e6-118">Do not attempt to do this.</span></span> <span data-ttu-id="fa8e6-119">Au lieu de cela, si vous avez besoin de le faire, créez un indicateur et définissez-le dans le gestionnaire d’événements de [**reconnaissance**](inkrecognizercontext-recognition.md) .</span><span class="sxs-lookup"><span data-stu-id="fa8e6-119">Instead, if you need to do this, create a flag and set it in the [**Recognition**](inkrecognizercontext-recognition.md) event handler.</span></span> <span data-ttu-id="fa8e6-120">Vous pouvez ensuite interroger cet indicateur pour déterminer quand modifier les propriétés de **InkRecognizerContext** en dehors du gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="fa8e6-120">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="fa8e6-121">Cette méthode d’événement est définie dans l' \_ interface IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="fa8e6-121">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="fa8e6-122">L' \_ interface IInkEvents implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IRERecognitionWithAlternates.</span><span class="sxs-lookup"><span data-stu-id="fa8e6-122">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognitionWithAlternates.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa8e6-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa8e6-123">Requirements</span></span>



| <span data-ttu-id="fa8e6-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa8e6-124">Requirement</span></span> | <span data-ttu-id="fa8e6-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa8e6-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa8e6-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa8e6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="fa8e6-127">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa8e6-127">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="fa8e6-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa8e6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="fa8e6-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa8e6-129">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="fa8e6-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa8e6-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa8e6-131"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="fa8e6-131"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="fa8e6-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fa8e6-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="fa8e6-133"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa8e6-133"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="fa8e6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa8e6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa8e6-135">**InkRecognizerContext, classe**</span><span class="sxs-lookup"><span data-stu-id="fa8e6-135">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="fa8e6-136">**Méthode BackgroundRecognizeWithAlternates**</span><span class="sxs-lookup"><span data-stu-id="fa8e6-136">**BackgroundRecognizeWithAlternates Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)
</dt> <dt>

[<span data-ttu-id="fa8e6-137">**Recognize, méthode**</span><span class="sxs-lookup"><span data-stu-id="fa8e6-137">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="fa8e6-138">**Interface IInkRecognitionResult**</span><span class="sxs-lookup"><span data-stu-id="fa8e6-138">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

