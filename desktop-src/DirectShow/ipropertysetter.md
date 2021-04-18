---
description: 'L’interface IPropertySetter définit les propriétés d’un effet ou d’une transition dans les services de modification DirectShow (DES). Pour utiliser cette interface, créez une instance d’un objet d’accesseur Set de propriété (CLSID \_ PropertySetter) et associez-la à un effet ou une transition en appelant la méthode IAMTimelineObj :: SetPropertySetter. Pour plus d’informations, consultez Utilisation des effets et des transitions. en général, une application doit appeler uniquement la méthode IPropertySetter :: ClearProps pour effacer les propriétés existantes, et la méthode IPropertySetter :: AddProp pour ajouter de nouvelles propriétés. Les autres méthodes sur cette interface sont appelées par d’autres composants DES.'
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Interface IPropertySetter (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8f8aaadea2f0fb63287775294a7c61f01b3730df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540542"
---
# <a name="ipropertysetter-interface"></a><span data-ttu-id="e3c23-105">Interface IPropertySetter</span><span class="sxs-lookup"><span data-stu-id="e3c23-105">IPropertySetter interface</span></span>

> [!Note]  
> <span data-ttu-id="e3c23-106">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e3c23-106">\[Deprecated.</span></span> <span data-ttu-id="e3c23-107">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e3c23-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e3c23-108">L' `IPropertySetter` interface définit les propriétés d’un effet ou d’une transition dans les [services de modification DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="e3c23-108">The `IPropertySetter` interface sets properties on an effect or transition in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="e3c23-109">Pour utiliser cette interface, créez une instance d’un objet d’accesseur Set de propriété (CLSID \_ PropertySetter) et associez-la à un effet ou une transition en appelant la méthode [**IAMTimelineObj :: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) .</span><span class="sxs-lookup"><span data-stu-id="e3c23-109">To use this interface, create an instance of a property setter object (CLSID\_PropertySetter), and associate it with an effect or transition by calling the [**IAMTimelineObj::SetPropertySetter**](iamtimelineobj-setpropertysetter.md) method.</span></span> <span data-ttu-id="e3c23-110">Pour plus d’informations, consultez [utilisation des effets et des transitions](working-with-effects-and-transitions.md).</span><span class="sxs-lookup"><span data-stu-id="e3c23-110">For more information, see [Working with Effects and Transitions](working-with-effects-and-transitions.md).</span></span>

<span data-ttu-id="e3c23-111">En règle générale, une application doit appeler uniquement la méthode [**IPropertySetter :: ClearProps**](ipropertysetter-clearprops.md) pour effacer les propriétés existantes, et la méthode [**IPropertySetter :: AddProp**](ipropertysetter-addprop.md) pour ajouter de nouvelles propriétés.</span><span class="sxs-lookup"><span data-stu-id="e3c23-111">Usually an application needs to call only the [**IPropertySetter::ClearProps**](ipropertysetter-clearprops.md) method to clear existing properties, and the [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) method to add new properties.</span></span> <span data-ttu-id="e3c23-112">Les autres méthodes sur cette interface sont appelées par d’autres composants DES.</span><span class="sxs-lookup"><span data-stu-id="e3c23-112">The other methods on this interface are called by other DES components.</span></span>

## <a name="members"></a><span data-ttu-id="e3c23-113">Membres</span><span class="sxs-lookup"><span data-stu-id="e3c23-113">Members</span></span>

<span data-ttu-id="e3c23-114">L’interface **IPropertySetter** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e3c23-114">The **IPropertySetter** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e3c23-115">**IPropertySetter** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="e3c23-115">**IPropertySetter** also has these types of members:</span></span>

-   [<span data-ttu-id="e3c23-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e3c23-116">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e3c23-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="e3c23-117">Methods</span></span>

<span data-ttu-id="e3c23-118">L’interface **IPropertySetter** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="e3c23-118">The **IPropertySetter** interface has these methods.</span></span>



| <span data-ttu-id="e3c23-119">Méthode</span><span class="sxs-lookup"><span data-stu-id="e3c23-119">Method</span></span>                                               | <span data-ttu-id="e3c23-120">Description</span><span class="sxs-lookup"><span data-stu-id="e3c23-120">Description</span></span>                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3c23-121">**AddProp**</span><span class="sxs-lookup"><span data-stu-id="e3c23-121">**AddProp**</span></span>](ipropertysetter-addprop.md)           | <span data-ttu-id="e3c23-122">Ajoute une propriété à la méthode setter de propriété, avec un tableau de paires heure-valeur qui définissent la valeur de la propriété sur une plage de temps.</span><span class="sxs-lookup"><span data-stu-id="e3c23-122">Adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span><br/> |
| [<span data-ttu-id="e3c23-123">**ClearProps**</span><span class="sxs-lookup"><span data-stu-id="e3c23-123">**ClearProps**</span></span>](ipropertysetter-clearprops.md)     | <span data-ttu-id="e3c23-124">Efface toutes les données de propriété de l’accesseur Set de propriété.</span><span class="sxs-lookup"><span data-stu-id="e3c23-124">Clears all property data from the property setter.</span></span><br/>                                                                                 |
| [<span data-ttu-id="e3c23-125">**CloneProps**</span><span class="sxs-lookup"><span data-stu-id="e3c23-125">**CloneProps**</span></span>](ipropertysetter-cloneprops.md)     | <span data-ttu-id="e3c23-126">Clone un ensemble de propriétés à partir de cet accesseur Set de propriété et les ajoute à un nouvel accesseur Set de propriété.</span><span class="sxs-lookup"><span data-stu-id="e3c23-126">Clones a set of properties from this property setter and adds them to a new property setter.</span></span><br/>                                       |
| [<span data-ttu-id="e3c23-127">**FreeProps**</span><span class="sxs-lookup"><span data-stu-id="e3c23-127">**FreeProps**</span></span>](ipropertysetter-freeprops.md)       | <span data-ttu-id="e3c23-128">Libère les ressources allouées par la méthode [**IPropertySetter :: GetProps**](ipropertysetter-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="e3c23-128">Frees resources allocated by the [**IPropertySetter::GetProps**](ipropertysetter-getprops.md) method.</span></span><br/>                             |
| [<span data-ttu-id="e3c23-129">**GetProps**</span><span class="sxs-lookup"><span data-stu-id="e3c23-129">**GetProps**</span></span>](ipropertysetter-getprops.md)         | <span data-ttu-id="e3c23-130">Récupère les propriétés définies sur cet objet, avec leurs valeurs correspondantes.</span><span class="sxs-lookup"><span data-stu-id="e3c23-130">Retrieves the properties set on this object, with their corresponding values.</span></span><br/>                                                      |
| [<span data-ttu-id="e3c23-131">**LoadFromBlob**</span><span class="sxs-lookup"><span data-stu-id="e3c23-131">**LoadFromBlob**</span></span>](ipropertysetter-loadfromblob.md) | <span data-ttu-id="e3c23-132">Charge des données de propriété à partir d’un format de persistance.</span><span class="sxs-lookup"><span data-stu-id="e3c23-132">Loads property data from a persistence format.</span></span><br/>                                                                                     |
| [<span data-ttu-id="e3c23-133">**LoadXML**</span><span class="sxs-lookup"><span data-stu-id="e3c23-133">**LoadXML**</span></span>](ipropertysetter-loadxml.md)           | <span data-ttu-id="e3c23-134">Charge des données de propriété exprimées en Extensible Markup Language (XML).</span><span class="sxs-lookup"><span data-stu-id="e3c23-134">Loads property data expressed in Extensible Markup Language (XML).</span></span><br/>                                                                 |
| [<span data-ttu-id="e3c23-135">**PrintXML**</span><span class="sxs-lookup"><span data-stu-id="e3c23-135">**PrintXML**</span></span>](ipropertysetter-printxml.md)         | <span data-ttu-id="e3c23-136">Convertit des données de propriété en une chaîne XML.</span><span class="sxs-lookup"><span data-stu-id="e3c23-136">Converts property data into an XML string.</span></span><br/>                                                                                         |
| [<span data-ttu-id="e3c23-137">**SaveToBlob**</span><span class="sxs-lookup"><span data-stu-id="e3c23-137">**SaveToBlob**</span></span>](ipropertysetter-savetoblob.md)     | <span data-ttu-id="e3c23-138">Enregistre les données de propriété dans un format de persistance.</span><span class="sxs-lookup"><span data-stu-id="e3c23-138">Saves the property data to a persistence format.</span></span><br/>                                                                                   |
| [<span data-ttu-id="e3c23-139">**SetProps**</span><span class="sxs-lookup"><span data-stu-id="e3c23-139">**SetProps**</span></span>](ipropertysetter-setprops.md)         | <span data-ttu-id="e3c23-140">Définit les propriétés de l’objet cible à l’état approprié pour l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e3c23-140">Sets the properties of the target object to the appropriate state for the specified time.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="e3c23-141">Notes</span><span class="sxs-lookup"><span data-stu-id="e3c23-141">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e3c23-142">Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.</span><span class="sxs-lookup"><span data-stu-id="e3c23-142">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e3c23-143">Pour obtenir qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="e3c23-143">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e3c23-144">Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="e3c23-144">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e3c23-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3c23-145">Requirements</span></span>



| <span data-ttu-id="e3c23-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3c23-146">Requirement</span></span> | <span data-ttu-id="e3c23-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3c23-147">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3c23-148">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3c23-148">Header</span></span><br/>  | <dl> <span data-ttu-id="e3c23-149"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3c23-149"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e3c23-150">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e3c23-150">Library</span></span><br/> | <dl> <span data-ttu-id="e3c23-151"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3c23-151"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
