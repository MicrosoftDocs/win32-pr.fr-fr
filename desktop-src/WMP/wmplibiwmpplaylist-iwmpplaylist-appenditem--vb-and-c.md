---
title: Méthode IWMPPlaylist appendItem
description: La méthode appendItem ajoute un élément multimédia à la fin d’une sélection.
ms.assetid: d659298b-ec4e-4771-8e9b-8cfd7b3e0eb2
keywords:
- méthode appendItem lecteur Windows Media
- méthode appendItem lecteur Windows Media, interface IWMPPlaylist
- Interface IWMPPlaylist lecteur Windows Media, méthode appendItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.appendItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a94e1b515ec6301830af2de06bae32602bdf66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543904"
---
# <a name="iwmpplaylistappenditem-method"></a><span data-ttu-id="dfcba-106">IWMPPlaylist :: appendItem, méthode</span><span class="sxs-lookup"><span data-stu-id="dfcba-106">IWMPPlaylist::appendItem method</span></span>

<span data-ttu-id="dfcba-107">La méthode **appendItem** ajoute un élément multimédia à la fin d’une sélection.</span><span class="sxs-lookup"><span data-stu-id="dfcba-107">The **appendItem** method adds a media item to the end of a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfcba-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfcba-108">Syntax</span></span>


```CSharp
public void appendItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub appendItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.appendItem
```





## <a name="parameters"></a><span data-ttu-id="dfcba-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfcba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfcba-110">*pIWMPMedia* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfcba-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfcba-111">Interface **wmplib. IWMPMedia** qui représente l’élément multimédia à ajouter.</span><span class="sxs-lookup"><span data-stu-id="dfcba-111">An **WMPLib.IWMPMedia** interface that represents the media item to be appended.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfcba-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dfcba-112">Return value</span></span>

<span data-ttu-id="dfcba-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="dfcba-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfcba-114">Notes</span><span class="sxs-lookup"><span data-stu-id="dfcba-114">Remarks</span></span>

<span data-ttu-id="dfcba-115">Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="dfcba-115">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="dfcba-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="dfcba-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="dfcba-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="dfcba-117">Examples</span></span>

<span data-ttu-id="dfcba-118">L’exemple suivant utilise **appendItem** pour ajouter l’élément multimédia actuel à la sélection nommée « ThreeList ».</span><span class="sxs-lookup"><span data-stu-id="dfcba-118">The following example uses **appendItem** to add the current media item to the playlist named "ThreeList".</span></span> <span data-ttu-id="dfcba-119">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="dfcba-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the current media item.
WMPLib.IWMPMedia currMedia = player.currentMedia;

// Get an interface to the playlist named "ThreeList".
WMPLib.IWMPPlaylist plThreeList = player.playlistCollection.getByName("ThreeList").Item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);
```


```VB

' Get an interface to the current media item.
Dim currMedia As WMPLib.IWMPMedia = player.currentMedia

&#39; Get an interface to the playlist named &quot;ThreeList&quot;.
Dim plThreeList As WMPLib.IWMPPlaylist = player.playlistCollection.getByName(&quot;ThreeList&quot;).Item(0)

&#39; Append the media item to the playlist.
plThreeList.appendItem(currMedia)
```





## <a name="requirements"></a><span data-ttu-id="dfcba-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfcba-120">Requirements</span></span>



| <span data-ttu-id="dfcba-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfcba-121">Requirement</span></span> | <span data-ttu-id="dfcba-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfcba-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfcba-123">Version</span><span class="sxs-lookup"><span data-stu-id="dfcba-123">Version</span></span><br/>   | <span data-ttu-id="dfcba-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="dfcba-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dfcba-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dfcba-125">Namespace</span></span><br/> | <span data-ttu-id="dfcba-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dfcba-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dfcba-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="dfcba-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dfcba-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dfcba-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfcba-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfcba-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfcba-130">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="dfcba-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dfcba-131">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="dfcba-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





