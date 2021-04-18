---
title: Méthode IWMPMedia getMarkerTime
description: La méthode getMarkerTime retourne l’heure du marqueur au niveau de l’index spécifié.
ms.assetid: 1c617e3a-0978-479c-a636-b655082232c1
keywords:
- méthode getMarkerTime lecteur Windows Media
- méthode getMarkerTime lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, méthode getMarkerTime
topic_type:
- apiref
api_name:
- IWMPMedia.getMarkerTime
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df171977adeee3b597cab1f40469af1d975425c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533446"
---
# <a name="iwmpmediagetmarkertime-method"></a><span data-ttu-id="8afea-106">IWMPMedia :: getMarkerTime, méthode</span><span class="sxs-lookup"><span data-stu-id="8afea-106">IWMPMedia::getMarkerTime method</span></span>

<span data-ttu-id="8afea-107">La méthode **getMarkerTime** retourne l’heure du marqueur au niveau de l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="8afea-107">The **getMarkerTime** method returns the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="8afea-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8afea-108">Syntax</span></span>


```CSharp
public System.Double getMarkerTime(
  System.Int32 MarkerNum
);
```


```VB

Public Function getMarkerTime( _
  ByVal MarkerNum As System.Int32 _
) As System.Double
Implements IWMPMedia.getMarkerTime
```





## <a name="parameters"></a><span data-ttu-id="8afea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8afea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8afea-110">*MarkerNum* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8afea-110">*MarkerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8afea-111">**System. Int32** qui est l’index du marqueur.</span><span class="sxs-lookup"><span data-stu-id="8afea-111">A **System.Int32** that is the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8afea-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8afea-112">Return value</span></span>

<span data-ttu-id="8afea-113">**System. double** qui correspond à l’heure du marqueur.</span><span class="sxs-lookup"><span data-stu-id="8afea-113">A **System.Double** that is the marker time.</span></span>

## <a name="remarks"></a><span data-ttu-id="8afea-114">Notes</span><span class="sxs-lookup"><span data-stu-id="8afea-114">Remarks</span></span>

<span data-ttu-id="8afea-115">Cette méthode retourne la **valeur null** si le marqueur spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="8afea-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="8afea-116">Certains éléments multimédias ne contiennent pas de marqueurs.</span><span class="sxs-lookup"><span data-stu-id="8afea-116">Some media items do not contain markers.</span></span> <span data-ttu-id="8afea-117">Utilisez **markerCount** pour déterminer le nombre de marqueurs qui se trouvent dans l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="8afea-117">Use **markerCount** to find out how many markers are in the current media item.</span></span>

<span data-ttu-id="8afea-118">Les numéros d’index des marqueurs commencent à 1.</span><span class="sxs-lookup"><span data-stu-id="8afea-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="8afea-119">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="8afea-119">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="8afea-120">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="8afea-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8afea-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="8afea-121">Examples</span></span>

<span data-ttu-id="8afea-122">L’exemple de code suivant utilise **getMarkerTime** pour remplir une zone de texte multiligne avec l’emplacement de chaque marqueur.</span><span class="sxs-lookup"><span data-stu-id="8afea-122">The following code example uses **getMarkerTime** to fill a multi-line text box with the location of each marker.</span></span> <span data-ttu-id="8afea-123">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="8afea-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of marker times.
string[] markers = new string[mcount];

// Verify that at least one marker exists in the current media.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker information in the array.
        markers[i] = "Marker number " + i + " occurs at ";
        markers[i] += player.currentMedia.getMarkerTime(i).ToString();
        markers[i] += " second(s).";
    }

    // Display the marker times in the text box.
    markerTimes.Lines = markers;
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of marker times.
Dim markers(mcount) As String

&#39; Verify that at least one marker exists in the current media.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker information in the array.
        markers(i) = (&quot;Marker number &quot; + i + &quot; occurs at &quot;)
        markers(i) += player.currentMedia.getMarkerTime(i).ToString()
        markers(i) += &quot; second(s).&quot;

    Next i

    &#39; Display the marker times in the text box.
    markerTimes.Lines = markers

End If
```





## <a name="requirements"></a><span data-ttu-id="8afea-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8afea-124">Requirements</span></span>



| <span data-ttu-id="8afea-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8afea-125">Requirement</span></span> | <span data-ttu-id="8afea-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8afea-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8afea-127">Version</span><span class="sxs-lookup"><span data-stu-id="8afea-127">Version</span></span><br/>   | <span data-ttu-id="8afea-128">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8afea-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8afea-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8afea-129">Namespace</span></span><br/> | <span data-ttu-id="8afea-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8afea-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8afea-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="8afea-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8afea-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="8afea-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8afea-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8afea-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8afea-134">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8afea-134">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8afea-135">**IWMPMedia. markerCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="8afea-135">**IWMPMedia.markerCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-markercount--vb-and-c.md)
</dt> </dl>

 

 





