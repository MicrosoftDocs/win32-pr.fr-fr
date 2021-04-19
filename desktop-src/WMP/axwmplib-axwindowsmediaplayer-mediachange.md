---
title: Événement MediaChange de l’objet AxWindowsMediaPlayer
description: L’événement MediaChange se produit lorsqu’un élément multimédia change. | Événement MediaChange de l’objet AxWindowsMediaPlayer
ms.assetid: 0a2380ff-df50-4092-a952-812184822719
keywords:
- Événement MediaChange de l’objet AxWindowsMediaPlayer du lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175a7ed6ca57e3083d307cfe218d09233410053c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543806"
---
# <a name="mediachange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="1b618-105">Événement MediaChange de l’objet AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="1b618-105">MediaChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="1b618-106">L’événement MediaChange se produit lorsqu’un élément multimédia change.</span><span class="sxs-lookup"><span data-stu-id="1b618-106">The MediaChange event occurs when a media item changes.</span></span>

``` syntax
[C#]
private void player_MediaChange(
  object sender,
  _WMPOCXEvents_MediaChangeEvent e
)

[Visual Basic]
Private Sub player_MediaChange(  
  sender As Object,  
  e As _WMPOCXEvents_MediaChangeEvent
) Handles player.MediaChange
```

## <a name="event-data"></a><span data-ttu-id="1b618-107">Données d'événements</span><span class="sxs-lookup"><span data-stu-id="1b618-107">Event Data</span></span>

<span data-ttu-id="1b618-108">Le gestionnaire associé à cet événement est de type **AxWMPLib. \_ WMPOCXEvents \_ MediaChangeEventHandler**.</span><span class="sxs-lookup"><span data-stu-id="1b618-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_MediaChangeEventHandler**.</span></span> <span data-ttu-id="1b618-109">Ce gestionnaire reçoit un argument de type **AxWMPLib. \_ WMPOCXEvents \_ MediaChangeEvent**, qui contient la propriété suivante associée à cet événement.</span><span class="sxs-lookup"><span data-stu-id="1b618-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_MediaChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="1b618-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="1b618-110">Property</span></span> | <span data-ttu-id="1b618-111">Description</span><span class="sxs-lookup"><span data-stu-id="1b618-111">Description</span></span>                                                                                                    |
|----------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b618-112">Élément</span><span class="sxs-lookup"><span data-stu-id="1b618-112">Item</span></span>     | <span data-ttu-id="1b618-113">Élément multimédia System. ObjectThe modifié.</span><span class="sxs-lookup"><span data-stu-id="1b618-113">System.ObjectThe media item that changed.</span></span> <span data-ttu-id="1b618-114">Vous pouvez effectuer un cast de ce en une interface IWMPMedia pour y accéder.</span><span class="sxs-lookup"><span data-stu-id="1b618-114">You can cast this to an IWMPMedia interface to access it.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="1b618-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="1b618-115">Examples</span></span>

<span data-ttu-id="1b618-116">L’exemple suivant utilise une étiquette pour afficher le nom de l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="1b618-116">The following example uses a label to display the name of the current media item.</span></span> <span data-ttu-id="1b618-117">Le code met à jour le texte de l’étiquette avec chaque occurrence de l’événement MediaChange.</span><span class="sxs-lookup"><span data-stu-id="1b618-117">The code updates the text in the label with each occurrence of the MediaChange Event.</span></span> <span data-ttu-id="1b618-118">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="1b618-118">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the MediaChange event.
player.MediaChange += new AxWMPLib._WMPOCXEvents_MediaChangeEventHandler(player_MediaChange);

private void player_MediaChange(object sender, AxWMPLib._WMPOCXEvents_MediaChangeEvent e)
{
    // Get an interface to the changed media item that is returned in the event data. 
    WMPLib.IWMPMedia3 changedItem = (WMPLib.IWMPMedia3)e.item;

    // Display the name of the changed media item.
    mediaName.Text = changedItem.name;
}
```


```VB

Public Sub player_MediaChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_MediaChangeEvent) Handles player.MediaChange

    &#39; Get an interface to the changed media item that is returned in the event data.
    Dim changedItem As WMPLib.IWMPMedia3 = e.item

    &#39; Display the name of the changed media item.
    mediaName.Text = changedItem.name

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1b618-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b618-119">Requirements</span></span>



| <span data-ttu-id="1b618-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b618-120">Requirement</span></span> | <span data-ttu-id="1b618-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b618-121">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b618-122">Version</span><span class="sxs-lookup"><span data-stu-id="1b618-122">Version</span></span><br/>   | <span data-ttu-id="1b618-123">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1b618-123">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="1b618-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1b618-124">Namespace</span></span><br/> | <span data-ttu-id="1b618-125">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="1b618-125">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="1b618-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="1b618-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1b618-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1b618-127"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b618-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b618-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b618-129">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="1b618-129">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1b618-130">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="1b618-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





