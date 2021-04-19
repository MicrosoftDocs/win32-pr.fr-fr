---
title: Méthode IWMPMedia setItemInfo
description: La méthode setItemInfo définit la valeur de l’attribut spécifié pour l’élément multimédia.
ms.assetid: 247bbba5-7d9b-489d-8e41-ae8ec6e266fd
keywords:
- méthode setItemInfo lecteur Windows Media
- méthode setItemInfo lecteur Windows Media, interface IWMPMedia
- Interface IWMPMedia lecteur Windows Media, méthode setItemInfo
topic_type:
- apiref
api_name:
- IWMPMedia.setItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6702c80c13090a370e2922ccecade49bc06645de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520955"
---
# <a name="iwmpmediasetiteminfo-method"></a><span data-ttu-id="6d6a8-106">IWMPMedia :: setItemInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="6d6a8-106">IWMPMedia::setItemInfo method</span></span>

<span data-ttu-id="6d6a8-107">La méthode **setItemInfo** définit la valeur de l’attribut spécifié pour l’élément multimédia.</span><span class="sxs-lookup"><span data-stu-id="6d6a8-107">The **setItemInfo** method sets the value of the specified attribute for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d6a8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d6a8-108">Syntax</span></span>


```CSharp
public void setItemInfo(
  System.String bstrItemName,
  System.String bstrVal
);
```


```VB

Public Sub setItemInfo( _
  ByVal bstrItemName As System.String, _
  ByVal bstrVal As System.String _
)
Implements IWMPMedia.setItemInfo
```





## <a name="parameters"></a><span data-ttu-id="6d6a8-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d6a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d6a8-110">*bstrItemName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d6a8-110">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d6a8-111">**System. String** qui est le nom de l’attribut.</span><span class="sxs-lookup"><span data-stu-id="6d6a8-111">A **System.String** that is the attribute name.</span></span>

</dd> <dt>

<span data-ttu-id="6d6a8-112">*bstrVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d6a8-112">*bstrVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d6a8-113">**System. String** qui est la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="6d6a8-113">A **System.String** that is the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d6a8-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d6a8-114">Return value</span></span>

<span data-ttu-id="6d6a8-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6d6a8-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d6a8-116">Notes</span><span class="sxs-lookup"><span data-stu-id="6d6a8-116">Remarks</span></span>

<span data-ttu-id="6d6a8-117">La propriété **attributeCount** obtient le nombre d’attributs disponibles pour un élément multimédia donné.</span><span class="sxs-lookup"><span data-stu-id="6d6a8-117">The **attributeCount** property gets the number of attributes available for a given media item.</span></span> <span data-ttu-id="6d6a8-118">Les numéros d’index peuvent ensuite être utilisés avec la méthode **getAttributeName** pour déterminer les noms des attributs intégrés qui peuvent être utilisés avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6d6a8-118">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="6d6a8-119">Avant d’utiliser cette méthode, utilisez la méthode **isReadOnlyItem** pour déterminer si un attribut particulier peut être défini.</span><span class="sxs-lookup"><span data-stu-id="6d6a8-119">Before using this method, use the **isReadOnlyItem** method to discover whether a particular attribute can be set.</span></span>

<span data-ttu-id="6d6a8-120">Avant d’appeler cette méthode, vous devez disposer d’un accès complet à la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6d6a8-120">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="6d6a8-121">Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="6d6a8-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="6d6a8-122">Remarque</span><span class="sxs-lookup"><span data-stu-id="6d6a8-122">Note</span></span>

<span data-ttu-id="6d6a8-123">Si vous incorporez le contrôle du lecteur Windows Media dans votre application, les attributs de fichier que vous modifiez ne seront pas écrits dans le fichier multimédia numérique tant que l’utilisateur n’aura pas exécuté le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="6d6a8-123">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span>

## <a name="examples"></a><span data-ttu-id="6d6a8-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="6d6a8-124">Examples</span></span>

<span data-ttu-id="6d6a8-125">L’exemple suivant utilise **setItemInfo** pour modifier la valeur de l’attribut genre pour l’élément multimédia actuel.</span><span class="sxs-lookup"><span data-stu-id="6d6a8-125">The following example uses **setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="6d6a8-126">Une zone de texte permet à l’utilisateur d’entrer une chaîne, qui est ensuite utilisée pour modifier les informations d’attribut en réponse à l’événement de clic d’un bouton.</span><span class="sxs-lookup"><span data-stu-id="6d6a8-126">A text box allows the user to enter a string, which is then used to change the attribute information in response to the Click event of a button.</span></span> <span data-ttu-id="6d6a8-127">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="6d6a8-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setNewGenre_Click(object sender, System.EventArgs e)
{
    // Store a WMPLib.IWMPMedia3 interface to the current media item. 
    WMPLib.IWMPMedia3 cm = (WMPLib.IWMPMedia3)player.currentMedia;

    // Get the user input from the TextBox. 
    string atValue = genText.Text;

    // Test for read-only status of the attribute. 
    if( cm.isReadOnlyItem("Genre") == false )
    {
        // Change the attribute value. 
        cm.setItemInfo("Genre", atValue);
    } 
}
```


```VB

Public Sub setNewGenre_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setNewGenre.Click

    &#39; Store a WMPLib.IWMPMedia3 interface to the current media item. 
    Dim cm As WMPLib.IWMPMedia3 = player.currentMedia

    &#39; Get the user input from the TextBox. 
    Dim atValue = genText.Text

    &#39; Test for read-only status of the attribute. 
    If (cm.isReadOnlyItem(&quot;Genre&quot;) = False) Then

        &#39; Change the attribute value. 
        cm.setItemInfo(&quot;Genre&quot;, atValue)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6d6a8-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d6a8-128">Requirements</span></span>



| <span data-ttu-id="6d6a8-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d6a8-129">Requirement</span></span> | <span data-ttu-id="6d6a8-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d6a8-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d6a8-131">Version</span><span class="sxs-lookup"><span data-stu-id="6d6a8-131">Version</span></span><br/>   | <span data-ttu-id="6d6a8-132">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="6d6a8-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6d6a8-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="6d6a8-133">Namespace</span></span><br/> | <span data-ttu-id="6d6a8-134">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6d6a8-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6d6a8-135">Assembly</span><span class="sxs-lookup"><span data-stu-id="6d6a8-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6d6a8-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6d6a8-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d6a8-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d6a8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d6a8-138">**Interface IWMPMedia (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6d6a8-138">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6d6a8-139">**IWMPMedia. attributeCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6d6a8-139">**IWMPMedia.attributeCount (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-attributecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6d6a8-140">**IWMPMedia. getAttributeName (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6d6a8-140">**IWMPMedia.getAttributeName (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-getattributename--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6d6a8-141">**IWMPMedia. isReadOnlyItem (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="6d6a8-141">**IWMPMedia.isReadOnlyItem (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-isreadonlyitem--vb-and-c.md)
</dt> </dl>

 

 





