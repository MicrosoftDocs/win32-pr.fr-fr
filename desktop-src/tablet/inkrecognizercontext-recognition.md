---
description: Se produit lorsque le InkRecognizerContext a généré des résultats de la méthode BackgroundRecognize.
ms.assetid: 0cc319af-cd0b-4089-928b-cae6c86f6f61
title: Événement InkRecognizerContext. Recognition (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86da1a7470169f9f978e92a87f3e32f7e63acb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520715"
---
# <a name="inkrecognizercontextrecognition-event"></a><span data-ttu-id="8c30a-103">Événement InkRecognizerContext. Recognition</span><span class="sxs-lookup"><span data-stu-id="8c30a-103">InkRecognizerContext.Recognition event</span></span>

<span data-ttu-id="8c30a-104">Se produit lorsque le [**InkRecognizerContext**](inkrecognizercontext-class.md) a généré des résultats de la méthode [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) .</span><span class="sxs-lookup"><span data-stu-id="8c30a-104">Occurs when the [**InkRecognizerContext**](inkrecognizercontext-class.md) has generated results from the [**BackgroundRecognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c30a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c30a-105">Syntax</span></span>


```C++
void Recognition(
  [in] BSTR                 RecognizedString,
  [in] VARIANT              CustomData,
  [in] InkRecognitionStatus RecognitionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="8c30a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c30a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c30a-107">*RecognizedString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c30a-107">*RecognizedString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c30a-108">Texte de résultat de la reconnaissance avec la confiance la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="8c30a-108">The recognition result text with the highest confidence.</span></span>

<span data-ttu-id="8c30a-109">Pour plus d’informations sur le type de données BSTR, consultez la page [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="8c30a-109">For more information about the BSTR data type, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c30a-110">*CustomData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c30a-110">*CustomData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c30a-111">Objet qui contient les données personnalisées pour le résultat de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="8c30a-111">The object that contains the custom data for the recognition result.</span></span>

<span data-ttu-id="8c30a-112">Pour plus d’informations sur la structure de la variante, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="8c30a-112">For more information about the VARIANT structure, see the [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c30a-113">*RecognitionStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8c30a-113">*RecognitionStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c30a-114">État de reconnaissance en tant que résultat de reconnaissance le plus récent.</span><span class="sxs-lookup"><span data-stu-id="8c30a-114">The recognition status as of the most recent recognition result.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c30a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8c30a-115">Return value</span></span>

<span data-ttu-id="8c30a-116">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8c30a-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c30a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="8c30a-117">Remarks</span></span>

<span data-ttu-id="8c30a-118">Le comportement de l’interface de programmation d’applications (API) est imprévisible si vous essayez d’accéder à l’objet [**InkRecognizerContext**](inkrecognizercontext-class.md) d’origine à partir du gestionnaire d’événements de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="8c30a-118">The behavior of the application programming interface (API) is unpredictable if you try to gain access to the original [**InkRecognizerContext**](inkrecognizercontext-class.md) object from the recognition event handler.</span></span> <span data-ttu-id="8c30a-119">N’essayez pas de le faire.</span><span class="sxs-lookup"><span data-stu-id="8c30a-119">Do not attempt to do this.</span></span> <span data-ttu-id="8c30a-120">Au lieu de cela, si vous avez besoin de le faire, créez un indicateur et définissez-le dans le gestionnaire d’événements de [reconnaissance](ink-recognition.md) .</span><span class="sxs-lookup"><span data-stu-id="8c30a-120">Instead, if you need to do this, create a flag and set it in the [Recognition](ink-recognition.md) event handler.</span></span> <span data-ttu-id="8c30a-121">Vous pouvez ensuite interroger cet indicateur pour déterminer quand modifier les propriétés de **InkRecognizerContext** en dehors du gestionnaire d’événements.</span><span class="sxs-lookup"><span data-stu-id="8c30a-121">Then you can poll that flag to determine when to change the **InkRecognizerContext** properties outside of the event handler.</span></span>

<span data-ttu-id="8c30a-122">Cette méthode d’événement est définie dans l' \_ interface IInkEvents.</span><span class="sxs-lookup"><span data-stu-id="8c30a-122">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="8c30a-123">L' \_ interface IInkEvents implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IRERecognition.</span><span class="sxs-lookup"><span data-stu-id="8c30a-123">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IRERecognition.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c30a-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c30a-124">Requirements</span></span>



| <span data-ttu-id="8c30a-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8c30a-125">Requirement</span></span> | <span data-ttu-id="8c30a-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c30a-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c30a-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c30a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8c30a-128">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8c30a-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8c30a-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c30a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8c30a-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8c30a-130">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8c30a-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c30a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c30a-132"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="8c30a-132"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8c30a-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8c30a-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="8c30a-134"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c30a-134"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8c30a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8c30a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c30a-136">**InkRecognizerContext, classe**</span><span class="sxs-lookup"><span data-stu-id="8c30a-136">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> <dt>

[<span data-ttu-id="8c30a-137">**Méthode BackgroundRecognize**</span><span class="sxs-lookup"><span data-stu-id="8c30a-137">**BackgroundRecognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognize)
</dt> <dt>

[<span data-ttu-id="8c30a-138">**Énumération InkRecognitionStatus**</span><span class="sxs-lookup"><span data-stu-id="8c30a-138">**InkRecognitionStatus Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionstatus)
</dt> <dt>

[<span data-ttu-id="8c30a-139">**Recognize, méthode**</span><span class="sxs-lookup"><span data-stu-id="8c30a-139">**Recognize Method**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize)
</dt> <dt>

[<span data-ttu-id="8c30a-140">**Interface IInkRecognitionResult**</span><span class="sxs-lookup"><span data-stu-id="8c30a-140">**IInkRecognitionResult Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)
</dt> </dl>

 

