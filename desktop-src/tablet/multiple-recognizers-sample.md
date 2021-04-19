---
description: Cet exemple illustre des fonctionnalités avancées de l’interface de programmation d’applications (API) MicrosoftTablet PC Automation utilisées pour la reconnaissance de l’écriture manuscrite.
ms.assetid: c9e6613c-5797-44c3-8ce1-92d4d1459ecf
title: Exemple de reconnaissance multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a21d24001e3544be16dde4d288a8adc7ea0081f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535484"
---
# <a name="multiple-recognizers-sample"></a><span data-ttu-id="ac0a4-103">Exemple de reconnaissance multiple</span><span class="sxs-lookup"><span data-stu-id="ac0a4-103">Multiple Recognizers Sample</span></span>

<span data-ttu-id="ac0a4-104">Cet exemple illustre des fonctionnalités avancées de l’interface de programmation d’applications (API) MicrosoftTablet PC Automation utilisées pour la reconnaissance de l' *écriture manuscrite* .</span><span class="sxs-lookup"><span data-stu-id="ac0a4-104">This sample demonstrates advanced features of the MicrosoftTablet PC Automation application programming interface (API) used for *handwriting* recognition.</span></span>

<span data-ttu-id="ac0a4-105">Les éléments suivants sont abordés :</span><span class="sxs-lookup"><span data-stu-id="ac0a4-105">It includes the following:</span></span>

-   <span data-ttu-id="ac0a4-106">Énumération des détecteurs installés</span><span class="sxs-lookup"><span data-stu-id="ac0a4-106">Enumerating the installed recognizers</span></span>
-   <span data-ttu-id="ac0a4-107">Création d’un *contexte* de module de reconnaissance avec un module de reconnaissance de langage spécifique</span><span class="sxs-lookup"><span data-stu-id="ac0a4-107">Creating a *recognizer context* with a specific language recognizer</span></span>
-   <span data-ttu-id="ac0a4-108">Sérialisation des résultats de la reconnaissance avec une collection de traits</span><span class="sxs-lookup"><span data-stu-id="ac0a4-108">Serializing recognition results with a stroke collection</span></span>
-   <span data-ttu-id="ac0a4-109">Organisation des collections Stroke en collection personnalisée dans l’objet [**InkDisp**](inkdisp-class.md)</span><span class="sxs-lookup"><span data-stu-id="ac0a4-109">Organizing stroke collections into a custom collection within the [**InkDisp**](inkdisp-class.md) object</span></span>
-   <span data-ttu-id="ac0a4-110">Sérialiser des objets *Ink* vers et les récupérer à partir d’un fichier *Ink SERIALIZED format (ISF)*</span><span class="sxs-lookup"><span data-stu-id="ac0a4-110">Serializing *ink* objects to and retrieving them from an *ink serialized format (ISF)* file</span></span>
-   <span data-ttu-id="ac0a4-111">Définition des repères d’entrée du module de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="ac0a4-111">Setting recognizer input guides</span></span>
-   <span data-ttu-id="ac0a4-112">Utilisation de la reconnaissance synchrone et asynchrone</span><span class="sxs-lookup"><span data-stu-id="ac0a4-112">Using synchronous and asynchronous recognition</span></span>

## <a name="ink-headers"></a><span data-ttu-id="ac0a4-113">En-têtes d’encre</span><span class="sxs-lookup"><span data-stu-id="ac0a4-113">Ink Headers</span></span>

<span data-ttu-id="ac0a4-114">Tout d’abord, incluez les en-têtes pour les interfaces d’automatisation Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-114">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="ac0a4-115">Celles-ci sont installées avec le kit de développement logiciel (SDK) de Microsoft Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-115">These are installed with the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="ac0a4-116">Le fichier EventSinks. h définit les interfaces IInkEventsImpl et IInkRecognitionEventsImpl.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-116">The EventSinks.h file defines the IInkEventsImpl and IInkRecognitionEventsImpl interfaces.</span></span>


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a><span data-ttu-id="ac0a4-117">Énumération des détecteurs installés</span><span class="sxs-lookup"><span data-stu-id="ac0a4-117">Enumerating the Installed Recognizers</span></span>

<span data-ttu-id="ac0a4-118">La méthode LoadMenu de l’application remplit le menu créer de nouveaux traits avec les module de reconnaissance disponibles.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-118">The application's LoadMenu method populates the Create New Strokes menu with the available recognizers.</span></span> <span data-ttu-id="ac0a4-119">Un [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) est créé.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-119">An [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) is created.</span></span> <span data-ttu-id="ac0a4-120">Si la propriété [**languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) d’un objet **InkRecognizers** n’est pas vide, le module de reconnaissance est un module de *reconnaissance de texte* et la valeur de sa propriété [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) est ajoutée au menu.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-120">If the [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) property of an **InkRecognizers** object is not empty, then the recognizer is a *text recognizer*, and the value of its [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) property is added to the menu.</span></span>


```C++
// Create the enumerator for the installed recognizers
hr = m_spIInkRecognizers.CoCreateInstance(CLSID_InkRecognizers);
...
    // Filter out non-language recognizers by checking for
    // the languages supported by the recognizer - there is not
    // any if it is a gesture or object recognizer.
    CComVariant vLanguages;
    if (SUCCEEDED(spIInkRecognizer->get_Languages(&vLanguages)))
    {
        if ((VT_ARRAY == (VT_ARRAY & vLanguages.vt))           // it should be an array
            && (NULL != vLanguages.parray)
            && (0 < vLanguages.parray->rgsabound[0].cElements)) // with at least one element
        {
            // This is a language recognizer. Add its name to the menu.
            CComBSTR bstrName;
            if (SUCCEEDED(spIInkRecognizer->get_Name(&bstrName)))
                ...
        }
    }
```



## <a name="creating-an-ink-collector"></a><span data-ttu-id="ac0a4-121">Création d’un collecteur d’encre</span><span class="sxs-lookup"><span data-stu-id="ac0a4-121">Creating an Ink Collector</span></span>

<span data-ttu-id="ac0a4-122">La méthode OnCreate de l’application crée un objet [**InkCollector**](inkcollector-class.md) , le connecte à sa source d’événement et active la collecte d’encre.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-122">The application's OnCreate method creates an [**InkCollector**](inkcollector-class.md) object, connects it to its event source, and enables ink collection.</span></span>


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a><span data-ttu-id="ac0a4-123">Création d’un contexte de module de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="ac0a4-123">Creating a Recognizer Context</span></span>

<span data-ttu-id="ac0a4-124">La méthode CreateRecoContext de l’application crée et initialise un nouveau contexte de module de reconnaissance et configure les repères pris en charge par le langage associé.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-124">The application's CreateRecoContext method creates and initializes a new recognizer context, and sets up the guides supported by the associated language.</span></span> <span data-ttu-id="ac0a4-125">La méthode [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) de l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) crée un objet [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) pour le langage.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-125">The [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object's [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) method creates a [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) object for the language.</span></span> <span data-ttu-id="ac0a4-126">Si nécessaire, l’ancien contexte du module de reconnaissance est remplacé.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-126">If necessary, the old recognizer context is replaced.</span></span> <span data-ttu-id="ac0a4-127">Le contexte est connecté à sa source d’événement.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-127">The context is connected to its event source.</span></span> <span data-ttu-id="ac0a4-128">Enfin, la propriété [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) du contexte de module de reconnaissance est vérifiée pour déterminer les guides pris en charge par le contexte de module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-128">Finally, the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the recognizer context is checked for which guides the recognizer context supports.</span></span>


```C++
// Create a recognizer context
CComPtr<IInkRecognizerContext2> spNewContext;
if (FAILED(pIInkRecognizer2->CreateRecognizerContext(&spNewContext)))
    return false;

// Replace the current context with the new one
if (m_spIInkRecoContext != NULL)
{
    // Close the connection to the recognition events source
    IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventUnadvise(m_spIInkRecoContext);
}
m_spIInkRecoContext.Attach(spNewContext.Detach());

// Establish a connection with the recognizer context's event source
if (FAILED(IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkRecoContext)))
    ...

// Set the guide if it's supported by the recognizer and has been created 
int cRows = 0, cColumns = 0;
InkRecognizerCapabilities dwCapabilities = IRC_DontCare;
if (SUCCEEDED(pIInkRecognizer->get_Capabilities(&dwCapabilities)))
    ...
```



## <a name="collecting-strokes-and-displaying-recognition-results"></a><span data-ttu-id="ac0a4-129">Collecte des traits et affichage des résultats de la reconnaissance</span><span class="sxs-lookup"><span data-stu-id="ac0a4-129">Collecting Strokes and Displaying Recognition Results</span></span>

<span data-ttu-id="ac0a4-130">La méthode OnStroke de l’application met à jour le [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) du collecteur d’encres, annule les demandes de reconnaissance asynchrone existantes et crée une demande de reconnaissance sur le contexte du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-130">The application's OnStroke method updates the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) of the ink collector, cancels existing asynchronous recognition requests, and creates a recognition request on the recognizer context.</span></span>


```C++
// Add the new stroke to the current collection
hr = m_spIInkStrokes->Add(pIInkStroke);

if (SUCCEEDED(hr))
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();

    // Ask the context to update the recognition results with newly added strokes
    // When the results are ready, the recognizer context returns them
    // through the corresponding event RecognitionWithAlternates
    CComVariant vCustomData;
    m_spIInkRecoContext->BackgroundRecognize(vCustomData);
}
```



<span data-ttu-id="ac0a4-131">La méthode de l’application `OnRecognition` envoie les résultats de la demande de reconnaissance à la méthode de la fenêtre de sortie `UpdateString` .</span><span class="sxs-lookup"><span data-stu-id="ac0a4-131">The application's `OnRecognition` method sends the results of the recognition request to the output window's `UpdateString` method.</span></span>


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a><span data-ttu-id="ac0a4-132">Suppression de traits et de résultats de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="ac0a4-132">Deleting Strokes and Recognition Results</span></span>

<span data-ttu-id="ac0a4-133">La méthode OnClear de l’application supprime tous les traits et résultats de la reconnaissance de l’objet [**InkDisp**](inkdisp-class.md) et efface les fenêtres.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-133">The application's OnClear method deletes all strokes and recognition results from the [**InkDisp**](inkdisp-class.md) object and clears the windows.</span></span> <span data-ttu-id="ac0a4-134">L’Association du contexte du module de reconnaissance avec sa collection [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) est supprimée.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-134">The recognizer context's association with its [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is removed.</span></span>


```C++
// Detach the current stroke collection from the recognizer context and release it
if (m_spIInkRecoContext != NULL)
    m_spIInkRecoContext->putref_Strokes(NULL);

m_spIInkStrokes.Release();

// Clear the custom strokes collection
if (m_spIInkCustomStrokes != NULL)
    m_spIInkCustomStrokes->Clear();

// Delete all strokes from the Ink object
// Passing NULL as a stroke collection pointer means asking to delete all strokes
m_spIInkDisp->DeleteStrokes(NULL);

// Get a new stroke collection from the ink object
...
// Ask for an empty collection by passing an empty variant 
if (SUCCEEDED(m_spIInkDisp->CreateStrokes(v, &m_spIInkStrokes)))
{
    // Attach it to the recognizer context
    if (FAILED(m_spIInkRecoContext->putref_Strokes(m_spIInkStrokes)))
        ...
}
```



## <a name="changing-recognizer-contexts"></a><span data-ttu-id="ac0a4-135">Modification des contextes de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="ac0a4-135">Changing Recognizer Contexts</span></span>

<span data-ttu-id="ac0a4-136">La méthode OnNewStrokes de l’application est appelée quand l’utilisateur sélectionne un module de reconnaissance dans le menu créer de nouveaux traits.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-136">The application's OnNewStrokes method is called when the user selects a recognizer in the Create New Strokes menu.</span></span> <span data-ttu-id="ac0a4-137">Le [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) actuel est enregistré.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-137">The current [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) is saved.</span></span> <span data-ttu-id="ac0a4-138">Si un module de reconnaissance linguistique différent a été sélectionné, un nouveau contexte de module de reconnaissance est créé.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-138">If a different language recognizer was selected, a new recognizer context is created.</span></span> <span data-ttu-id="ac0a4-139">Ensuite, un nouveau **InkStrokes** est attaché au nouveau contexte de module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-139">Then, a new **InkStrokes** is attached to the new recognizer context.</span></span>


```C++
// Save the current stroke collection if there is any
if (m_spIInkRecoContext != NULL)
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();
    
    // Let the context know that there'll be no more input 
    // for the attached stroke collection
    m_spIInkRecoContext->EndInkInput();

    // Add the stroke collection to the Ink object's CustomStrokes collection
    SaveStrokeCollection();
}
...
// If a different recognizer was selected, create a new recognizer context
// Else, reuse the same recognizer context
if (wID != m_nCmdRecognizer)
{
    // Get a pointer to the recognizer object from the recognizer collection  
    CComPtr<IInkRecognizer> spIInkRecognizer;
    if ((m_spIInkRecognizers == NULL)
        || FAILED(m_spIInkRecognizers->Item(wID - ID_RECOGNIZER_FIRST,
                                             &spIInkRecognizer))
        || (false == CreateRecoContext(spIInkRecognizer)))
    {
        // restore the cursor
        ::SetCursor(hCursor);
        return 0;
    }

    // Update the status bar
    m_bstrCurRecoName.Empty();
    spIInkRecognizer->get_Name(&m_bstrCurRecoName);
    UpdateStatusBar();

    // Store the selected recognizer's command id
    m_nCmdRecognizer = wID;
}
```



<span data-ttu-id="ac0a4-140">Il appelle ensuite StartNewStrokeCollection, qui crée un [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) vide et l’attache au contexte du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-140">It then calls StartNewStrokeCollection, which creates an empty [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) and attaches it to the recognizer context.</span></span>

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a><span data-ttu-id="ac0a4-141">Enregistrement de la collection Strokes pour un contexte de module de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="ac0a4-141">Saving the Strokes Collection for a Recognizer Context</span></span>

<span data-ttu-id="ac0a4-142">La méthode de l’application `SaveStrokeCollection` recherche un contexte de module de reconnaissance existant et finalise la reconnaissance de la collection de traits en cours.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-142">The application's `SaveStrokeCollection` method checks for an existing recognizer context, and finalizes the recognition of the current strokes collection.</span></span> <span data-ttu-id="ac0a4-143">La collection [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) est ensuite ajoutée au [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) de l’objet Ink.</span><span class="sxs-lookup"><span data-stu-id="ac0a4-143">Then the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is added to the [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) of the ink object.</span></span>


```C++
if (m_spIInkRecoContext != NULL)
{
    if (SUCCEEDED(m_spIInkStrokes->get_Count(&lCount)) && 0 != lCount)
    {
        CComPtr<IInkRecognitionResult> spIInkRecoResult;
        InkRecognitionStatus RecognitionStatus;
        if (SUCCEEDED(m_spIInkRecoContext->Recognize(&RecognitionStatus, &spIInkRecoResult)))
        {
            if (SUCCEEDED(spIInkRecoResult->SetResultOnStrokes()))
            {
                CComBSTR bstr;
                spIInkRecoResult->get_TopString(&bstr);
                m_wndResults.UpdateString(bstr);
            }
            ...
        }
    }
    // Detach the stroke collection from the old recognizer context
    m_spIInkRecoContext->putref_Strokes(NULL);
}

// Now add it to the ink's custom strokes collection
// Each item (stroke collection) of the custom strokes must be identified
// by a unique string. Here we generate a GUID for this.
if ((0 != lCount) && (m_spIInkCustomStrokes != NULL))
{
    GUID guid;
    WCHAR szGuid[40]; // format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"
    if (SUCCEEDED(::CoCreateGuid(&guid)) 
        && (::StringFromGUID2(guid, szGuid, countof(szGuid)) != 0))
    {
        CComBSTR bstrGuid(szGuid);
        if (FAILED(m_spIInkCustomStrokes->Add(bstrGuid, m_spIInkStrokes)))
            ...
```



 

 
