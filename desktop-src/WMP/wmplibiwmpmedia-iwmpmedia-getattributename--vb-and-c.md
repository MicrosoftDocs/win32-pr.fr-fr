---
title: Méthode IWMPMedia getAttributeName
description: La méthode getAttributeName retourne le nom de l’attribut correspondant à l’index spécifié.
ms.assetid: d2496484-34cc-4222-9bc3-1d3ebb9a4173
keywords:
- méthode getAttributeName lecteur Windows Media
- méthode getAttributeName lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, méthode getAttributeName
topic_type:
- apiref
api_name:
- IWMPMedia.getAttributeName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb40ef8c0c984258dc11dd00c80807db2f4eb64a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525625"
---
# <a name="iwmpmediagetattributename-method"></a><span data-ttu-id="892b5-106">IWMPMedia :: getAttributeName, méthode</span><span class="sxs-lookup"><span data-stu-id="892b5-106">IWMPMedia::getAttributeName method</span></span>

<span data-ttu-id="892b5-107">La méthode **getAttributeName** retourne le nom de l’attribut correspondant à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="892b5-107">The **getAttributeName** method returns the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="892b5-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="892b5-108">Syntax</span></span>


```CSharp
public System.String getAttributeName(
  System.Int32 lIndex
);
```


```VB

Public Function getAttributeName( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPMedia.getAttributeName
```





## <a name="parameters"></a><span data-ttu-id="892b5-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="892b5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="892b5-110">*Lindex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="892b5-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="892b5-111">**System. Int32** qui est l’index.</span><span class="sxs-lookup"><span data-stu-id="892b5-111">A **System.Int32** that is the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="892b5-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="892b5-112">Return value</span></span>

<span data-ttu-id="892b5-113">**System. String** qui est le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="892b5-113">A **System.String** that is the attribute name.</span></span>

## <a name="remarks"></a><span data-ttu-id="892b5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="892b5-114">Remarks</span></span>

<span data-ttu-id="892b5-115">Le nom d’attribut retourné peut être utilisé conjointement avec **getItemInfo** pour récupérer la valeur d’un attribut nommé spécifique.</span><span class="sxs-lookup"><span data-stu-id="892b5-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="892b5-116">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="892b5-116">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="892b5-117">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="892b5-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="892b5-118">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="892b5-118">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="892b5-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="892b5-119">Examples</span></span>

<span data-ttu-id="892b5-120">L’exemple suivant utilise **getAttributeName** pour remplir une zone de texte multiligne avec l’index et le nom de chaque attribut de l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="892b5-120">The following example uses **getAttributeName** to fill a multi-line text box with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="892b5-121">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="892b5-121">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface for the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes for the current media item. 
int attCount = cm.attributeCount;

// Create an array of strings to hold the index and name for each attribute.
string[] attInfo = new string[attCount];

// Loop through the attribute list.
for (int i = 0; i < attCount; i++)
{
    // Store the attribute index and name in the array.
    attInfo[i] = ("Attribute " + i + ": " + cm.getAttributeName(i));
}

// Display the attribute information in the text box.
attributeNames.Lines = attInfo;
```


```VB

' Store an IWMPMedia3 interface for the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes for the current media. 
Dim attCount As Integer = cm.attributeCount

&#39; Create an array of strings to hold the index and name for each attribute.
Dim attInfo(attCount) As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (attCount - 1)

    &#39; Store the attribute index and name in the array.
    attInfo(i) = (&quot;Attribute &quot; + i.ToString() + &quot;: &quot; + cm.getAttributeName(i))

Next i

&#39; Display the attribute information in the text box.
attributeNames.Lines = attInfo
```





## <a name="requirements"></a><span data-ttu-id="892b5-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="892b5-122">Requirements</span></span>



| <span data-ttu-id="892b5-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="892b5-123">Requirement</span></span> | <span data-ttu-id="892b5-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="892b5-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="892b5-125">Version</span><span class="sxs-lookup"><span data-stu-id="892b5-125">Version</span></span><br/>   | <span data-ttu-id="892b5-126">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="892b5-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="892b5-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="892b5-127">Namespace</span></span><br/> | <span data-ttu-id="892b5-128">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="892b5-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="892b5-129">Assembly</span><span class="sxs-lookup"><span data-stu-id="892b5-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="892b5-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="892b5-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="892b5-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="892b5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="892b5-132">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="892b5-132">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="892b5-133">**IWMPMedia. getItemInfo (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="892b5-133">**IWMPMedia.getItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getiteminfo--vb-and-c.md)
</dt> </dl>

 

 





