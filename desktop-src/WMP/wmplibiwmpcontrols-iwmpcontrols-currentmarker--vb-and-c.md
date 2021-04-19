---
title: IWMPControls propriété currentMarker
description: La propriété currentMarker obtient ou définit le numéro de marqueur actuel.
ms.assetid: faf8c32a-66de-47ce-aa3d-6699d9f9bdda
keywords:
- propriété currentMarker lecteur Windows Media
- propriété currentMarker lecteur Windows Media, interface IWMPControls
- Interface IWMPControls lecteur Windows Media, propriété currentMarker
topic_type:
- apiref
api_name:
- IWMPControls.currentMarker
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfbcea42594b15b8da08248d38b5d8f72a1de29d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526854"
---
# <a name="iwmpcontrolscurrentmarker-property"></a><span data-ttu-id="3e634-106">IWMPControls :: currentMarker, propriété</span><span class="sxs-lookup"><span data-stu-id="3e634-106">IWMPControls::currentMarker property</span></span>

<span data-ttu-id="3e634-107">La propriété **currentMarker** obtient ou définit le numéro de marqueur actuel.</span><span class="sxs-lookup"><span data-stu-id="3e634-107">The **currentMarker** property gets or sets the current marker number.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e634-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e634-108">Syntax</span></span>


```CSharp
public System.Int32 currentMarker {get; set;}
```


```VB

Public Property currentMarker As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="3e634-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3e634-109">Property value</span></span>

<span data-ttu-id="3e634-110">**System. Int32** qui est le numéro de marqueur.</span><span class="sxs-lookup"><span data-stu-id="3e634-110">A **System.Int32** that is the marker number.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e634-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3e634-111">Remarks</span></span>

<span data-ttu-id="3e634-112">La définition de **currentMarker** entraîne le démarrage de la lecture à partir du marqueur spécifié.</span><span class="sxs-lookup"><span data-stu-id="3e634-112">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="3e634-113">Avant de tenter de définir **currentMarker**, déterminez si un fichier a des marqueurs et combien il a à l’aide de **IWMPMedia. markerCount**.</span><span class="sxs-lookup"><span data-stu-id="3e634-113">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **IWMPMedia.markerCount**.</span></span> <span data-ttu-id="3e634-114">Si un fichier n’a pas de marqueur, la définition de **currentMarker** sur n’importe quelle valeur, sauf zéro, génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="3e634-114">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="3e634-115">Si vous définissez **currentMarker** sur un nombre supérieur à **markerCount** , une erreur est également générée.</span><span class="sxs-lookup"><span data-stu-id="3e634-115">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="3e634-116">La propriété **currentMarker** retourne toujours le marqueur actuel ou le dernier marqueur, ce qui signifie que la position de fichier réelle peut être soit au marqueur actuel, soit avant le marqueur suivant.</span><span class="sxs-lookup"><span data-stu-id="3e634-116">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="3e634-117">Les marqueurs sont numérotés à partir de 1. par conséquent, si un fichier a des marqueurs, vous pouvez affecter la valeur zéro à **currentMarker** pour changer la position du fichier.</span><span class="sxs-lookup"><span data-stu-id="3e634-117">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="3e634-118">Tant que l’élément multimédia actuel n’est pas défini (à l’aide de **AxWindowsMediaPlayer. URL** ou de **AxWindowsMediaPlayer. CurrentMedia**), **currentMarker** retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="3e634-118">Until the current media item is set (using **AxWindowsMediaPlayer.URL** or **AxWindowsMediaPlayer.currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="3e634-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="3e634-119">Examples</span></span>

<span data-ttu-id="3e634-120">L’exemple suivant utilise **currentMarker** pour démarrer la lecture vidéo à partir du marqueur qui correspond à la propriété SelectedIndex d’une zone de liste qui a été remplie avec des identificateurs de marqueur.</span><span class="sxs-lookup"><span data-stu-id="3e634-120">The following example uses **currentMarker** to start video playback from the marker that corresponds to the SelectedIndex property of a list box which has been filled with marker identifiers.</span></span> <span data-ttu-id="3e634-121">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="3e634-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Fill the list box with the marker identifiers of the current media item.
markers.Items.Add("Begining");
markers.Items.Add("Sunrise");
markers.Items.Add("Car chase");
markers.Items.Add("Happy ending");

// Set the currentMarker to the marker selected from the list box.
private void markers_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    int selectedMarker = ((System.Windows.Forms.ListBox)sender).SelectedIndex;

    player.Ctlcontrols.currentMarker = selectedMarker;
}
```


```VB

' Fill the list box with the marker identifiers of the current media item.
markers.Items.Add(&quot;Begining&quot;)
markers.Items.Add(&quot;Sunrise&quot;)
markers.Items.Add(&quot;Car chase&quot;)
markers.Items.Add(&quot;Happy ending&quot;)

&#39; Set the currentMarker to the marker selected from the list box.
Public Sub markers_SelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles markers.SelectedIndexChanged

    Dim lb As System.Windows.Forms.ListBox = sender
    Dim selectedMarker As Integer = lb.SelectedIndex

    player.Ctlcontrols.currentMarker = selectedMarker

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3e634-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e634-122">Requirements</span></span>



| <span data-ttu-id="3e634-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e634-123">Requirement</span></span> | <span data-ttu-id="3e634-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e634-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e634-125">Version</span><span class="sxs-lookup"><span data-stu-id="3e634-125">Version</span></span><br/>   | <span data-ttu-id="3e634-126">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3e634-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3e634-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3e634-127">Namespace</span></span><br/> | <span data-ttu-id="3e634-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3e634-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3e634-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="3e634-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3e634-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3e634-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e634-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e634-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e634-132">**AxWindowsMediaPlayer. currentMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3e634-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3e634-133">**AxWindowsMediaPlayer. URL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3e634-133">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3e634-134">**Interface IWMPControls (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3e634-134">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3e634-135">**IWMPMedia. markerCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="3e634-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





