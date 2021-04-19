---
title: Événement CurrentItemChange de l’objet AxWindowsMediaPlayer
description: L’événement CurrentItemChange se produit lorsque la valeur de IWMPControls. currentItem change.
ms.assetid: c5eeafd2-405b-4808-97d1-399a2344ca42
keywords:
- Événement CurrentItemChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- CurrentItemChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c33bb3e9c4c1e512e742c0e679f3c5b53a29735
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541015"
---
# <a name="currentitemchange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="9ccf3-104">Événement CurrentItemChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="9ccf3-104">CurrentItemChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="9ccf3-105">L’événement CurrentItemChange se produit lorsque la valeur de IWMPControls. modifications de **CurrentItem** .</span><span class="sxs-lookup"><span data-stu-id="9ccf3-105">The CurrentItemChange event occurs when the value of IWMPControls.**currentItem** changes.</span></span>

``` syntax
[C#]
private void player_CurrentItemChange(
  object sender,
  _WMPOCXEvents_CurrentItemChangeEvent e
)

[Visual Basic]
Private Sub player_CurrentItemChange(  
  sender As Object,
  e As _WMPOCXEvents_CurrentItemChangeEvent
) Handles player.CurrentItemChange
```

## <a name="event-data"></a><span data-ttu-id="9ccf3-106">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="9ccf3-106">Event Data</span></span>

<span data-ttu-id="9ccf3-107">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="9ccf3-107">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEventHandler**.</span></span> <span data-ttu-id="9ccf3-108">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ CurrentItemChangeEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="9ccf3-108">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_CurrentItemChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="9ccf3-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="9ccf3-109">Property</span></span>   | <span data-ttu-id="9ccf3-110">Description</span><span class="sxs-lookup"><span data-stu-id="9ccf3-110">Description</span></span>                                                                                                   |
|------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ccf3-111">pdispMedia</span><span class="sxs-lookup"><span data-stu-id="9ccf3-111">pdispMedia</span></span> | <span data-ttu-id="9ccf3-112">System. ObjectThe nouvel élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="9ccf3-112">System.ObjectThe new current media item.</span></span> <span data-ttu-id="9ccf3-113">Vous pouvez effectuer un cast de ce en une interface IWMPMedia pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="9ccf3-113">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="9ccf3-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="9ccf3-114">Examples</span></span>

<span data-ttu-id="9ccf3-115">L’exemple suivant montre un gestionnaire d’événements pour l’événement CurrentItemChange.</span><span class="sxs-lookup"><span data-stu-id="9ccf3-115">The following example demonstrates an event handler for the CurrentItemChange event.</span></span> <span data-ttu-id="9ccf3-116">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="9ccf3-116">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the CurrentItemChange event
player.CurrentItemChange += new AxWMPLib._WMPOCXEvents_CurrentItemChangeEventHandler(player_CurrentItemChange);

private void player_CurrentItemChange(object sender, AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent e)
{
    // Display the name of the new media item.
    mediaText.Text = player.currentMedia.name;
}
```


```VB

Public Sub player_CurrentItemChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_CurrentItemChangeEvent) Handles player.CurrentItemChange

    &#39; Display the name of the new media item.
    mediaText.Text = player.currentMedia.name

End Sub
```





## <a name="requirements"></a><span data-ttu-id="9ccf3-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9ccf3-117">Requirements</span></span>



| <span data-ttu-id="9ccf3-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9ccf3-118">Requirement</span></span> | <span data-ttu-id="9ccf3-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="9ccf3-119">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ccf3-120">Version</span><span class="sxs-lookup"><span data-stu-id="9ccf3-120">Version</span></span><br/>   | <span data-ttu-id="9ccf3-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="9ccf3-121">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="9ccf3-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9ccf3-122">Namespace</span></span><br/> | <span data-ttu-id="9ccf3-123">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="9ccf3-123">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="9ccf3-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="9ccf3-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="9ccf3-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="9ccf3-125"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ccf3-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9ccf3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ccf3-127">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9ccf3-127">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9ccf3-128">**IWMPControls. currentItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9ccf3-128">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="9ccf3-129">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="9ccf3-129">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





