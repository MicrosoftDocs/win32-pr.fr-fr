---
description: Contient une liste des protocoles à utiliser par DCOM. Elle contient un objet pour chaque protocole.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: Collection DCOMProtocols
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: 705940dae0f7ebe885db4c295714df538c56c705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483216"
---
# <a name="dcomprotocols-collection"></a><span data-ttu-id="5b400-104">Collection DCOMProtocols</span><span class="sxs-lookup"><span data-stu-id="5b400-104">DCOMProtocols collection</span></span>

<span data-ttu-id="5b400-105">Contient une liste des protocoles à utiliser par DCOM.</span><span class="sxs-lookup"><span data-stu-id="5b400-105">Contains a list of the protocols to be used by DCOM.</span></span> <span data-ttu-id="5b400-106">Elle contient un objet pour chaque protocole.</span><span class="sxs-lookup"><span data-stu-id="5b400-106">It contains an object for each protocol.</span></span>

<span data-ttu-id="5b400-107">Cette collection prend en charge les méthodes [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) et [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) de l’objet [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="5b400-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="5b400-108">Membres</span><span class="sxs-lookup"><span data-stu-id="5b400-108">Members</span></span>

<span data-ttu-id="5b400-109">La collection **DCOMProtocols** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mais n’a pas de membres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="5b400-109">The **DCOMProtocols** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="5b400-110">Regroupements connexes</span><span class="sxs-lookup"><span data-stu-id="5b400-110">Related Collections</span></span>

<span data-ttu-id="5b400-111">Vous pouvez naviguer à partir de cette collection vers l’un des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="5b400-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="5b400-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5b400-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="5b400-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="5b400-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="5b400-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="5b400-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="5b400-115">Vous pouvez accéder à cette collection à partir des regroupements suivants :</span><span class="sxs-lookup"><span data-stu-id="5b400-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="5b400-116">**Causes**</span><span class="sxs-lookup"><span data-stu-id="5b400-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="5b400-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5b400-117">Properties</span></span>

<span data-ttu-id="5b400-118">Les propriétés suivantes sont prises en charge par l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection :</span><span class="sxs-lookup"><span data-stu-id="5b400-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="5b400-119">Nom</span><span class="sxs-lookup"><span data-stu-id="5b400-119">Name</span></span>](#name)
-   [<span data-ttu-id="5b400-120">Commande</span><span class="sxs-lookup"><span data-stu-id="5b400-120">Order</span></span>](#order)
-   [<span data-ttu-id="5b400-121">ProtocolCode</span><span class="sxs-lookup"><span data-stu-id="5b400-121">ProtocolCode</span></span>](#protocolcode)

### <a name="name"></a><span data-ttu-id="5b400-122">Nom</span><span class="sxs-lookup"><span data-stu-id="5b400-122">Name</span></span>



| <span data-ttu-id="5b400-123">Entrée</span><span class="sxs-lookup"><span data-stu-id="5b400-123">Entry</span></span> | <span data-ttu-id="5b400-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b400-124">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b400-125">Description</span><span class="sxs-lookup"><span data-stu-id="5b400-125">Description</span></span>    | <span data-ttu-id="5b400-126">Nom du protocole.</span><span class="sxs-lookup"><span data-stu-id="5b400-126">The name of the protocol.</span></span> <span data-ttu-id="5b400-127">Cette propriété est retournée lorsque la méthode de propriété [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="5b400-127">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="5b400-128">Accès</span><span class="sxs-lookup"><span data-stu-id="5b400-128">Access</span></span>         | <span data-ttu-id="5b400-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b400-129">ReadWrite</span></span>                                                                                                                                                   |
| <span data-ttu-id="5b400-130">Type</span><span class="sxs-lookup"><span data-stu-id="5b400-130">Type</span></span>           | <span data-ttu-id="5b400-131">String</span><span class="sxs-lookup"><span data-stu-id="5b400-131">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="5b400-132">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="5b400-132">Default</span></span>        | <span data-ttu-id="5b400-133">« Nouveau protocole »</span><span class="sxs-lookup"><span data-stu-id="5b400-133">"New Protocol"</span></span>                                                                                                                                              |
| <span data-ttu-id="5b400-134">Système minimal</span><span class="sxs-lookup"><span data-stu-id="5b400-134">Minimum system</span></span> | <span data-ttu-id="5b400-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5b400-135">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="order"></a><span data-ttu-id="5b400-136">Commande</span><span class="sxs-lookup"><span data-stu-id="5b400-136">Order</span></span>



| <span data-ttu-id="5b400-137">Entrée</span><span class="sxs-lookup"><span data-stu-id="5b400-137">Entry</span></span> | <span data-ttu-id="5b400-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b400-138">Value</span></span> |
|----------------|-----------------------------------------|
| <span data-ttu-id="5b400-139">Description</span><span class="sxs-lookup"><span data-stu-id="5b400-139">Description</span></span>    | <span data-ttu-id="5b400-140">Ordre dans lequel le protocole doit être essayé.</span><span class="sxs-lookup"><span data-stu-id="5b400-140">The order in which to try the protocol.</span></span> |
| <span data-ttu-id="5b400-141">Accès</span><span class="sxs-lookup"><span data-stu-id="5b400-141">Access</span></span>         | <span data-ttu-id="5b400-142">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5b400-142">ReadWrite</span></span>                               |
| <span data-ttu-id="5b400-143">Type</span><span class="sxs-lookup"><span data-stu-id="5b400-143">Type</span></span>           | <span data-ttu-id="5b400-144">Long (0-65000)</span><span class="sxs-lookup"><span data-stu-id="5b400-144">Long (0-65000)</span></span>                          |
| <span data-ttu-id="5b400-145">Default</span><span class="sxs-lookup"><span data-stu-id="5b400-145">Default</span></span>        | <span data-ttu-id="5b400-146">0</span><span class="sxs-lookup"><span data-stu-id="5b400-146">0</span></span>                                       |
| <span data-ttu-id="5b400-147">Système minimal</span><span class="sxs-lookup"><span data-stu-id="5b400-147">Minimum system</span></span> | <span data-ttu-id="5b400-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5b400-148">Windows 2000</span></span>                            |



 

### <a name="protocolcode"></a><span data-ttu-id="5b400-149">ProtocolCode</span><span class="sxs-lookup"><span data-stu-id="5b400-149">ProtocolCode</span></span>



| <span data-ttu-id="5b400-150">Entrée</span><span class="sxs-lookup"><span data-stu-id="5b400-150">Entry</span></span> | <span data-ttu-id="5b400-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b400-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b400-152">Description</span><span class="sxs-lookup"><span data-stu-id="5b400-152">Description</span></span>    | <span data-ttu-id="5b400-153">Code qui spécifie la séquence de protocole RPC.</span><span class="sxs-lookup"><span data-stu-id="5b400-153">The code specifying the RPC protocol sequence.</span></span> <span data-ttu-id="5b400-154">Les codes de protocole pris en charge sont les suivants : ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ SPX.</span><span class="sxs-lookup"><span data-stu-id="5b400-154">The supported protocol codes include the following: ncacn\_ip\_tcp, ncacn\_http, ncacn\_spx.</span></span> <span data-ttu-id="5b400-155">Cette propriété est retournée lorsque la méthode de propriété de [**clé**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) est appelée sur un objet de cette collection.</span><span class="sxs-lookup"><span data-stu-id="5b400-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="5b400-156">Accès</span><span class="sxs-lookup"><span data-stu-id="5b400-156">Access</span></span>         | <span data-ttu-id="5b400-157">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="5b400-157">WriteOnce</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="5b400-158">Type</span><span class="sxs-lookup"><span data-stu-id="5b400-158">Type</span></span>           | <span data-ttu-id="5b400-159">String</span><span class="sxs-lookup"><span data-stu-id="5b400-159">String</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="5b400-160">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="5b400-160">Default</span></span>        | <span data-ttu-id="5b400-161">""</span><span class="sxs-lookup"><span data-stu-id="5b400-161">""</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5b400-162">Système minimal</span><span class="sxs-lookup"><span data-stu-id="5b400-162">Minimum system</span></span> | <span data-ttu-id="5b400-163">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5b400-163">Windows 2000</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="5b400-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b400-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b400-165">Regroupements d’administration COM+</span><span class="sxs-lookup"><span data-stu-id="5b400-165">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
