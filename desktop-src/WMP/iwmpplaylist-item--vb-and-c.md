---
title: IWMPPlaylist. Item (VB et C)
description: La propriété Item ( \_ méthode d’extraction d’élément dans C \) obtient une interface vers l’élément multimédia au niveau de l’index spécifié.
ms.assetid: 874663e2-0b89-4ef7-9d4a-3a334482b352
keywords:
- IWMPPlaylist. Item (VB et C) lecteur Windows Media
topic_type:
- apiref
api_name:
- IWMPPlaylist.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1318f37c3f590eec2c97252e2f484b0d1bc6d83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525932"
---
# <a name="iwmpplaylistitem-vb-and-c"></a><span data-ttu-id="109d1-104">IWMPPlaylist. Item (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="109d1-104">IWMPPlaylist.Item (VB and C#)</span></span>

<span data-ttu-id="109d1-105">La propriété **Item** (méthode d' **extraction d' \_ élément** en C#) obtient une interface vers l’élément multimédia à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="109d1-105">The **Item** property (the **get\_Item** method in C#) gets an interface to the media item at the specified index.</span></span>


```
[Visual Basic]
ReadOnly Property Item(
  lIndex As System.Int32
) As IWMPMedia
```




```
[C#]
IWMPMedia get_Item (
  System.Int32 lIndex 
);
```



## <a name="parameters"></a><span data-ttu-id="109d1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="109d1-106">Parameters</span></span>

<span data-ttu-id="109d1-107">*lIndex*</span><span class="sxs-lookup"><span data-stu-id="109d1-107">*lIndex*</span></span>

<span data-ttu-id="109d1-108">**System. Int32** qui est l’index de l’élément multimédia dans la sélection.</span><span class="sxs-lookup"><span data-stu-id="109d1-108">A **System.Int32** that is the index of the media item in the playlist.</span></span>

## <a name="property-value"></a><span data-ttu-id="109d1-109">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="109d1-109">Property Value</span></span>

<span data-ttu-id="109d1-110">Interface **wmplib. IWMPMedia** qui fournit l’accès à l’élément multimédia à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="109d1-110">An **WMPLib.IWMPMedia** interface that provides access to the media item at the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="109d1-111">Notes</span><span class="sxs-lookup"><span data-stu-id="109d1-111">Remarks</span></span>

<span data-ttu-id="109d1-112">**IWMPPlaylist. Item** est une propriété en lecture seule dans Visual Basic qui accepte un paramètre, tandis que en C#, elle est appelée méthode **IWMPPlaylist. obten \_ Item** .</span><span class="sxs-lookup"><span data-stu-id="109d1-112">**IWMPPlaylist.Item** is a read-only property in Visual Basic that takes a parameter, while in C# it is referred to as the **IWMPPlaylist.get\_Item** method.</span></span>

## <a name="examples"></a><span data-ttu-id="109d1-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="109d1-113">Examples</span></span>

<span data-ttu-id="109d1-114">L’exemple suivant utilise la propriété **Item** (méthode d' **extraction d' \_ élément** en C#) pour récupérer un élément multimédia à partir d’une sélection en fonction d’une sélection de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="109d1-114">The following example uses the **Item** property (the **get\_Item** method in C#) to retrieve a media item from a playlist based on a user selection.</span></span> <span data-ttu-id="109d1-115">Une zone de liste a été créée avec le nom weblist et contient les titres de la sélection appelée audioPlaylist.</span><span class="sxs-lookup"><span data-stu-id="109d1-115">A list box was created with the name weblist, and filled with the titles from the playlist called audioPlaylist.</span></span> <span data-ttu-id="109d1-116">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="109d1-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void weblist_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Store the index of the selected item in the list box.
    int index = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    // Store the corresponding media item from the playlist.
    WMPLib.IWMPMedia listItem = audioPlaylist.get_Item(index);

    // Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL;
}
```


```VB

Public Sub weblist_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles weblist.SelectedIndexChanged

    &#39; Store the index of the selected item in the list box.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim index As Integer = lb.SelectedIndex

    &#39; Store the corresponding media item from the playlist.
    Dim listItem As WMPLib.IWMPMedia = audioPlaylist.Item(index)

    &#39; Set the player URL to the URL of the selected media item.
    player.URL = listItem.sourceURL

End Sub
```





## <a name="requirements"></a><span data-ttu-id="109d1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="109d1-117">Requirements</span></span>



| <span data-ttu-id="109d1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="109d1-118">Requirement</span></span> | <span data-ttu-id="109d1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="109d1-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="109d1-120">Version</span><span class="sxs-lookup"><span data-stu-id="109d1-120">Version</span></span><br/>   | <span data-ttu-id="109d1-121">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="109d1-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="109d1-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="109d1-122">Namespace</span></span><br/> | <span data-ttu-id="109d1-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="109d1-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="109d1-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="109d1-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="109d1-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="109d1-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="109d1-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="109d1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="109d1-127">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="109d1-127">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="109d1-128">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="109d1-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="109d1-129">**IWMPPlaylist. insertItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="109d1-129">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="109d1-130">**IWMPPlaylist. removeItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="109d1-130">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="109d1-131">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="109d1-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="109d1-132">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="109d1-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





