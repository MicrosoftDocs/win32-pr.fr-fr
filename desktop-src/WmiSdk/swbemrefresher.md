---
description: L’objet SWbemRefresher est un objet conteneur qui peut actualiser les données pour tous les objets qui y sont ajoutés. Ensemble d’objets ajoutés, chaque élément représenté par une instance SWbemRefreshableItem peut être traité comme une collection et être énuméré.
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: Objet SWbemRefresher (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f763ec4f738b612b9f2fef32871a63d6b170f96d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953425"
---
# <a name="swbemrefresher-object"></a><span data-ttu-id="3b8ef-104">Objet SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="3b8ef-104">SWbemRefresher object</span></span>

<span data-ttu-id="3b8ef-105">L’objet **SWbemRefresher** est un objet conteneur qui peut actualiser les données de tous les objets qui y sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-105">The **SWbemRefresher** object is a container object that can refresh the data for all the objects that are added to it.</span></span> <span data-ttu-id="3b8ef-106">Les instances uniques et les énumérateurs d’instance peuvent être ajoutés ou supprimés du conteneur.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-106">Single instances and instance enumerators can be added or removed from the container.</span></span> <span data-ttu-id="3b8ef-107">Le jeu d’objets ajoutés, chaque élément représenté par une instance [**SWbemRefreshableItem**](swbemrefreshableitem.md) , peut être traité comme une collection et être énuméré.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-107">The set of added objects, each item represented by an [**SWbemRefreshableItem**](swbemrefreshableitem.md) instance, can be treated as a collection and enumerated.</span></span> <span data-ttu-id="3b8ef-108">Les instances WMI de toute classe peuvent être ajoutées à l’objet **SWbemRefresher** .</span><span class="sxs-lookup"><span data-stu-id="3b8ef-108">WMI instances from any class can be added to the **SWbemRefresher** object.</span></span> <span data-ttu-id="3b8ef-109">Même si le fournisseur des données d’instance n’est pas un fournisseur à hautes performances, l’objet [**actualisateur**](swbemrefresher-refresh.md) peut toujours mettre à jour les données lors de l’appel d’actualisation.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-109">Even if the provider for the instance data is not a high-performance provider, the refresher object can still update the data on the [**Refresh**](swbemrefresher-refresh.md) call.</span></span> <span data-ttu-id="3b8ef-110">Si les données sont fournies par le biais d’un fournisseur de haute performance et que la propriété [**reconnexion automatique**](swbemrefresher-autoreconnect.md) a la **valeur true**, l’objet **SWbemRefresher** tente de rétablir une connexion rompue au fournisseur de données.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-110">If the data is supplied through a high-performance provider and the [**AutoReconnect**](swbemrefresher-autoreconnect.md) property is **TRUE**, then the **SWbemRefresher** object attempts to reestablish a broken connection to the data provider.</span></span> <span data-ttu-id="3b8ef-111">Cet objet peut être créé par l’appel VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="3b8ef-111">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="3b8ef-112">L’opération d’actualisation peut être effectuée en appelant la méthode [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) ou la méthode [**SWbemObjectEx. Refresh \_**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="3b8ef-112">The refresh operation can be carried out by calling either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="3b8ef-113">Membres</span><span class="sxs-lookup"><span data-stu-id="3b8ef-113">Members</span></span>

<span data-ttu-id="3b8ef-114">L’objet **SWbemRefresher** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3b8ef-114">The **SWbemRefresher** object has these types of members:</span></span>

-   [<span data-ttu-id="3b8ef-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3b8ef-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="3b8ef-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b8ef-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3b8ef-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3b8ef-117">Methods</span></span>

<span data-ttu-id="3b8ef-118">L’objet **SWbemRefresher** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-118">The **SWbemRefresher** object has these methods.</span></span>



| <span data-ttu-id="3b8ef-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="3b8ef-119">Method</span></span>                                        | <span data-ttu-id="3b8ef-120">Description</span><span class="sxs-lookup"><span data-stu-id="3b8ef-120">Description</span></span>                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b8ef-121">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="3b8ef-121">**Add**</span></span>](swbemrefresher-add.md)             | <span data-ttu-id="3b8ef-122">Ajoute un nouvel objet actualisable à la collection dans l’objet actualisateur.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-122">Adds a new refreshable object to the collection in the refresher object.</span></span><br/>                   |
| [<span data-ttu-id="3b8ef-123">**AddEnum**</span><span class="sxs-lookup"><span data-stu-id="3b8ef-123">**AddEnum**</span></span>](swbemrefresher-addenum.md)     | <span data-ttu-id="3b8ef-124">Ajoute un nouvel énumérateur à l’objet actualisateur.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-124">Adds a new enumerator to the refresher object.</span></span><br/>                                             |
| [<span data-ttu-id="3b8ef-125">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="3b8ef-125">**DeleteAll**</span></span>](swbemrefresher-deleteall.md) | <span data-ttu-id="3b8ef-126">Supprime tous les éléments de la collection dans l’objet actualisateur.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-126">Removes all items from the collection in the refresher object.</span></span><br/>                             |
| [<span data-ttu-id="3b8ef-127">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3b8ef-127">**Item**</span></span>](swbemrefresher-item.md)           | <span data-ttu-id="3b8ef-128">Retourne un élément d’actualisation spécifié à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-128">Returns a specified refresher item from the collection.</span></span><br/>                                    |
| [<span data-ttu-id="3b8ef-129">**Générer**</span><span class="sxs-lookup"><span data-stu-id="3b8ef-129">**Refresh**</span></span>](swbemrefresher-refresh.md)     | <span data-ttu-id="3b8ef-130">Met à jour tous les éléments contenus dans l’objet actualisateur.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-130">Updates all the items that are contained in the refresher object.</span></span><br/>                          |
| [<span data-ttu-id="3b8ef-131">**Installez**</span><span class="sxs-lookup"><span data-stu-id="3b8ef-131">**Remove**</span></span>](swbemrefresher-remove.md)       | <span data-ttu-id="3b8ef-132">Supprime l’objet d’élément d’actualisation ou le jeu d’objets avec un index spécifié de l’actualisateur.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-132">Removes the refresher item object or object set with a specified index from the refresher.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3b8ef-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3b8ef-133">Properties</span></span>

<span data-ttu-id="3b8ef-134">L’objet **SWbemRefresher** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-134">The **SWbemRefresher** object has these properties.</span></span>



| <span data-ttu-id="3b8ef-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="3b8ef-135">Property</span></span>                                                         | <span data-ttu-id="3b8ef-136">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="3b8ef-136">Access type</span></span>          | <span data-ttu-id="3b8ef-137">Description</span><span class="sxs-lookup"><span data-stu-id="3b8ef-137">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3b8ef-138">**Reconnexion automatique**</span><span class="sxs-lookup"><span data-stu-id="3b8ef-138">**AutoReconnect**</span></span>](swbemrefresher-autoreconnect.md)<br/> | <span data-ttu-id="3b8ef-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b8ef-139">Read-only</span></span><br/> | <span data-ttu-id="3b8ef-140">Indique si l’actualisateur se reconnecte automatiquement à un fournisseur distant si la connexion est interrompue.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-140">Indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span><br/> |
| [<span data-ttu-id="3b8ef-141">**Saut**</span><span class="sxs-lookup"><span data-stu-id="3b8ef-141">**Count**</span></span>](swbemrefresher-count.md)<br/>                 | <span data-ttu-id="3b8ef-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3b8ef-142">Read-only</span></span><br/> | <span data-ttu-id="3b8ef-143">Contient le nombre d’éléments dans l’objet actualisateur.</span><span class="sxs-lookup"><span data-stu-id="3b8ef-143">Contains the number of items in the refresher object.</span></span><br/>                                                      |



 

## <a name="examples"></a><span data-ttu-id="3b8ef-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="3b8ef-144">Examples</span></span>

<span data-ttu-id="3b8ef-145">L’exemple suivant illustre la création d’un objet **SWbemRefresher** à l’aide des méthodes [**Add**](swbemrefresher-add.md) et [**AddEnum**](swbemrefresher-addenum.md) pour stocker une instance unique et une instance d’énumération, l’actualisation des données et l’utilisation de la propriété Item pour obtenir les objets [**SWbemRefreshableItem**](swbemrefreshableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="3b8ef-145">The following example illustrates creating an **SWbemRefresher** object, using the [**Add**](swbemrefresher-add.md) and [**AddEnum**](swbemrefresher-addenum.md) methods to store a single instance and an enumeration instance, the refreshing of the data, and using the Item property to obtain the [**SWbemRefreshableItem**](swbemrefreshableitem.md) objects.</span></span>


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a><span data-ttu-id="3b8ef-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b8ef-146">Requirements</span></span>



| <span data-ttu-id="3b8ef-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b8ef-147">Requirement</span></span> | <span data-ttu-id="3b8ef-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b8ef-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b8ef-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b8ef-149">Minimum supported client</span></span><br/> | <span data-ttu-id="3b8ef-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b8ef-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3b8ef-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3b8ef-151">Minimum supported server</span></span><br/> | <span data-ttu-id="3b8ef-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b8ef-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3b8ef-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="3b8ef-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b8ef-154"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b8ef-154"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b8ef-155">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3b8ef-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b8ef-156"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3b8ef-156"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3b8ef-157">DLL</span><span class="sxs-lookup"><span data-stu-id="3b8ef-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b8ef-158"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b8ef-158"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b8ef-159">CLSID</span><span class="sxs-lookup"><span data-stu-id="3b8ef-159">CLSID</span></span><br/>                    | <span data-ttu-id="3b8ef-160">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="3b8ef-160">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="3b8ef-161">IID</span><span class="sxs-lookup"><span data-stu-id="3b8ef-161">IID</span></span><br/>                      | <span data-ttu-id="3b8ef-162">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="3b8ef-162">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="3b8ef-163">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b8ef-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b8ef-164">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="3b8ef-164">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="3b8ef-165">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="3b8ef-165">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="3b8ef-166">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="3b8ef-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




