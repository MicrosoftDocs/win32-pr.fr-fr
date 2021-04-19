---
title: Propriété Duration de IWMPMedia
description: La propriété Duration obtient la durée en secondes de l’élément multimédia actuel.
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- propriété Duration du lecteur Windows Media
- propriété Duration lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, propriété Duration
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f796cab042713082ce2066659f62736855e62787
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545650"
---
# <a name="iwmpmediaduration-property"></a><span data-ttu-id="73a28-106">IWMPMedia ::d propriété figuration</span><span class="sxs-lookup"><span data-stu-id="73a28-106">IWMPMedia::duration property</span></span>

<span data-ttu-id="73a28-107">La propriété **Duration** obtient la durée en secondes de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="73a28-107">The **duration** property gets the duration in seconds of the current media item.</span></span>

<span data-ttu-id="73a28-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="73a28-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a28-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="73a28-109">Syntax</span></span>


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a><span data-ttu-id="73a28-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="73a28-110">Property value</span></span>

<span data-ttu-id="73a28-111">**System. double** qui correspond à la durée en secondes.</span><span class="sxs-lookup"><span data-stu-id="73a28-111">A **System.Double** that is the duration in seconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="73a28-112">Notes</span><span class="sxs-lookup"><span data-stu-id="73a28-112">Remarks</span></span>

<span data-ttu-id="73a28-113">Si cette propriété est utilisée avec un élément multimédia autre que celui spécifié dans AxWindowsMediaPlayer. currentMedia, elle ne peut pas contenir de valeur valide.</span><span class="sxs-lookup"><span data-stu-id="73a28-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span>

<span data-ttu-id="73a28-114">Pour récupérer la durée des fichiers qui ne sont pas dans la bibliothèque de l’utilisateur, vous devez attendre que le lecteur Windows Media ouvre le fichier. autrement dit, le **OpenState** actuel doit être égal à **MediaOpen**.</span><span class="sxs-lookup"><span data-stu-id="73a28-114">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current **OpenState** must equal **MediaOpen**.</span></span> <span data-ttu-id="73a28-115">Vous pouvez le vérifier en gérant **AxWindowsMediaPlayer. \_ Événement WMPOCXEvents \_ OpenStateChange** ou en vérifiant régulièrement la valeur de **AxWindowsMediaPlayer. openState**.</span><span class="sxs-lookup"><span data-stu-id="73a28-115">You can verify this by handling the **AxWindowsMediaPlayer.\_WMPOCXEvents\_OpenStateChange** event or by periodically checking the value of **AxWindowsMediaPlayer.openState**.</span></span>

<span data-ttu-id="73a28-116">Pour les sélections, la durée de chaque élément multimédia peut être récupérée lors de l’ouverture de l’élément multimédia individuel, plutôt que lors de l’ouverture de la sélection.</span><span class="sxs-lookup"><span data-stu-id="73a28-116">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="73a28-117">Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="73a28-117">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="73a28-118">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="73a28-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="73a28-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="73a28-119">Examples</span></span>

<span data-ttu-id="73a28-120">L’exemple suivant utilise **Duration** pour afficher l’heure restante dans l’élément multimédia actuel dans une étiquette.</span><span class="sxs-lookup"><span data-stu-id="73a28-120">The following example uses **duration** to display the time remaining in the current media item in a label.</span></span> <span data-ttu-id="73a28-121">Un minuteur met à jour le texte de l’étiquette chaque seconde.</span><span class="sxs-lookup"><span data-stu-id="73a28-121">A timer updates the text in the label every second.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="73a28-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="73a28-122">Requirements</span></span>



| <span data-ttu-id="73a28-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="73a28-123">Requirement</span></span> | <span data-ttu-id="73a28-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="73a28-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73a28-125">Version</span><span class="sxs-lookup"><span data-stu-id="73a28-125">Version</span></span><br/>   | <span data-ttu-id="73a28-126">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="73a28-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="73a28-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="73a28-127">Namespace</span></span><br/> | <span data-ttu-id="73a28-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="73a28-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="73a28-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="73a28-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="73a28-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="73a28-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a28-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73a28-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a28-132">**AxWindowsMediaPlayer. currentMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="73a28-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="73a28-133">**AxWindowsMediaPlayer. openState (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="73a28-133">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="73a28-134">**Événement AxWindowsMediaPlayer. OpenStateChange (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="73a28-134">**AxWindowsMediaPlayer.OpenStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="73a28-135">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="73a28-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="73a28-136">**IWMPMedia. durationString (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="73a28-136">**IWMPMedia.durationString (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 





