---
description: Cet exemple illustre des fonctionnalités avancées de l’interface de programmation d’applications (API) MicrosoftTablet PC Automation utilisées pour la reconnaissance de l’écriture manuscrite.
ms.assetid: c9e6613c-5797-44c3-8ce1-92d4d1459ecf
title: Exemple de reconnaissance multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d687f1bddd1f3c57cc482070b8e5826126b6e5b0f716fa3649df01ad6eab30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856548"
---
# <a name="multiple-recognizers-sample"></a>Exemple de reconnaissance multiple

Cet exemple illustre des fonctionnalités avancées de l’interface de programmation d’applications (API) MicrosoftTablet PC Automation utilisées pour la reconnaissance de l' *écriture manuscrite* .

Les éléments suivants sont abordés :

-   Énumération des détecteurs installés
-   Création d’un *contexte* de module de reconnaissance avec un module de reconnaissance de langage spécifique
-   Sérialisation des résultats de la reconnaissance avec une collection de traits
-   Organisation des collections Stroke en collection personnalisée dans l’objet [**InkDisp**](inkdisp-class.md)
-   Sérialiser des objets *Ink* vers et les récupérer à partir d’un fichier *Ink SERIALIZED format (ISF)*
-   Définition des repères d’entrée du module de reconnaissance
-   Utilisation de la reconnaissance synchrone et asynchrone

## <a name="ink-headers"></a>En-têtes d’encre

Tout d’abord, incluez les en-têtes pour les interfaces d’automatisation Tablet PC. celles-ci sont installées avec le kit de développement logiciel (SDK) de Microsoft Windows XP Tablet PC Edition.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Le fichier EventSinks. h définit les interfaces IInkEventsImpl et IInkRecognitionEventsImpl.


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a>Énumération des détecteurs installés

La méthode LoadMenu de l’application remplit le menu créer de nouveaux traits avec les module de reconnaissance disponibles. Un [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) est créé. Si la propriété [**languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) d’un objet **InkRecognizers** n’est pas vide, le module de reconnaissance est un module de *reconnaissance de texte* et la valeur de sa propriété [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) est ajoutée au menu.


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



## <a name="creating-an-ink-collector"></a>Création d’un collecteur d’encre

La méthode OnCreate de l’application crée un objet [**InkCollector**](inkcollector-class.md) , le connecte à sa source d’événement et active la collecte d’encre.


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a>Création d’un contexte de module de reconnaissance

La méthode CreateRecoContext de l’application crée et initialise un nouveau contexte de module de reconnaissance et configure les repères pris en charge par le langage associé. La méthode [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) de l’objet [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) crée un objet [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) pour le langage. Si nécessaire, l’ancien contexte du module de reconnaissance est remplacé. Le contexte est connecté à sa source d’événement. Enfin, la propriété [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) du contexte de module de reconnaissance est vérifiée pour déterminer les guides pris en charge par le contexte de module de reconnaissance.


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



## <a name="collecting-strokes-and-displaying-recognition-results"></a>Collecte des traits et affichage des résultats de la reconnaissance

La méthode OnStroke de l’application met à jour le [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) du collecteur d’encres, annule les demandes de reconnaissance asynchrone existantes et crée une demande de reconnaissance sur le contexte du module de reconnaissance.


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



La méthode de l’application `OnRecognition` envoie les résultats de la demande de reconnaissance à la méthode de la fenêtre de sortie `UpdateString` .


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a>Suppression de traits et de résultats de reconnaissance

La méthode OnClear de l’application supprime tous les traits et résultats de la reconnaissance de l’objet [**InkDisp**](inkdisp-class.md) et efface les fenêtres. L’Association du contexte du module de reconnaissance avec sa collection [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) est supprimée.


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



## <a name="changing-recognizer-contexts"></a>Modification des contextes de reconnaissance

La méthode OnNewStrokes de l’application est appelée quand l’utilisateur sélectionne un module de reconnaissance dans le menu créer de nouveaux traits. Le [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) actuel est enregistré. Si un module de reconnaissance linguistique différent a été sélectionné, un nouveau contexte de module de reconnaissance est créé. Ensuite, un nouveau **InkStrokes** est attaché au nouveau contexte de module de reconnaissance.


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



Il appelle ensuite StartNewStrokeCollection, qui crée un [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) vide et l’attache au contexte du module de reconnaissance.

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a>Enregistrement de la collection Strokes pour un contexte de module de reconnaissance

La méthode de l’application `SaveStrokeCollection` recherche un contexte de module de reconnaissance existant et finalise la reconnaissance de la collection de traits en cours. La collection [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) est ensuite ajoutée au [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) de l’objet Ink.


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



 

 
