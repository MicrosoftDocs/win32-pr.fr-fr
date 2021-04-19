---
title: IWMPMedia propriété attributeCount
description: La propriété attributeCount obtient le nombre d’attributs qui peuvent être interrogés et/ou définis pour l’élément multimédia.
ms.assetid: 527298ff-365d-41b0-90dd-e236d6adf6fa
keywords:
- propriété attributeCount lecteur Windows Media
- propriété attributeCount lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, propriété attributeCount
topic_type:
- apiref
api_name:
- IWMPMedia.attributeCount
- IWMPMedia.get_attributeCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5a56d06a54590afd315f04a90aa582f3a364db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535373"
---
# <a name="iwmpmediaattributecount-property"></a><span data-ttu-id="231a1-106">IWMPMedia :: attributeCount, propriété</span><span class="sxs-lookup"><span data-stu-id="231a1-106">IWMPMedia::attributeCount property</span></span>

<span data-ttu-id="231a1-107">La propriété **attributeCount** obtient le nombre d’attributs qui peuvent être interrogés et/ou définis pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="231a1-107">The **attributeCount** property gets the number of attributes that can be queried and/or set for the media item.</span></span>

<span data-ttu-id="231a1-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="231a1-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="231a1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="231a1-109">Syntax</span></span>


```CSharp
public System.Int32 attributeCount {get;}
```


```VB

Public ReadOnly Property attributeCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="231a1-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="231a1-110">Property value</span></span>

<span data-ttu-id="231a1-111">**System. Int32** qui est le nombre.</span><span class="sxs-lookup"><span data-stu-id="231a1-111">A **System.Int32** that is the count.</span></span>

## <a name="remarks"></a><span data-ttu-id="231a1-112">Notes</span><span class="sxs-lookup"><span data-stu-id="231a1-112">Remarks</span></span>

<span data-ttu-id="231a1-113">Avant d’utiliser cette propriété, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="231a1-113">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="231a1-114">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="231a1-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="231a1-115">Pour plus d’informations sur les attributs pris en charge par le lecteur Windows Media, consultez la [référence d’attribut](attribute-reference.md).</span><span class="sxs-lookup"><span data-stu-id="231a1-115">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="231a1-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="231a1-116">Examples</span></span>

<span data-ttu-id="231a1-117">L’exemple suivant utilise **attributeCount** pour déterminer le nombre d’attributs disponibles dans l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="231a1-117">The following example uses **attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="231a1-118">Le code utilise cette valeur pour afficher une liste de noms d’attributs et de valeurs dans une zone de texte.</span><span class="sxs-lookup"><span data-stu-id="231a1-118">The code uses that value to display a list of attribute names and values in a text box.</span></span> <span data-ttu-id="231a1-119">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="231a1-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store an IWMPMedia3 interface to the current media item. 
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Store the number of attributes in the current media item using attributeCount.
int numAttributes = cm.attributeCount;

// Create strings to hold each attribute name and value.
string atName;
string atValue;

// Create an array to hold the attribute list.
string [] atList = new string[numAttributes];

// Loop through the attribute list.   
for (int i = 0; i < numAttributes; i++)
{
    // Fill the strings with the attribute information.
    atName = cm.getAttributeName(i);
    atValue = cm.getItemInfo(atName);

    // Store the attribute information in an array.
    atList[i] = (atName + ": " + atValue);
}

// Display the attribute information in the text box.
attributeList.Lines = atList;
```


```VB

' Store an IWMPMedia3 interface to the current media item. 
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Store the number of attributes in the current media item using attributeCount.
Dim numAttributes As Integer = cm.attributeCount

&#39; Create strings to hold each attribute name and value.
Dim atName As String
Dim atValue As String

&#39; Create an array to hold the attribute list.
Dim atList(numAttributes) As String

&#39; Loop through the attribute list.   
For i As Integer = 0 To (numAttributes - 1)

    &#39; Fill the strings with the attribute information.
    atName = cm.getAttributeName(i)
    atValue = cm.getItemInfo(atName)

    &#39; Store the attribute information in an array.
    atList(i) = (atName + &quot;: &quot; + atValue)

Next i

&#39; Display the attribute information in the text box.
attributeList.Lines = atList
```





## <a name="requirements"></a><span data-ttu-id="231a1-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="231a1-120">Requirements</span></span>



| <span data-ttu-id="231a1-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="231a1-121">Requirement</span></span> | <span data-ttu-id="231a1-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="231a1-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="231a1-123">Version</span><span class="sxs-lookup"><span data-stu-id="231a1-123">Version</span></span><br/>   | <span data-ttu-id="231a1-124">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="231a1-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="231a1-125">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="231a1-125">Namespace</span></span><br/> | <span data-ttu-id="231a1-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="231a1-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="231a1-127">Assembly</span><span class="sxs-lookup"><span data-stu-id="231a1-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="231a1-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="231a1-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="231a1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="231a1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="231a1-130">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="231a1-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





