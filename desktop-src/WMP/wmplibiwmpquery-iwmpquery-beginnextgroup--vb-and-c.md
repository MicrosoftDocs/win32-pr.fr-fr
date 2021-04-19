---
title: Méthode IWMPQuery beginNextGroup
description: La méthode beginNextGroup commence un nouveau groupe de conditions. | Méthode IWMPQuery beginNextGroup
ms.assetid: 15d20c9f-2ce7-4a86-9054-b7317ebe1a0a
keywords:
- méthode beginNextGroup lecteur Windows Media
- méthode beginNextGroup lecteur Windows Media, interface IWMPQuery
- Interface IWMPQuery lecteur Windows Media, méthode beginNextGroup
topic_type:
- apiref
api_name:
- IWMPQuery.beginNextGroup
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866727f821fb40b6bf09f3ee2cf0231c4ffc3005
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525545"
---
# <a name="iwmpquerybeginnextgroup-method"></a><span data-ttu-id="599ec-107">IWMPQuery :: beginNextGroup, méthode</span><span class="sxs-lookup"><span data-stu-id="599ec-107">IWMPQuery::beginNextGroup method</span></span>

<span data-ttu-id="599ec-108">La méthode **beginNextGroup** commence un nouveau groupe de conditions.</span><span class="sxs-lookup"><span data-stu-id="599ec-108">The **beginNextGroup** method begins a new condition group.</span></span>

## <a name="syntax"></a><span data-ttu-id="599ec-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="599ec-109">Syntax</span></span>


```CSharp
public void beginNextGroup();
```


```VB

Public Sub beginNextGroup()
Implements IWMPQuery.beginNextGroup
```





## <a name="parameters"></a><span data-ttu-id="599ec-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="599ec-110">Parameters</span></span>

<span data-ttu-id="599ec-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="599ec-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="599ec-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="599ec-112">Return value</span></span>

<span data-ttu-id="599ec-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="599ec-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="599ec-114">Notes</span><span class="sxs-lookup"><span data-stu-id="599ec-114">Remarks</span></span>

<span data-ttu-id="599ec-115">Le démarrage d’un nouveau groupe de conditions implique que vous avez terminé le groupe de conditions actuel.</span><span class="sxs-lookup"><span data-stu-id="599ec-115">Beginning a new condition group implies that you have completed the current condition group.</span></span> <span data-ttu-id="599ec-116">Le nouveau groupe de conditions est toujours concaténé au groupe de conditions précédent à l’aide de **ou** logique.</span><span class="sxs-lookup"><span data-stu-id="599ec-116">The new condition group is always concatenated to the previous condition group by using **OR** logic.</span></span>

## <a name="examples"></a><span data-ttu-id="599ec-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="599ec-117">Examples</span></span>

<span data-ttu-id="599ec-118">L’exemple suivant crée une requête complexe en peignant deux groupes qui contiennent chacun une condition.</span><span class="sxs-lookup"><span data-stu-id="599ec-118">The following example creates a complex query by combing two groups that each contain a condition.</span></span> <span data-ttu-id="599ec-119">Les résultats de la requête sont extraits sous la forme d’une collection de chaînes et s’affichent dans une zone de liste.</span><span class="sxs-lookup"><span data-stu-id="599ec-119">The results of the query are extracted as a string collection and displayed in a list box.</span></span> <span data-ttu-id="599ec-120">L’objet **AxWMPLib. AxWindowsMediaPlayer** est représenté par la variable Player.</span><span class="sxs-lookup"><span data-stu-id="599ec-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Get a new Query interface.
WMPLib.IWMPMediaCollection2 mc = (WMPLib.IWMPMediaCollection2)player.mediaCollection;
WMPLib.IWMPQuery q = mc.createQuery();

// Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi");

// Begin another Query group.
q.beginNextGroup();

// Add a condition to the new group understanding that it will be combined with the
// first group using OR logic.
q.addCondition("Title", "Contains", "Capriol");

// Query the media collection and get a string collection containing the result.
// In this case, the string collection will contain the titles of all audio items that
// match the query.
WMPLib.IWMPStringCollection2 result = (WMPLib.IWMPStringCollection2)mc.getStringCollectionByQuery("Title", q, "audio", "", false);

// Display the results by adding them to a list box.
for (int i = 0; i < result.count; i++)
{
    complexQueryResults.Items.Add(result.Item(i));
}
```


```VB

' Get a new Query interface.
Dim mc As WMPLib.IWMPMediaCollection2 = player.mediaCollection
Dim q As WMPLib.IWMPQuery = mc.createQuery()

' Add a condition to the Query. 
q.addCondition("WM/Composer", "Equals", "Antonio Vivaldi")

' Begin another Query group.
q.beginNextGroup()

' Add a condition to the new group understanding that it will be combined with the
' first group using OR logic.
q.addCondition("Title", "Contains", "Capriol")

' Query the media collection and get a string collection containing the result.
' In this case, the string collection will contain the titles of all audio items that
' match the query.
Dim result As WMPLib.IWMPStringCollection2 = mc.getStringCollectionByQuery("Title", q, "audio", "", False)

' Display the results by adding them to a list box.
For i As Integer = 0 To (result.count - 1)

    complexQueryResults.Items.Add(result.Item(i))

Next i
```





## <a name="requirements"></a><span data-ttu-id="599ec-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="599ec-121">Requirements</span></span>



| <span data-ttu-id="599ec-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="599ec-122">Requirement</span></span> | <span data-ttu-id="599ec-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="599ec-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="599ec-124">Version</span><span class="sxs-lookup"><span data-stu-id="599ec-124">Version</span></span><br/>   | <span data-ttu-id="599ec-125">Lecteur Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="599ec-125">Windows Media Player 11.</span></span><br/>                                                                                    |
| <span data-ttu-id="599ec-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="599ec-126">Namespace</span></span><br/> | <span data-ttu-id="599ec-127">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="599ec-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="599ec-128">Assembly</span><span class="sxs-lookup"><span data-stu-id="599ec-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="599ec-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="599ec-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="599ec-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="599ec-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="599ec-131">**IWMPMediaCollection2. createQuery (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="599ec-131">**IWMPMediaCollection2.createQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-createquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="599ec-132">**IWMPMediaCollection2. getPlaylistByQuery (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="599ec-132">**IWMPMediaCollection2.getPlaylistByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getplaylistbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="599ec-133">**IWMPMediaCollection2. getStringCollectionByQuery (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="599ec-133">**IWMPMediaCollection2.getStringCollectionByQuery (VB and C#)**</span></span>](wmplibiwmpmediacollection2-iwmpmediacollection2-getstringcollectionbyquery--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="599ec-134">**Interface IWMPQuery (VB et C#)**</span><span class="sxs-lookup"><span data-stu-id="599ec-134">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
</dt> </dl>

 

 





