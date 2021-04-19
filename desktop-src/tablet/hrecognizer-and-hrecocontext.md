---
description: Vous faites référence à un module de reconnaissance d’encre avec un handle HRECOGNIZER et un contexte de reconnaissance comme handle HRECOCONTEXT. Une bibliothèque de liens dynamiques (DLL) de module de reconnaissance peut implémenter des identificateurs pour plusieurs langages.
ms.assetid: 23002d02-cf8f-489b-a50f-4a18ac091825
title: HRECOGNIZER et HRECOCONTEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12af1bb5569a22a612f0a3ed667a55aac81da2c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514839"
---
# <a name="hrecognizer-and-hrecocontext"></a><span data-ttu-id="21de8-103">HRECOGNIZER et HRECOCONTEXT</span><span class="sxs-lookup"><span data-stu-id="21de8-103">HRECOGNIZER and HRECOCONTEXT</span></span>

<span data-ttu-id="21de8-104">Vous faites référence à un module de reconnaissance d’encre avec un handle [HRECOGNIZER](hrecognizer-handle.md) et un contexte de reconnaissance comme handle [HRECOCONTEXT](hrecocontext-handle.md) .</span><span class="sxs-lookup"><span data-stu-id="21de8-104">You reference an ink recognizer with an [HRECOGNIZER](hrecognizer-handle.md) handle and a recognizer context as an [HRECOCONTEXT](hrecocontext-handle.md) handle.</span></span>

<span data-ttu-id="21de8-105">Une bibliothèque de liens dynamiques (DLL) de module de reconnaissance peut implémenter des identificateurs pour plusieurs langages.</span><span class="sxs-lookup"><span data-stu-id="21de8-105">A recognizer dynamic-link library (DLL) can implement recognizers for more than one language.</span></span> <span data-ttu-id="21de8-106">Si c’est le cas, chaque langue est sélectionnée par un CLSID qui est passé lors de la création de l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) dans l’application.</span><span class="sxs-lookup"><span data-stu-id="21de8-106">If so, each language is selected by a CLSID that is passed in when creating the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object in the application.</span></span> <span data-ttu-id="21de8-107">En outre, une DLL de reconnaissance peut créer plusieurs descripteurs de reconnaissance lorsqu’elle est chargée, une ou plusieurs pour chaque langue reconnue.</span><span class="sxs-lookup"><span data-stu-id="21de8-107">In addition, a recognizer DLL can create multiple recognizer handles when it is loaded, one or more for each language recognized.</span></span>

<span data-ttu-id="21de8-108">Un contexte de module de reconnaissance est créé pour représenter l’événement qui consiste à reconnaître un élément d’encre spécifique.</span><span class="sxs-lookup"><span data-stu-id="21de8-108">A recognizer context is created to represent the event of recognizing a specific piece of ink.</span></span> <span data-ttu-id="21de8-109">Lorsque le contexte est créé, le descripteur d’objets de module de reconnaissance associé est passé à la fonction [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) .</span><span class="sxs-lookup"><span data-stu-id="21de8-109">When the context is created, the associated recognizer objects handle is passed to the [**CreateContext**](/windows/desktop/api/recapis/nf-recapis-createcontext) function.</span></span> <span data-ttu-id="21de8-110">Cela associe le langage au contexte du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="21de8-110">This associates the language with the recognizer context.</span></span>

<span data-ttu-id="21de8-111">Un contexte de module de reconnaissance peut représenter la reconnaissance de toute l’encre dans le corps d’un message électronique, l’encre d’un champ unique dans une application ou une ligne unique de texte écrite dans le panneau de saisie Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="21de8-111">A recognizer context may represent the recognition of all the ink in the body of an email, the ink of a single field within an application, or a single line of text written in the Tablet PC Input Panel.</span></span> <span data-ttu-id="21de8-112">Le volume d’encre dans un contexte de reconnaissance unique peut varier d’un trait unique à une page entière ou plus.</span><span class="sxs-lookup"><span data-stu-id="21de8-112">The volume of ink in a single recognizer context may vary from a single stroke to a whole page or more.</span></span>

<span data-ttu-id="21de8-113">Le contexte du module de reconnaissance est défini par les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="21de8-113">The recognizer context is defined by the settings of:</span></span>

-   <span data-ttu-id="21de8-114">Guide de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="21de8-114">The recognition guide.</span></span>
-   <span data-ttu-id="21de8-115">N’importe quel Factoids.</span><span class="sxs-lookup"><span data-stu-id="21de8-115">Any factoids.</span></span>
-   <span data-ttu-id="21de8-116">Indicateurs éventuels.</span><span class="sxs-lookup"><span data-stu-id="21de8-116">Any flags.</span></span>
-   <span data-ttu-id="21de8-117">Contexte de texte.</span><span class="sxs-lookup"><span data-stu-id="21de8-117">The text context.</span></span>
-   <span data-ttu-id="21de8-118">Liste de mots.</span><span class="sxs-lookup"><span data-stu-id="21de8-118">Any word list.</span></span>
-   <span data-ttu-id="21de8-119">Mode de saisie semi-automatique des caractères.</span><span class="sxs-lookup"><span data-stu-id="21de8-119">The character Autocomplete mode.</span></span>

<span data-ttu-id="21de8-120">Le handle du contexte de module de reconnaissance est passé à toutes les fonctions qui utilisent ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="21de8-120">The handle for the recognizer context is passed to all functions that use these settings.</span></span> <span data-ttu-id="21de8-121">La modification d’un paramètre modifie le contexte du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="21de8-121">Changing a setting changes the recognizer context.</span></span>

<span data-ttu-id="21de8-122">L’application peut utiliser plusieurs contextes pour reconnaître l’encre à partir de différentes parties de l’écran.</span><span class="sxs-lookup"><span data-stu-id="21de8-122">The application may use several contexts to recognize ink from different parts of the screen.</span></span> <span data-ttu-id="21de8-123">Un contexte individuel peut reconnaître plusieurs lignes de texte.</span><span class="sxs-lookup"><span data-stu-id="21de8-123">An individual context can recognize multiple lines of text.</span></span> <span data-ttu-id="21de8-124">Toutefois, un contexte individuel ne peut pas traiter deux paragraphes écrits côte à côte, par exemple plusieurs colonnes dans un article de journal.</span><span class="sxs-lookup"><span data-stu-id="21de8-124">However, an individual context cannot process two paragraphs written side by side, such as multiple columns in a newspaper article.</span></span>

<span data-ttu-id="21de8-125">Pour reconnaître une nouvelle encre, créez un nouveau contexte.</span><span class="sxs-lookup"><span data-stu-id="21de8-125">To recognize new ink, create a new context.</span></span> <span data-ttu-id="21de8-126">Vous pouvez également utiliser la fonction [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) pour effectuer une copie d’un contexte qui n’a pas l’encre et les résultats, ou la fonction [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) pour effacer un contexte de son encre et de ses résultats.</span><span class="sxs-lookup"><span data-stu-id="21de8-126">As an alternative, use the [**CloneContext**](/windows/desktop/api/recapis/nf-recapis-clonecontext) function to make a copy of a context that does not have the ink and results, or the [**ResetContext**](/windows/desktop/api/recapis/nf-recapis-resetcontext) function to clear a context of its ink and results.</span></span> <span data-ttu-id="21de8-127">Avec ces approches, une application Ink peut réutiliser un contexte.</span><span class="sxs-lookup"><span data-stu-id="21de8-127">With these approaches, an ink application can reuse a context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21de8-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="21de8-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21de8-129">**SetGuide fonction)**</span><span class="sxs-lookup"><span data-stu-id="21de8-129">**SetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setguide)
</dt> <dt>

[<span data-ttu-id="21de8-130">**GetGuide fonction)**</span><span class="sxs-lookup"><span data-stu-id="21de8-130">**GetGuide Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getguide)
</dt> <dt>

[<span data-ttu-id="21de8-131">**SetFactoid fonction)**</span><span class="sxs-lookup"><span data-stu-id="21de8-131">**SetFactoid Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setfactoid)
</dt> <dt>

[<span data-ttu-id="21de8-132">**SetFlags fonction)**</span><span class="sxs-lookup"><span data-stu-id="21de8-132">**SetFlags Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setflags)
</dt> <dt>

[<span data-ttu-id="21de8-133">**SetEnabledUnicodeRanges fonction)**</span><span class="sxs-lookup"><span data-stu-id="21de8-133">**SetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="21de8-134">**GetEnabledUnicodeRanges fonction)**</span><span class="sxs-lookup"><span data-stu-id="21de8-134">**GetEnabledUnicodeRanges Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-getenabledunicoderanges)
</dt> <dt>

[<span data-ttu-id="21de8-135">**SetCACMode fonction)**</span><span class="sxs-lookup"><span data-stu-id="21de8-135">**SetCACMode Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setcacmode)
</dt> <dt>

[<span data-ttu-id="21de8-136">**SetTextContext fonction)**</span><span class="sxs-lookup"><span data-stu-id="21de8-136">**SetTextContext Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-settextcontext)
</dt> <dt>

[<span data-ttu-id="21de8-137">**SetWordList fonction)**</span><span class="sxs-lookup"><span data-stu-id="21de8-137">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 



