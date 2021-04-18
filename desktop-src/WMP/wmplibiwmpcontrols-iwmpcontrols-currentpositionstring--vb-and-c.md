---
title: IWMPControls propriété currentPositionString
description: La propriété currentPositionString obtient la position actuelle dans l’élément multimédia sous la forme d’une chaîne au format HH MM SS (heures, minutes et secondes).
ms.assetid: cd28dafa-b6a4-4bed-aa5d-7e7be6af1426
keywords:
- propriété currentPositionString lecteur Windows Media
- propriété currentPositionString lecteur Windows Media, interface IWMPControls
- Interface IWMPControls lecteur Windows Media, propriété currentPositionString
topic_type:
- apiref
api_name:
- IWMPControls.currentPositionString
- IWMPControls.get_currentPositionString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e941fceb61e4f00393b05f96489ec7ac8e950f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526853"
---
# <a name="iwmpcontrolscurrentpositionstring-property"></a><span data-ttu-id="0c6f0-106">IWMPControls :: currentPositionString, propriété</span><span class="sxs-lookup"><span data-stu-id="0c6f0-106">IWMPControls::currentPositionString property</span></span>

<span data-ttu-id="0c6f0-107">La propriété **currentPositionString** obtient la position actuelle dans l’élément multimédia sous la forme d’une chaîne au format hh : mm : SS (heures, minutes et secondes).</span><span class="sxs-lookup"><span data-stu-id="0c6f0-107">The **currentPositionString** property gets the current position in the media item as a string formatted as HH:MM:SS (hours, minutes, and seconds).</span></span>

<span data-ttu-id="0c6f0-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c6f0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c6f0-109">Syntax</span></span>


```CSharp
public System.String currentPositionString {get;}
```


```VB

Public ReadOnly Property currentPositionString As System.String
```





## <a name="property-value"></a><span data-ttu-id="0c6f0-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0c6f0-110">Property value</span></span>

<span data-ttu-id="0c6f0-111">**System. String** mis en forme qui correspond à la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-111">A formatted **System.String** that is the current position.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c6f0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0c6f0-112">Remarks</span></span>

<span data-ttu-id="0c6f0-113">Si l’élément multimédia a une valeur inférieure à une heure, la position actuelle est au format MM : SS (minutes et secondes).</span><span class="sxs-lookup"><span data-stu-id="0c6f0-113">If the media item is less than an hour long, the current position is formatted as MM:SS (minutes and seconds).</span></span>

## <a name="examples"></a><span data-ttu-id="0c6f0-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="0c6f0-114">Examples</span></span>

<span data-ttu-id="0c6f0-115">L’exemple suivant démarre une minuterie qui déclenche un événement à intervalles d’une seconde.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-115">The following example starts a timer that triggers an event at one-second intervals.</span></span> <span data-ttu-id="0c6f0-116">Dans le gestionnaire d’événements du minuteur, une étiquette est mise à jour avec **currentPositionString**.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-116">In the timer event handler, a label is updated with the **currentPositionString**.</span></span> <span data-ttu-id="0c6f0-117">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="0c6f0-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 
   
// Update the text of the label with the currentPositionString.
private void TimerEventProcessor(object sender, System.EventArgs e)
{
    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString;
}
```


```VB

' Set the timer to fire an event every second and start the timer.
timer.Interval = 1000
timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
&#39; determine when to start and stop the timer. 

&#39; Update the text of the label with the currentPositionString.
Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    currentPositionLabel.Text = player.Ctlcontrols.currentPositionString

End Sub
```





## <a name="requirements"></a><span data-ttu-id="0c6f0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c6f0-118">Requirements</span></span>



| <span data-ttu-id="0c6f0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c6f0-119">Requirement</span></span> | <span data-ttu-id="0c6f0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c6f0-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c6f0-121">Version</span><span class="sxs-lookup"><span data-stu-id="0c6f0-121">Version</span></span><br/>   | <span data-ttu-id="0c6f0-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0c6f0-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0c6f0-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0c6f0-123">Namespace</span></span><br/> | <span data-ttu-id="0c6f0-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0c6f0-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0c6f0-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="0c6f0-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0c6f0-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0c6f0-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c6f0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c6f0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c6f0-128">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0c6f0-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0c6f0-129">**IWMPControls. currentPosition (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0c6f0-129">**IWMPControls.currentPosition (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





