---
title: Événement PlayStateChange de l’objet AxWindowsMediaPlayer
description: L’événement PlayStateChange se produit lorsque l’état de lecture du contrôle du lecteur Windows Media change.
ms.assetid: f8823c90-2084-4771-a2fe-7081d4e49e63
keywords:
- Événement PlayStateChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- PlayStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af97803224df89287847ee2b9ef83d8e976d91b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526018"
---
# <a name="playstatechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="010a7-104">Événement PlayStateChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="010a7-104">PlayStateChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="010a7-105">L’événement PlayStateChange se produit lorsque l’état de lecture du contrôle du lecteur Windows Media change.</span><span class="sxs-lookup"><span data-stu-id="010a7-105">The PlayStateChange event occurs when the play state of the Windows Media Player control changes.</span></span>

``` syntax
[C#]
private void player_PlayStateChange(
  object sender,
  _WMPOCXEvents_PlayStateChangeEvent e
)

[Visual Basic]
 Private Sub player_PlayStateChange(   
 sender As Object,  
 e As _WMPOCXEvents_PlayStateChangeEvent 
 ) Handles player.PlayStateChange
 
```

## <a name="event-data"></a><span data-ttu-id="010a7-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="010a7-106">Event Data</span></span>

<span data-ttu-id="010a7-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ PlayStateChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="010a7-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_PlayStateChangeEventHandler**.</span></span> <span data-ttu-id="010a7-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ PlayStateChangeEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="010a7-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_PlayStateChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="010a7-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="010a7-109">Property</span></span>     | <span data-ttu-id="010a7-110">Description</span><span class="sxs-lookup"><span data-stu-id="010a7-110">Description</span></span>                                     |
|--------------|-------------------------------------------------|
| <span data-ttu-id="010a7-111">**newState**</span><span class="sxs-lookup"><span data-stu-id="010a7-111">**newState**</span></span> | <span data-ttu-id="010a7-112">System. Int32Specifies : nouvel État.</span><span class="sxs-lookup"><span data-stu-id="010a7-112">System.Int32Specifies the new state.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="010a7-113">Notes</span><span class="sxs-lookup"><span data-stu-id="010a7-113">Remarks</span></span>

<span data-ttu-id="010a7-114">Il n’est pas garanti que les États du lecteur Windows Media se produisent dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="010a7-114">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="010a7-115">En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements.</span><span class="sxs-lookup"><span data-stu-id="010a7-115">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="010a7-116">Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.</span><span class="sxs-lookup"><span data-stu-id="010a7-116">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="010a7-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="010a7-117">Examples</span></span>

<span data-ttu-id="010a7-118">L’exemple suivant montre un gestionnaire d’événements pour l’événement PlayStateChange qui affiche l’état de lecture actuel dans une étiquette.</span><span class="sxs-lookup"><span data-stu-id="010a7-118">The following example demonstrates an event handler for the PlayStateChange Event that displays the current play state in a label.</span></span> <span data-ttu-id="010a7-119">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="010a7-119">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test the current state of the player and display a message for each state.
    switch (e.newState)
    {
        case 0:    // Undefined
            currentStateLabel.Text = "Undefined";
            break;

        case 1:    // Stopped
            currentStateLabel.Text = "Stopped";
            break;

        case 2:    // Paused
            currentStateLabel.Text = "Paused";
            break;

        case 3:    // Playing
            currentStateLabel.Text = "Playing";
            break;

        case 4:    // ScanForward
            currentStateLabel.Text = "ScanForward";
            break;

        case 5:    // ScanReverse
            currentStateLabel.Text = "ScanReverse";
            break;

        case 6:    // Buffering
            currentStateLabel.Text = "Buffering";
            break;

        case 7:    // Waiting
            currentStateLabel.Text = "Waiting";
            break;

        case 8:    // MediaEnded
            currentStateLabel.Text = "MediaEnded";
            break;

        case 9:    // Transitioning
            currentStateLabel.Text = "Transitioning";
            break;

        case 10:   // Ready
            currentStateLabel.Text = "Ready";
            break;

        case 11:   // Reconnecting
            currentStateLabel.Text = "Reconnecting";
            break;

        case 12:   // Last
            currentStateLabel.Text = "Last";
            break;

        default:
            currentStateLabel.Text = ("Unknown State: " + e.newState.ToString());
            break;
    }
}
```




```VB
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    ' Test the current state of the player, display a message for each state.
    Select Case e.newState

        Case 0 ' Undefined
            currentStateLabel.Text = "Undefined"

        Case 1 ' Stopped
            currentStateLabel.Text = "Stopped"

        Case 2 ' Paused
            currentStateLabel.Text = "Paused"

        Case 3 ' Playing
            currentStateLabel.Text = "Playing"

        Case 4 ' ScanForward
            currentStateLabel.Text = "ScanForward"

        Case 5 ' ScanReverse
            currentStateLabel.Text = "ScanReverse"

        Case 6 ' Buffering
            currentStateLabel.Text = "Buffering"

        Case 7 ' Waiting
            currentStateLabel.Text = "Waiting"

        Case 8 ' MediaEnded
            currentStateLabel.Text = "MediaEnded"

        Case 9 ' Transitioning
            currentStateLabel.Text = "Transitioning"

        Case 10 ' Ready
            currentStateLabel.Text = "Ready"

        Case 11 ' Reconnecting
            currentStateLabel.Text = "Reconnecting"

        Case 12 ' Last
            currentStateLabel.Text = "Last"

        Case Else
            currentStateLabel.Text = ("Unknown State: " + e.newState.ToString())

    End Select

End Sub
```



## <a name="requirements"></a><span data-ttu-id="010a7-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="010a7-120">Requirements</span></span>



| <span data-ttu-id="010a7-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="010a7-121">Requirement</span></span> | <span data-ttu-id="010a7-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="010a7-122">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="010a7-123">Version</span><span class="sxs-lookup"><span data-stu-id="010a7-123">Version</span></span><br/>   | <span data-ttu-id="010a7-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="010a7-124">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="010a7-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="010a7-125">Namespace</span></span><br/> | <span data-ttu-id="010a7-126">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="010a7-126">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="010a7-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="010a7-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="010a7-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="010a7-128"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="010a7-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="010a7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="010a7-130">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="010a7-130">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="010a7-131">**AxWindowsMediaPlayer. lecture (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="010a7-131">**AxWindowsMediaPlayer.playState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-playstate--vb-and-c.md)
</dt> </dl>

 

 





