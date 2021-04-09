---
description: Récupère des informations sur les classes d’événements.
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: Collection EventClassesForIID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110559"
---
# <a name="eventclassesforiid-collection"></a><span data-ttu-id="f4f90-103">Collection EventClassesForIID</span><span class="sxs-lookup"><span data-stu-id="f4f90-103">EventClassesForIID collection</span></span>

<span data-ttu-id="f4f90-104">Récupère des informations sur les classes d’événements.</span><span class="sxs-lookup"><span data-stu-id="f4f90-104">Retrieves information regarding event classes.</span></span>

<span data-ttu-id="f4f90-105">La connexion entre le serveur de publication et le ou les abonnés est gérée par un objet [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) , qui est un composant com+ contenant les interfaces et les méthodes utilisées par un serveur de publication pour déclencher des événements.</span><span class="sxs-lookup"><span data-stu-id="f4f90-105">The connection between publisher and subscriber(s) is managed by an [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) object, which is a COM+ component that contains the interfaces and methods used by a publisher to fire events.</span></span>

<span data-ttu-id="f4f90-106">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="f4f90-106">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="f4f90-107">Membres</span><span class="sxs-lookup"><span data-stu-id="f4f90-107">Members</span></span>

<span data-ttu-id="f4f90-108">La collection **EventClassesForIID** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f4f90-108">The **EventClassesForIID** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="f4f90-109">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="f4f90-109">Related Collections</span></span>

<span data-ttu-id="f4f90-110">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="f4f90-110">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="f4f90-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="f4f90-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="f4f90-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="f4f90-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="f4f90-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="f4f90-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="f4f90-114">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="f4f90-114">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="f4f90-115">**Causes**</span><span class="sxs-lookup"><span data-stu-id="f4f90-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="f4f90-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f4f90-116">Properties</span></span>

<span data-ttu-id="f4f90-117">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="f4f90-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="f4f90-118">Application</span><span class="sxs-lookup"><span data-stu-id="f4f90-118">Application</span></span>](#application)
-   [<span data-ttu-id="f4f90-119">Nombre de bits</span><span class="sxs-lookup"><span data-stu-id="f4f90-119">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="f4f90-120">IDENTIFICATEUR</span><span class="sxs-lookup"><span data-stu-id="f4f90-120">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="f4f90-121">Description</span><span class="sxs-lookup"><span data-stu-id="f4f90-121">Description</span></span>](#description)
-   [<span data-ttu-id="f4f90-122">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="f4f90-122">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="f4f90-123">ProgID</span><span class="sxs-lookup"><span data-stu-id="f4f90-123">ProgID</span></span>](#progid)

### <a name="application"></a><span data-ttu-id="f4f90-124">Application</span><span class="sxs-lookup"><span data-stu-id="f4f90-124">Application</span></span>



| <span data-ttu-id="f4f90-125">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4f90-125">Entry</span></span> | <span data-ttu-id="f4f90-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4f90-126">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="f4f90-127">Description</span><span class="sxs-lookup"><span data-stu-id="f4f90-127">Description</span></span>    | <span data-ttu-id="f4f90-128">GUID de l’application contenant la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="f4f90-128">The GUID for the application containing the event class.</span></span> |
| <span data-ttu-id="f4f90-129">Accès</span><span class="sxs-lookup"><span data-stu-id="f4f90-129">Access</span></span>         | <span data-ttu-id="f4f90-130">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4f90-130">ReadOnly</span></span>                                                 |
| <span data-ttu-id="f4f90-131">Type</span><span class="sxs-lookup"><span data-stu-id="f4f90-131">Type</span></span>           | <span data-ttu-id="f4f90-132">String</span><span class="sxs-lookup"><span data-stu-id="f4f90-132">String</span></span>                                                   |
| <span data-ttu-id="f4f90-133">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f4f90-133">Default</span></span>        | <span data-ttu-id="f4f90-134">N/A</span><span class="sxs-lookup"><span data-stu-id="f4f90-134">N/A</span></span>                                                      |
| <span data-ttu-id="f4f90-135">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f4f90-135">Minimum system</span></span> | <span data-ttu-id="f4f90-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4f90-136">Windows XP</span></span>                                               |



 

### <a name="bitness"></a><span data-ttu-id="f4f90-137">Nombre de bits</span><span class="sxs-lookup"><span data-stu-id="f4f90-137">Bitness</span></span>



| <span data-ttu-id="f4f90-138">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4f90-138">Entry</span></span> | <span data-ttu-id="f4f90-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4f90-139">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f90-140">Description</span><span class="sxs-lookup"><span data-stu-id="f4f90-140">Description</span></span>    | <span data-ttu-id="f4f90-141">Représente le type de bits binaire de la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="f4f90-141">Represents the binary bitness type of the event class.</span></span> <span data-ttu-id="f4f90-142">Sur les systèmes qui utilisent Windows 64 bits, cette propriété permet de faire la distinction entre les composants 64 bits et les composants 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f4f90-142">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="f4f90-143">Accès</span><span class="sxs-lookup"><span data-stu-id="f4f90-143">Access</span></span>         | <span data-ttu-id="f4f90-144">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4f90-144">ReadOnly</span></span>                                                                                                                                                                |
| <span data-ttu-id="f4f90-145">Type</span><span class="sxs-lookup"><span data-stu-id="f4f90-145">Type</span></span>           | <span data-ttu-id="f4f90-146">Valeurs possibles longues : COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0X2)</span><span class="sxs-lookup"><span data-stu-id="f4f90-146">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                           |
| <span data-ttu-id="f4f90-147">Default</span><span class="sxs-lookup"><span data-stu-id="f4f90-147">Default</span></span>        | <span data-ttu-id="f4f90-148">N/A</span><span class="sxs-lookup"><span data-stu-id="f4f90-148">N/A</span></span>                                                                                                                                                                     |
| <span data-ttu-id="f4f90-149">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f4f90-149">Minimum system</span></span> | <span data-ttu-id="f4f90-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4f90-150">Windows XP</span></span>                                                                                                                                                              |



 

### <a name="clsid"></a><span data-ttu-id="f4f90-151">CLSID</span><span class="sxs-lookup"><span data-stu-id="f4f90-151">CLSID</span></span>



| <span data-ttu-id="f4f90-152">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4f90-152">Entry</span></span> | <span data-ttu-id="f4f90-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4f90-153">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f90-154">Description</span><span class="sxs-lookup"><span data-stu-id="f4f90-154">Description</span></span>    | <span data-ttu-id="f4f90-155">GUID de la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="f4f90-155">The GUID for the event class.</span></span> <span data-ttu-id="f4f90-156">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="f4f90-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f4f90-157">Accès</span><span class="sxs-lookup"><span data-stu-id="f4f90-157">Access</span></span>         | <span data-ttu-id="f4f90-158">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4f90-158">ReadOnly</span></span>                                                                                                                                                      |
| <span data-ttu-id="f4f90-159">Type</span><span class="sxs-lookup"><span data-stu-id="f4f90-159">Type</span></span>           | <span data-ttu-id="f4f90-160">String</span><span class="sxs-lookup"><span data-stu-id="f4f90-160">String</span></span>                                                                                                                                                        |
| <span data-ttu-id="f4f90-161">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f4f90-161">Default</span></span>        | <span data-ttu-id="f4f90-162">N/A</span><span class="sxs-lookup"><span data-stu-id="f4f90-162">N/A</span></span>                                                                                                                                                           |
| <span data-ttu-id="f4f90-163">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f4f90-163">Minimum system</span></span> | <span data-ttu-id="f4f90-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4f90-164">Windows XP</span></span>                                                                                                                                                    |



 

### <a name="description"></a><span data-ttu-id="f4f90-165">Description</span><span class="sxs-lookup"><span data-stu-id="f4f90-165">Description</span></span>



| <span data-ttu-id="f4f90-166">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4f90-166">Entry</span></span> | <span data-ttu-id="f4f90-167">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4f90-167">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="f4f90-168">Description</span><span class="sxs-lookup"><span data-stu-id="f4f90-168">Description</span></span>    | <span data-ttu-id="f4f90-169">Décrit la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="f4f90-169">Describes the event class.</span></span> |
| <span data-ttu-id="f4f90-170">Accès</span><span class="sxs-lookup"><span data-stu-id="f4f90-170">Access</span></span>         | <span data-ttu-id="f4f90-171">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4f90-171">ReadOnly</span></span>                   |
| <span data-ttu-id="f4f90-172">Type</span><span class="sxs-lookup"><span data-stu-id="f4f90-172">Type</span></span>           | <span data-ttu-id="f4f90-173">String</span><span class="sxs-lookup"><span data-stu-id="f4f90-173">String</span></span>                     |
| <span data-ttu-id="f4f90-174">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f4f90-174">Default</span></span>        | <span data-ttu-id="f4f90-175">""</span><span class="sxs-lookup"><span data-stu-id="f4f90-175">""</span></span>                         |
| <span data-ttu-id="f4f90-176">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f4f90-176">Minimum system</span></span> | <span data-ttu-id="f4f90-177">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4f90-177">Windows XP</span></span>                 |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="f4f90-178">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="f4f90-178">IsPrivateComponent</span></span>



| <span data-ttu-id="f4f90-179">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4f90-179">Entry</span></span> | <span data-ttu-id="f4f90-180">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4f90-180">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="f4f90-181">Description</span><span class="sxs-lookup"><span data-stu-id="f4f90-181">Description</span></span>    | <span data-ttu-id="f4f90-182">Indique si le composant de la classe d’événements est privé.</span><span class="sxs-lookup"><span data-stu-id="f4f90-182">Indicates whether the event class component is private.</span></span> |
| <span data-ttu-id="f4f90-183">Accès</span><span class="sxs-lookup"><span data-stu-id="f4f90-183">Access</span></span>         | <span data-ttu-id="f4f90-184">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4f90-184">ReadOnly</span></span>                                                |
| <span data-ttu-id="f4f90-185">Type</span><span class="sxs-lookup"><span data-stu-id="f4f90-185">Type</span></span>           | <span data-ttu-id="f4f90-186">Bool</span><span class="sxs-lookup"><span data-stu-id="f4f90-186">Bool</span></span>                                                    |
| <span data-ttu-id="f4f90-187">Default</span><span class="sxs-lookup"><span data-stu-id="f4f90-187">Default</span></span>        | <span data-ttu-id="f4f90-188">False</span><span class="sxs-lookup"><span data-stu-id="f4f90-188">False</span></span>                                                   |
| <span data-ttu-id="f4f90-189">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f4f90-189">Minimum system</span></span> | <span data-ttu-id="f4f90-190">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4f90-190">Windows XP</span></span>                                              |



 

### <a name="progid"></a><span data-ttu-id="f4f90-191">ProgID</span><span class="sxs-lookup"><span data-stu-id="f4f90-191">ProgID</span></span>



| <span data-ttu-id="f4f90-192">Entrée</span><span class="sxs-lookup"><span data-stu-id="f4f90-192">Entry</span></span> | <span data-ttu-id="f4f90-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4f90-193">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4f90-194">Description</span><span class="sxs-lookup"><span data-stu-id="f4f90-194">Description</span></span>    | <span data-ttu-id="f4f90-195">Nom convivial utilisé pour identifier la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="f4f90-195">A friendly name used to identify the event class.</span></span> <span data-ttu-id="f4f90-196">Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="f4f90-196">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f4f90-197">Accès</span><span class="sxs-lookup"><span data-stu-id="f4f90-197">Access</span></span>         | <span data-ttu-id="f4f90-198">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4f90-198">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="f4f90-199">Type</span><span class="sxs-lookup"><span data-stu-id="f4f90-199">Type</span></span>           | <span data-ttu-id="f4f90-200">String</span><span class="sxs-lookup"><span data-stu-id="f4f90-200">String</span></span>                                                                                                                                                                              |
| <span data-ttu-id="f4f90-201">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="f4f90-201">Default</span></span>        | <span data-ttu-id="f4f90-202">""</span><span class="sxs-lookup"><span data-stu-id="f4f90-202">""</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="f4f90-203">Système minimal</span><span class="sxs-lookup"><span data-stu-id="f4f90-203">Minimum system</span></span> | <span data-ttu-id="f4f90-204">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f4f90-204">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="f4f90-205">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4f90-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f90-206">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="f4f90-206">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
