---
title: AxWindowsMediaPlayer. currentMedia, propriété
description: La propriété currentMedia obtient ou définit l’interface IWMPMedia qui correspond à l’élément multimédia actuel.
ms.assetid: 814ccb1d-713d-4b91-b225-d2199a7c9b6b
keywords:
- propriété currentMedia lecteur Windows Media
- propriété currentMedia lecteur Windows Media, classe AxWindowsMediaPlayer
- Classe AxWindowsMediaPlayer lecteur Windows Media, propriété currentMedia
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.currentMedia
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3720a36d2a1969c652ed757f31301cf6a9ead706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533417"
---
# <a name="axwindowsmediaplayercurrentmedia-property"></a><span data-ttu-id="433e5-106">AxWindowsMediaPlayer. currentMedia, propriété</span><span class="sxs-lookup"><span data-stu-id="433e5-106">AxWindowsMediaPlayer.currentMedia property</span></span>

<span data-ttu-id="433e5-107">La propriété currentMedia obtient ou définit l’interface IWMPMedia qui correspond à l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="433e5-107">The currentMedia property gets or sets the IWMPMedia interface that corresponds to the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="433e5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="433e5-108">Syntax</span></span>


```CSharp
public IWMPMedia currentMedia {get; set;}
```


```VB

Public Property currentMedia As IWMPMedia
```





## <a name="property-value"></a><span data-ttu-id="433e5-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="433e5-109">Property value</span></span>

<span data-ttu-id="433e5-110">Interface WMPLib. IWMPMedia qui fournit l’accès à l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="433e5-110">The WMPLib.IWMPMedia interface that provides access to the current media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="433e5-111">Notes</span><span class="sxs-lookup"><span data-stu-id="433e5-111">Remarks</span></span>

<span data-ttu-id="433e5-112">Si AxWindowsMediaPlayer. Settings. la propriété **AutoStart** a la valeur true, la lecture commence automatiquement chaque fois que vous définissez **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="433e5-112">If the AxWindowsMediaPlayer.settings.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="433e5-113">Vous pouvez récupérer une interface IWMPMedia pour un élément multimédia donné via la propriété IWMPPlaylist. Item (méthode IWMPPlaylist. obtenir un \_ élément en C#).</span><span class="sxs-lookup"><span data-stu-id="433e5-113">You can retrieve an IWMPMedia interface for a given media item through the IWMPPlaylist.Item property (the IWMPPlaylist.get\_Item method in C#).</span></span> <span data-ttu-id="433e5-114">Pour charger un élément multimédia à l’aide d’un nom de fichier, définissez la propriété URL ou utilisez newMedia.</span><span class="sxs-lookup"><span data-stu-id="433e5-114">To load a media item using a file name, set the URL property or use newMedia.</span></span>

## <a name="examples"></a><span data-ttu-id="433e5-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="433e5-115">Examples</span></span>

<span data-ttu-id="433e5-116">L’exemple suivant récupère le premier élément multimédia de la bibliothèque et utilise la propriété currentMedia pour définir l’élément multimédia récupéré comme élément multimédia actuel et afficher son nom.</span><span class="sxs-lookup"><span data-stu-id="433e5-116">The following example retrieves the first media item in the library and uses the currentMedia property to set the retrieved media item as the current media item and display its name.</span></span> <span data-ttu-id="433e5-117">L’objet AxWMPLib. AxWindowsMediaPlayer est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="433e5-117">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Get an interface to the first media item in the library. 
WMPLib.IWMPMedia3 firstMedia = (WMPLib.IWMPMedia3)player.mediaCollection.getAll().get_Item(0);

// Make the retrieved media item the current media item.
player.currentMedia = firstMedia;

// Display the name of the current media item.
currentMediaLabel.Text = ("Found first media item. Name = " + player.currentMedia.name);
```


```VB

' Get an interface to the first media item in the library. 
Dim firstMedia As WMPLib.IWMPMedia3 = player.mediaCollection.getAll().Item(0)

&#39; Make the retrieved media item the current media item.
player.currentMedia = firstMedia

&#39; Display the name of the current media item.
currentMediaLabel.Text = (&quot;Found first media item. Name = &quot; + player.currentMedia.name)
```





## <a name="requirements"></a><span data-ttu-id="433e5-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="433e5-118">Requirements</span></span>



| <span data-ttu-id="433e5-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="433e5-119">Requirement</span></span> | <span data-ttu-id="433e5-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="433e5-120">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="433e5-121">Version</span><span class="sxs-lookup"><span data-stu-id="433e5-121">Version</span></span><br/>   | <span data-ttu-id="433e5-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="433e5-122">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="433e5-123">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="433e5-123">Namespace</span></span><br/> | <span data-ttu-id="433e5-124">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="433e5-124">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="433e5-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="433e5-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="433e5-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="433e5-126"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="433e5-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="433e5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="433e5-128">**Objet AxWindowsMediaPlayer (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="433e5-128">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="433e5-129">**AxWindowsMediaPlayer. newMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="433e5-129">**AxWindowsMediaPlayer.newMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-newmedia.md)
</dt> <dt>

[<span data-ttu-id="433e5-130">**AxWindowsMediaPlayer. URL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="433e5-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="433e5-131">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="433e5-131">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="433e5-132">**IWMPPlaylist. Item (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="433e5-132">**IWMPPlaylist.Item (VB and C#)**</span></span>](iwmpplaylist-item--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="433e5-133">**IWMPSettings. AutoStart (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="433e5-133">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> </dl>

 

 





