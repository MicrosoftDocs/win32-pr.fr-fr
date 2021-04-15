---
description: L’exemple de saisie semi-automatique montre comment implémenter la saisie semi-automatique de caractères en japonais à l’aide des interfaces de programmation d’applications (API) de reconnaissance.
ms.assetid: 237e33bc-3708-4128-8749-d3d031f7237a
title: Exemple de saisie semi-automatique de caractères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4853cdef72a087aff3b9b726f0c83af9038ef5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524399"
---
# <a name="character-autocomplete-sample"></a><span data-ttu-id="2068d-103">Exemple de saisie semi-automatique de caractères</span><span class="sxs-lookup"><span data-stu-id="2068d-103">Character Autocomplete Sample</span></span>

<span data-ttu-id="2068d-104">L’exemple de saisie semi-automatique montre comment implémenter la saisie semi-automatique de caractères en japonais à l’aide des interfaces de programmation d’applications (API) de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="2068d-104">The Autocomplete sample demonstrates how to implement character Autocomplete in Japanese by using the recognition application programming interfaces (APIs).</span></span>

<span data-ttu-id="2068d-105">Les fonctionnalités suivantes sont utilisées dans cet exemple :</span><span class="sxs-lookup"><span data-stu-id="2068d-105">The following features are used in this sample:</span></span>

-   <span data-ttu-id="2068d-106">Utilisation d’un *collecteur d’encre*</span><span class="sxs-lookup"><span data-stu-id="2068d-106">Using an *ink collector*</span></span>
-   <span data-ttu-id="2068d-107">Utilisation d’un contexte de module de *reconnaissance*</span><span class="sxs-lookup"><span data-stu-id="2068d-107">Using a *recognizer context*</span></span>

## <a name="initializing-the-ink-collector-and-recognizer-context"></a><span data-ttu-id="2068d-108">Initialisation du collecteur d’encre et du contexte du module de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="2068d-108">Initializing the Ink Collector and Recognizer Context</span></span>

<span data-ttu-id="2068d-109">Les objets [**InkCollector**](inkcollector-class.md) et [**InkRecognizerContext**](inkrecognizercontext-class.md) sont déclarés en tant que classes qui peuvent déclencher des événements.</span><span class="sxs-lookup"><span data-stu-id="2068d-109">The [**InkCollector**](inkcollector-class.md) and [**InkRecognizerContext**](inkrecognizercontext-class.md) objects are declared as classes that can raise events.</span></span>


```C++
Dim WithEvents ic As InkCollector
Dim WithEvents rc As InkRecognizerContext
```



<span data-ttu-id="2068d-110">Le gestionnaire d’événements Load du formulaire crée un collecteur d’encres, associe le collecteur d’encre à la zone d’image et active la collecte d’encre.</span><span class="sxs-lookup"><span data-stu-id="2068d-110">The form's Load event handler creates an ink collector, associates the ink collector to picture box, and enables ink collection.</span></span> <span data-ttu-id="2068d-111">Le gestionnaire d’événements charge ensuite le module de reconnaissance japonais par défaut et initialise les propriétés des traits et du repère du contexte du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="2068d-111">The event handler then loads the default Japanese recognizer, and initializes the recognizer context 's Guide and Strokes properties.</span></span>


```C++
Private Sub Form_Load()
   ' Set the ink collector to work in the small frame window
    Set ic = New InkCollector    ic.hWnd = fraBox.hWnd    ic.Enabled = True
    
    ' Get the Japanese recognizer
    LoadRecognizer

    ' Initialize the recognizer context
    Dim Guide As New InkRecognizerGuide
    Dim FrameRectangle As New InkRectangle
    Dim Top As Long
    Dim Bottom As Long
    Dim Left As Long
    Dim Right As Long
    Top = 0
    Left = 0
    Bottom = fraBox.ScaleHeight
    Right = fraBox.ScaleWidth
    ic.Renderer.PixelToInkSpace Me.hdc, Top, Left
    ic.Renderer.PixelToInkSpace Me.hdc, Bottom, Right
    FrameRectangle.Bottom = Bottom
    FrameRectangle.Top = Top
    FrameRectangle.Left = Left
    FrameRectangle.Right = Right
    Guide.Columns = 1
    Guide.Rows = 1
    Guide.Midline = -1 ' Do not use midline
    Guide.DrawnBox = FrameRectangle
    Guide.WritingBox = FrameRectangle
    Set rc.Guide = Guide
    
    ' Set the strokes collection on the recognizer context
    Set ink = ic.ink    Set rc.Strokes = ic.ink.Strokes
End Sub
```



## <a name="loading-the-default-japanese-recognizer"></a><span data-ttu-id="2068d-112">Chargement du module de reconnaissance japonais par défaut</span><span class="sxs-lookup"><span data-stu-id="2068d-112">Loading the Default Japanese Recognizer</span></span>

<span data-ttu-id="2068d-113">La méthode [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) de [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) est appelée pour récupérer le module de reconnaissance par défaut pour la langue japonaise.</span><span class="sxs-lookup"><span data-stu-id="2068d-113">The [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) method of the [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) is called to retrieve the default recognizer for the Japanese language.</span></span> <span data-ttu-id="2068d-114">Ensuite, la propriété [**languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) de l’objet IInkRecognizer est vérifiée pour déterminer si le module de reconnaissance prend en charge la langue japonaise.</span><span class="sxs-lookup"><span data-stu-id="2068d-114">Next, the IInkRecognizer object's [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) property is checked to determine if the recognizer supports the Japanese language.</span></span> <span data-ttu-id="2068d-115">Si c’est le cas, la méthode [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) du module de reconnaissance est utilisée pour générer un contexte de module de reconnaissance pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="2068d-115">If it does, then the recognizer's [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) method is used to generate a recognizer context for the form.</span></span>


```C++
Private Sub LoadRecognizer()
    On Error GoTo NoRecognizer
    ' Get a Japanese recognizer context
    Dim recos As New InkRecognizers
    Dim JapaneseReco As IInkRecognizer
    Set JapaneseReco = recos.GetDefaultRecognizer(&H411)
    If JapaneseReco Is Nothing Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    
    ' Check that this is indeed a Japanese recognizer
    Dim IsJapanese As Boolean
    Dim lan As Integer
    IsJapanese = False
    For lan = LBound(JapaneseReco.Languages) To UBound(JapaneseReco.Languages)
        If JapaneseReco.Languages(lan) = &H411 Then
            IsJapanese = True
        End If
    Next lan
    If Not IsJapanese Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    Set rc = JapaneseReco.CreateRecognizerContext
    Exit Sub
NoRecognizer:
    MsgBox "Japanese Recognizers are not installed on this system. Exiting."
    End
End Sub
```



## <a name="handling-the-stroke-event"></a><span data-ttu-id="2068d-116">Gestion de l’événement Stroke</span><span class="sxs-lookup"><span data-stu-id="2068d-116">Handling the Stroke Event</span></span>

<span data-ttu-id="2068d-117">Le gestionnaire d’événements [**Stroke**](inkcollector-stroke.md) arrête d’abord la reconnaissance en arrière-plan dans le contexte du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="2068d-117">The [**Stroke**](inkcollector-stroke.md) event handler first halts background recognition on the recognizer context.</span></span> <span data-ttu-id="2068d-118">Ensuite, il ajoute le nouveau trait à la propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) du contexte du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="2068d-118">Then, it adds the new stroke to the recognizer context's [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property.</span></span> <span data-ttu-id="2068d-119">Enfin, il définit la propriété [**InkRecognizerCharacterAutoCompletionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) du contexte de reconnaissance et appelle la méthode [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) du contexte de reconnaissance pour chacun des trois modes de saisie semi-automatique de caractères.</span><span class="sxs-lookup"><span data-stu-id="2068d-119">Finally, it sets the recognizer context's [**InkRecognizerCharacterAutoCompletionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) property and calls the recognizer context's [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method for each of the three character Autocomplete modes.</span></span> <span data-ttu-id="2068d-120">Le paramètre *CustomData* de l’appel de méthode **BackgroundRecognizeWithAlternates** est utilisé pour identifier les résultats de reconnaissance qui sont retournés dans l’événement [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) .</span><span class="sxs-lookup"><span data-stu-id="2068d-120">The *CustomData* parameter of the **BackgroundRecognizeWithAlternates** method call is used to identify which recognition results are returned in the [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) event.</span></span>


```C++
Private Sub ic_Stroke(ByVal Cursor As MSINKAUTLib.IInkCursor, ByVal Stroke As MSINKAUTLib.IInkStrokeDisp, Cancel As Boolean)

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' Add the new stroke
    rc.Strokes.Add Stroke

    ' Get a result for all three CAC modes
    rc.CharacterAutoCompletionMode = IRCACM_Full rc.BackgroundRecognizeWithAlternates 0 rc.CharacterAutoCompletionMode = IRCACM_Prefix rc.BackgroundRecognizeWithAlternates 1 rc.CharacterAutoCompletionMode = IRCACM_Random rc.BackgroundRecognizeWithAlternates 2
End Sub
```



## <a name="handling-the-recognition-with-alternates-event"></a><span data-ttu-id="2068d-121">Gestion de la reconnaissance avec l’événement de substitution</span><span class="sxs-lookup"><span data-stu-id="2068d-121">Handling the Recognition with Alternates Event</span></span>

<span data-ttu-id="2068d-122">Le gestionnaire de l’événement [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) vérifie d’abord le paramètre *RecognitionStatus* .</span><span class="sxs-lookup"><span data-stu-id="2068d-122">The handler for the [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) event first checks the *RecognitionStatus* parameter.</span></span> <span data-ttu-id="2068d-123">En cas d’erreur dans la reconnaissance, le gestionnaire d’événements ignore les résultats de la reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="2068d-123">If there is an error in recognition, the event handler ignores the recognition results.</span></span> <span data-ttu-id="2068d-124">Dans le cas contraire, le gestionnaire d’événements ajoute le paramètre *RecognitionResult* à la zone d’image appropriée et enregistre la chaîne de résultat.</span><span class="sxs-lookup"><span data-stu-id="2068d-124">Otherwise, the event handler adds the *RecognitionResult* parameter to the appropriate picture box and saves the result string.</span></span> <span data-ttu-id="2068d-125">Le paramètre *CustomData* est défini dans l’appel à la méthode [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) et identifie le mode de saisie semi-automatique des caractères qui a été utilisé par le contexte du module de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="2068d-125">The *CustomData* parameter is set in the call to the [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method and identifies which character Autocomplete mode was used by the recognizer context.</span></span>


```C++
Private Sub rc_RecognitionWithAlternates(ByVal RecognitionResult As MSINKAUTLib.IInkRecognitionResult, ByVal vCustomParam As Variant, ByVal RecognitionStatus As MSINKAUTLib.InkRecognitionStatus)
    ' Get the alternates from the recognition result
    ' and display them in the right place
    Dim ResultString As String
    Dim alts As IInkRecognitionAlternates
    Dim alt As IInkRecognitionAlternate
        
    On Error GoTo EndFunc

    If RecognitionStatus = IRS_NoError Then
        ' Fill a string with all the characters for this CAC mode
        Set alts = RecognitionResult.AlternatesFromSelection
        For Each alt In alts
            ResultString = ResultString + alt.String
        Next alt
        ' Display the string
        Dim r As RECT
        r.Left = 0
        r.Top = 0
        r.Right = 1000
        r.Bottom = 1000
        PctResult(vCustomParam).Cls
        DrawText PctResult(vCustomParam).hdc, StrPtr(ResultString), Len(ResultString), r, 0
        If vCustomParam = 0 Then
            FullCACText = ResultString
        Else
            If vCustomParam = 1 Then
                PrefixCACText = ResultString
            Else
                If vCustomParam = 2 Then
                    RandomCACText = ResultString
                End If
            End If
        End If
    End If
    Exit Sub
EndFunc:
    MsgBox Err.Description
End Sub
```



## <a name="painting-the-form"></a><span data-ttu-id="2068d-126">Peindre le formulaire</span><span class="sxs-lookup"><span data-stu-id="2068d-126">Painting the Form</span></span>

<span data-ttu-id="2068d-127">Le gestionnaire d’événements Paint efface les zones d’image résultats et y ajoute les résultats de reconnaissance enregistrés.</span><span class="sxs-lookup"><span data-stu-id="2068d-127">The Paint event handler clears the results picture boxes and adds the saved recognition results to them.</span></span>

## <a name="deleting-the-strokes"></a><span data-ttu-id="2068d-128">Suppression des traits</span><span class="sxs-lookup"><span data-stu-id="2068d-128">Deleting the Strokes</span></span>

<span data-ttu-id="2068d-129">La méthode du formulaire `CmdClear_Click` gère la commande Clear.</span><span class="sxs-lookup"><span data-stu-id="2068d-129">The form's `CmdClear_Click` method handles the Clear command.</span></span> <span data-ttu-id="2068d-130">Si le [**InkCollector**](inkcollector-class.md) collecte actuellement de l’encre, une boîte de message s’affiche et la commande est ignorée.</span><span class="sxs-lookup"><span data-stu-id="2068d-130">If the [**InkCollector**](inkcollector-class.md) is currently collecting ink, then a message box is displayed and the command is ignored.</span></span> <span data-ttu-id="2068d-131">Dans le cas contraire, le gestionnaire d’événements arrête la reconnaissance en arrière-plan, efface la propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) du contexte de module de reconnaissance et supprime les traits de l’objet [**InkDisp**](inkdisp-class.md) du formulaire.</span><span class="sxs-lookup"><span data-stu-id="2068d-131">Otherwise, the event handler stops background recognition, clears the [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property of the recognizer context, and deletes the strokes from the form's [**InkDisp**](inkdisp-class.md) object.</span></span> <span data-ttu-id="2068d-132">Ensuite, le gestionnaire d’événements redessine la zone d’image à laquelle est associé le collecteur d’encre et efface les chaînes de reconnaissance et les zones d’image.</span><span class="sxs-lookup"><span data-stu-id="2068d-132">Then, the event handler redraws the picture box to which the ink collector is associated, and clears the recognition strings and picture boxes.</span></span>


```C++
If Not (ic.CollectingInk) Then

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' ...
    Set rc.Strokes = Nothing

    ' Delete all the strokes from the ink object
    ic.Ink.DeleteStrokes strokesToDelete

    ' Refresh the window
    fraBox.Refresh

    ' refresh the recognizer context
    Set rc.Strokes = ic.Ink.Strokes

    ' Clear the result strings
    FullCACText = ""
    PrefixCACText = ""
    RandomCACText = ""

    ' Clear the result windows
    PctResult(0).Cls
    PctResult(1).Cls
    PctResult(2).Cls

Else
    MsgBox "Cannot clear ink while the ink collector is busy."
End If
```



 

 
