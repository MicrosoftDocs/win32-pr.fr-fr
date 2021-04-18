---
title: IWMPControls currentItem, propriété
description: La propriété currentItem obtient ou définit l’élément multimédia actuel dans une sélection.
ms.assetid: 0a331b1f-95bd-48ea-b951-1ca35cc96865
keywords:
- propriété currentItem lecteur Windows Media
- propriété currentItem lecteur Windows Media, interface IWMPControls
- Interface IWMPControls lecteur Windows Media, propriété currentItem
topic_type:
- apiref
api_name:
- IWMPControls.currentItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae04eb333e2fd347fa6f88b33ec2482a4dd8fd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526855"
---
# <a name="iwmpcontrolscurrentitem-property"></a><span data-ttu-id="8b6e9-106">IWMPControls :: currentItem, propriété</span><span class="sxs-lookup"><span data-stu-id="8b6e9-106">IWMPControls::currentItem property</span></span>

<span data-ttu-id="8b6e9-107">La propriété **CurrentItem** obtient ou définit l’élément multimédia actuel dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-107">The **currentItem** property gets or sets the current media item in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b6e9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b6e9-108">Syntax</span></span>


```CSharp
public IWMPMedia currentItem {get; set;}
```


```VB

Public Property currentItem As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="8b6e9-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8b6e9-109">Property value</span></span>

<span data-ttu-id="8b6e9-110">Interface **wmplib. IWMPMedia** qui représente l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-110">A **WMPLib.IWMPMedia** interface that represents the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b6e9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="8b6e9-111">Remarks</span></span>

<span data-ttu-id="8b6e9-112">Cette propriété fonctionne uniquement avec les éléments de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-112">This property works only with items in the current playlist.</span></span> <span data-ttu-id="8b6e9-113">La définition de **CurrentItem** sur l’interface d’un élément multimédia enregistré n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-113">Setting **currentItem** to the interface of a saved media item is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="8b6e9-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="8b6e9-114">Examples</span></span>

<span data-ttu-id="8b6e9-115">L’exemple suivant utilise **CurrentItem** pour définir l’élément multimédia actuel du joueur sur un élément sélectionné dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-115">The following example uses **currentItem** to set the player's current media item to an item selected from a list box.</span></span> <span data-ttu-id="8b6e9-116">La zone de liste a été remplie avec tous les éléments de la sélection actuelle.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-116">The list box has been filled with all of the items in the current playlist.</span></span> <span data-ttu-id="8b6e9-117">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="8b6e9-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playItem_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedItem = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop();

    // Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.get_Item(selectedItem);
    
    // Play the current item.
    player.Ctlcontrols.play();
}
```


```VB

Public Sub playItem_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles playItem.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedItem As Integer = lb.SelectedIndex

    &#39; Ensure that the previous media item is stopped.
    player.Ctlcontrols.stop()

    &#39; Set the current item to the item selected from the list box.
    player.Ctlcontrols.currentItem = player.currentPlaylist.Item(selectedItem)

    &#39; Play the current item.
    player.Ctlcontrols.play()

End Sub
```





## <a name="requirements"></a><span data-ttu-id="8b6e9-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b6e9-118">Requirements</span></span>



| <span data-ttu-id="8b6e9-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b6e9-119">Requirement</span></span> | <span data-ttu-id="8b6e9-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b6e9-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b6e9-121">Version</span><span class="sxs-lookup"><span data-stu-id="8b6e9-121">Version</span></span><br/>   | <span data-ttu-id="8b6e9-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8b6e9-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8b6e9-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8b6e9-123">Namespace</span></span><br/> | <span data-ttu-id="8b6e9-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8b6e9-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8b6e9-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="8b6e9-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8b6e9-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8b6e9-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b6e9-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8b6e9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b6e9-128">**IWMPControlsInterface (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8b6e9-128">**IWMPControlsInterface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8b6e9-129">**IWMPMediaInterface (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8b6e9-129">**IWMPMediaInterface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8b6e9-130">**IWMPPlaylistCollection. getByName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8b6e9-130">**IWMPPlaylistCollection.getByName(VB and C#)**</span></span>](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





