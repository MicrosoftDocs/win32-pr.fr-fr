---
description: Représente n’importe quelle collection dans le catalogue COM+. Utilisez-le pour énumérer, ajouter, supprimer et récupérer des éléments dans une collection et pour accéder aux regroupements associés.
ms.assetid: 2530e44f-c428-4baa-88e1-8d01eaf234cc
title: COMAdminCatalogCollection, classe (comadmin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalogCollection
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 985a6b947708542ec3ce1dc6ecc835c94259b315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748661"
---
# <a name="comadmincatalogcollection-class"></a><span data-ttu-id="6a7f5-104">COMAdminCatalogCollection, classe</span><span class="sxs-lookup"><span data-stu-id="6a7f5-104">COMAdminCatalogCollection class</span></span>

<span data-ttu-id="6a7f5-105">Représente n’importe quelle collection dans le catalogue COM+.</span><span class="sxs-lookup"><span data-stu-id="6a7f5-105">Represents any collection in the COM+ catalog.</span></span> <span data-ttu-id="6a7f5-106">Utilisez-le pour énumérer, ajouter, supprimer et récupérer des éléments dans une collection et pour accéder aux regroupements associés.</span><span class="sxs-lookup"><span data-stu-id="6a7f5-106">Use it to enumerate, add, remove, and retrieve items in a collection and to access related collections.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="6a7f5-107">Quand implémenter</span><span class="sxs-lookup"><span data-stu-id="6a7f5-107">When to implement</span></span>

<span data-ttu-id="6a7f5-108">Cette classe est implémentée par COM+.</span><span class="sxs-lookup"><span data-stu-id="6a7f5-108">This class is implemented by COM+.</span></span>



| <span data-ttu-id="6a7f5-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a7f5-109">Requirement</span></span> | <span data-ttu-id="6a7f5-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a7f5-110">Value</span></span> |
|------------|--------------------------------------------------|
| <span data-ttu-id="6a7f5-111">Interfaces</span><span class="sxs-lookup"><span data-stu-id="6a7f5-111">Interfaces</span></span> | [<span data-ttu-id="6a7f5-112">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="6a7f5-112">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) |



 

## <a name="when-to-use"></a><span data-ttu-id="6a7f5-113">Quand l’utiliser</span><span class="sxs-lookup"><span data-stu-id="6a7f5-113">When to use</span></span>

<span data-ttu-id="6a7f5-114">Utilisez des objets créés à partir de la classe **COMAdminCatalogCollection** lorsque vous souhaitez manipuler par programmation une collection dans le catalogue com+.</span><span class="sxs-lookup"><span data-stu-id="6a7f5-114">Use objects created from the **COMAdminCatalogCollection** class when you want to programmatically manipulate a collection in the COM+ catalog.</span></span> <span data-ttu-id="6a7f5-115">Ces regroupements correspondent aux dossiers de l’outil d’administration Services de composants.</span><span class="sxs-lookup"><span data-stu-id="6a7f5-115">These collections correspond to folders in the Component Services administration tool.</span></span> <span data-ttu-id="6a7f5-116">Les éléments contenus dans les dossiers correspondent à des éléments dans des collections, que vous pouvez représenter à l’aide d’objets créés à partir de la classe [**COMAdminCatalogObject**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="6a7f5-116">Items inside the folders correspond to items in collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="6a7f5-117">Pour plus d’informations sur les regroupements du catalogue et leurs propriétés, consultez [regroupements d’administration com+](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="6a7f5-117">For information regarding the collections on the catalog and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="6a7f5-118">Pour une introduction à l’administration par programme de COM+, consultez automatisation de l' [administration com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="6a7f5-118">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6a7f5-119">Notes</span><span class="sxs-lookup"><span data-stu-id="6a7f5-119">Remarks</span></span>

<span data-ttu-id="6a7f5-120">Vous ne pouvez pas créer directement un objet **COMAdminCatalogCollection** .</span><span class="sxs-lookup"><span data-stu-id="6a7f5-120">You cannot directly create a **COMAdminCatalogCollection** object.</span></span> <span data-ttu-id="6a7f5-121">Pour utiliser les méthodes de cet objet, vous devez créer un objet [**COMAdminCatalog**](comadmincatalog.md) , obtenir une référence à [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), puis utiliser [**ICOMAdminCatalog :: GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) pour obtenir une référence à une interface [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) qui représente une collection de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="6a7f5-121">To use the methods this object, you must create a [**COMAdminCatalog**](comadmincatalog.md) object, obtain a reference to [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog), and then use [**ICOMAdminCatalog::GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) to get a reference to an [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection) interface that represents a top-level collection.</span></span> <span data-ttu-id="6a7f5-122">Cela est illustré dans l’exemple suivant, où « cocollection » doit être remplacé par le nom de l’une des collections d’administration COM+ de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="6a7f5-122">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```C++
    HRESULT hr = CoCreateInstance(CLSID_COMAdminCatalog, NULL, 
      CLSCTX_INPROC_SERVER, IID_IUnknown, (void**)&pUnknown);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pUnknown->QueryInterface(IID_ICOMAdminCatalog, 
      (void**)&pCatalog); 
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
    hr = pCatalog->GetCollection(L"TopCollection", 
      (IDispatch**)&pTopColl);
    if (FAILED (hr)) exit(0);  // Replace with specific error handling.
```



<span data-ttu-id="6a7f5-123">Pour utiliser cette classe à partir de Microsoft Visual Basic, ajoutez une référence à la bibliothèque de types d’administration COM+.</span><span class="sxs-lookup"><span data-stu-id="6a7f5-123">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="6a7f5-124">Un objet COMAdminCatalogCollection peut être créé en appelant [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) sur un objet [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="6a7f5-124">A COMAdminCatalogCollection object can be created by calling [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) on a [**COMAdminCatalog**](comadmincatalog.md) object.</span></span> <span data-ttu-id="6a7f5-125">Cela est illustré dans l’exemple suivant, où « cocollection » doit être remplacé par le nom de l’une des collections d’administration COM+ de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="6a7f5-125">This is shown in the following example, where "TopCollection" must be replaced by the name of one of the top-level COM+ administration collections.</span></span>


```VB
Dim objCatalog As COMAdmin.COMAdminCatalog
Set objCatalog = CreateObject("COMAdmin.COMAdminCatalog")
Dim objTopCollection As COMAdmin.COMAdminCatalogCollection
Set objTopCollection = objCatalog.GetCollection("TopCollection")

```



## <a name="requirements"></a><span data-ttu-id="6a7f5-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a7f5-126">Requirements</span></span>



| <span data-ttu-id="6a7f5-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a7f5-127">Requirement</span></span> | <span data-ttu-id="6a7f5-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a7f5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a7f5-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a7f5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6a7f5-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a7f5-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6a7f5-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a7f5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6a7f5-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a7f5-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a7f5-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a7f5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a7f5-134"><dt>Comadmin. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a7f5-134"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a7f5-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="6a7f5-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6a7f5-136"><dt>Comadmin. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a7f5-136"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a7f5-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a7f5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a7f5-138">**COMAdminCatalog**</span><span class="sxs-lookup"><span data-stu-id="6a7f5-138">**COMAdminCatalog**</span></span>](comadmincatalog.md)
</dt> <dt>

[<span data-ttu-id="6a7f5-139">**COMAdminCatalogObject**</span><span class="sxs-lookup"><span data-stu-id="6a7f5-139">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="6a7f5-140">**ICatalogCollection**</span><span class="sxs-lookup"><span data-stu-id="6a7f5-140">**ICatalogCollection**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
</dt> </dl>

 

 




