---
title: IWMPSettings. isAvailable (VB et C)
description: La propriété isAvailable (la \_ méthode obtenir IsAvailable dans C \) obtient une valeur qui indique si une action spécifiée peut être exécutée.
ms.assetid: 9db1fc50-5c2a-4d2d-b1ed-02b8e6571372
keywords:
- Lecteur Windows Media IWMPSettings. isAvailable (VB et C)
topic_type:
- apiref
api_name:
- IWMPSettings.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e932f0adb325c4c2f9f88e9f80d75ecaecd3ca85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539576"
---
# <a name="iwmpsettingsisavailable-vb-and-c"></a><span data-ttu-id="7e266-104">IWMPSettings. isAvailable (VB et C#)</span><span class="sxs-lookup"><span data-stu-id="7e266-104">IWMPSettings.isAvailable (VB and C#)</span></span>

<span data-ttu-id="7e266-105">La propriété **isAvailable** (la méthode **obtenir \_ isAvailable** en C#) obtient une valeur qui indique si une action spécifiée peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="7e266-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value that indicates whether a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
System.Boolean get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="7e266-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e266-106">Parameters</span></span>

<span data-ttu-id="7e266-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="7e266-107">*bstrItem*</span></span>

<span data-ttu-id="7e266-108">**System. String** qui est l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="7e266-108">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="7e266-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e266-109">Value</span></span>              | <span data-ttu-id="7e266-110">Description</span><span class="sxs-lookup"><span data-stu-id="7e266-110">Description</span></span>                                                                                                             |
|--------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e266-111">démarrage automatique</span><span class="sxs-lookup"><span data-stu-id="7e266-111">AutoStart</span></span>          | <span data-ttu-id="7e266-112">Détecte si la propriété AutoStart peut être définie pour spécifier que le lecteur Windows Media démarre automatiquement la lecture.</span><span class="sxs-lookup"><span data-stu-id="7e266-112">Discovers whether the autoStart property can be set to specify that Windows Media Player starts playback automatically.</span></span> |
| <span data-ttu-id="7e266-113">Balance</span><span class="sxs-lookup"><span data-stu-id="7e266-113">Balance</span></span>            | <span data-ttu-id="7e266-114">Détecte si la propriété de balance peut être utilisée pour définir le solde stéréo.</span><span class="sxs-lookup"><span data-stu-id="7e266-114">Discovers whether the balance property can be used to set the stereo balance.</span></span>                                           |
| <span data-ttu-id="7e266-115">BaseURL</span><span class="sxs-lookup"><span data-stu-id="7e266-115">BaseURL</span></span>            | <span data-ttu-id="7e266-116">Détecte si la propriété baseURL peut être définie pour spécifier une URL de base.</span><span class="sxs-lookup"><span data-stu-id="7e266-116">Discovers whether the baseURL property can be set to specify a base URL.</span></span>                                                |
| <span data-ttu-id="7e266-117">DefaultFrame</span><span class="sxs-lookup"><span data-stu-id="7e266-117">DefaultFrame</span></span>       | <span data-ttu-id="7e266-118">Détecte si la propriété defaultFrame peut être définie pour spécifier le frame par défaut.</span><span class="sxs-lookup"><span data-stu-id="7e266-118">Discovers whether the defaultFrame property can be set to specify the default frame.</span></span>                                    |
| <span data-ttu-id="7e266-119">EnableErrorDialogs</span><span class="sxs-lookup"><span data-stu-id="7e266-119">EnableErrorDialogs</span></span> | <span data-ttu-id="7e266-120">Détecte si la propriété enableErrorDialogs peut être définie pour activer ou désactiver l’affichage des boîtes de dialogue d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7e266-120">Discovers whether the enableErrorDialogs property can be set to enable or disable displaying error dialog boxes.</span></span>        |
| <span data-ttu-id="7e266-121">GetMode</span><span class="sxs-lookup"><span data-stu-id="7e266-121">GetMode</span></span>            | <span data-ttu-id="7e266-122">Détecte si la méthode getMode peut être utilisée pour récupérer la boucle en cours ou le mode de lecture aléatoire.</span><span class="sxs-lookup"><span data-stu-id="7e266-122">Discovers whether the getMode method can be used to retrieve the current loop or shuffle mode.</span></span>                          |
| <span data-ttu-id="7e266-123">InvokeURLs</span><span class="sxs-lookup"><span data-stu-id="7e266-123">InvokeURLs</span></span>         | <span data-ttu-id="7e266-124">Détecte si la propriété invokeURLs peut être définie pour spécifier si les événements d’URL doivent lancer un navigateur Web.</span><span class="sxs-lookup"><span data-stu-id="7e266-124">Discovers whether the invokeURLs property can be set to specify whether URL events should launch a Web browser.</span></span>         |
| <span data-ttu-id="7e266-125">Désactiver le son</span><span class="sxs-lookup"><span data-stu-id="7e266-125">Mute</span></span>               | <span data-ttu-id="7e266-126">Détecte si la propriété muet peut être définie pour spécifier si la sortie audio est activée ou désactivée.</span><span class="sxs-lookup"><span data-stu-id="7e266-126">Discovers whether the mute property can be set to specify whether the audio output is on or off.</span></span>                        |
| <span data-ttu-id="7e266-127">PlayCount</span><span class="sxs-lookup"><span data-stu-id="7e266-127">PlayCount</span></span>          | <span data-ttu-id="7e266-128">Détecte si la propriété playCount peut être définie pour spécifier le nombre de fois qu’un élément multimédia doit être lu.</span><span class="sxs-lookup"><span data-stu-id="7e266-128">Discovers whether the playCount property can be set to specify the number times a media item will play.</span></span>                 |
| <span data-ttu-id="7e266-129">Tarif</span><span class="sxs-lookup"><span data-stu-id="7e266-129">Rate</span></span>               | <span data-ttu-id="7e266-130">Détecte si la propriété rate peut être définie pour contrôler la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="7e266-130">Discovers whether the rate property can be set to control the playback rate.</span></span>                                            |
| <span data-ttu-id="7e266-131">SetMode</span><span class="sxs-lookup"><span data-stu-id="7e266-131">SetMode</span></span>            | <span data-ttu-id="7e266-132">Détecte si la méthode setMode peut être utilisée pour spécifier la boucle actuelle ou le mode de lecture aléatoire.</span><span class="sxs-lookup"><span data-stu-id="7e266-132">Discovers whether the setMode method can be used to specify the current loop or shuffle mode.</span></span>                           |
| <span data-ttu-id="7e266-133">Volume</span><span class="sxs-lookup"><span data-stu-id="7e266-133">Volume</span></span>             | <span data-ttu-id="7e266-134">Détecte si la propriété de volume peut être définie pour spécifier le volume audio.</span><span class="sxs-lookup"><span data-stu-id="7e266-134">Discovers whether the volume property can be set to specify the audio volume.</span></span>                                           |



 

## <a name="property-value"></a><span data-ttu-id="7e266-135">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="7e266-135">Property Value</span></span>

<span data-ttu-id="7e266-136">Valeur **System. Boolean** indiquant si l’action spécifiée peut être exécutée.</span><span class="sxs-lookup"><span data-stu-id="7e266-136">A **System.Boolean** value indicating whether the specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e266-137">Notes</span><span class="sxs-lookup"><span data-stu-id="7e266-137">Remarks</span></span>

<span data-ttu-id="7e266-138">**IWMPSettings. isIdentical** est une propriété de Visual Basic qui accepte un paramètre.</span><span class="sxs-lookup"><span data-stu-id="7e266-138">**IWMPSettings.isIdentical** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="7e266-139">En C#, on parle de méthode **IWMPSettings. obten \_ isIdentical** .</span><span class="sxs-lookup"><span data-stu-id="7e266-139">In C# it is referred to as the **IWMPSettings.get\_isIdentical** method.</span></span>

## <a name="examples"></a><span data-ttu-id="7e266-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="7e266-140">Examples</span></span>

<span data-ttu-id="7e266-141">L’exemple suivant teste chacune des propriétés **IWMPSettings** à l’aide de la propriété **isAvailable** (méthode d’extraction de la méthode **\_ IsAvailable** en C#).</span><span class="sxs-lookup"><span data-stu-id="7e266-141">The following example tests each of the **IWMPSettings** properties using the **isAvailable** property (the **get\_isAvailable** method in C#).</span></span> <span data-ttu-id="7e266-142">Le nom de la propriété et le résultat de chaque test sont affichés dans une zone de texte multiligne.</span><span class="sxs-lookup"><span data-stu-id="7e266-142">The property name and the result of each test are displayed in a multi-line text box.</span></span> <span data-ttu-id="7e266-143">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="7e266-143">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Create a string array that contains a list of IWMPSettings properties.
string[] propertyList = new string[12]{
    "AutoStart", "Balance", "BaseURL", "DefaultFrame", "EnableErrorDialogs",
    "GetMode", "InvokeURLs", "Mute", "PlayCount", "Rate", "SetMode", "Volume"
};

// Create another string array of the same size to hold the result of each
// call to get_isAvailable.
string[] results = new string[12];

// Test each property using get_isAvailable and add the name of the property
// and the result of the test to the results array.
for (int i = 0; i < propertyList.Length; i++)
{
    bool isAvailable = player.settings.get_isAvailable(propertyList[i]);

    results[i] = (propertyList[i] + " = " + isAvailable.ToString());
}

// Display the results in a multi-line text box.
playerSettings.Lines = results;
```


```VB

'  Create a string array that contains a list of IWMPSettings properties.
Dim propertyList As String() = New String(11) { _
    &quot;AutoStart&quot;, &quot;Balance&quot;, &quot;BaseURL&quot;, &quot;DefaultFrame&quot;, &quot;EnableErrorDialogs&quot;, _
    &quot;GetMode&quot;, &quot;InvokeURLs&quot;, &quot;Mute&quot;, &quot;PlayCount&quot;, &quot;Rate&quot;, &quot;SetMode&quot;, &quot;Volume&quot; _
}

&#39;  Create another string array of the same size to hold the result of each
&#39;  call to get_isAvailable.
Dim results(12) As String

&#39;  Test each property using isAvailable and add the name of the property
&#39;  and the result of the test to the results array.
For i As Integer = 0 To (propertyList.Length - 1)

    Dim isAvailable As Boolean = player.settings.isAvailable(propertyList(i))
    results(i) = (propertyList(i) + &quot; = &quot; + isAvailable.ToString())

Next i

&#39;  Display the results in a multi-line text box.
playerSettings.Lines = results
```





## <a name="requirements"></a><span data-ttu-id="7e266-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e266-144">Requirements</span></span>



| <span data-ttu-id="7e266-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e266-145">Requirement</span></span> | <span data-ttu-id="7e266-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e266-146">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e266-147">Version</span><span class="sxs-lookup"><span data-stu-id="7e266-147">Version</span></span><br/>   | <span data-ttu-id="7e266-148">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7e266-148">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="7e266-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7e266-149">Namespace</span></span><br/> | <span data-ttu-id="7e266-150">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="7e266-150">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="7e266-151">Assembly</span><span class="sxs-lookup"><span data-stu-id="7e266-151">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7e266-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="7e266-152"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e266-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e266-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e266-154">**Interface IWMPSettings (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-154">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e266-155">**IWMPSettings. AutoStart (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-155">**IWMPSettings.autoStart (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-autostart--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e266-156">**IWMPSettings. balance (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-156">**IWMPSettings.balance (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-balance--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e266-157">**IWMPSettings. baseURL (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-157">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e266-158">**IWMPSettings. defaultFrame (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-158">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e266-159">**IWMPSettings. enableErrorDialogs (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-159">**IWMPSettings.enableErrorDialogs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e266-160">**IWMPSettings. getMode (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-160">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e266-161">**IWMPSettings. invokeURLs (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-161">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e266-162">**IWMPSettings. MUTE (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-162">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e266-163">**IWMPSettings. playCount (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-163">**IWMPSettings.playCount (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-playcount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e266-164">**IWMPSettings. rate (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-164">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e266-165">**IWMPSettings. setMode (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-165">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7e266-166">**IWMPSettings. volume (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="7e266-166">**IWMPSettings.volume (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-volume--vb-and-c.md)
</dt> </dl>

 

 





