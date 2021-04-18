---
title: IWMPPlaylist removeItem, méthode
description: La méthode removeItem supprime l’élément multimédia spécifié de la sélection.
ms.assetid: 8b5a4c34-863d-4963-97c8-cc5aa2223ab5
keywords:
- méthode removeItem lecteur Windows Media
- méthode removeItem lecteur Windows Media, interface IWMPPlaylist
- Interface IWMPPlaylist lecteur Windows Media, removeItem, méthode
topic_type:
- apiref
api_name:
- IWMPPlaylist.removeItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec845b7657e04f17c47119dd169032ebe5815786
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526007"
---
# <a name="iwmpplaylistremoveitem-method"></a><span data-ttu-id="cc12e-106">IWMPPlaylist :: removeItem, méthode</span><span class="sxs-lookup"><span data-stu-id="cc12e-106">IWMPPlaylist::removeItem method</span></span>

<span data-ttu-id="cc12e-107">La méthode **RemoveItem** supprime l’élément multimédia spécifié de la sélection.</span><span class="sxs-lookup"><span data-stu-id="cc12e-107">The **removeItem** method removes the specified media item from the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc12e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc12e-108">Syntax</span></span>


```CSharp
public void removeItem(
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub removeItem( _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.removeItem
```





## <a name="parameters"></a><span data-ttu-id="cc12e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc12e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc12e-110">*pIWMPMedia* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cc12e-110">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cc12e-111">Interface **wmplib. IWMPMedia** qui représente l’élément multimédia à supprimer de la sélection.</span><span class="sxs-lookup"><span data-stu-id="cc12e-111">A **WMPLib.IWMPMedia** interface that represents the media item to remove from the playlist.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc12e-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cc12e-112">Return value</span></span>

<span data-ttu-id="cc12e-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="cc12e-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc12e-114">Notes</span><span class="sxs-lookup"><span data-stu-id="cc12e-114">Remarks</span></span>

<span data-ttu-id="cc12e-115">Si l’élément supprimé est la piste en cours de lecture, la lecture s’arrête et l’élément suivant dans la sélection devient le suivi actuel.</span><span class="sxs-lookup"><span data-stu-id="cc12e-115">If the item removed is the currently playing track, playback stops and the next item in the playlist becomes the current one.</span></span>

<span data-ttu-id="cc12e-116">S’il n’y a pas d’élément suivant, l’élément précédent est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cc12e-116">If there is no next item, the previous item is used.</span></span> <span data-ttu-id="cc12e-117">Si aucun autre élément n’est présent, la propriété **AxWindowsMediaPlayer. currentMedia** retourne la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="cc12e-117">If there are no other items, then the **AxWindowsMediaPlayer.currentMedia** property will return **NULL**.</span></span>

<span data-ttu-id="cc12e-118">Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="cc12e-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="cc12e-119">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="cc12e-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc12e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc12e-120">Requirements</span></span>



| <span data-ttu-id="cc12e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc12e-121">Requirement</span></span> | <span data-ttu-id="cc12e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc12e-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc12e-123">Version</span><span class="sxs-lookup"><span data-stu-id="cc12e-123">Version</span></span><br/>   | <span data-ttu-id="cc12e-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cc12e-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="cc12e-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cc12e-125">Namespace</span></span><br/> | <span data-ttu-id="cc12e-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="cc12e-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="cc12e-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="cc12e-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="cc12e-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="cc12e-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc12e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc12e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc12e-130">**AxWindowsMediaPlayer. currentMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cc12e-130">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cc12e-131">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cc12e-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cc12e-132">**Interface IWMPPlaylist (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cc12e-132">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cc12e-133">**IWMPPlaylist. insertItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cc12e-133">**IWMPPlaylist.insertItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-insertitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cc12e-134">**IWMPPlaylist. Item (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cc12e-134">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cc12e-135">**IWMPSettings2. mediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cc12e-135">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="cc12e-136">**IWMPSettings2. requestMediaAccessRights (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="cc12e-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





