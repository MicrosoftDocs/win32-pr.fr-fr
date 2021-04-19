---
title: Méthode IWMPMediaCollection getAttributeStringCollection
description: La méthode getAttributeStringCollection retourne une interface IWMPStringCollection qui représente l’ensemble de toutes les valeurs d’un attribut spécifié dans un type de média.
ms.assetid: 5ac19c04-75db-4618-9c4e-b20e2f709024
keywords:
- méthode getAttributeStringCollection lecteur Windows Media
- méthode getAttributeStringCollection lecteur Windows Media, interface IWMPMediaCollection
- Interface IWMPMediaCollection lecteur Windows Media, méthode getAttributeStringCollection
topic_type:
- apiref
api_name:
- IWMPMediaCollection.getAttributeStringCollection
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bef25cd811890e82273fd5d634633e25e7ec460c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534918"
---
# <a name="iwmpmediacollectiongetattributestringcollection-method"></a><span data-ttu-id="4c77d-106">IWMPMediaCollection :: getAttributeStringCollection, méthode</span><span class="sxs-lookup"><span data-stu-id="4c77d-106">IWMPMediaCollection::getAttributeStringCollection method</span></span>

<span data-ttu-id="4c77d-107">La méthode **getAttributeStringCollection** retourne une interface **IWMPStringCollection** qui représente l’ensemble de toutes les valeurs d’un attribut spécifié dans un type de média.</span><span class="sxs-lookup"><span data-stu-id="4c77d-107">The **getAttributeStringCollection** method returns an **IWMPStringCollection** interface that represents the set of all values for a specified attribute within a media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c77d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4c77d-108">Syntax</span></span>


```CSharp
public IWMPStringCollection getAttributeStringCollection(
  System.String bstrAttribute,
  System.String bstrMediaType
);
```


```VB

Public Function getAttributeStringCollection( _
  ByVal bstrAttribute As System.String, _
  ByVal bstrMediaType As System.String _
) As IWMPStringCollection
Implements IWMPMediaCollection.getAttributeStringCollection
```





## <a name="parameters"></a><span data-ttu-id="4c77d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4c77d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c77d-110">*bstrAttribute* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c77d-110">*bstrAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c77d-111">**System. String** qui est l’attribut pour lequel les valeurs sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="4c77d-111">A **System.String** that is the attribute for which the values are retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="4c77d-112">*bstrMediaType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4c77d-112">*bstrMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c77d-113">**System. String** qui est le type de média pour lequel les valeurs sont récupérées.</span><span class="sxs-lookup"><span data-stu-id="4c77d-113">A **System.String** that is the media type for which the values are retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c77d-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4c77d-114">Return value</span></span>

<span data-ttu-id="4c77d-115">Interface **wmplib. IWMPStringCollection** pour les valeurs récupérées.</span><span class="sxs-lookup"><span data-stu-id="4c77d-115">A **WMPLib.IWMPStringCollection** interface for the retrieved values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4c77d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="4c77d-116">Remarks</span></span>

<span data-ttu-id="4c77d-117">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="4c77d-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="4c77d-118">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4c77d-118">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="4c77d-119">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="4c77d-119">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="4c77d-120">Exemples</span><span class="sxs-lookup"><span data-stu-id="4c77d-120">Examples</span></span>

<span data-ttu-id="4c77d-121">L’exemple suivant utilise **getAttributeStringCollection** pour afficher une liste de valeurs qui correspondent à un attribut particulier pour les éléments audio de la collection de supports.</span><span class="sxs-lookup"><span data-stu-id="4c77d-121">The following example uses **getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="4c77d-122">Une zone de liste permet à l’utilisateur de sélectionner un attribut, tel qu’un artiste, un genre ou un album, et une zone de texte multiligne affiche le résultat.</span><span class="sxs-lookup"><span data-stu-id="4c77d-122">A list box allows the user to select an attribute, such as Artist, Genre, or Album and a multi-line text box displays the result.</span></span> <span data-ttu-id="4c77d-123">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="4c77d-123">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void audioAttributes_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Retrieve the attribute type from the ListBox
    string attributeType = (string)((System.Windows.Forms.ListBox)sender).SelectedItem;

    // Get an interface to the mediaCollection.  
    WMPLib.IWMPMediaCollection2 library = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

    // Get an interface to the string collection for the attribute type the user selects.
    WMPLib.IWMPStringCollection2 all = (WMPLib.IWMPStringCollection2)library.getAttributeStringCollection(attributeType, "Audio");

    // Clear the text box of previous results.
    attributeValues.Clear();

    // Create an array to hold the attribute values.
    string[] attributeArray = new string[all.count];
    
    // Loop through the string collection.
    for (int i = 0; i < all.count; i++)
    {
        // Store the items in the array.
        attributeArray[i] = all.Item(i);
    }

    // Display the items in the text box.
    attributeValues.Lines = attributeArray;
}
```


```VB

Public Sub audioAttributes_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles audioAttributes.SelectedIndexChanged

    &#39; Retrieve the attribute type from the ListBox
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim attributeType As String = lb.SelectedItem

    &#39; Get an interface to the mediaCollection.  
    Dim library As WMPLib.IWMPMediaCollection2 = player.mediaCollection

    &#39; Get an interface to the string collection for the attribute type the user selects.
    Dim all As WMPLib.IWMPStringCollection2 = library.getAttributeStringCollection(attributeType, &quot;Audio&quot;)

    &#39; Clear the text box of previous results.
    attributeValues.Clear()

    &#39; Create an array to hold the attribute values.
    Dim attributeArray(all.count) As String

    &#39; Loop through the string collection.
    For i As Integer = 0 To (all.count - 1)

        &#39; Store the items in the array.
        attributeArray(i) = all.Item(i)

    Next i

    &#39; Display the items in the text box.
    attributeValues.Lines = attributeArray

End Sub
```





## <a name="requirements"></a><span data-ttu-id="4c77d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c77d-124">Requirements</span></span>



| <span data-ttu-id="4c77d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c77d-125">Requirement</span></span> | <span data-ttu-id="4c77d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c77d-126">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c77d-127">Version</span><span class="sxs-lookup"><span data-stu-id="4c77d-127">Version</span></span><br/>   | <span data-ttu-id="4c77d-128">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="4c77d-128">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="4c77d-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4c77d-129">Namespace</span></span><br/> | <span data-ttu-id="4c77d-130">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="4c77d-130">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="4c77d-131">Assembly</span><span class="sxs-lookup"><span data-stu-id="4c77d-131">Assembly</span></span><br/>  | <dl> <span data-ttu-id="4c77d-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="4c77d-132"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c77d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4c77d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c77d-134">**Interface IWMPMediaCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4c77d-134">**IWMPMediaCollection Interface (VB and C#)**</span></span>](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="4c77d-135">**Interface IWMPStringCollection (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="4c77d-135">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





