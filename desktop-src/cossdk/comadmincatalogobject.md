---
description: Représente des éléments dans les collections du catalogue COM+. Utilisez-le pour récupérer et modifier les propriétés exposées par un élément dans une collection.
ms.assetid: 1d7f248b-20ec-4b34-88ab-3c68bef72b5a
title: COMAdminCatalogObject, classe (comadmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogObject
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 19fb873e29ad235b11dfe6e7a95b2ad47a8405b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110646"
---
# <a name="comadmincatalogobject-class"></a><span data-ttu-id="2c1f9-104">COMAdminCatalogObject, classe</span><span class="sxs-lookup"><span data-stu-id="2c1f9-104">COMAdminCatalogObject class</span></span>

<span data-ttu-id="2c1f9-105">Représente des éléments dans les collections du catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-105">Represents items in collections in the COM+ catalog.</span></span> <span data-ttu-id="2c1f9-106">Utilisez-le pour récupérer et modifier les propriétés exposées par un élément dans une collection.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-106">Use it to retrieve and modify properties exposed by an item in a collection.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="2c1f9-107">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="2c1f9-107">When to implement</span></span>

<span data-ttu-id="2c1f9-108">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="2c1f9-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c1f9-109">Requirement</span></span> | <span data-ttu-id="2c1f9-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c1f9-110">Value</span></span> |
|------------|------------------------------------------|
| <span data-ttu-id="2c1f9-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="2c1f9-111">Interfaces</span></span> | [<span data-ttu-id="2c1f9-112">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="2c1f9-112">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) |



 

## <a name="when-to-use"></a><span data-ttu-id="2c1f9-113">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="2c1f9-113">When to use</span></span>

<span data-ttu-id="2c1f9-114">Utilisez les objets créés à partir de la classe **COMAdminCatalogObject** pour modifier les propriétés des éléments contenus dans les collections du catalogue com+.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-114">Use objects created from the **COMAdminCatalogObject** class to modify the properties of items contained in collections in the COM+ catalog.</span></span> <span data-ttu-id="2c1f9-115">Ces éléments correspondent aux éléments affichés dans les dossiers de l’arborescence de la console de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-115">These items correspond to items shown inside folders in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="2c1f9-116">Les dossiers de l’outil d’administration Services de composants correspondent aux regroupements du catalogue, que vous pouvez représenter à l’aide d’objets créés à partir de la classe [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="2c1f9-116">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span>

<span data-ttu-id="2c1f9-117">Les collections et les éléments exposés via [**COMAdminCatalogCollection**](comadmincatalogcollection.md) et **COMAdminCatalogObject** ne sont pas tous disponibles dans l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-117">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and **COMAdminCatalogObject** are available in the Component Services administration tool.</span></span>

<span data-ttu-id="2c1f9-118">Pour plus d’informations sur des regroupements spécifiques et leurs propriétés, consultez [regroupements d’administration com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="2c1f9-118">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="2c1f9-119">Pour une introduction à l’administration par programme de COM+, consultez automatisation de l' [administration com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="2c1f9-119">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2c1f9-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2c1f9-120">Remarks</span></span>

<span data-ttu-id="2c1f9-121">Vous ne pouvez pas créer directement un objet **COMAdminCatalogObject** .</span><span class="sxs-lookup"><span data-stu-id="2c1f9-121">You cannot directly create a **COMAdminCatalogObject** object.</span></span> <span data-ttu-id="2c1f9-122">Pour utiliser les méthodes de cet objet, vous devez créer un objet [**COMAdminCatalog**](comadmincatalog.md) , obtenir une référence [**à ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), puis utiliser [**ICOMAdminCatalog :: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) pour obtenir une référence à une interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) qui représente une collection de niveau supérieur ou utiliser [**ICatalogCollection :: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) pour accéder aux collections qui ne sont pas de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-122">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection or use [**ICatalogCollection::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) to access collections that are not top-level.</span></span>

<span data-ttu-id="2c1f9-123">Une fois que vous avez une référence à l’interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) de la collection qui vous intéresse, appelez [**ICatalogCollection ::P opulate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) pour remplir la collection avec tous ses éléments.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-123">After you have a reference to the [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface of the collection in which you are interested, call [**ICatalogCollection::Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) to populate the collection with all of its items.</span></span> <span data-ttu-id="2c1f9-124">Itérez au sein de chacun des éléments de la collection en appelant [**ICatalogCollection :: obtenir l' \_ élément**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) pour obtenir une référence à chaque interface [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) .</span><span class="sxs-lookup"><span data-stu-id="2c1f9-124">Iterate through each of the items in the collection by calling [**ICatalogCollection::get\_Item**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-get_item) to get a reference to each [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject) interface.</span></span> <span data-ttu-id="2c1f9-125">Lorsque vous trouvez l’élément qui vous intéresse, vous pouvez modifier les propriétés de l’élément et quitter l’itération.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-125">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="2c1f9-126">Si vous apportez des modifications à des éléments d’une collection, vous devez appeler [**ICatalogCollection :: SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) pour enregistrer les modifications dans le catalogue com+.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-126">If you make any changes to any items in a collection, you must call [**ICatalogCollection::SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="2c1f9-127">Cela est illustré dans l’exemple suivant, où « la collection de la collection » doit être remplacée par le nom de l’une des collections d’administration COM+ de niveau supérieur ; « ItemName » doit être remplacé par le nom de l’élément qui vous intéresse ; « PropertyName » doit être remplacé par le nom de la propriété que vous modifiez dans l’élément ; et varNewProp doivent être remplacés par un VARIANT qui contient la nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-127">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and varNewProp must be replaced by a VARIANT that contains the new value for the property.</span></span>


```C++
// Convert ItemName to a BSTR.
bstrItemName = SysAllocString(L"ItemName");
HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
  CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
  (void**)&pCatalog); 
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
hr = pCatalog->GetCollection(L"TopCollection", 
  (IDispatch**)&pTopColl);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Populate the TopCollection collection.
hr = pTopColl->Populate();
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
// Get the number of items in the collection.
hr = pTopColl->get_Count(&lCount);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
VARIANT varName;
VariantInit(&varName);
// Iterate through each item in the collection.
for (LONG lIdx = 0; lIdx < lCount; lIdx++) {
    hr = pTopColl->get_Item(lIdx, (IDispatch**)&pItem);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    hr = pItem->get_Name(&varName);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    // Compare the item name to bstrItemName.
    hr = VarBstrCmp(varName.bstrVal, bstrItemName, 1024L, NULL);
    if (FAILED(hr)) exit(0);  // Replace with specific error handling.
    if (VARCMP_EQ == hr) {  // The strings are equal.
        // Use the put_Value method to modify properties of the item.
        hr = pItem->put_Value(L"PropertyName", varNewProp);
        if (FAILED(hr)) exit(0);  // Replace with specific error handling.
        break;  // Exit the iteration.
    }
}
hr = pTopColl->SaveChanges(&lNum);
if (FAILED(hr)) exit(0);  // Replace with specific error handling.
SysFreeString(bstrItemName);


```



<span data-ttu-id="2c1f9-128">Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types d’administration COM+.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-128">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="2c1f9-129">Un objet COMAdminCatalogCollection peut être créé en appelant [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) sur un objet [**COMAdminCatalog**](comadmincatalog.md) ou [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="2c1f9-129">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) or [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

<span data-ttu-id="2c1f9-130">Appelez la méthode [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) pour remplir la collection avec tous ses éléments.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-130">Call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object to populate the collection with all of its items.</span></span> <span data-ttu-id="2c1f9-131">Itérez au sein de chacun des éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-131">Iterate through each of the items in the collection.</span></span> <span data-ttu-id="2c1f9-132">Lorsque vous trouvez l’élément qui vous intéresse, vous pouvez modifier les propriétés de l’élément et quitter l’itération.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-132">When you find the item of interest, you can modify the item's properties and exit the iteration.</span></span> <span data-ttu-id="2c1f9-133">Si vous apportez des modifications à des éléments d’une collection, vous devez appeler la méthode [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) de l’objet **COMAdminCatalogCollection** pour enregistrer les modifications apportées au catalogue com+.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-133">If you make any changes to any items in a collection, you must call the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method of the **COMAdminCatalogCollection** object to save the changes to the COM+ catalog.</span></span>

<span data-ttu-id="2c1f9-134">Cela est illustré dans l’exemple suivant, où « la collection de la collection » doit être remplacée par le nom de l’une des collections d’administration COM+ de niveau supérieur ; « ItemName » doit être remplacé par le nom de l’élément qui vous intéresse ; « PropertyName » doit être remplacé par le nom de la propriété que vous modifiez dans l’élément ; et NewPropValue doivent être remplacés par la nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="2c1f9-134">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections; "ItemName" must be replaced by the name of the item that you are interested in; "PropertyName" must be replaced by the name of the property that you are modifying in the item; and NewPropValue must be replaced by the new value for the property.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")
objTopCollection.Populate
Dim objItem As COMAdmin.COMAdminCatalogObject
For Each objItem in objTopCollection
    If objItem.Name = "ItemName" Then
        objItem.Value("PropertyName") = NewPropValue
        Exit For
    End If
Next
objAppCollection.SaveChanges

```



## <a name="requirements"></a><span data-ttu-id="2c1f9-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c1f9-135">Requirements</span></span>



| <span data-ttu-id="2c1f9-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c1f9-136">Requirement</span></span> | <span data-ttu-id="2c1f9-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c1f9-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c1f9-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c1f9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2c1f9-139">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c1f9-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2c1f9-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c1f9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2c1f9-141">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c1f9-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c1f9-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c1f9-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c1f9-143"><dt>Comadmin. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c1f9-143"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c1f9-144">MIDL</span><span class="sxs-lookup"><span data-stu-id="2c1f9-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2c1f9-145"><dt>Comadmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2c1f9-145"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c1f9-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c1f9-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c1f9-147">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="2c1f9-147">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="2c1f9-148">**COMAdminCatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="2c1f9-148">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="2c1f9-149">**ICatalogObject**</span><span class="sxs-lookup"><span data-stu-id="2c1f9-149">**ICatalogObject**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)
</dt> </dl>

 

 




