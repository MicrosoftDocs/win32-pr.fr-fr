---
title: Méthode IWMPMedia getMarkerName
description: La méthode getMarkerName retourne le nom du marqueur à l’index spécifié.
ms.assetid: 77f893cf-1669-41e3-9f62-8a1081e37add
keywords:
- méthode getMarkerName lecteur Windows Media
- méthode getMarkerName lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, méthode getMarkerName
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e6ba6a7bb640a397cce9c7dfd22b5f9b6203c47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521722"
---
# <a name="iwmpmediagetmarkername-method"></a><span data-ttu-id="47153-106">IWMPMedia :: getMarkerName, méthode</span><span class="sxs-lookup"><span data-stu-id="47153-106">IWMPMedia::getMarkerName method</span></span>

<span data-ttu-id="47153-107">La méthode **getMarkerName** retourne le nom du marqueur à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="47153-107">The **getMarkerName** method returns the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="47153-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47153-108">Syntax</span></span>


```CSharp
public System.String getMarkerName(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerName( _
  ByVal MarkerNum As System.Int32 _
) As System.String
Implements IWMPMedia.getMarkerName
```





## <a name="parameters"></a><span data-ttu-id="47153-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47153-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47153-110">*MarkerNum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47153-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47153-111">**System. Int32** qui est l’index du marqueur.</span><span class="sxs-lookup"><span data-stu-id="47153-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47153-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47153-112">Return value</span></span>

<span data-ttu-id="47153-113">**System. String** qui est le nom du marqueur.</span><span class="sxs-lookup"><span data-stu-id="47153-113">A **System.String** that is the marker name.</span></span>

## <a name="remarks"></a><span data-ttu-id="47153-114">Notes</span><span class="sxs-lookup"><span data-stu-id="47153-114">Remarks</span></span>

<span data-ttu-id="47153-115">Cette méthode retourne la **valeur null** si le marqueur spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="47153-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="47153-116">Certains éléments multimédias ne contiennent pas de marqueurs.</span><span class="sxs-lookup"><span data-stu-id="47153-116">Some media items do not contain markers.</span></span> <span data-ttu-id="47153-117">Utilisez **markerCount** pour déterminer le nombre de marqueurs qui se trouvent dans l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="47153-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="47153-118">Les numéros d’index des marqueurs commencent à 1.</span><span class="sxs-lookup"><span data-stu-id="47153-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="47153-119">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="47153-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="47153-120">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="47153-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="47153-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="47153-121">Examples</span></span>

<span data-ttu-id="47153-122">L’exemple de code suivant utilise **getMarkerName** pour remplir une zone de texte multiligne avec les noms des marqueurs dans l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="47153-122">The following code example uses **getMarkerName** to fill a multi-line text box with the names of the markers in the current media item.</span></span> <span data-ttu-id="47153-123">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="47153-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker names
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markers[i] = player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerNames.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mCount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker names
Dim markers(mCount) As String

&#39; Verify that at least one marker exists in the current media.
If (mCount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mCount

        &#39; Store the marker name in the array.
        markers(i) = player.currentMedia.getMarkerName(i)

    Next i

End If

&#39; Display the marker names in the text box.
markerNames.Lines = markers
```





## <a name="requirements"></a><span data-ttu-id="47153-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47153-124">Requirements</span></span>



| <span data-ttu-id="47153-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47153-125">Requirement</span></span> | <span data-ttu-id="47153-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="47153-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47153-127">Version</span><span class="sxs-lookup"><span data-stu-id="47153-127">Version</span></span><br/>   | <span data-ttu-id="47153-128">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="47153-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="47153-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="47153-129">Namespace</span></span><br/> | <span data-ttu-id="47153-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="47153-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="47153-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="47153-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="47153-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="47153-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47153-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47153-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47153-134">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="47153-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="47153-135">**IWMPMedia. markerCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="47153-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





