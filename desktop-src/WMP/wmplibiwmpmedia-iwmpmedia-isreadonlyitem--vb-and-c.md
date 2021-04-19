---
title: Méthode IWMPMedia isReadOnlyItem
description: La méthode isReadOnlyItem retourne une valeur indiquant si les attributs de l’élément multimédia spécifié peuvent être modifiés.
ms.assetid: c810c5c1-8cb9-4ac7-ac49-1ebdc86f5d7f
keywords:
- méthode isReadOnlyItem lecteur Windows Media
- méthode isReadOnlyItem lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, méthode isReadOnlyItem
topic_type:
- apiref
api_name:
- IWMPMedia.isReadOnlyItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21d3dfefc1222832783e62962298da8bcb02b25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525624"
---
# <a name="iwmpmediaisreadonlyitem-method"></a><span data-ttu-id="6f2ea-106">IWMPMedia :: isReadOnlyItem, méthode</span><span class="sxs-lookup"><span data-stu-id="6f2ea-106">IWMPMedia::isReadOnlyItem method</span></span>

<span data-ttu-id="6f2ea-107">La méthode **isReadOnlyItem** retourne une valeur indiquant si les attributs de l’élément multimédia spécifié peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="6f2ea-107">The **isReadOnlyItem** method returns a value indicating whether the attributes of the specified media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f2ea-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f2ea-108">Syntax</span></span>


```CSharp
public System.Boolean isReadOnlyItem(
  System.String bstrItemName
);
```


```VB

Public Function isReadOnlyItem( _
  ByVal bstrItemName As System.String _
) As System.Boolean
Implements IWMPMedia.isReadOnlyItem
```





## <a name="parameters"></a><span data-ttu-id="6f2ea-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f2ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f2ea-110">*bstrItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f2ea-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f2ea-111">**System. String** qui est le nom de l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="6f2ea-111">A **System.String** that is the name of the media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f2ea-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f2ea-112">Return value</span></span>

<span data-ttu-id="6f2ea-113">Valeur **System. Boolean** qui indique si les attributs sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6f2ea-113">A **System.Boolean** value that indicates whether the attributes are read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f2ea-114">Notes</span><span class="sxs-lookup"><span data-stu-id="6f2ea-114">Remarks</span></span>

<span data-ttu-id="6f2ea-115">Si un attribut est en lecture seule, il ne peut pas être défini à l’aide de la méthode **setItemInfo** .</span><span class="sxs-lookup"><span data-stu-id="6f2ea-115">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="6f2ea-116">Notez que cette méthode peut retourner des valeurs différentes pour un attribut particulier lorsqu’elle est utilisée avec différentes versions du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6f2ea-116">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="6f2ea-117">Avant d’appeler cette méthode, vous devez disposer d’un accès en lecture à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6f2ea-117">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="6f2ea-118">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6f2ea-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6f2ea-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="6f2ea-119">Examples</span></span>

<span data-ttu-id="6f2ea-120">L’exemple suivant utilise **isReadOnlyItem** pour remplir une zone de texte multiligne avec des informations sur l’élément multimédia en cours.</span><span class="sxs-lookup"><span data-stu-id="6f2ea-120">The following example uses **isReadOnlyItem** to fill a multi-line text box with information about the current media item.</span></span> <span data-ttu-id="6f2ea-121">Le code affiche chaque attribut de l’élément multimédia en cours, ainsi que le texte indiquant si l’attribut est en lecture seule ou en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6f2ea-121">The code displays each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="6f2ea-122">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="6f2ea-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Store a WMPLib.IWMPMedia3 interface to the current media item.
WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

// Get the number of attributes in the current media item.
int attCount = player.currentMedia.attributeCount;

// Create an array to store the list of attribute information.
string[] atInfo = new string[attCount];

// Create a variable to hold each attribute name.
string atName;

// Loop through the attribute list.
for (int i = 0; i < cm.attributeCount; i++)
{
    // Get the attribute name.
    atName = cm.getAttributeName(i);

    // Test whether the attribute is read-only.
    string test = ((cm.isReadOnlyItem(atName)) ? "Read-Only" : "Read/Write");

    // Store the attribute information in the array.
    atInfo[i] = (atName + " is " + test);
}

// Display the attribute information in the text box.
rwText.Lines = atInfo;
```


```VB

' Store a WMPLib.IWMPMedia3 interface to the current media item.
Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

&#39; Get the number of attributes in the current media item.
Dim attCount As Integer = player.currentMedia.attributeCount

&#39; Create an array to store the list of attribute information.
Dim atInfo(attCount) As String

&#39; Create a variable to hold each attribute name.
Dim atName As String

&#39; Loop through the attribute list.
For i As Integer = 0 To (cm.attributeCount - 1)

    &#39; Get the attribute name.
    atName = cm.getAttributeName(i)

    &#39; Test whether the attribute is read-only.
    If (cm.isReadOnlyItem(atName)) Then

        atInfo(i) = (atName + &quot; is Read-Only&quot;)

    Else

        atInfo(i) = (atName + &quot; is Read/Write&quot;)

    End If

Next i

&#39; Display the attribute information in the text box.
rwText.Lines = atInfo
```





## <a name="requirements"></a><span data-ttu-id="6f2ea-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f2ea-123">Requirements</span></span>



| <span data-ttu-id="6f2ea-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f2ea-124">Requirement</span></span> | <span data-ttu-id="6f2ea-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f2ea-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f2ea-126">Version</span><span class="sxs-lookup"><span data-stu-id="6f2ea-126">Version</span></span><br/>   | <span data-ttu-id="6f2ea-127">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6f2ea-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6f2ea-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6f2ea-128">Namespace</span></span><br/> | <span data-ttu-id="6f2ea-129">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6f2ea-130">Assembly</span><span class="sxs-lookup"><span data-stu-id="6f2ea-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6f2ea-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6f2ea-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f2ea-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f2ea-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f2ea-133">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-133">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6f2ea-134">**IWMPMedia. setItemInfo (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6f2ea-134">**IWMPMedia.setItemInfo (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





