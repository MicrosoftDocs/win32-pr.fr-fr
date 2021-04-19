---
title: IWMPMediaCollection2 createQuery, méthode
description: La méthode createQuery retourne une interface IWMPQuery qui représente une nouvelle requête.
ms.assetid: a12da325-e77e-4e44-93d1-5e9c5733ea44
keywords:
- méthode createQuery lecteur Windows Media
- createQuery, méthode lecteur Windows Media, interface IWMPMediaCollection2
- Interface IWMPMediaCollection2 lecteur Windows Media, createQuery, méthode
topic_type:
- apiref
api_name:
- IWMPMediaCollection2.createQuery
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 318b27a20ba801e1fbed58ff79c5bed7841f8c29
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545683"
---
# <a name="iwmpmediacollection2createquery-method"></a><span data-ttu-id="0adeb-106">IWMPMediaCollection2 :: createQuery, méthode</span><span class="sxs-lookup"><span data-stu-id="0adeb-106">IWMPMediaCollection2::createQuery method</span></span>

<span data-ttu-id="0adeb-107">La `createQuery` méthode retourne une interface **IWMPQuery** qui représente une nouvelle requête.</span><span class="sxs-lookup"><span data-stu-id="0adeb-107">The `createQuery` method returns an **IWMPQuery** interface that represents a new query.</span></span>

## <a name="syntax"></a><span data-ttu-id="0adeb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0adeb-108">Syntax</span></span>


```CSharp
public IWMPQuery createQuery();
```


```VB

Public Function createQuery() As IWMPQuery
Implements IWMPMediaCollection2.createQuery
```





## <a name="parameters"></a><span data-ttu-id="0adeb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0adeb-109">Parameters</span></span>

<span data-ttu-id="0adeb-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="0adeb-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0adeb-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0adeb-111">Return value</span></span>

<span data-ttu-id="0adeb-112">Interface **wmplib. IWMPQuery** qui représente une nouvelle requête vide.</span><span class="sxs-lookup"><span data-stu-id="0adeb-112">A **WMPLib.IWMPQuery** interface that represents a new, empty query.</span></span>

## <a name="remarks"></a><span data-ttu-id="0adeb-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0adeb-113">Remarks</span></span>

<span data-ttu-id="0adeb-114">La création d’une nouvelle requête est la première étape de la création d’une requête composée.</span><span class="sxs-lookup"><span data-stu-id="0adeb-114">Creating a new query is the first step toward creating a compound query.</span></span>

## <a name="examples"></a><span data-ttu-id="0adeb-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="0adeb-115">Examples</span></span>

<span data-ttu-id="0adeb-116">L’exemple suivant utilise `createQuery` pour récupérer une interface **IWMPQuery** qui est initialisée à la valeur null.</span><span class="sxs-lookup"><span data-stu-id="0adeb-116">The following example uses `createQuery` to get an **IWMPQuery** interface that is initialized to null.</span></span> <span data-ttu-id="0adeb-117">Étant donné que cette requête n’a aucune condition ajoutée, quand elle est utilisée en tant qu’argument dans la méthode **getStringCollectionByQuery** , la méthode retourne une collection de chaînes qui contient tous les éléments multimédias du type de média spécifié.</span><span class="sxs-lookup"><span data-stu-id="0adeb-117">Because this query has no conditions added to it, when it is used as an argument in the **getStringCollectionByQuery** method, the method will return a string collection that contains all of the media items of the specified media type.</span></span> <span data-ttu-id="0adeb-118">La collection de chaînes est ensuite affichée dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="0adeb-118">The string collection is then displayed in a list box.</span></span>


```CSharp
// Get an IWMPMediaCollection2 interface so that you can access the createQuery and
// getStringCollectionByQuery methods.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;

// Create an IWMPQuery interface with no conditions added to it.
WMPLib.IWMPQuery nullQuery = mc.createQuery();

// Get a string collection that contains the titles of all the audio items in the media
// collection.
WMPLib.IWMPStringCollection2 allTitles = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", nullQuery, "audio", "", false);

// Display the titles by adding them to a list box.
for (int i = 0; i < allTitles.count; i++)
{
    queryResults.Items.Add(allTitles.Item(i));
}
```


```VB

' Get an IWMPMediaCollection2 interface so that you can access
&#39; the createQuery and getStringCollectionByQuery methods.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection

&#39; Create an IWMPQuery interface with no conditions added to it.
Dim nullQuery As WMPLib.IWMPQuery = mc.createQuery()

&#39; Get a string collection that contains the titles of all the audio items in the media
&#39; collection
Dim allTitles As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery(&quot;Title&quot;, nullQuery, &quot;audio&quot;, &quot;&quot;, False)

&#39; Display the titles by adding them to a ListBox
For i As Integer = 0 To (allTitles.count - 1)

    queryResults.Items.Add(allTitles.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="0adeb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0adeb-119">Requirements</span></span>



| <span data-ttu-id="0adeb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0adeb-120">Requirement</span></span> | <span data-ttu-id="0adeb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="0adeb-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0adeb-122">Version</span><span class="sxs-lookup"><span data-stu-id="0adeb-122">Version</span></span><br/>   | <span data-ttu-id="0adeb-123">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="0adeb-123">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="0adeb-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0adeb-124">Namespace</span></span><br/> | <span data-ttu-id="0adeb-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0adeb-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0adeb-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="0adeb-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0adeb-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0adeb-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0adeb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0adeb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0adeb-129">**Interface IWMPMediaCollection2 (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0adeb-129">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0adeb-130">**Interface IWMPQuery (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="0adeb-130">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





