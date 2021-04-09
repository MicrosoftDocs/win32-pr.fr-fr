---
description: L’objet diviseur utilise un RecognizerContext pour améliorer son analyse des segments de reconnaissance et pour générer un texte de reconnaissance pour les éléments d’écriture manuscrite.
ms.assetid: 33d9abc4-151e-47b4-b66f-ff6adfe21222
title: Utilisation d’un contexte de module de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdea8c59bc894a6962e8bbe7e58f316327a548e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034061"
---
# <a name="working-with-a-recognizer-context"></a><span data-ttu-id="e119b-103">Utilisation d’un contexte de module de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="e119b-103">Working with a Recognizer Context</span></span>

<span data-ttu-id="e119b-104">L’objet [**diviseur**](inkdivider-class.md) utilise un [**RecognizerContext**](inkrecognizercontext-class.md) pour améliorer son analyse des segments de reconnaissance et pour générer un texte de reconnaissance pour les éléments d’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="e119b-104">The [**Divider**](inkdivider-class.md) object uses a [**RecognizerContext**](inkrecognizercontext-class.md) to improve its analysis of recognition segments and to generate recognition text for handwriting elements.</span></span>

<span data-ttu-id="e119b-105">Vous pouvez définir le contexte de module de reconnaissance à l’aide de la propriété [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) de l’objet [**diviseur**](inkdivider-class.md) ou en fournissant le contexte de module de reconnaissance dans l’appel au constructeur de [diviseur](/previous-versions/ms839465(v=msdn.10)) (en code managé).</span><span class="sxs-lookup"><span data-stu-id="e119b-105">You can set the recognizer context by using the [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property of the [**Divider**](inkdivider-class.md) object or by supplying the recognizer context in the call to the [Divider](/previous-versions/ms839465(v=msdn.10)) constructor (in managed code).</span></span> <span data-ttu-id="e119b-106">Si un contexte de module de reconnaissance pour un module de reconnaissance sans écriture manuscrite ou pour un module de reconnaissance qui ne prend pas en charge la fonctionnalité d’entrée libre est assigné à la propriété **RecognizerContext** , une exception est levée.</span><span class="sxs-lookup"><span data-stu-id="e119b-106">If a recognizer context for a non-handwriting recognizer or for a recognizer that does not support the free input capability is assigned to the **RecognizerContext** property, then an exception is thrown.</span></span>

<span data-ttu-id="e119b-107">Si les identifiants ne sont pas installés ou si un contexte de module de reconnaissance n’est pas assigné à l’objet de [**séparateur**](inkdivider-class.md) , l’objet de **séparateur** n’utilise pas de contexte de module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="e119b-107">If recognizers are not installed or a recognizer context is not assigned to the [**Divider**](inkdivider-class.md) object, the **Divider** object does not use a recognizer context.</span></span> <span data-ttu-id="e119b-108">Dans ce cas, la fonction d’analyse de la disposition effectue la Division du segment, et aucun texte n’est associé à l’objet [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) .</span><span class="sxs-lookup"><span data-stu-id="e119b-108">In this case, the layout analysis feature performs the segment division, and no text is associated with the [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) object.</span></span>

> [!Note]  
> <span data-ttu-id="e119b-109">La propriété [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) ne peut pas être modifiée une fois que les traits ont été assignés à l’objet [**diviseur**](inkdivider-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e119b-109">The [**RecognizerContext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext) property cannot be changed after strokes have been assigned to the [**Divider**](inkdivider-class.md) object.</span></span> <span data-ttu-id="e119b-110">L’objet **diviseur** utilise les valeurs de propriété par défaut de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e119b-110">The **Divider** object uses the default property values of the [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span>

 

<span data-ttu-id="e119b-111">L’objet [**diviseur**](inkdivider-class.md) applique le contexte du module de reconnaissance aux éléments d’écriture manuscrite lors de l’analyse de la disposition.</span><span class="sxs-lookup"><span data-stu-id="e119b-111">The [**Divider**](inkdivider-class.md) object applies the recognizer context to handwritten elements during layout analysis.</span></span> <span data-ttu-id="e119b-112">Tous les traits que vous attribuez directement au contexte de module de reconnaissance sont ignorés par l’objet de **séparateur** .</span><span class="sxs-lookup"><span data-stu-id="e119b-112">Any strokes you assign directly to the recognizer context are ignored by the **Divider** object.</span></span> <span data-ttu-id="e119b-113">Pour plus d’informations sur la reconnaissance de texte, consultez à propos de la reconnaissance de l' [écriture manuscrite](about-handwriting-recognition.md).</span><span class="sxs-lookup"><span data-stu-id="e119b-113">For more information about text recognition, see [About Handwriting Recognition](about-handwriting-recognition.md).</span></span>

 

 
