---
title: IWMPMedia propriété markerCount
description: La propriété markerCount obtient le nombre de marqueurs dans l’élément multimédia.
ms.assetid: d1ccaa9b-98fb-4c53-8064-ee4bf718d18a
keywords:
- propriété markerCount lecteur Windows Media
- propriété markerCount lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, propriété markerCount
topic_type:
- apiref
api_name:
- IWMPMedia.markerCount
- IWMPMedia.get_markerCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdad591d8be66dcd20bc5e59d206a637d9b1181f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526849"
---
# <a name="iwmpmediamarkercount-property"></a><span data-ttu-id="2e734-106">IWMPMedia :: markerCount, propriété</span><span class="sxs-lookup"><span data-stu-id="2e734-106">IWMPMedia::markerCount property</span></span>

<span data-ttu-id="2e734-107">La propriété **markerCount** obtient le nombre de marqueurs dans l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="2e734-107">The **markerCount** property gets the number of markers in the media item.</span></span>

<span data-ttu-id="2e734-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2e734-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e734-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e734-109">Syntax</span></span>


```CSharp
public System.Int32 markerCount {get;}
```


```VB

Public ReadOnly Property markerCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="2e734-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="2e734-110">Property value</span></span>

<span data-ttu-id="2e734-111">**System. Int32** qui est le nombre de marqueurs.</span><span class="sxs-lookup"><span data-stu-id="2e734-111">A **System.Int32** that is the marker count.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e734-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2e734-112">Remarks</span></span>

<span data-ttu-id="2e734-113">Cette propriété retourne la valeur zéro si un fichier n’a pas de marqueurs, ou si l’élément multimédia n’est pas le même que celui spécifié dans AxWindowsMediaPlayer. currentMedia.</span><span class="sxs-lookup"><span data-stu-id="2e734-113">This property returns zero if a file has no markers, or if the media item is not the same as the one specified in AxWindowsMediaPlayer.currentMedia.</span></span>

<span data-ttu-id="2e734-114">Les numéros des marqueurs commencent à 1.</span><span class="sxs-lookup"><span data-stu-id="2e734-114">Marker numbers start at 1.</span></span>

<span data-ttu-id="2e734-115">Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="2e734-115">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="2e734-116">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="2e734-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="2e734-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="2e734-117">Examples</span></span>

<span data-ttu-id="2e734-118">L’exemple suivant utilise **markerCount** pour récupérer le nombre de marqueurs dans l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="2e734-118">The following example uses **markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="2e734-119">Cette valeur est ensuite utilisée comme limite supérieure pour une structure de bouclage, qui itère au sein de la liste de marqueurs pour récupérer chaque nom de marqueur et l’affiche dans une zone de texte multiligne.</span><span class="sxs-lookup"><span data-stu-id="2e734-119">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name and display it in a multi-line text box.</span></span> <span data-ttu-id="2e734-120">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="2e734-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get the number of markers in the current media item.
int mcount = player.currentMedia.markerCount;

// Create an array to store the list of markers.
string[] markerNames = new string[mcount];

// Verify that at least one marker exists in the current media item.
if (mcount > 0)
{
    // Loop through the marker list.
    for (int i = 1; i < mcount + 1; i++)
    {
        // Store the marker name in the array.
        markerNames[i]= player.currentMedia.getMarkerName(i);
    }

    // Display the marker names in the text box.
    markerList.Lines = markerNames;            
}
```


```VB

' Get the number of markers in the current media item.
Dim mcount As Integer = player.currentMedia.markerCount

&#39; Create an array to store the list of markers.
Dim markerNames(mcount) As String

&#39; Verify that at least one marker exists in the current media item.
If (mcount > 0) Then

    &#39; Loop through the marker list.
    For i As Integer = 1 To mcount

        &#39; Store the marker name in the array.
        markerNames(i) = player.currentMedia.getMarkerName(i)

    Next i

    &#39; Display the marker names in the text box.
    markerList.Lines = markerNames

End If
```





## <a name="requirements"></a><span data-ttu-id="2e734-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e734-121">Requirements</span></span>



| <span data-ttu-id="2e734-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e734-122">Requirement</span></span> | <span data-ttu-id="2e734-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e734-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e734-124">Version</span><span class="sxs-lookup"><span data-stu-id="2e734-124">Version</span></span><br/>   | <span data-ttu-id="2e734-125">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2e734-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2e734-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2e734-126">Namespace</span></span><br/> | <span data-ttu-id="2e734-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2e734-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2e734-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="2e734-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2e734-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2e734-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e734-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e734-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e734-131">**AxWindowsMediaPlayer. currentMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2e734-131">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2e734-132">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="2e734-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





