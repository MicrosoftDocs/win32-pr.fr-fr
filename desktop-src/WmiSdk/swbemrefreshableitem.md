---
description: Représente un élément unique dans un objet SWbemRefresher.
ms.assetid: 6a12c8eb-3ef9-4292-810c-6954294fc8c7
ms.tgt_platform: multiple
title: Objet SWbemRefreshableItem (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem
- ISWbemRefreshableItem
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bc4f85145926aba2bd050052c33eb5669dfee8a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761413"
---
# <a name="swbemrefreshableitem-object"></a><span data-ttu-id="5dc85-103">Objet SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="5dc85-103">SWbemRefreshableItem object</span></span>

<span data-ttu-id="5dc85-104">L’objet **SWbemRefreshableItem** représente un élément unique dans un objet [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="5dc85-104">The **SWbemRefreshableItem** object represents a single item in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="5dc85-105">Un objet **SWbemRefreshableItem** est obtenu par le biais des méthodes [**Add**](swbemrefresher-add.md) et [**AddEnum**](swbemrefresher-addenum.md) de [**SWbemRefresher**](swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="5dc85-105">An **SWbemRefreshableItem** object is obtained through the [**Add**](swbemrefresher-add.md) and [**AddEnum**](swbemrefresher-addenum.md) methods of [**SWbemRefresher**](swbemrefresher.md).</span></span> <span data-ttu-id="5dc85-106">Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](creating-an-object-using-vbscript.md) .</span><span class="sxs-lookup"><span data-stu-id="5dc85-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="5dc85-107">Membres</span><span class="sxs-lookup"><span data-stu-id="5dc85-107">Members</span></span>

<span data-ttu-id="5dc85-108">L’objet **SWbemRefreshableItem** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5dc85-108">The **SWbemRefreshableItem** object has these types of members:</span></span>

-   [<span data-ttu-id="5dc85-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5dc85-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5dc85-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5dc85-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5dc85-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5dc85-111">Methods</span></span>

<span data-ttu-id="5dc85-112">L’objet **SWbemRefreshableItem** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5dc85-112">The **SWbemRefreshableItem** object has these methods.</span></span>



| <span data-ttu-id="5dc85-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="5dc85-113">Method</span></span>                                        | <span data-ttu-id="5dc85-114">Description</span><span class="sxs-lookup"><span data-stu-id="5dc85-114">Description</span></span>                                                                                                             |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dc85-115">**Installez**</span><span class="sxs-lookup"><span data-stu-id="5dc85-115">**Remove**</span></span>](swbemrefreshableitem-remove.md) | <span data-ttu-id="5dc85-116">Supprime l’objet **SWbemRefreshableItem** de l’objet [**SWbemRefresher**](swbemrefresher.md) parent.</span><span class="sxs-lookup"><span data-stu-id="5dc85-116">Removes the **SWbemRefreshableItem** object from the parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="5dc85-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5dc85-117">Properties</span></span>

<span data-ttu-id="5dc85-118">L’objet **SWbemRefreshableItem** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5dc85-118">The **SWbemRefreshableItem** object has these properties.</span></span>



| <span data-ttu-id="5dc85-119">Propriété</span><span class="sxs-lookup"><span data-stu-id="5dc85-119">Property</span></span>                                                       | <span data-ttu-id="5dc85-120">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="5dc85-120">Access type</span></span>           | <span data-ttu-id="5dc85-121">Description</span><span class="sxs-lookup"><span data-stu-id="5dc85-121">Description</span></span>                                                                                                                          |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5dc85-122">**Évaluer**</span><span class="sxs-lookup"><span data-stu-id="5dc85-122">**Index**</span></span>](swbemrefreshableitem-index.md)<br/>         | <span data-ttu-id="5dc85-123">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5dc85-123">Read/write</span></span><br/> | <span data-ttu-id="5dc85-124">Index de l’élément dans son objet [**SWbemRefresher**](swbemrefresher.md) parent.</span><span class="sxs-lookup"><span data-stu-id="5dc85-124">Index of the item in its parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span><br/>                                          |
| [<span data-ttu-id="5dc85-125">**IsSet**</span><span class="sxs-lookup"><span data-stu-id="5dc85-125">**IsSet**</span></span>](swbemrefreshableitem-isset.md)<br/>         | <span data-ttu-id="5dc85-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5dc85-126">Read/write</span></span><br/> | <span data-ttu-id="5dc85-127">Indique si l’objet **SWbemRefreshableItem** représente un objet unique ou un jeu d’objets.</span><span class="sxs-lookup"><span data-stu-id="5dc85-127">Indicates whether the **SWbemRefreshableItem** object represents a single object or an object set.</span></span><br/>                        |
| [<span data-ttu-id="5dc85-128">**Dessin**</span><span class="sxs-lookup"><span data-stu-id="5dc85-128">**Object**</span></span>](swbemrefreshableitem-object.md)<br/>       | <span data-ttu-id="5dc85-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5dc85-129">Read/write</span></span><br/> | <span data-ttu-id="5dc85-130">Représente un objet [**SWbemObject**](swbemobject.md) unique qui est actualisé.</span><span class="sxs-lookup"><span data-stu-id="5dc85-130">Represents a single [**SWbemObject**](swbemobject.md) object that is refreshed.</span></span><br/>                                          |
| [<span data-ttu-id="5dc85-131">**ObjectSet**</span><span class="sxs-lookup"><span data-stu-id="5dc85-131">**ObjectSet**</span></span>](swbemrefreshableitem-objectset.md)<br/> | <span data-ttu-id="5dc85-132">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5dc85-132">Read/write</span></span><br/> | <span data-ttu-id="5dc85-133">Représente le jeu d’objets à actualiser.</span><span class="sxs-lookup"><span data-stu-id="5dc85-133">Represents the object set to be refreshed.</span></span><br/>                                                                                |
| [<span data-ttu-id="5dc85-134">**Actualisateur**</span><span class="sxs-lookup"><span data-stu-id="5dc85-134">**Refresher**</span></span>](swbemrefreshableitem-refresher.md)<br/> | <span data-ttu-id="5dc85-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5dc85-135">Read-only</span></span><br/>  | <span data-ttu-id="5dc85-136">Représente l’objet [**SWbemRefresher**](swbemrefresher.md) parent qui contient l’objet **SWbemRefreshableItem** .</span><span class="sxs-lookup"><span data-stu-id="5dc85-136">Represents the parent [**SWbemRefresher**](swbemrefresher.md) object which contains the **SWbemRefreshableItem** object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5dc85-137">Notes</span><span class="sxs-lookup"><span data-stu-id="5dc85-137">Remarks</span></span>

<span data-ttu-id="5dc85-138">La méthode VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) ne peut pas être utilisée pour créer des objets **SWbemRefreshableItem** directement.</span><span class="sxs-lookup"><span data-stu-id="5dc85-138">The VBScript method [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) cannot be used to create **SWbemRefreshableItem** objects directly.</span></span>

## <a name="examples"></a><span data-ttu-id="5dc85-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="5dc85-139">Examples</span></span>

<span data-ttu-id="5dc85-140">Le script suivant illustre la création d’un objet [**SWbemRefresher**](swbemrefresher.md) et l’ajout d’un objet unique et d’un énumérateur **SWbemRefreshableItem** .</span><span class="sxs-lookup"><span data-stu-id="5dc85-140">The following script illustrates the creation of an [**SWbemRefresher**](swbemrefresher.md) object and the addition of single object and enumerator **SWbemRefreshableItem** to it.</span></span>


```VB
' Get some namespace connections
set cimv2 = GetObject("winmgmts:root\cimv2")
set default = GetObject("winmgmts:root\default")    

' Create a refresher
set refresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object to the refresher.
' The @ is used because this is a singleton 
' system class so only one instance exists.
set item1 = refresher.Add (default, "__CIMOMIdentification=@").Object
MsgBox "WMI Version " item1
' Add an enumerator to the refresher.
' Note that the SWbemRefreshableItem.ObjectSet 
' property must be used to designate
' this as an object set rather than a single object.
set item2 = refresher.AddEnum (cimv2, "Win32_Process").ObjectSet

' Loop three times, refreshing the items

For I= 1 To 3
MsgBox "Refresh number " & I
refresher.Refresh

' Iterate through the collection of
' processes in item2 with name of wscript
    For each process in item2
        If process.name = "wscript.exe" then
        MsgBox "Process " & process.Name & _
           " Page Faults " & process.PageFaults
        End If
    Next 
Next

' Clear out the refresher
refresher.DeleteAll 

' The following should return 0
MsgBox "Number of items in Refresher after DeleteAll " _
    & refresher.Count
```



## <a name="requirements"></a><span data-ttu-id="5dc85-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5dc85-141">Requirements</span></span>



| <span data-ttu-id="5dc85-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5dc85-142">Requirement</span></span> | <span data-ttu-id="5dc85-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="5dc85-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5dc85-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dc85-144">Minimum supported client</span></span><br/> | <span data-ttu-id="5dc85-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5dc85-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5dc85-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5dc85-146">Minimum supported server</span></span><br/> | <span data-ttu-id="5dc85-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5dc85-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5dc85-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="5dc85-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dc85-149"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dc85-149"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5dc85-150">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5dc85-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="5dc85-151"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5dc85-151"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5dc85-152">DLL</span><span class="sxs-lookup"><span data-stu-id="5dc85-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5dc85-153"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5dc85-153"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5dc85-154">CLSID</span><span class="sxs-lookup"><span data-stu-id="5dc85-154">CLSID</span></span><br/>                    | <span data-ttu-id="5dc85-155">CLSID \_ SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="5dc85-155">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="5dc85-156">IID</span><span class="sxs-lookup"><span data-stu-id="5dc85-156">IID</span></span><br/>                      | <span data-ttu-id="5dc85-157">IID \_ ISWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="5dc85-157">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="5dc85-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5dc85-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dc85-159">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="5dc85-159">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




