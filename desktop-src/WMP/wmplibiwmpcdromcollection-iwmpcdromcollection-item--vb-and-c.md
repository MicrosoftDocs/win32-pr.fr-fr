---
title: Méthode d’élément IWMPCdromCollection
description: La méthode Item retourne une interface IWMPCdrom à l’index donné.
ms.assetid: 66e51aa9-39c8-4b79-9cc7-d7125516e87e
keywords:
- Méthode Item lecteur Windows Media
- Méthode Item lecteur Windows Media, interface IWMPCdromCollection
- Interface IWMPCdromCollection lecteur Windows Media, méthode d’élément
topic_type:
- apiref
api_name:
- IWMPCdromCollection.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf0c4a0c79a17b1e6956ba640daec74f0cbb2825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535266"
---
# <a name="iwmpcdromcollectionitem-method"></a><span data-ttu-id="0b9bb-106">IWMPCdromCollection :: Item, méthode</span><span class="sxs-lookup"><span data-stu-id="0b9bb-106">IWMPCdromCollection::Item method</span></span>

<span data-ttu-id="0b9bb-107">La méthode **Item** retourne une interface **IWMPCdrom** à l’index donné.</span><span class="sxs-lookup"><span data-stu-id="0b9bb-107">The **Item** method returns an **IWMPCdrom** interface at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b9bb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0b9bb-108">Syntax</span></span>


```CSharp
public IWMPCdrom Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPCdrom
Implements IWMPCdromCollection.Item
```





## <a name="parameters"></a><span data-ttu-id="0b9bb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b9bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b9bb-110">*Lindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0b9bb-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b9bb-111">**System. Int32** qui est l’index.</span><span class="sxs-lookup"><span data-stu-id="0b9bb-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b9bb-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b9bb-112">Return value</span></span>

<span data-ttu-id="0b9bb-113">Interface **wmplib. IWMPCdrom** .</span><span class="sxs-lookup"><span data-stu-id="0b9bb-113">A **WMPLib.IWMPCdrom** interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b9bb-114">Notes</span><span class="sxs-lookup"><span data-stu-id="0b9bb-114">Remarks</span></span>

<span data-ttu-id="0b9bb-115">Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis.</span><span class="sxs-lookup"><span data-stu-id="0b9bb-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="0b9bb-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0b9bb-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0b9bb-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="0b9bb-117">Examples</span></span>

<span data-ttu-id="0b9bb-118">L’exemple suivant utilise **Item** pour afficher le spécificateur de lecteur et le nom de la sélection à partir de chaque CD disponible sur l’ordinateur dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="0b9bb-118">The following example uses **Item** to display the drive specifier and playlist name from each CD available on the computer in a list box.</span></span> <span data-ttu-id="0b9bb-119">Si le lecteur contient réellement du contenu DVD, Windows XP ou version ultérieure est requis.</span><span class="sxs-lookup"><span data-stu-id="0b9bb-119">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="0b9bb-120">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="0b9bb-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store the number of available drives.
int numDrives = player.cdromCollection.count;

// Loop through the available drives.
for (int i = 0; i < numDrives; i++)
{
    // Store the drive specifier and playlist name for this drive in a string.
    string pl = player.cdromCollection.Item(i).driveSpecifier + " ";
    pl += player.cdromCollection.Item(i).Playlist.name;

    // Add the string to a list box.
    myPlaylists.Items.Add(pl);
}
```


```VB

' Store the number of available drives.
Dim numDrives As Integer = player.cdromCollection.count

&#39; Loop through the available drives.
For i As Integer = 0 To (numDrives - 1)

    &#39; Store the drive specifier and playlist name for this drive in a string.
    Dim pl As String = player.cdromCollection.Item(i).driveSpecifier + &quot; &quot;
    pl += player.cdromCollection.Item(i).Playlist.name

    &#39; Add the string to a list box.
    myPlaylists.Items.Add(pl)

Next i
```





## <a name="requirements"></a><span data-ttu-id="0b9bb-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b9bb-121">Requirements</span></span>



| <span data-ttu-id="0b9bb-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b9bb-122">Requirement</span></span> | <span data-ttu-id="0b9bb-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b9bb-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b9bb-124">Version</span><span class="sxs-lookup"><span data-stu-id="0b9bb-124">Version</span></span><br/>   | <span data-ttu-id="0b9bb-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0b9bb-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0b9bb-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0b9bb-126">Namespace</span></span><br/> | <span data-ttu-id="0b9bb-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0b9bb-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0b9bb-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="0b9bb-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0b9bb-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0b9bb-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b9bb-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b9bb-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b9bb-131">**Interface IWMPCdrom (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0b9bb-131">**IWMPCdrom Interface (VB and C#)**</span></span>](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0b9bb-132">**Interface IWMPCdromCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0b9bb-132">**IWMPCdromCollection Interface (VB and C#)**</span></span>](iwmpcdromcollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0b9bb-133">**IWMPCdromCollection. Count (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0b9bb-133">**IWMPCdromCollection.count (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-count--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0b9bb-134">**IWMPCdromCollection. getByDriveSpecifier (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0b9bb-134">**IWMPCdromCollection.getByDriveSpecifier (VB and C#)**</span></span>](wmplibiwmpcdromcollection-iwmpcdromcollection-getbydrivespecifier--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0b9bb-135">**IWMPPlaylist.name (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0b9bb-135">**IWMPPlaylist.name (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-name--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0b9bb-136">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0b9bb-136">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0b9bb-137">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0b9bb-137">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





