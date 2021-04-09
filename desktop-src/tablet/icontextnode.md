---
description: Représente un nœud dans une arborescence d’objets qui sont créés dans le cadre de l’analyse de l’encre.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: Interface IContextNode (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dbc9d7a0c1cc6ededf5d59585c806b54d6cfa32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034015"
---
# <a name="icontextnode-interface"></a><span data-ttu-id="0a6e4-103">Interface IContextNode</span><span class="sxs-lookup"><span data-stu-id="0a6e4-103">IContextNode interface</span></span>

<span data-ttu-id="0a6e4-104">Représente un nœud dans une arborescence d’objets qui sont créés dans le cadre de l’analyse de l’encre.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-104">Represents a node in a tree of objects that are created as part of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="0a6e4-105">Membres</span><span class="sxs-lookup"><span data-stu-id="0a6e4-105">Members</span></span>

<span data-ttu-id="0a6e4-106">L’interface **IContextNode** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0a6e4-106">The **IContextNode** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0a6e4-107">**IContextNode** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="0a6e4-107">**IContextNode** also has these types of members:</span></span>

-   [<span data-ttu-id="0a6e4-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0a6e4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0a6e4-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="0a6e4-109">Methods</span></span>

<span data-ttu-id="0a6e4-110">L’interface **IContextNode** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-110">The **IContextNode** interface has these methods.</span></span>



| <span data-ttu-id="0a6e4-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="0a6e4-111">Method</span></span>                                                                                  | <span data-ttu-id="0a6e4-112">Description</span><span class="sxs-lookup"><span data-stu-id="0a6e4-112">Description</span></span>                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a6e4-113">**AddContextLink**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-113">**AddContextLink**</span></span>](icontextnode-addcontextlink.md)                                   | <span data-ttu-id="0a6e4-114">Ajoute un nouveau [**IContextLink**](icontextlink.md) à la collection de liens de contexte de l’objet **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="0a6e4-114">Adds a new [**IContextLink**](icontextlink.md) to the **IContextNode** object's context link collection.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="0a6e4-115">**AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-115">**AddPropertyData**</span></span>](icontextnode-addpropertydata.md)                                 | <span data-ttu-id="0a6e4-116">Ajoute un élément de données spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-116">Adds a piece of application-specific data.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="0a6e4-117">**Confirmer**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-117">**Confirm**</span></span>](icontextnode-confirm.md)                                                 | <span data-ttu-id="0a6e4-118">Modifie le type de confirmation, qui contrôle ce que l’objet [**IInkAnalyzer**](iinkanalyzer.md) peut modifier à propos du **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-118">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the **IContextNode**.</span></span><br/>                                                                         |
| [<span data-ttu-id="0a6e4-119">**ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-119">**ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)                       | <span data-ttu-id="0a6e4-120">Détermine si l’objet **IContextNode** contient des données stockées sous l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-120">Determines whether the **IContextNode** object contains data stored under the specified identifier.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="0a6e4-121">**CreatePartiallyPopulatedSubNode**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-121">**CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md) | <span data-ttu-id="0a6e4-122">Crée un objet **IContextNode** enfant qui contient uniquement des informations sur le type, l’identificateur et l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-122">Creates a child **IContextNode** object that contains only information on type, identifier, and location.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="0a6e4-123">**CreateSubNode**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-123">**CreateSubNode**</span></span>](icontextnode-createsubnode.md)                                     | <span data-ttu-id="0a6e4-124">Crée un nouvel objet **IContextNode** enfant.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-124">Creates a new child **IContextNode** object.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="0a6e4-125">**DeleteContextLink**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-125">**DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)                             | <span data-ttu-id="0a6e4-126">Supprime un objet [**IContextLink**](icontextlink.md) de la collection de liens de l’objet **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="0a6e4-126">Deletes an [**IContextLink**](icontextlink.md) object from the **IContextNode** object's link collection.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="0a6e4-127">**DeleteSubNode**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-127">**DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)                                     | <span data-ttu-id="0a6e4-128">Supprime un **IContextNode** enfant.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-128">Removes a child **IContextNode**.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="0a6e4-129">**GetContextLinks**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-129">**GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)                                 | <span data-ttu-id="0a6e4-130">Récupère une collection d’objets [**IContextLink**](icontextlink.md) qui représentent des relations avec d’autres objets **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="0a6e4-130">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other **IContextNode** objects.</span></span><br/>                                                                          |
| [<span data-ttu-id="0a6e4-131">**GetId**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-131">**GetId**</span></span>](icontextnode-getid.md)                                                     | <span data-ttu-id="0a6e4-132">Récupère l’identificateur pour l’objet **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="0a6e4-132">Retrieves the identifier for the **IContextNode** object.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="0a6e4-133">**GetLocation**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-133">**GetLocation**</span></span>](icontextnode-getlocation.md)                                         | <span data-ttu-id="0a6e4-134">Récupère la position et la taille de l’objet **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="0a6e4-134">Retrieves the position and size of the **IContextNode** object.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="0a6e4-135">**GetParentNode**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-135">**GetParentNode**</span></span>](icontextnode-getparentnode.md)                                     | <span data-ttu-id="0a6e4-136">Récupère le nœud parent de ce **IContextNode** dans l’arborescence du nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-136">Retrieves the parent node of this **IContextNode** in the context node tree.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="0a6e4-137">**GetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-137">**GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)                     | <span data-ttu-id="0a6e4-138">Récupère la valeur qui indique si un objet **IContextNode** est partiellement rempli ou entièrement rempli.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-138">Retrieves the value that indicates whether an **IContextNode** object is partially populated or fully populated.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="0a6e4-139">**GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-139">**GetPropertyData**</span></span>](icontextnode-getpropertydata.md)                                 | <span data-ttu-id="0a6e4-140">Récupère des données spécifiques à l’application ou d’autres données de propriété en fonction de l’identificateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-140">Retrieves application-specific data or other property data given the specified identifier.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="0a6e4-141">**GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-141">**GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)                           | <span data-ttu-id="0a6e4-142">Récupère les identificateurs pour lesquels il existe des données de propriété.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-142">Retrieves the identifiers for which there is property data.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="0a6e4-143">**GetStrokeCount**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-143">**GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)                                   | <span data-ttu-id="0a6e4-144">Récupère le nombre de traits associés à l’objet **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="0a6e4-144">Retrieves the number of strokes associated with the **IContextNode** object.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="0a6e4-145">**GetStrokeId**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-145">**GetStrokeId**</span></span>](icontextnode-getstrokeid.md)                                         | <span data-ttu-id="0a6e4-146">Récupère l’identificateur de trait pour le trait référencé par une valeur d’index dans l’objet **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="0a6e4-146">Retrieves the stroke identifier for the stroke referenced by an index value within the **IContextNode** object.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="0a6e4-147">**GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-147">**GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)                                       | <span data-ttu-id="0a6e4-148">Récupère un tableau d’identificateurs pour les traits dans l’objet **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="0a6e4-148">Retrieves an array of identifiers for the strokes within the **IContextNode** object.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="0a6e4-149">**GetStrokePacketDataById**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-149">**GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)                 | <span data-ttu-id="0a6e4-150">Récupère un tableau qui contient les données de propriété de paquet pour le trait spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-150">Retrieves an array containing the packet property data for the specified stroke.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="0a6e4-151">**GetStrokePacketDescriptionById**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-151">**GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)   | <span data-ttu-id="0a6e4-152">Récupère un tableau contenant les identificateurs de propriété de paquet pour le trait spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-152">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="0a6e4-153">**GetSubNodes**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-153">**GetSubNodes**</span></span>](icontextnode-getsubnodes.md)                                         | <span data-ttu-id="0a6e4-154">Récupère les nœuds enfants directs de l’objet **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="0a6e4-154">Retrieves the direct child nodes of the **IContextNode** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="0a6e4-155">**GetType**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-155">**GetType**</span></span>](icontextnode-gettype.md)                                                 | <span data-ttu-id="0a6e4-156">Récupère le type de l’objet **IContextNode** .</span><span class="sxs-lookup"><span data-stu-id="0a6e4-156">Retrieves the type of the **IContextNode** object.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="0a6e4-157">**GetTypeName**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-157">**GetTypeName**</span></span>](icontextnode-gettypename.md)                                         | <span data-ttu-id="0a6e4-158">Récupère un nom de type explicite de ce **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-158">Retrieves a human-readable type name of this **IContextNode**.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="0a6e4-159">**IsConfirmed**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-159">**IsConfirmed**</span></span>](icontextnode-isconfirmed.md)                                         | <span data-ttu-id="0a6e4-160">Récupère une valeur qui indique si l’objet **IContextNode** est confirmé.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-160">Retrieves a value that indicates whether the **IContextNode** object is confirmed.</span></span> <span data-ttu-id="0a6e4-161">[**IInkAnalyzer**](iinkanalyzer.md) ne peut pas modifier le type de nœud et les traits associés pour les objets **IContextNode** confirmés.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-161">[**IInkAnalyzer**](iinkanalyzer.md) cannot change the node type and associated strokes for confirmed **IContextNode** objects.</span></span><br/> |
| [<span data-ttu-id="0a6e4-162">**LoadPropertiesData**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-162">**LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)                           | <span data-ttu-id="0a6e4-163">Recrée les données de propriété internes et spécifiques à l’application pour un tableau d’octets précédemment créé avec [**IContextNode :: SavePropertiesData**](icontextnode-savepropertiesdata.md).</span><span class="sxs-lookup"><span data-stu-id="0a6e4-163">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span><br/>                  |
| [<span data-ttu-id="0a6e4-164">**MoveSubNodeToPosition**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-164">**MoveSubNodeToPosition**</span></span>](icontextnode-movesubnodetoposition.md)                     | <span data-ttu-id="0a6e4-165">Réorganise un objet **IContextNode** enfant spécifié à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-165">Reorders a specified child **IContextNode** object to the specified index.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="0a6e4-166">**RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-166">**RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)                           | <span data-ttu-id="0a6e4-167">Supprime une partie des données spécifiques à l’application.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-167">Removes a piece of application-specific data.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="0a6e4-168">**Apparenter**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-168">**Reparent**</span></span>](icontextnode-reparent.md)                                               | <span data-ttu-id="0a6e4-169">Déplace cet objet **IContextNode** de la collection de sous-nœuds du nœud de contexte parent vers la collection de sous-nœuds du nœud de contexte spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-169">Moves this **IContextNode** object from its parent context node's subnodes collection to the specified context node's subnodes collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="0a6e4-170">**ReparentStrokeByIdToNode**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-170">**ReparentStrokeByIdToNode**</span></span>](icontextnode-reparentstrokebyidtonode.md)               | <span data-ttu-id="0a6e4-171">Déplace les données de trait de ce **IContextNode** vers le **IContextNode** spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-171">Moves stroke data from this **IContextNode** to the specified **IContextNode**.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="0a6e4-172">**SavePropertiesData**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-172">**SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)                           | <span data-ttu-id="0a6e4-173">Récupère un tableau d’octets qui contient les données de propriété internes et spécifiques à l’application pour ce **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-173">Retrieves an array of bytes that contains the application-specific and internal property data for this **IContextNode**.</span></span><br/>                                                                                           |
| [<span data-ttu-id="0a6e4-174">**SetLocation**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-174">**SetLocation**</span></span>](icontextnode-setlocation.md)                                         | <span data-ttu-id="0a6e4-175">Met à jour la position et la taille de ce **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-175">Updates the position and size of this **IContextNode**.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="0a6e4-176">**SetPartiallyPopulated**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-176">**SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)                     | <span data-ttu-id="0a6e4-177">Modifie la valeur qui indique si ce **IContextNode** est partiellement ou entièrement rempli.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-177">Modifies the value that indicates whether this **IContextNode** is partially or fully populated.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="0a6e4-178">**SetStrokes**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-178">**SetStrokes**</span></span>](icontextnode-setstrokes.md)                                           | <span data-ttu-id="0a6e4-179">Associe les traits spécifiés à ce **IContextNode**.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-179">Associates the specified strokes with this **IContextNode**.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="0a6e4-180">Notes</span><span class="sxs-lookup"><span data-stu-id="0a6e4-180">Remarks</span></span>

<span data-ttu-id="0a6e4-181">Les types de nœuds sont décrits dans les constantes de [type de nœud de contexte](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="0a6e4-181">The types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="0a6e4-182">Exemples</span><span class="sxs-lookup"><span data-stu-id="0a6e4-182">Examples</span></span>

<span data-ttu-id="0a6e4-183">L’exemple suivant montre une méthode qui examine un **IContextNode**; la méthode effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a6e4-183">The following example shows a method that examines an **IContextNode**; the method does the following:</span></span>

-   <span data-ttu-id="0a6e4-184">Obtient le type du nœud de contexte.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-184">Gets the context node's type.</span></span> <span data-ttu-id="0a6e4-185">Si le nœud de contexte est une encre non classifiée, un indicateur d’analyse ou un nœud de reconnaissance personnalisé, il appelle une méthode d’assistance pour examiner des propriétés spécifiques du type de nœud.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-185">If the context node is an unclassified ink, analysis hint, or custom recognizer node, it calls a helper method to examine specific properties of the node type.</span></span>
-   <span data-ttu-id="0a6e4-186">Si le nœud possède des sous-nœuds, il examine chaque sous-nœud en s’appelant lui-même.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-186">If the node has subnodes, it examines each subnode by calling itself.</span></span>
-   <span data-ttu-id="0a6e4-187">Si le nœud est un nœud feuille manuscrit, il examine les données de trait du nœud en appelant une méthode d’assistance.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-187">If the node is an ink leaf node, it examines the stroke data for the node by calling a helper method.</span></span>

<span data-ttu-id="0a6e4-188">L’API position InkAnalysis vous permet de créer un nœud de ligne qui contient des mots et des mots de texte.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-188">Ihe InkAnalysis API allows you to create a line node that contains ink words and text words.</span></span> <span data-ttu-id="0a6e4-189">Toutefois, l’analyseur ignore ces nœuds mixtes et les traite comme des nœuds étrangers.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-189">However, the parser will ignore these mixed nodes and will treat them like foreign nodes.</span></span> <span data-ttu-id="0a6e4-190">Cela aura un impact sur l’exactitude de l’analyse de la détection des annotations manuscrites lorsque l’utilisateur final écrit sur ce nœud mixte.</span><span class="sxs-lookup"><span data-stu-id="0a6e4-190">This will have impact the parsing accuracy of detecting ink annotations when the end user writes on or around this mixed node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="0a6e4-191">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a6e4-191">Requirements</span></span>



| <span data-ttu-id="0a6e4-192">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a6e4-192">Requirement</span></span> | <span data-ttu-id="0a6e4-193">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a6e4-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a6e4-194">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a6e4-194">Minimum supported client</span></span><br/> | <span data-ttu-id="0a6e4-195">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a6e4-195">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0a6e4-196">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a6e4-196">Minimum supported server</span></span><br/> | <span data-ttu-id="0a6e4-197">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a6e4-197">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="0a6e4-198">En-tête</span><span class="sxs-lookup"><span data-stu-id="0a6e4-198">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a6e4-199"><dt>IACom. h (nécessite également IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="0a6e4-199"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="0a6e4-200">DLL</span><span class="sxs-lookup"><span data-stu-id="0a6e4-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a6e4-201"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a6e4-201"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="0a6e4-202">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a6e4-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a6e4-203">**IContextNodes**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-203">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="0a6e4-204">Types de nœuds de contexte</span><span class="sxs-lookup"><span data-stu-id="0a6e4-204">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="0a6e4-205">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="0a6e4-205">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="0a6e4-206">Référence de l’analyse de l’encre</span><span class="sxs-lookup"><span data-stu-id="0a6e4-206">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

