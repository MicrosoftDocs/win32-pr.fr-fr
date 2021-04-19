---
description: Les qualificateurs facultatifs traitent les situations récurrentes non communes à toutes les implémentations compatibles CIM, qui ne sont pas requises pour interpréter ces qualificateurs.
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: Qualificateurs facultatifs
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 36fe1b9ceee1211a3b09ce70e03044b7af57eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536632"
---
# <a name="optional-qualifiers"></a><span data-ttu-id="4136e-103">Qualificateurs facultatifs</span><span class="sxs-lookup"><span data-stu-id="4136e-103">Optional Qualifiers</span></span>

<span data-ttu-id="4136e-104">Les qualificateurs facultatifs traitent les situations récurrentes non communes à toutes les implémentations compatibles CIM, qui ne sont pas requises pour interpréter ces qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="4136e-104">Optional qualifiers address recurring situations not common to all CIM-compliant implementations, which are not required to interpret these qualifiers.</span></span> <span data-ttu-id="4136e-105">Les qualificateurs facultatifs sont fournis dans la spécification pour éviter les qualificateurs définis par l’utilisateur aléatoires qui peuvent se produire dans ces situations récurrentes.</span><span class="sxs-lookup"><span data-stu-id="4136e-105">Optional qualifiers are provided in the specification to avoid random user-defined qualifiers that might occur in these recurring situations.</span></span>

<dt>

<span data-ttu-id="4136e-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Supprimer**</span><span class="sxs-lookup"><span data-stu-id="4136e-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-107">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4136e-107">Data type: **boolean**</span></span>

<span data-ttu-id="4136e-108">S’applique à : associations, références</span><span class="sxs-lookup"><span data-stu-id="4136e-108">Applies to: associations, references</span></span>

<span data-ttu-id="4136e-109">Pour les associations, indique si l’Association qualifiée doit être supprimée si l’un des objets référencés dans l’Association est supprimé et si l’objet respectif référencé dans l’Association est qualifié avec **IfDeleted**.</span><span class="sxs-lookup"><span data-stu-id="4136e-109">For associations, indicates whether the qualified association must be deleted if any of the objects referenced in the association are deleted and if the respective object referenced in the association is qualified with **IfDeleted**.</span></span> <span data-ttu-id="4136e-110">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="4136e-110">The default is **FALSE**.</span></span>

<span data-ttu-id="4136e-111">Pour les références, ce qualificateur indique si l’objet référencé doit être supprimé si l’Association contenant la référence est supprimée et qualifiée avec **IfDeleted**, ou si l’un des objets référencés dans l’Association est supprimé et que l’objet respectif référencé dans l’Association est qualifié avec **IfDeleted**.</span><span class="sxs-lookup"><span data-stu-id="4136e-111">For references, this qualifier indicates whether the referenced object must be deleted if the association containing the reference is deleted and qualified with **IfDeleted**, or if any of the objects referenced in the association are deleted and the respective object referenced in the association is qualified with **IfDeleted**.</span></span>

<span data-ttu-id="4136e-112">Utilisation : les applications doivent suivre les associations et les références marquées avec le qualificateur **Delete** et supprimer l’Association ou la référence de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="4136e-112">Usage: Applications must track associations and references marked with the **Delete** qualifier and delete the association or reference appropriately.</span></span> <span data-ttu-id="4136e-113">Si un objet de l’Association a été supprimé mais n’est pas marqué avec **IfDeleted**, l’Association ne doit pas être supprimée.</span><span class="sxs-lookup"><span data-stu-id="4136e-113">If an object in the association has been deleted but is not marked with **IfDeleted**, then the association should not be deleted.</span></span>

<span data-ttu-id="4136e-114">Cette règle d’utilisation doit être vérifiée lorsque le modèle de sécurité CIM est défini.</span><span class="sxs-lookup"><span data-stu-id="4136e-114">This usage rule must be verified when the CIM security model is defined.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Complexes**</span><span class="sxs-lookup"><span data-stu-id="4136e-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Expensive**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-116">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4136e-116">Data type: **boolean**</span></span>

<span data-ttu-id="4136e-117">S’applique à : propriétés, références, classes, associations, méthodes</span><span class="sxs-lookup"><span data-stu-id="4136e-117">Applies to: properties, references, classes, associations, methods</span></span>

<span data-ttu-id="4136e-118">Indique si l’action implicite requiert un calcul extensif.</span><span class="sxs-lookup"><span data-stu-id="4136e-118">Indicates whether the implied action requires extensive computation.</span></span> <span data-ttu-id="4136e-119">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="4136e-119">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**</span><span class="sxs-lookup"><span data-stu-id="4136e-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-121">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4136e-121">Data type: **boolean**</span></span>

<span data-ttu-id="4136e-122">S’applique à : associations et références</span><span class="sxs-lookup"><span data-stu-id="4136e-122">Applies to: associations and references</span></span>

<span data-ttu-id="4136e-123">Indique si tous les objets d’une association qui sont qualifiés par **Delete** doivent être supprimés si l’objet référencé ou l’Association est supprimé.</span><span class="sxs-lookup"><span data-stu-id="4136e-123">Indicates whether all objects within an association that is qualified by **Delete** must be deleted if the referenced object or the association is deleted.</span></span> <span data-ttu-id="4136e-124">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="4136e-124">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indexée**</span><span class="sxs-lookup"><span data-stu-id="4136e-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indexed**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-126">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4136e-126">Data type: **boolean**</span></span>

<span data-ttu-id="4136e-127">S’applique à : propriétés, méthodes</span><span class="sxs-lookup"><span data-stu-id="4136e-127">Applies to: properties, methods</span></span>

<span data-ttu-id="4136e-128">Indique si une propriété de classe doit être indexée.</span><span class="sxs-lookup"><span data-stu-id="4136e-128">Indicates whether a class property should be indexed.</span></span> <span data-ttu-id="4136e-129">En cas d’application aux propriétés dans les classes hébergées par le référentiel, cela a uniquement la signification de la création (au moment de la création de la classe) d’une recherche de requête secondaire rapide pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4136e-129">When applied to properties in classes hosted by the repository, this only has the meaning of creating (at the time of class creation) a fast secondary query lookup for that property.</span></span>

<span data-ttu-id="4136e-130">Seule la valeur **true** (valeur par défaut) est autorisée.</span><span class="sxs-lookup"><span data-stu-id="4136e-130">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Masquer**</span><span class="sxs-lookup"><span data-stu-id="4136e-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Invisible**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-132">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4136e-132">Data type: **boolean**</span></span>

<span data-ttu-id="4136e-133">S’applique à : associations, propriétés, méthodes, références, classes</span><span class="sxs-lookup"><span data-stu-id="4136e-133">Applies to: associations, properties, methods, references, classes</span></span>

<span data-ttu-id="4136e-134">Indique si l’Association est définie uniquement à des fins internes (par exemple, pour la définition de la sémantique de dépendance) et ne doit pas être affichée (par exemple, dans les mappages).</span><span class="sxs-lookup"><span data-stu-id="4136e-134">Indicates whether the association is defined only for internal purposes (for example, for definition of dependency semantics) and should not be displayed (for example, in maps).</span></span> <span data-ttu-id="4136e-135">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="4136e-135">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Conséquent**</span><span class="sxs-lookup"><span data-stu-id="4136e-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Large**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-137">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4136e-137">Data type: **boolean**</span></span>

<span data-ttu-id="4136e-138">S’applique à : Properties, classes</span><span class="sxs-lookup"><span data-stu-id="4136e-138">Applies to: properties, classes</span></span>

<span data-ttu-id="4136e-139">Indique si la propriété ou la classe requiert une grande quantité d’espace de stockage.</span><span class="sxs-lookup"><span data-stu-id="4136e-139">Indicates whether the property or class requires a large amount of storage space.</span></span> <span data-ttu-id="4136e-140">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="4136e-140">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Non \_ null**</span><span class="sxs-lookup"><span data-stu-id="4136e-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Not\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-142">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4136e-142">Data type: **boolean**</span></span>

<span data-ttu-id="4136e-143">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="4136e-143">Applies to: properties</span></span>

<span data-ttu-id="4136e-144">Indique si une propriété de classe ne peut pas prendre la valeur **null** (**VT \_ null**).</span><span class="sxs-lookup"><span data-stu-id="4136e-144">Indicates whether a class property cannot take on a value of **NULL** (**VT\_NULL**).</span></span> <span data-ttu-id="4136e-145">Seule la valeur **true** (valeur par défaut) est autorisée.</span><span class="sxs-lookup"><span data-stu-id="4136e-145">Only the value **TRUE** (default) is allowed.</span></span>

<span data-ttu-id="4136e-146">Si ce qualificateur est spécifié, WMI n’autorise pas la création d’instances avec la propriété définie sur **null**, et les propriétés **null** retournent le code d’erreur **\_ \_ \_ null non conforme WBEM E** .</span><span class="sxs-lookup"><span data-stu-id="4136e-146">If this qualifier is specified, WMI does not allow creation of instances with the property set to **NULL**, and **NULL** properties return the **WBEM\_E\_ILLEGAL\_NULL** error code.</span></span>

<span data-ttu-id="4136e-147">Notez que la [**clé**](standard-qualifiers.md) et les qualificateurs **indexés** impliquent déjà ce comportement.</span><span class="sxs-lookup"><span data-stu-id="4136e-147">Note that the [**Key**](standard-qualifiers.md) and **Indexed** qualifiers already imply this behavior.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Moteur**</span><span class="sxs-lookup"><span data-stu-id="4136e-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-149">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4136e-149">Data type: **string**</span></span>

<span data-ttu-id="4136e-150">S’applique à : any</span><span class="sxs-lookup"><span data-stu-id="4136e-150">Applies to: Any</span></span>

<span data-ttu-id="4136e-151">Indique que l’élément de schéma est dynamique et donc rempli par un fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4136e-151">Indication that the schema element is dynamic and thus populated by a provider.</span></span> <span data-ttu-id="4136e-152">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="4136e-152">The default is **NULL**.</span></span> <span data-ttu-id="4136e-153">Ce qualificateur est un handle spécifique à l’implémentation de l’instrumentation.</span><span class="sxs-lookup"><span data-stu-id="4136e-153">This qualifier is an implementation-specific handle to the instrumentation.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Pratiqué**</span><span class="sxs-lookup"><span data-stu-id="4136e-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Experimental**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-155">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="4136e-155">Data type: **boolean**</span></span>

<span data-ttu-id="4136e-156">S’applique à : any</span><span class="sxs-lookup"><span data-stu-id="4136e-156">Applies to: any</span></span>

<span data-ttu-id="4136e-157">Indique que l’élément spécifié a été proposé pour faire partie d’une version ultérieure des schémas CIM, mais qu’il ne fait pas encore partie du schéma standard.</span><span class="sxs-lookup"><span data-stu-id="4136e-157">Indicates that the specified element has been proposed to be a part of a future release of the CIM Schemas, but is not yet part of the standard Schema.</span></span> <span data-ttu-id="4136e-158">Au lieu de cela, l’élément est disponible pour permettre aux utilisateurs d’expérimenter, d’implémenter et de fournir des commentaires sur.</span><span class="sxs-lookup"><span data-stu-id="4136e-158">Instead, the element is available for users to experiment, implement, and provide feedback on.</span></span> <span data-ttu-id="4136e-159">En fonction des commentaires, l’élément peut être ajouté à la norme comme présenté, modifié ou supprimé.</span><span class="sxs-lookup"><span data-stu-id="4136e-159">Based on feedback, the element may added to the standard as presented, modified, or removed.</span></span> <span data-ttu-id="4136e-160">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="4136e-160">The default is **FALSE**.</span></span> <span data-ttu-id="4136e-161">Une implémentation n’a pas besoin de prendre en charge un élément avec ce qualificateur.</span><span class="sxs-lookup"><span data-stu-id="4136e-161">An implementation does not have to support an element with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="4136e-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-163">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4136e-163">Data type: **string**</span></span>

<span data-ttu-id="4136e-164">S’applique à : propriétés, références, méthodes, paramètres</span><span class="sxs-lookup"><span data-stu-id="4136e-164">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="4136e-165">Type spécifique assigné à un élément de données.</span><span class="sxs-lookup"><span data-stu-id="4136e-165">Specific type assigned to a data item.</span></span> <span data-ttu-id="4136e-166">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="4136e-166">The default is **NULL**.</span></span>

<span data-ttu-id="4136e-167">Utilisation : vous devez utiliser le qualificateur **SyntaxType** avec ce qualificateur.</span><span class="sxs-lookup"><span data-stu-id="4136e-167">Usage: You must use the **SyntaxType** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**</span><span class="sxs-lookup"><span data-stu-id="4136e-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-169">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4136e-169">Data type: **string**</span></span>

<span data-ttu-id="4136e-170">S’applique à : propriétés, références, méthodes, paramètres</span><span class="sxs-lookup"><span data-stu-id="4136e-170">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="4136e-171">Format du qualificateur de **syntaxe** .</span><span class="sxs-lookup"><span data-stu-id="4136e-171">Format of the **Syntax** qualifier.</span></span> <span data-ttu-id="4136e-172">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="4136e-172">The default is **NULL**.</span></span>

<span data-ttu-id="4136e-173">Utilisation : vous devez utiliser le qualificateur de **syntaxe** avec ce qualificateur.</span><span class="sxs-lookup"><span data-stu-id="4136e-173">Usage: You must use the **Syntax** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="4136e-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-175">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4136e-175">Data type: **string**</span></span>

<span data-ttu-id="4136e-176">S’applique à : classes, propriétés, méthodes, associations, indications, références</span><span class="sxs-lookup"><span data-stu-id="4136e-176">Applies to: classes, properties, methods, associations, indications, references</span></span>

<span data-ttu-id="4136e-177">Circonstances dans lesquelles un déclencheur est déclenché.</span><span class="sxs-lookup"><span data-stu-id="4136e-177">Circumstances under which a trigger is fired.</span></span> <span data-ttu-id="4136e-178">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="4136e-178">The default is **NULL**.</span></span> <span data-ttu-id="4136e-179">Les types de déclencheurs varient selon la construction du modèle méta.</span><span class="sxs-lookup"><span data-stu-id="4136e-179">The trigger types vary by meta-model construct.</span></span>

<span data-ttu-id="4136e-180">Pour les classes et les associations, les valeurs autorisées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="4136e-180">For classes and associations, the legal values are:</span></span>

<span data-ttu-id="4136e-181">Créer</span><span class="sxs-lookup"><span data-stu-id="4136e-181">Create</span></span>

<span data-ttu-id="4136e-182">DELETE</span><span class="sxs-lookup"><span data-stu-id="4136e-182">Delete</span></span>

<span data-ttu-id="4136e-183">Update</span><span class="sxs-lookup"><span data-stu-id="4136e-183">Update</span></span>

<span data-ttu-id="4136e-184">Accès</span><span class="sxs-lookup"><span data-stu-id="4136e-184">Access</span></span>

<span data-ttu-id="4136e-185">Pour les propriétés et les références, les valeurs autorisées sont : Update et Access.</span><span class="sxs-lookup"><span data-stu-id="4136e-185">For properties and references, the legal values are: Update and Access.</span></span>

<span data-ttu-id="4136e-186">Pour les méthodes, les valeurs autorisées sont avant et après.</span><span class="sxs-lookup"><span data-stu-id="4136e-186">For methods, the legal values are Before and After.</span></span>

<span data-ttu-id="4136e-187">Pour les indications, la valeur légale est levée.</span><span class="sxs-lookup"><span data-stu-id="4136e-187">For indications, the legal value is Thrown.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**</span><span class="sxs-lookup"><span data-stu-id="4136e-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-189">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="4136e-189">Data type: **string array**</span></span>

<span data-ttu-id="4136e-190">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="4136e-190">Applies to: properties</span></span>

<span data-ttu-id="4136e-191">Ensemble de valeurs indiquant que la valeur de la propriété associée est inconnue (la propriété ne peut pas être considérée comme ayant une valeur valide ou explicite).</span><span class="sxs-lookup"><span data-stu-id="4136e-191">Set of values indicating that the value of the associated property is unknown (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="4136e-192">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="4136e-192">The default is **NULL**.</span></span>

<span data-ttu-id="4136e-193">Les conventions et restrictions utilisées pour définir des valeurs inconnues sont les mêmes que celles applicables au qualificateur [**ValueMap**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="4136e-193">The conventions and restrictions used for defining unknown values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="4136e-194">Notez que ce qualificateur ne peut pas être substitué.</span><span class="sxs-lookup"><span data-stu-id="4136e-194">Note that this qualifier cannot be overridden.</span></span> <span data-ttu-id="4136e-195">Il est déraisonnable de permettre à une sous-classe de traiter une valeur comme une valeur connue quand elle est traitée comme inconnue par une classe parente.</span><span class="sxs-lookup"><span data-stu-id="4136e-195">It is unreasonable to permit a subclass to treat a value as a known value when it is treated as unknown by some parent class.</span></span>

</dd> <dt>

<span data-ttu-id="4136e-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**</span><span class="sxs-lookup"><span data-stu-id="4136e-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**</span></span>
</dt> <dd>

<span data-ttu-id="4136e-197">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="4136e-197">Data type: **string array**</span></span>

<span data-ttu-id="4136e-198">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="4136e-198">Applies to: properties</span></span>

<span data-ttu-id="4136e-199">Ensemble de valeurs indiquant que la valeur de la propriété associée n’est pas prise en charge (la propriété ne peut pas être considérée comme ayant une valeur valide ou explicite).</span><span class="sxs-lookup"><span data-stu-id="4136e-199">Set of values indicating that the value of the associated property is unsupported (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="4136e-200">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="4136e-200">The default is **NULL**.</span></span>

<span data-ttu-id="4136e-201">Les conventions et restrictions utilisées pour définir des valeurs non prises en charge sont les mêmes que celles applicables au qualificateur [**ValueMap**](standard-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="4136e-201">The conventions and restrictions used for defining unsupported values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="4136e-202">Notez que ce qualificateur ne peut pas être substitué.</span><span class="sxs-lookup"><span data-stu-id="4136e-202">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="4136e-203">Il est déraisonnable de permettre à une sous-classe de traiter une valeur comme une valeur prise en charge qui est traitée comme inconnue par une classe parente.</span><span class="sxs-lookup"><span data-stu-id="4136e-203">It is unreasonable to permit a subclass to treat a value as a supported value that is treated as unknown by some parent class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4136e-204">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4136e-204">Requirements</span></span>



| <span data-ttu-id="4136e-205">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4136e-205">Requirement</span></span> | <span data-ttu-id="4136e-206">Valeur</span><span class="sxs-lookup"><span data-stu-id="4136e-206">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4136e-207">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4136e-207">Minimum supported client</span></span><br/> | <span data-ttu-id="4136e-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4136e-208">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4136e-209">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4136e-209">Minimum supported server</span></span><br/> | <span data-ttu-id="4136e-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4136e-210">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4136e-211">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4136e-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4136e-212">Qualificateurs WMI</span><span class="sxs-lookup"><span data-stu-id="4136e-212">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="4136e-213">Ajout d’un qualificateur</span><span class="sxs-lookup"><span data-stu-id="4136e-213">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




