---
title: IWMPMediaCollection méthode Remove
description: La méthode Remove supprime un élément spécifié de la collection de supports.
ms.assetid: 2ed45159-0a92-4353-8bf1-1d20de404bf7
keywords:
- Méthode Remove Windows Media Player
- Remove, méthode lecteur Windows Media, interface IWMPMediaCollection
- Interface IWMPMediaCollection lecteur Windows Media, méthode Remove
topic_type:
- apiref
api_name:
- IWMPMediaCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d341f8974255dab5e3cdce356a9b221eddff193c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544058"
---
# <a name="iwmpmediacollectionremove-method"></a><span data-ttu-id="b9bd0-106">IWMPMediaCollection :: Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="b9bd0-106">IWMPMediaCollection::remove method</span></span>

<span data-ttu-id="b9bd0-107">La `remove` méthode supprime un élément spécifié de la collection de supports.</span><span class="sxs-lookup"><span data-stu-id="b9bd0-107">The `remove` method removes a specified item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9bd0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9bd0-108">Syntax</span></span>


```CSharp
public void remove(
  IWMPMedia pItem,
  System.Boolean varfDeleteFile
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPMedia, _
  ByVal varfDeleteFile As System.Boolean _
)
Implements IWMPMediaCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="b9bd0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9bd0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9bd0-110">*pItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9bd0-110">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9bd0-111">Interface **wmplib. IWMPMedia** qui identifie l’élément à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b9bd0-111">A **WMPLib.IWMPMedia** interface that identifies the item to remove.</span></span>

</dd> <dt>

<span data-ttu-id="b9bd0-112">*varfDeleteFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b9bd0-112">*varfDeleteFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9bd0-113">Valeur **System. Boolean** qui spécifie si la méthode doit supprimer l’élément spécifié de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b9bd0-113">A **System.Boolean** value that specifies whether the method should remove the specified item from the library.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9bd0-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b9bd0-114">Return value</span></span>

<span data-ttu-id="b9bd0-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b9bd0-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9bd0-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b9bd0-116">Remarks</span></span>

<span data-ttu-id="b9bd0-117">Cette méthode supprime un élément de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b9bd0-117">This method deletes an item from the library.</span></span> <span data-ttu-id="b9bd0-118">Cette méthode ne supprime pas les fichiers de l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b9bd0-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="b9bd0-119">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="b9bd0-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="b9bd0-120">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b9bd0-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b9bd0-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="b9bd0-121">Examples</span></span>

<span data-ttu-id="b9bd0-122">L’exemple suivant, après l’invite de l’utilisateur, supprime définitivement le premier élément multimédia de la collection de supports à l’aide de `remove` .</span><span class="sxs-lookup"><span data-stu-id="b9bd0-122">The following example, after prompting the user, permanently deletes the first media item in the media collection by using `remove`.</span></span> <span data-ttu-id="b9bd0-123">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="b9bd0-123">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first item from the media collection. 
WMPLib.IWMPMedia3 media = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Store the name of the retrieved media item.
string mediaName = media.name;

// Prepare a message, a caption and buttons for the user prompt.
string message = ("OK to permanently delete " + mediaName + "?");
string caption = "Confirm deletion";
System.Windows.Forms.MessageBoxButtons buttons = System.Windows.Forms.MessageBoxButtons.OKCancel;

// Prompt the user for permission to delete the object.
System.Windows.Forms.DialogResult result = System.Windows.Forms.MessageBox.Show(message, caption, buttons);

// Check the user response.
if (result == System.Windows.Forms.DialogResult.OK)
{
    // Permanently delete the item.
    player.mediaCollection.remove(media, true);

    // Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show("Deleted item " + mediaName);
}
```


```VB

' Get an interface to the first item from the media collection. 
Dim media As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Store the name of the retrieved media item.
Dim mediaName As String = media.name

&#39; Prepare a message, a caption and buttons for the user prompt.
Dim message As String = (&quot;OK to permanently delete &quot; + mediaName + &quot;?&quot;)
Dim caption As String = &quot;Confirm deletion&quot;
Dim buttons As System.Windows.Forms.MessageBoxButtons = System.Windows.Forms.MessageBoxButtons.OKCancel

&#39; Prompt the user for permission to delete the object.
Dim result As System.Windows.Forms.DialogResult = System.Windows.Forms.MessageBox.Show(message, caption, buttons)

&#39; Check the user response.
If (result = System.Windows.Forms.DialogResult.OK) Then

    &#39; Permanently delete the item.
    player.mediaCollection.remove(media, True)

    &#39; Report that the item was deleted.
    System.Windows.Forms.MessageBox.Show(&quot;Deleted item &quot; + mediaName)

End If
```





## <a name="requirements"></a><span data-ttu-id="b9bd0-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9bd0-124">Requirements</span></span>



| <span data-ttu-id="b9bd0-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9bd0-125">Requirement</span></span> | <span data-ttu-id="b9bd0-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9bd0-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9bd0-127">Version</span><span class="sxs-lookup"><span data-stu-id="b9bd0-127">Version</span></span><br/>   | <span data-ttu-id="b9bd0-128">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b9bd0-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b9bd0-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b9bd0-129">Namespace</span></span><br/> | <span data-ttu-id="b9bd0-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b9bd0-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b9bd0-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="b9bd0-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b9bd0-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b9bd0-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9bd0-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9bd0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9bd0-134">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b9bd0-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9bd0-135">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b9bd0-135">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b9bd0-136">**IWMPMediaCollection. Add (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="b9bd0-136">**IWMPMediaCollection.add (VB and C#)**</span></span>](wmplibiwmpmediacollection-iwmpmediacollection-add--vb-and-c.md)
</dt> </dl>

 

 





