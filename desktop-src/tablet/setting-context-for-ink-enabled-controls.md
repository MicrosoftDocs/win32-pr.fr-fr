---
description: Toute reconnaissance pour les contrôles avec reconnaissance de l’encre se produit via un objet RecognizerContext. Les API de technologie Tablet PC vous permettent de définir la propriété Factoid sur un objet RecognizerContext.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Définition du contexte pour les contrôles Ink-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6776978834f030353a84c04f03e5ecf05ba060cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320426"
---
# <a name="setting-context-for-ink-enabled-controls"></a><span data-ttu-id="593b8-104">Définition du contexte pour les contrôles Ink-Enabled</span><span class="sxs-lookup"><span data-stu-id="593b8-104">Setting Context for Ink-Enabled Controls</span></span>

<span data-ttu-id="593b8-105">Toute reconnaissance pour les contrôles avec reconnaissance de l’encre se produit via un objet [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="593b8-105">All recognition for ink-enabled controls occurs through a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="593b8-106">Les API de technologie Tablet PC vous permettent de définir la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) sur un objet **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="593b8-106">The Tablet PC Technology APIs enable you to set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on a **RecognizerContext** object.</span></span>

<span data-ttu-id="593b8-107">Si vous créez une application compatible avec l’écriture manuscrite, utilisez les propriétés [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) et [**de la**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) zone de texte de l’objet [**RecognizerContext**](inkrecognizercontext-class.md) pour définir des contextes.</span><span class="sxs-lookup"><span data-stu-id="593b8-107">If you are creating an ink-enabled application, use the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) and [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) properties to set contexts.</span></span>

<span data-ttu-id="593b8-108">Vous pouvez transmettre les valeurs de chaîne des noms dans les étendues d’entrée définies dans l’énumération [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) à la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) , séparées par une ouverture ( !</span><span class="sxs-lookup"><span data-stu-id="593b8-108">You may pass in the string values of the names in the input scopes defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property, delimited with an opening (!</span></span> <span data-ttu-id="593b8-109">et une fermeture).</span><span class="sxs-lookup"><span data-stu-id="593b8-109">and a closing ).</span></span> <span data-ttu-id="593b8-110">Par exemple, pour définir le contexte d’un objet [**RecognizerContext**](inkrecognizercontext-class.md) de façon à ce qu’il s’écarte des caractères utilisés dans une URL, utilisez la syntaxe indiquée dans les exemples C suivants \# :</span><span class="sxs-lookup"><span data-stu-id="593b8-110">For example, to set the context for a [**RecognizerContext**](inkrecognizercontext-class.md) object to bias toward characters used in a URL, use the syntax shown in the following C\# examples:</span></span>


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> <span data-ttu-id="593b8-111">Les étendues d’entrée telles qu’elles sont définies dans l’énumération [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) remplacent les Factoids disponibles dans les versions précédentes du kit de développement logiciel (SDK) de Windows XP Tablet PC Edition, bien que ces Factoids continuent de fonctionner pour assurer la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="593b8-111">The input scopes as defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration supersede the factoids that were available in previous versions of the Windows XP Tablet PC Edition SDK, although these factoids will continue to work in order to provide backward compatibility.</span></span>

 

<span data-ttu-id="593b8-112">L’exemple C suivant \# définit la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) pour les codes postaux :</span><span class="sxs-lookup"><span data-stu-id="593b8-112">The following C\# example sets the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property for postal codes:</span></span>


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



<span data-ttu-id="593b8-113">Vous pouvez combiner des étendues d’entrée à l’aide de la syntaxe d’expression régulière d’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="593b8-113">You can combine input scopes by using the handwriting regular expression syntax.</span></span> <span data-ttu-id="593b8-114">Pour plus d’informations sur l’utilisation de la syntaxe des expressions régulières, consultez [étendues d’entrée personnalisées avec des expressions régulières](custom-input-scopes-with-regular-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="593b8-114">For more details about using regular expression syntax, see [Custom Input Scopes with Regular Expressions](custom-input-scopes-with-regular-expressions.md).</span></span>

<span data-ttu-id="593b8-115">Vous pouvez définir des indicateurs de reconnaissance sur l’objet [**RecognizerContext**](inkrecognizercontext-class.md) pour affecter le comportement du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="593b8-115">You can set recognition flags on the [**RecognizerContext**](inkrecognizercontext-class.md) object to affect the behavior of the recognizer.</span></span> <span data-ttu-id="593b8-116">L’un de ces indicateurs est l’indicateur de **forçage** dans l’énumération [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) du **RecognizerContext**.</span><span class="sxs-lookup"><span data-stu-id="593b8-116">One such flag is the **Coerce** flag in the [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) enumeration of the **RecognizerContext**.</span></span> <span data-ttu-id="593b8-117">L’indicateur de **forçage** force le module de reconnaissance à retourner un résultat qui correspond à la définition de la Factoid définie.</span><span class="sxs-lookup"><span data-stu-id="593b8-117">The **Coerce** flag forces the recognizer to return a result that matches the definition of the factoid that is set.</span></span> <span data-ttu-id="593b8-118">Par exemple, si vous avez un formulaire qui oblige l’utilisateur à entrer une quantité numérique, il peut être utile de définir le **\_ nombre** Factoid et de définir la propriété [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) sur **force**.</span><span class="sxs-lookup"><span data-stu-id="593b8-118">For example, if you have a form that requires the user to enter a numerical quantity, it may be useful to set the **IS\_NUMBER** factoid and also set the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**.</span></span> <span data-ttu-id="593b8-119">Dans cette instance, l’indicateur de **forçage** garantit que le module de reconnaissance retourne uniquement des nombres.</span><span class="sxs-lookup"><span data-stu-id="593b8-119">In that instance, the **Coerce** flag guarantees that the recognizer returns only numbers.</span></span>

<span data-ttu-id="593b8-120">L’exemple C suivant \# définit la propriété [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) sur **force**:</span><span class="sxs-lookup"><span data-stu-id="593b8-120">The following C\# example sets the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**:</span></span>


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



<span data-ttu-id="593b8-121">Toutefois, soyez vigilant lorsque vous décidez de définir l’indicateur de **forçage** .</span><span class="sxs-lookup"><span data-stu-id="593b8-121">However, use caution when deciding to set the **Coerce** flag.</span></span> <span data-ttu-id="593b8-122">L’indicateur force le module de reconnaissance à correspondre uniquement à la définition de Factoid.</span><span class="sxs-lookup"><span data-stu-id="593b8-122">The flag forces the recognizer to match only the definition of the factoid.</span></span> <span data-ttu-id="593b8-123">Par exemple, si vous définissez l' \_ \_ étendue d’entrée FULLTELEPHONENUMBER et l’indicateur de **forçage** , le module de reconnaissance retourne des résultats qui correspondent exactement à la définition de l’étendue de l' \_ entrée de FULLTELEPHONENUMBER de téléphone \_ uniquement.</span><span class="sxs-lookup"><span data-stu-id="593b8-123">For example, if you set the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag, the recognizer returns results that exactly match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope only.</span></span> <span data-ttu-id="593b8-124">Si un utilisateur écrit « 911 » avec l' \_ \_ étendue d’entrée de téléphone FULLTELEPHONENUMBER et l’indicateur de **forçage** défini, le module de reconnaissance peut retourner une chaîne vide ou une chaîne aléatoire au format (xxx) xxx-xxxx (où X est un chiffre).</span><span class="sxs-lookup"><span data-stu-id="593b8-124">If a user writes "911" with the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag set, the recognizer may return either an empty string or a random string in the format of (XXX) XXX-XXXX (where X is a digit).</span></span> <span data-ttu-id="593b8-125">Le format XXX ne correspond pas à la définition de l' \_ opérateur is Telephone \_ FULLTELEPHONENUMBER Factoid, même s’il s’agit d’un numéro de téléphone valide.</span><span class="sxs-lookup"><span data-stu-id="593b8-125">The format of XXX does not match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER factoid, even though it is a valid phone number.</span></span>

<span data-ttu-id="593b8-126">Pour obtenir la liste des formats pris en charge pour chaque étendue d’entrée, consultez la référence [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) .</span><span class="sxs-lookup"><span data-stu-id="593b8-126">For lists of the supported formats for each input scope, see the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) reference.</span></span>

<span data-ttu-id="593b8-127">Pour rétablir la valeur par défaut d’un champ pour le module de reconnaissance, affectez la valeur \_ par défaut à Factoid, comme dans l’exemple C suivant \# :</span><span class="sxs-lookup"><span data-stu-id="593b8-127">To return a field to the default setting for the recognizer, set the factoid to IS\_DEFAULT , as in the following C\# example:</span></span>


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



<span data-ttu-id="593b8-128">Pour les applications qui utilisent le contrôle [InkEdit](inkedit-control-reference.md) , définissez le type Factoid pour le contrôle en spécifiant :</span><span class="sxs-lookup"><span data-stu-id="593b8-128">For applications that use the [InkEdit](inkedit-control-reference.md) control, set the factoid type for the control by specifying:</span></span>


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



<span data-ttu-id="593b8-129">Où `IS_INPUTSCOPE` est le nom de l’étendue d’entrée que vous souhaitez appliquer.</span><span class="sxs-lookup"><span data-stu-id="593b8-129">Where `IS_INPUTSCOPE` is the name of the input scope you want to apply.</span></span>

<span data-ttu-id="593b8-130">Le contrôle [InkEdit](inkedit-control-reference.md) n’expose pas un objet [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="593b8-130">The [InkEdit](inkedit-control-reference.md) control does not expose a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="593b8-131">Vous pouvez toujours assigner le contexte à l’aide de la propriété [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) du contrôle InkEdit, mais vous ne pouvez pas définir l’indicateur **WORDMODE** .</span><span class="sxs-lookup"><span data-stu-id="593b8-131">You can still assign context by using the [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) property of the InkEdit control, but you cannot set the **WORDMODE** flag.</span></span>

 

 
