---
description: L’exemple de saisie semi-automatique montre comment implémenter la saisie semi-automatique de caractères en japonais à l’aide des interfaces de programmation d’applications (API) de reconnaissance.
ms.assetid: 237e33bc-3708-4128-8749-d3d031f7237a
title: Exemple de saisie semi-automatique de caractères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485955e1b4254fe6f2dcf4c278aca4be0b4e2b5e41617434c6f2881cfb0b02d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093053"
---
# <a name="character-autocomplete-sample"></a>Exemple de saisie semi-automatique de caractères

L’exemple de saisie semi-automatique montre comment implémenter la saisie semi-automatique de caractères en japonais à l’aide des interfaces de programmation d’applications (API) de reconnaissance.

Les fonctionnalités suivantes sont utilisées dans cet exemple :

-   Utilisation d’un *collecteur d’encre*
-   Utilisation d’un contexte de module de *reconnaissance*

## <a name="initializing-the-ink-collector-and-recognizer-context"></a>Initialisation du collecteur d’encre et du contexte du module de reconnaissance

Les objets [**InkCollector**](inkcollector-class.md) et [**InkRecognizerContext**](inkrecognizercontext-class.md) sont déclarés en tant que classes qui peuvent déclencher des événements.


```C++
Dim WithEvents ic As InkCollector
Dim WithEvents rc As InkRecognizerContext
```



Le gestionnaire d’événements Load du formulaire crée un collecteur d’encres, associe le collecteur d’encre à la zone d’image et active la collecte d’encre. Le gestionnaire d’événements charge ensuite le module de reconnaissance japonais par défaut et initialise les propriétés des traits et du repère du contexte du module de reconnaissance.


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



## <a name="loading-the-default-japanese-recognizer"></a>Chargement du module de reconnaissance japonais par défaut

La méthode [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) de [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) est appelée pour récupérer le module de reconnaissance par défaut pour la langue japonaise. Ensuite, la propriété [**languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) de l’objet IInkRecognizer est vérifiée pour déterminer si le module de reconnaissance prend en charge la langue japonaise. Si c’est le cas, la méthode [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) du module de reconnaissance est utilisée pour générer un contexte de module de reconnaissance pour le formulaire.


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



## <a name="handling-the-stroke-event"></a>Gestion de l’événement Stroke

Le gestionnaire d’événements [**Stroke**](inkcollector-stroke.md) arrête d’abord la reconnaissance en arrière-plan dans le contexte du module de reconnaissance. Ensuite, il ajoute le nouveau trait à la propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) du contexte du module de reconnaissance. Enfin, il définit la propriété [**InkRecognizerCharacterAutoCompletionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) du contexte de reconnaissance et appelle la méthode [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) du contexte de reconnaissance pour chacun des trois modes de saisie semi-automatique de caractères. Le paramètre *CustomData* de l’appel de méthode **BackgroundRecognizeWithAlternates** est utilisé pour identifier les résultats de reconnaissance qui sont retournés dans l’événement [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) .


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



## <a name="handling-the-recognition-with-alternates-event"></a>Gestion de la reconnaissance avec l’événement de substitution

Le gestionnaire de l’événement [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) vérifie d’abord le paramètre *RecognitionStatus* . En cas d’erreur dans la reconnaissance, le gestionnaire d’événements ignore les résultats de la reconnaissance. Dans le cas contraire, le gestionnaire d’événements ajoute le paramètre *RecognitionResult* à la zone d’image appropriée et enregistre la chaîne de résultat. Le paramètre *CustomData* est défini dans l’appel à la méthode [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) et identifie le mode de saisie semi-automatique des caractères qui a été utilisé par le contexte du module de reconnaissance.


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



## <a name="painting-the-form"></a>Peindre le formulaire

le gestionnaire d’événements Paint efface les zones d’image résultats et y ajoute les résultats de reconnaissance enregistrés.

## <a name="deleting-the-strokes"></a>Suppression des traits

La méthode du formulaire `CmdClear_Click` gère la commande Clear. Si le [**InkCollector**](inkcollector-class.md) collecte actuellement de l’encre, une boîte de message s’affiche et la commande est ignorée. Dans le cas contraire, le gestionnaire d’événements arrête la reconnaissance en arrière-plan, efface la propriété [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) du contexte de module de reconnaissance et supprime les traits de l’objet [**InkDisp**](inkdisp-class.md) du formulaire. Ensuite, le gestionnaire d’événements redessine la zone d’image à laquelle est associé le collecteur d’encre et efface les chaînes de reconnaissance et les zones d’image.


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



 

 
