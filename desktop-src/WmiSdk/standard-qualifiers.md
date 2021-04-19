---
description: Toutes les implémentations compatibles CIM doivent gérer un ensemble standard de qualificateurs.
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: Qualificateurs standard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 710e93e53f9e414a44dc14ebafea426f5d7f9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527808"
---
# <a name="standard-qualifiers"></a><span data-ttu-id="94065-103">Qualificateurs standard</span><span class="sxs-lookup"><span data-stu-id="94065-103">Standard Qualifiers</span></span>

<span data-ttu-id="94065-104">Toutes les implémentations compatibles CIM doivent gérer un ensemble standard de qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="94065-104">All CIM-compliant implementations must handle a standard set of qualifiers.</span></span> <span data-ttu-id="94065-105">Aucun objet spécifique n’a tous les qualificateurs listés.</span><span class="sxs-lookup"><span data-stu-id="94065-105">Any specific object does not have all of the qualifiers listed.</span></span> <span data-ttu-id="94065-106">En règle générale, les classes d’extension fournissent des qualificateurs supplémentaires pour faciliter la configuration des instances de classe et d’autres opérations sur la classe.</span><span class="sxs-lookup"><span data-stu-id="94065-106">Usually, extension classes supply additional qualifiers to facilitate provision of class instances and other operations on the class.</span></span>

<span data-ttu-id="94065-107">Il incombe au fournisseur d’appliquer les qualificateurs.</span><span class="sxs-lookup"><span data-stu-id="94065-107">It is the responsibility of the provider to enforce the qualifiers.</span></span> <span data-ttu-id="94065-108">WMI n’applique pas de qualificateurs, mais les utilise uniquement pour informer l’utilisateur de la façon dont la propriété est utilisée.</span><span class="sxs-lookup"><span data-stu-id="94065-108">WMI does not enforce qualifiers, but uses them only to inform the user about how the property is used.</span></span>

> [!Note]  
> <span data-ttu-id="94065-109">WMI est conforme à la spécification CIM 2,5.</span><span class="sxs-lookup"><span data-stu-id="94065-109">WMI is compliant with the CIM 2.5 specification.</span></span>

 

<span data-ttu-id="94065-110">Les qualificateurs présentent les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="94065-110">Qualifiers have the following limitations:</span></span>

-   <span data-ttu-id="94065-111">Tous les qualificateurs standard ne peuvent pas être utilisés ensemble.</span><span class="sxs-lookup"><span data-stu-id="94065-111">Not all standard qualifiers can be used together.</span></span>
-   <span data-ttu-id="94065-112">Tous les qualificateurs ne peuvent pas être appliqués à toutes les constructions, telles que l’Association ou la référence.</span><span class="sxs-lookup"><span data-stu-id="94065-112">Not all qualifiers can be applied to all constructs, such as association or reference.</span></span> <span data-ttu-id="94065-113">Ces limitations sont identifiées dans la liste s’applique à.</span><span class="sxs-lookup"><span data-stu-id="94065-113">These limitations are identified in the Applies to list.</span></span>
-   <span data-ttu-id="94065-114">Pour une construction particulière, telle que l’Association ou la référence, l’utilisation des qualificateurs légaux peut être plus contraignante, car certains qualificateurs s’excluent mutuellement, l’utilisation d’un qualificateur peut impliquer certaines restrictions sur la valeur d’une autre, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="94065-114">For a particular construct, such as association or reference, the use of the legal qualifiers can be further constrained because some qualifiers are mutually exclusive, the use of one qualifier may imply some restrictions on the value of another, and so on.</span></span> <span data-ttu-id="94065-115">Ces règles d’utilisation sont documentées.</span><span class="sxs-lookup"><span data-stu-id="94065-115">These usage rules are documented.</span></span>
-   <span data-ttu-id="94065-116">Les qualificateurs légaux sont hérités par des entités telles que des propriétés, des méthodes, des instances ou des sous-classes uniquement, et non par des associations ou des références.</span><span class="sxs-lookup"><span data-stu-id="94065-116">Legal qualifiers are inherited by entities such as properties, methods, instances, or subclasses only, not by associations or references.</span></span> <span data-ttu-id="94065-117">Par exemple, le qualificateur **MaxLen** qui s’applique aux propriétés n’est pas hérité par les références.</span><span class="sxs-lookup"><span data-stu-id="94065-117">For example, the **MaxLen** qualifier that applies to properties is not inherited by references.</span></span>

<span data-ttu-id="94065-118">La liste suivante répertorie les qualificateurs WMI standard.</span><span class="sxs-lookup"><span data-stu-id="94065-118">The following lists WMI standard qualifiers.</span></span>

<dt>

<span data-ttu-id="94065-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Abstraction**</span><span class="sxs-lookup"><span data-stu-id="94065-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Abstract**</span></span>
</dt> <dd>

<span data-ttu-id="94065-120">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-120">Data type: **boolean**</span></span>

<span data-ttu-id="94065-121">S’applique à : classes, associations, indications</span><span class="sxs-lookup"><span data-stu-id="94065-121">Applies to: classes, associations, indications</span></span>

<span data-ttu-id="94065-122">Indique si la classe est abstraite et sert uniquement de base pour les nouvelles classes.</span><span class="sxs-lookup"><span data-stu-id="94065-122">Indicates whether the class is abstract and serves only as a base for new classes.</span></span> <span data-ttu-id="94065-123">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-123">The default is **FALSE**.</span></span> <span data-ttu-id="94065-124">Vous ne pouvez pas créer d’instances de classes abstraites.</span><span class="sxs-lookup"><span data-stu-id="94065-124">You cannot create instances of abstract classes.</span></span> <span data-ttu-id="94065-125">L’absence de ce qualificateur indique que la classe n’est pas abstraite ; par conséquent, ce qualificateur est requis pour toutes les classes abstraites.</span><span class="sxs-lookup"><span data-stu-id="94065-125">The absence of this qualifier indicates that the class is not abstract; therefore, this qualifier is required for all abstract classes.</span></span>

</dd> <dt>

<span data-ttu-id="94065-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Rassemble**</span><span class="sxs-lookup"><span data-stu-id="94065-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Aggregate**</span></span>
</dt> <dd>

<span data-ttu-id="94065-127">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-127">Data type: **boolean**</span></span>

<span data-ttu-id="94065-128">S’applique à : références</span><span class="sxs-lookup"><span data-stu-id="94065-128">Applies to: references</span></span>

<span data-ttu-id="94065-129">Indique si la référence est le composant parent d’une association d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="94065-129">Indicates whether the reference is the parent component of an aggregation association.</span></span> <span data-ttu-id="94065-130">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-130">The default is **FALSE**.</span></span>

<span data-ttu-id="94065-131">Utilisation : les **qualificateurs Aggregation et** **Aggregate** sont utilisés ensemble l'   **agrégation** qualifie l’Association, et **Aggregate** spécifie la référence parente.</span><span class="sxs-lookup"><span data-stu-id="94065-131">Usage: The **Aggregation** and **Aggregate** qualifiers are used together   **Aggregation** qualifies the association, and **Aggregate** specifies the parent reference.</span></span>

</dd> <dt>

<span data-ttu-id="94065-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Agréger**</span><span class="sxs-lookup"><span data-stu-id="94065-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="94065-133">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-133">Data type: **boolean**</span></span>

<span data-ttu-id="94065-134">S’applique à : associations</span><span class="sxs-lookup"><span data-stu-id="94065-134">Applies to: associations</span></span>

<span data-ttu-id="94065-135">Indique si l’Association est une agrégation.</span><span class="sxs-lookup"><span data-stu-id="94065-135">Indicates whether the association is an aggregation.</span></span> <span data-ttu-id="94065-136">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-136">The default is **FALSE**.</span></span> <span data-ttu-id="94065-137">Utilisé avec **Aggregate**.</span><span class="sxs-lookup"><span data-stu-id="94065-137">Used with **Aggregate**.</span></span> <span data-ttu-id="94065-138">Ce qualificateur est requis pour toutes les associations d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="94065-138">This qualifier is required for all aggregation associations.</span></span>

</dd> <dt>

<span data-ttu-id="94065-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Affecté**</span><span class="sxs-lookup"><span data-stu-id="94065-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**</span></span>
</dt> <dd>

<span data-ttu-id="94065-140">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-140">Data type: **string**</span></span>

<span data-ttu-id="94065-141">S’applique à : propriétés, références, méthodes</span><span class="sxs-lookup"><span data-stu-id="94065-141">Applies to: properties, references, methods</span></span>

<span data-ttu-id="94065-142">Autre nom pour une propriété ou une méthode dans le schéma.</span><span class="sxs-lookup"><span data-stu-id="94065-142">Alternate name for a property or method in the schema.</span></span> <span data-ttu-id="94065-143">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-143">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span><span class="sxs-lookup"><span data-stu-id="94065-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span></span>
</dt> <dd>

<span data-ttu-id="94065-145">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-145">Data type: **string**</span></span>

<span data-ttu-id="94065-146">S’applique à : propriétés, paramètres</span><span class="sxs-lookup"><span data-stu-id="94065-146">Applies to: properties, parameters</span></span>

<span data-ttu-id="94065-147">Type du tableau qualifié.</span><span class="sxs-lookup"><span data-stu-id="94065-147">Type of the qualified array.</span></span>

<span data-ttu-id="94065-148">Les valeurs autorisées sont :</span><span class="sxs-lookup"><span data-stu-id="94065-148">Valid values are:</span></span>

-   <span data-ttu-id="94065-149">Bag (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="94065-149">bag (default)</span></span>
-   <span data-ttu-id="94065-150">indexé</span><span class="sxs-lookup"><span data-stu-id="94065-150">indexed</span></span>
-   <span data-ttu-id="94065-151">ordered</span><span class="sxs-lookup"><span data-stu-id="94065-151">ordered</span></span>

<span data-ttu-id="94065-152">Utilisation : appliquez ce type de qualificateur uniquement aux propriétés et aux paramètres qui sont des tableaux (définis à l’aide de la syntaxe de crochet).</span><span class="sxs-lookup"><span data-stu-id="94065-152">Usage: Apply this type of qualifier only to properties and parameters that are arrays (defined by using bracket syntax).</span></span>

</dd> <dt>

<span data-ttu-id="94065-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Pixels**</span><span class="sxs-lookup"><span data-stu-id="94065-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**BitMap**</span></span>
</dt> <dd>

<span data-ttu-id="94065-154">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="94065-154">Data type: **string array**</span></span>

<span data-ttu-id="94065-155">S’applique à : propriétés, méthodes, paramètres</span><span class="sxs-lookup"><span data-stu-id="94065-155">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="94065-156">Carte de positions de bits significatives où chaque position significative peut être « on » ou « OFF ».</span><span class="sxs-lookup"><span data-stu-id="94065-156">Map of significant bit positions where each significant position can be "on" or "off".</span></span> <span data-ttu-id="94065-157">Chaque bit « on » correspond à une valeur correspondante dans le tableau **BitValue** .</span><span class="sxs-lookup"><span data-stu-id="94065-157">Each "on" bit maps to a corresponding value in the **BitValues** array.</span></span> <span data-ttu-id="94065-158">En ayant plusieurs bits « on », plusieurs valeurs simultanées dans le tableau **BitValue** sont indiquées.</span><span class="sxs-lookup"><span data-stu-id="94065-158">By having multiple bits "on", multiple concurrent values in the **BitValues** array are indicated.</span></span> <span data-ttu-id="94065-159">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-159">The default is **NULL**.</span></span>

<span data-ttu-id="94065-160">Pour plus d’informations, consultez [bitmap et BitValue](bitmap-and-bitvalues.md).</span><span class="sxs-lookup"><span data-stu-id="94065-160">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="94065-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValue**</span><span class="sxs-lookup"><span data-stu-id="94065-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**</span></span>
</dt> <dd>

<span data-ttu-id="94065-162">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="94065-162">Data type: **string array**</span></span>

<span data-ttu-id="94065-163">S’applique à : propriétés, méthodes, paramètres</span><span class="sxs-lookup"><span data-stu-id="94065-163">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="94065-164">Traduction d’une valeur de position de bit en une **chaîne** associée.</span><span class="sxs-lookup"><span data-stu-id="94065-164">Translation of a bit position value into an associated **string**.</span></span> <span data-ttu-id="94065-165">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-165">The default is **NULL**.</span></span>

<span data-ttu-id="94065-166">Pour plus d’informations, consultez [bitmap et BitValue](bitmap-and-bitvalues.md).</span><span class="sxs-lookup"><span data-stu-id="94065-166">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="94065-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Constructeur**</span><span class="sxs-lookup"><span data-stu-id="94065-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Constructor**</span></span>
</dt> <dd>

<span data-ttu-id="94065-168">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-168">Data type: **boolean**</span></span>

<span data-ttu-id="94065-169">S’applique à : méthodes</span><span class="sxs-lookup"><span data-stu-id="94065-169">Applies to: methods</span></span>

<span data-ttu-id="94065-170">Indique si la méthode crée des instances.</span><span class="sxs-lookup"><span data-stu-id="94065-170">Indicates whether the method creates instances.</span></span> <span data-ttu-id="94065-171">Ces méthodes ne sont pas contractions pour agir sur une seule instance ou une seule classe.</span><span class="sxs-lookup"><span data-stu-id="94065-171">These methods are not constrained to acting on a single instance or a single class.</span></span> <span data-ttu-id="94065-172">Par exemple, un constructeur peut créer des instances d’association ainsi que des instances de la classe qui définit le constructeur.</span><span class="sxs-lookup"><span data-stu-id="94065-172">For example, a constructor can create association instances as well as instances of the class that defines the constructor.</span></span>

<span data-ttu-id="94065-173">Le qualificateur du **constructeur** est destiné uniquement à des fins d’information et il n’est pas prévu qu’il soit traité par le gestionnaire d’objets.</span><span class="sxs-lookup"><span data-stu-id="94065-173">The **Constructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="94065-174">Le gestionnaire d’objets n’a pas besoin d’appeler des méthodes de constructeur lors de la création d’un objet.</span><span class="sxs-lookup"><span data-stu-id="94065-174">The object manager does not have to call constructor methods when an object is created.</span></span> <span data-ttu-id="94065-175">De même, lorsqu’un constructeur est appelé, le gestionnaire d’objets n’a pas à appeler de méthodes de constructeur définies pour toute classe parente de la classe d’origine.</span><span class="sxs-lookup"><span data-stu-id="94065-175">Also when a constructor is called, the object manager does not have to invoke any constructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="94065-176">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-176">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**</span><span class="sxs-lookup"><span data-stu-id="94065-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**</span></span>
</dt> <dd>

<span data-ttu-id="94065-178">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-178">Data type: **string**</span></span>

<span data-ttu-id="94065-179">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="94065-179">Applies to: classes</span></span>

<span data-ttu-id="94065-180">Nom de la méthode par laquelle les instances de cette classe sont créées.</span><span class="sxs-lookup"><span data-stu-id="94065-180">Name of the method by which instances of this class are created.</span></span> <span data-ttu-id="94065-181">La valeur est soit « PutInstance », soit le nom d’une autre méthode qui crée les instances.</span><span class="sxs-lookup"><span data-stu-id="94065-181">The value is either "PutInstance" or the name of another method that creates the instances.</span></span> <span data-ttu-id="94065-182">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-182">The default is **NULL**.</span></span>

<span data-ttu-id="94065-183">Utilisation : ce qualificateur ne peut être utilisé que si le qualificateur **SupportsCreate** est présent.</span><span class="sxs-lookup"><span data-stu-id="94065-183">Usage: This qualifier can only be used if the **SupportsCreate** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="94065-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**</span><span class="sxs-lookup"><span data-stu-id="94065-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**</span></span>
</dt> <dd>

<span data-ttu-id="94065-185">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-185">Data type: **string**</span></span>

<span data-ttu-id="94065-186">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="94065-186">Applies to: classes</span></span>

<span data-ttu-id="94065-187">Nom de la méthode par laquelle les instances de cette classe sont supprimées.</span><span class="sxs-lookup"><span data-stu-id="94065-187">Name of the method by which instances of this class are deleted.</span></span> <span data-ttu-id="94065-188">La valeur est soit « DeleteInstance », soit le nom d’une autre méthode qui supprime les instances.</span><span class="sxs-lookup"><span data-stu-id="94065-188">The value is either "DeleteInstance", or the name of another method that deletes the instances.</span></span> <span data-ttu-id="94065-189">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-189">The default is **NULL**.</span></span>

<span data-ttu-id="94065-190">Utilisation : ce qualificateur ne peut être utilisé que si le qualificateur **SupportsDelete** est présent.</span><span class="sxs-lookup"><span data-stu-id="94065-190">Usage: This qualifier can only be used if the **SupportsDelete** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="94065-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="94065-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="94065-192">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-192">Data type: **string**</span></span>

<span data-ttu-id="94065-193">S’applique à : any</span><span class="sxs-lookup"><span data-stu-id="94065-193">Applies to: any</span></span>

<span data-ttu-id="94065-194">Description d’un élément nommé.</span><span class="sxs-lookup"><span data-stu-id="94065-194">Description of a named element.</span></span> <span data-ttu-id="94065-195">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-195">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destructeur**</span><span class="sxs-lookup"><span data-stu-id="94065-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destructor**</span></span>
</dt> <dd>

<span data-ttu-id="94065-197">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-197">Data type: **boolean**</span></span>

<span data-ttu-id="94065-198">S’applique à : méthodes</span><span class="sxs-lookup"><span data-stu-id="94065-198">Applies to: methods</span></span>

<span data-ttu-id="94065-199">Indique si la méthode supprime des instances.</span><span class="sxs-lookup"><span data-stu-id="94065-199">Indicates whether the method deletes instances.</span></span> <span data-ttu-id="94065-200">Les méthodes qui utilisent le qualificateur de **destructeur** suppriment la ou les instances auxquelles le destructeur est appliqué, et ne sont pas contractions pour agir sur une instance ou une classe unique.</span><span class="sxs-lookup"><span data-stu-id="94065-200">Methods using the **Destructor** qualifier delete the instance(s) to which the destructor is applied, and are not constrained to acting on a single instance or class.</span></span> <span data-ttu-id="94065-201">Par exemple, un destructeur peut supprimer des instances d’association ainsi que des instances de la classe qui définit le destructeur.</span><span class="sxs-lookup"><span data-stu-id="94065-201">For example, a destructor might delete association instances as well as instances of the class that defines the destructor.</span></span>

<span data-ttu-id="94065-202">Le qualificateur du **destructeur** est destiné uniquement à des fins d’information et il n’est pas prévu qu’il soit traité par le gestionnaire d’objets.</span><span class="sxs-lookup"><span data-stu-id="94065-202">The **Destructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="94065-203">Le gestionnaire d’objets n’a aucune obligation d’appeler une méthode qui a le qualificateur de **destructeur** lorsqu’une instance est supprimée.</span><span class="sxs-lookup"><span data-stu-id="94065-203">There is no obligation for the object manager to call a method that has the **Destructor** qualifier when an instance is deleted.</span></span> <span data-ttu-id="94065-204">En outre, lorsqu’un destructeur est appelé, le gestionnaire d’objets n’a pas à appeler les méthodes de destructeur définies pour toute classe parente de la classe d’origine.</span><span class="sxs-lookup"><span data-stu-id="94065-204">Also, when a destructor is called, the object manager does not have to invoke any destructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="94065-205">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-205">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="94065-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="94065-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-207">Data type: **string**</span></span>

<span data-ttu-id="94065-208">S’applique à : any</span><span class="sxs-lookup"><span data-stu-id="94065-208">Applies to: any</span></span>

<span data-ttu-id="94065-209">Nom affiché dans l’interface utilisateur au lieu du nom réel de l’élément.</span><span class="sxs-lookup"><span data-stu-id="94065-209">Name displayed in the UI instead of the actual name of the element.</span></span> <span data-ttu-id="94065-210">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-210">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**</span><span class="sxs-lookup"><span data-stu-id="94065-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**</span></span>
</dt> <dd>

<span data-ttu-id="94065-212">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-212">Data type: **string**</span></span>

<span data-ttu-id="94065-213">S’applique à : any</span><span class="sxs-lookup"><span data-stu-id="94065-213">Applies to: any</span></span>

<span data-ttu-id="94065-214">L’élément de type de chaîne qualifié contient une instance incorporée.</span><span class="sxs-lookup"><span data-stu-id="94065-214">The qualified string type element contains an embedded instance.</span></span> <span data-ttu-id="94065-215">La valeur de qualificateur spécifie le nom d’une classe CIM dans le même espace de noms que la classe qui possède l’élément qualifié.</span><span class="sxs-lookup"><span data-stu-id="94065-215">The qualifier value specifies the name of a CIM class in the same namespace as the class owning the qualified element.</span></span> <span data-ttu-id="94065-216">L’instance incorporée est une instance de la classe spécifiée, y compris les instances de ses sous-classes.</span><span class="sxs-lookup"><span data-stu-id="94065-216">The embedded instance is an instance of the specified class, including instances of its subclasses.</span></span> <span data-ttu-id="94065-217">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-217">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gabarit**</span><span class="sxs-lookup"><span data-stu-id="94065-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge**</span></span>
</dt> <dd>

<span data-ttu-id="94065-219">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-219">Data type: **boolean**</span></span>

<span data-ttu-id="94065-220">S’applique à : any</span><span class="sxs-lookup"><span data-stu-id="94065-220">Applies to: any</span></span>

<span data-ttu-id="94065-221">Indique si la propriété représente un entier non négatif, qui peut augmenter ou diminuer, mais ne dépassent jamais une valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="94065-221">Indicates whether the property represents a non-negative integer, which can increase or decrease, but never exceed a maximum value.</span></span> <span data-ttu-id="94065-222">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-222">The default is **FALSE**.</span></span>

<span data-ttu-id="94065-223">La valeur maximale de la propriété ne peut pas être supérieure à 2 ^*n* -1.</span><span class="sxs-lookup"><span data-stu-id="94065-223">The maximum value of the property cannot be greater than 2^*n* - 1.</span></span> <span data-ttu-id="94065-224">*N* peut être 8, 16, 32 ou 64 selon le type de données de la propriété à laquelle ce qualificateur est appliqué.</span><span class="sxs-lookup"><span data-stu-id="94065-224">*N* can be 8, 16, 32, or 64 depending on the data type of the property to which this qualifier is applied.</span></span> <span data-ttu-id="94065-225">La valeur d’une jauge a sa valeur maximale chaque fois que les informations qui sont modélisées sont supérieures ou égales à cette valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="94065-225">The value of a gauge has its maximum value whenever the information being modeled is greater or equal to that maximum value.</span></span> <span data-ttu-id="94065-226">Si les informations qui sont modélisées descendent ensuite en dessous de la valeur maximale, la jauge diminue également.</span><span class="sxs-lookup"><span data-stu-id="94065-226">If the information being modeled subsequently decreases below the maximum value, the gauge also decreases.</span></span> <span data-ttu-id="94065-227">Ce qualificateur ne s’applique qu’aux propriétés dont le type de données est unsigned Integer.</span><span class="sxs-lookup"><span data-stu-id="94065-227">This qualifier is applicable only to properties with an unsigned integer data type.</span></span>

</dd> <dt>

<span data-ttu-id="94065-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**Dans**</span><span class="sxs-lookup"><span data-stu-id="94065-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**In**</span></span>
</dt> <dd>

<span data-ttu-id="94065-229">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-229">Data type: **boolean**</span></span>

<span data-ttu-id="94065-230">S’applique à : paramètres</span><span class="sxs-lookup"><span data-stu-id="94065-230">Applies to: parameters</span></span>

<span data-ttu-id="94065-231">Indique si le paramètre est utilisé pour passer des valeurs à une méthode.</span><span class="sxs-lookup"><span data-stu-id="94065-231">Indicates whether the parameter is used to pass values to a method.</span></span> <span data-ttu-id="94065-232">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="94065-232">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, out**</span><span class="sxs-lookup"><span data-stu-id="94065-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, Out**</span></span>
</dt> <dd>

<span data-ttu-id="94065-234">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-234">Data type: **boolean**</span></span>

<span data-ttu-id="94065-235">S’applique à : paramètres</span><span class="sxs-lookup"><span data-stu-id="94065-235">Applies to: parameters</span></span>

<span data-ttu-id="94065-236">Indique si le paramètre est à la fois un paramètre d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="94065-236">Indicates whether the parameter is both an input and output parameter.</span></span>

</dd> <dt>

<span data-ttu-id="94065-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Essentiel**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="94065-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Key**](key-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="94065-238">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-238">Data type: **boolean**</span></span>

<span data-ttu-id="94065-239">S’applique à : propriétés, références</span><span class="sxs-lookup"><span data-stu-id="94065-239">Applies to: properties, references</span></span>

<span data-ttu-id="94065-240">Indique si la propriété fait partie du handle d’espace de noms.</span><span class="sxs-lookup"><span data-stu-id="94065-240">Indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="94065-241">Si plusieurs propriétés ont le qualificateur de [**clé**](key-qualifier.md) , toutes ces propriétés forment collectivement la clé (une clé composée).</span><span class="sxs-lookup"><span data-stu-id="94065-241">If more than one property has the [**Key**](key-qualifier.md) qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="94065-242">Lorsqu’elles sont prises en compte, les propriétés de clé doivent fournir une référence unique pour chaque instance de classe.</span><span class="sxs-lookup"><span data-stu-id="94065-242">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="94065-243">Si ce qualificateur est placé sur une propriété, seule la valeur **true** est autorisée.</span><span class="sxs-lookup"><span data-stu-id="94065-243">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="94065-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Différé**</span><span class="sxs-lookup"><span data-stu-id="94065-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Lazy**</span></span>
</dt> <dd>

<span data-ttu-id="94065-245">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="94065-245">Applies to: properties</span></span>

<span data-ttu-id="94065-246">Indique que la propriété est gourmande en ressources pour retourner et requiert beaucoup de temps processeur et de mémoire.</span><span class="sxs-lookup"><span data-stu-id="94065-246">Indicates that the property is resource-intensive to return and requires a lot of processor time and memory.</span></span> <span data-ttu-id="94065-247">WMI améliore les performances des requêtes en ne tentant pas de retourner les propriétés marquées avec le qualificateur **Lazy** .</span><span class="sxs-lookup"><span data-stu-id="94065-247">WMI improves the performance of queries by not attempting to return the properties marked with the **Lazy** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="94065-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**</span><span class="sxs-lookup"><span data-stu-id="94065-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**</span></span>
</dt> <dd>

<span data-ttu-id="94065-249">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="94065-249">Data type: **string array**</span></span>

<span data-ttu-id="94065-250">S’applique à : classes, propriétés, associations, indications, références</span><span class="sxs-lookup"><span data-stu-id="94065-250">Applies to: classes, properties, associations, indications, references</span></span>

<span data-ttu-id="94065-251">Ensemble de valeurs qui indiquent un chemin d’accès à un emplacement où vous pouvez trouver plus d’informations sur l’origine d’une propriété, d’une classe, d’une association, d’une indication ou d’une référence.</span><span class="sxs-lookup"><span data-stu-id="94065-251">Set of values that indicate a path to a location where you can find more information about the origin of a property, class, association, indication, or reference.</span></span> <span data-ttu-id="94065-252">La chaîne de mappage peut être un chemin d’accès de répertoire, une URL, une clé de Registre, un fichier include, une référence à une classe CIM ou un autre format.</span><span class="sxs-lookup"><span data-stu-id="94065-252">The mapping string can be a directory path, a URL, a registry key, an include file, reference to a CIM class, or some other format.</span></span> <span data-ttu-id="94065-253">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-253">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**</span><span class="sxs-lookup"><span data-stu-id="94065-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**</span></span>
</dt> <dd>

<span data-ttu-id="94065-255">Type de données : **int**</span><span class="sxs-lookup"><span data-stu-id="94065-255">Data type: **int**</span></span>

<span data-ttu-id="94065-256">S’applique à : références</span><span class="sxs-lookup"><span data-stu-id="94065-256">Applies to: references</span></span>

<span data-ttu-id="94065-257">Nombre maximal de valeurs qu’une référence donnée peut avoir pour chaque ensemble d’autres valeurs de référence dans l’Association.</span><span class="sxs-lookup"><span data-stu-id="94065-257">Maximum number of values a given reference can have for each set of other reference values in the association.</span></span> <span data-ttu-id="94065-258">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-258">The default is **NULL**.</span></span> <span data-ttu-id="94065-259">Par exemple, si une association associe une instance à des instances B et qu’il ne doit y avoir qu’une instance pour chaque instance B, la référence à un doit avoir au maximum un qualificateur.</span><span class="sxs-lookup"><span data-stu-id="94065-259">For example, if an association relates A instances to B instances and there must be at most one A instance for each B instance, then the reference to A should have a maximum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="94065-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span><span class="sxs-lookup"><span data-stu-id="94065-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span></span>
</dt> <dd>

<span data-ttu-id="94065-261">Type de données : **int**</span><span class="sxs-lookup"><span data-stu-id="94065-261">Data type: **int**</span></span>

<span data-ttu-id="94065-262">S’applique à : propriétés, méthodes, paramètres</span><span class="sxs-lookup"><span data-stu-id="94065-262">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="94065-263">Longueur maximale (en caractères) d’un élément de données de **type chaîne** et indique la prise en charge des tableaux de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="94065-263">Maximum length (in characters) of a **string** data item and indicates support of fixed-length arrays.</span></span>

<span data-ttu-id="94065-264">Si un tableau de longueur fixe est rencontré, le qualificateur **MaxLen** contient la longueur fixe trouvée lors de l’analyse.</span><span class="sxs-lookup"><span data-stu-id="94065-264">If a fixed-length array is encountered, the **MaxLen** qualifier contains the fixed length found during parsing.</span></span> <span data-ttu-id="94065-265">Si un tableau de longueur variable est rencontré, ce qualificateur n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="94065-265">If a variable-length array is encountered, then this qualifier is not used.</span></span> <span data-ttu-id="94065-266">**MaxLen** est utilisé pour suggérer le nombre maximal d’éléments qui doivent être stockés dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="94065-266">**MaxLen** is used to suggest the maximum number of elements that should be stored in an array.</span></span> <span data-ttu-id="94065-267">Lors du remplacement de la valeur par défaut, toute valeur entière non signée (**UInt32**) peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="94065-267">When overriding the default value, any unsigned integer value (**uint32**) can be specified.</span></span> <span data-ttu-id="94065-268">La valeur **null** (valeur par défaut) implique une longueur illimitée.</span><span class="sxs-lookup"><span data-stu-id="94065-268">A value of **NULL** (default) implies unlimited length.</span></span>

</dd> <dt>

<span data-ttu-id="94065-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span><span class="sxs-lookup"><span data-stu-id="94065-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="94065-270">Type de données : **int**</span><span class="sxs-lookup"><span data-stu-id="94065-270">Data type: **int**</span></span>

<span data-ttu-id="94065-271">S’applique à : propriétés, méthodes, paramètres</span><span class="sxs-lookup"><span data-stu-id="94065-271">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="94065-272">Valeur maximale de l’objet.</span><span class="sxs-lookup"><span data-stu-id="94065-272">Maximum value of the object.</span></span> <span data-ttu-id="94065-273">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-273">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**</span><span class="sxs-lookup"><span data-stu-id="94065-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**</span></span>
</dt> <dd>

<span data-ttu-id="94065-275">Type de données : **int**</span><span class="sxs-lookup"><span data-stu-id="94065-275">Data type: **int**</span></span>

<span data-ttu-id="94065-276">S’applique à : références</span><span class="sxs-lookup"><span data-stu-id="94065-276">Applies to: references</span></span>

<span data-ttu-id="94065-277">Cardinalité minimale de la référence (nombre minimal de valeurs qu’une référence donnée peut avoir pour chaque ensemble d’autres valeurs de référence dans l’Association).</span><span class="sxs-lookup"><span data-stu-id="94065-277">Minimum cardinality of the reference (the minimum number of values a given reference can have for each set of other reference values in the association).</span></span> <span data-ttu-id="94065-278">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="94065-278">The default is 0.</span></span>

<span data-ttu-id="94065-279">Par exemple, si une association associe des instances à B et qu’il doit y avoir au moins une instance pour chaque instance B, la référence à un doit avoir au minimum un qualificateur.</span><span class="sxs-lookup"><span data-stu-id="94065-279">For example, if an association relates A instances to B instances, and there must be at least one A instance for each B instance, then the reference to A should have a minimum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="94065-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span><span class="sxs-lookup"><span data-stu-id="94065-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="94065-281">Type de données : **int**</span><span class="sxs-lookup"><span data-stu-id="94065-281">Data type: **int**</span></span>

<span data-ttu-id="94065-282">S’applique à : propriétés, méthodes, paramètres</span><span class="sxs-lookup"><span data-stu-id="94065-282">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="94065-283">Indique la valeur minimale de l’objet.</span><span class="sxs-lookup"><span data-stu-id="94065-283">Indicates the minimum value of the object.</span></span> <span data-ttu-id="94065-284">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-284">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**</span><span class="sxs-lookup"><span data-stu-id="94065-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**</span></span>
</dt> <dd>

<span data-ttu-id="94065-286">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="94065-286">Data type: **string array**</span></span>

<span data-ttu-id="94065-287">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="94065-287">Applies to: properties</span></span>

<span data-ttu-id="94065-288">Ensemble de valeurs qui indiquent la correspondance entre la propriété d’un objet et d’autres propriétés dans le schéma CIM.</span><span class="sxs-lookup"><span data-stu-id="94065-288">Set of values that indicate correspondence between an object's property and other properties in the CIM schema.</span></span> <span data-ttu-id="94065-289">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-289">The default is **NULL**.</span></span>

<span data-ttu-id="94065-290">Les propriétés d’objet sont identifiées à l’aide de la syntaxe suivante.</span><span class="sxs-lookup"><span data-stu-id="94065-290">Object properties are identified using the following syntax.</span></span>

<span data-ttu-id="94065-291"><schema name> "\_" <class or association name> "." <property name></span><span class="sxs-lookup"><span data-stu-id="94065-291"><schema name> "\_" <class or association name> "." <property name></span></span>

</dd> <dt>

<span data-ttu-id="94065-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Non locale**</span><span class="sxs-lookup"><span data-stu-id="94065-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Nonlocal**</span></span>
</dt> <dd>

<span data-ttu-id="94065-293">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-293">Data type: **string**</span></span>

<span data-ttu-id="94065-294">S’applique à : références</span><span class="sxs-lookup"><span data-stu-id="94065-294">Applies to: references</span></span>

<span data-ttu-id="94065-295">Emplacement d’une instance, dont la valeur est <*namespacetype*>://<*namespacehandle*> la valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-295">Location of an instance, the value of which is <*namespacetype*>://<*namespacehandle*> The default is **NULL**.</span></span>

<span data-ttu-id="94065-296">Utilisation : ce qualificateur ne peut pas être utilisé avec le qualificateur **NonlocalType** .</span><span class="sxs-lookup"><span data-stu-id="94065-296">Usage: This qualifier cannot be used with the **NonlocalType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="94065-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**</span><span class="sxs-lookup"><span data-stu-id="94065-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**</span></span>
</dt> <dd>

<span data-ttu-id="94065-298">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-298">Data type: **string**</span></span>

<span data-ttu-id="94065-299">S’applique à : références</span><span class="sxs-lookup"><span data-stu-id="94065-299">Applies to: references</span></span>

<span data-ttu-id="94065-300">Type d’emplacement d’une instance.</span><span class="sxs-lookup"><span data-stu-id="94065-300">Type of location of an instance.</span></span> <span data-ttu-id="94065-301">Sa valeur est <namespacetype> .</span><span class="sxs-lookup"><span data-stu-id="94065-301">Its value is <namespacetype>.</span></span> <span data-ttu-id="94065-302">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-302">The default is **NULL**.</span></span>

<span data-ttu-id="94065-303">Utilisation : ce qualificateur ne peut pas être utilisé avec le qualificateur non **local** .</span><span class="sxs-lookup"><span data-stu-id="94065-303">Usage: This qualifier cannot be used with the **Nonlocal** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="94065-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span><span class="sxs-lookup"><span data-stu-id="94065-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span></span>
</dt> <dd>

<span data-ttu-id="94065-305">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-305">Data type: **string**</span></span>

<span data-ttu-id="94065-306">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="94065-306">Applies to: properties</span></span>

<span data-ttu-id="94065-307">Valeur qui indique que la propriété associée est **null** (la propriété n’a pas de valeur valide ou explicite).</span><span class="sxs-lookup"><span data-stu-id="94065-307">Value that indicates that the associated property is **NULL** (the property does not have a valid or meaningful value).</span></span> <span data-ttu-id="94065-308">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-308">The default is **NULL**.</span></span>

<span data-ttu-id="94065-309">Les conventions et restrictions utilisées pour définir les valeurs **null** sont les mêmes que celles applicables au qualificateur **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="94065-309">The conventions and restrictions used for defining **NULL** values are the same as those applicable to the **ValueMap** qualifier.</span></span> <span data-ttu-id="94065-310">Notez que ce qualificateur ne peut pas être substitué.</span><span class="sxs-lookup"><span data-stu-id="94065-310">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="94065-311">Il est déraisonnable de permettre à une sous-classe de retourner une valeur **null** différente de celle de la classe parente.</span><span class="sxs-lookup"><span data-stu-id="94065-311">It is unreasonable to permit a subclass to return a different **NULL** value than that of the parent class.</span></span>

</dd> <dt>

<span data-ttu-id="94065-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**À**</span><span class="sxs-lookup"><span data-stu-id="94065-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**Out**</span></span>
</dt> <dd>

<span data-ttu-id="94065-313">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-313">Data type: **boolean**</span></span>

<span data-ttu-id="94065-314">S’applique à : paramètres</span><span class="sxs-lookup"><span data-stu-id="94065-314">Applies to: parameters</span></span>

<span data-ttu-id="94065-315">Indique si le paramètre retourne des valeurs à partir d’une méthode.</span><span class="sxs-lookup"><span data-stu-id="94065-315">Indicates whether the parameter returns values from a method.</span></span> <span data-ttu-id="94065-316">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-316">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Remplacer**</span><span class="sxs-lookup"><span data-stu-id="94065-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Override**</span></span>
</dt> <dd>

<span data-ttu-id="94065-318">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-318">Data type: **string**</span></span>

<span data-ttu-id="94065-319">S’applique à : propriétés, méthodes, références</span><span class="sxs-lookup"><span data-stu-id="94065-319">Applies to: properties, methods, references</span></span>

<span data-ttu-id="94065-320">Classe parente ou construction subordonnée (propriété, méthode ou référence) qui est remplacée par la propriété, la méthode ou la référence du même nom dans la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="94065-320">Parent class or subordinate construct (property, method, or reference) which is overridden by the property, method, or reference of the same name in the derived class.</span></span> <span data-ttu-id="94065-321">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-321">The default is **NULL**.</span></span>

<span data-ttu-id="94065-322">Le format est le suivant :</span><span class="sxs-lookup"><span data-stu-id="94065-322">The format is:</span></span>

<span data-ttu-id="94065-323">\[<> de la *classe* . \] < *construction subordonnée*></span><span class="sxs-lookup"><span data-stu-id="94065-323">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="94065-324">Si le nom de la classe est omis, le remplacement s’applique à la construction subordonnée dans la classe parente de la hiérarchie de classes.</span><span class="sxs-lookup"><span data-stu-id="94065-324">If the class name is omitted, the override applies to the subordinate construct in the parent class in the class hierarchy.</span></span>

<span data-ttu-id="94065-325">Utilisation : le qualificateur **override** ne peut faire référence qu’à des constructions basées sur le même méta-modèle.</span><span class="sxs-lookup"><span data-stu-id="94065-325">Usage: The **Override** qualifier can refer to constructs based on the same meta model only.</span></span> <span data-ttu-id="94065-326">La modification d’un nom ou d’une signature de construction au cours d’une opération de remplacement n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="94065-326">It is not allowed to change a construct name or signature during an override operation.</span></span>

</dd> <dt>

<span data-ttu-id="94065-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**</span><span class="sxs-lookup"><span data-stu-id="94065-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**</span></span>
</dt> <dd>

<span data-ttu-id="94065-328">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="94065-328">Applies to: classes</span></span>

<span data-ttu-id="94065-329">Indique si la valeur de propriété d’une sous-classe remplace la valeur dans une classe parente.</span><span class="sxs-lookup"><span data-stu-id="94065-329">Indicates whether the property value on a subclass overrides the value in a parent class.</span></span> <span data-ttu-id="94065-330">L’implication fonctionnelle est que, si vous exécutez une requête sur la classe parente, et si votre clause **Where** comprend cette propriété, le parent doit retourner une instance avec la valeur substituée.</span><span class="sxs-lookup"><span data-stu-id="94065-330">The functional implication is that, if you perform a query against the parent class, and if your **WHERE** clause includes this property, the parent must return an instance with the overridden value.</span></span> <span data-ttu-id="94065-331">Par conséquent, la gestion Windows ajuste la clause **Where** de la requête envoyée à la classe parente pour exclure les références à cette propriété.</span><span class="sxs-lookup"><span data-stu-id="94065-331">As a result, Windows Management adjusts the **WHERE** clause of the query sent to the parent class to exclude references to this property.</span></span>

</dd> <dt>

<span data-ttu-id="94065-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagées**</span><span class="sxs-lookup"><span data-stu-id="94065-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagated**</span></span>
</dt> <dd>

<span data-ttu-id="94065-333">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-333">Data type: **string**</span></span>

<span data-ttu-id="94065-334">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="94065-334">Applies to: properties</span></span>

<span data-ttu-id="94065-335">Nom de la clé qui est propagée.</span><span class="sxs-lookup"><span data-stu-id="94065-335">Name of the key being propagated.</span></span> <span data-ttu-id="94065-336">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-336">The default is **NULL**.</span></span>

<span data-ttu-id="94065-337">L’utilisation de ce qualificateur suppose l’existence d’un seul qualificateur faible sur une référence qui a la classe conteneur comme cible.</span><span class="sxs-lookup"><span data-stu-id="94065-337">Use of this qualifier assumes the existence of only one weak qualifier on a reference that has the containing class as its target.</span></span> <span data-ttu-id="94065-338">La propriété associée doit avoir la même valeur que la propriété nommée par le qualificateur dans la classe de l’autre côté de l’Association faible.</span><span class="sxs-lookup"><span data-stu-id="94065-338">The associated property must have the same value as the property named by the qualifier in the class on the other side of the weak association.</span></span> <span data-ttu-id="94065-339">Le format est le suivant :</span><span class="sxs-lookup"><span data-stu-id="94065-339">The format is:</span></span>

<span data-ttu-id="94065-340">\[<> de la *classe* . \] < *construction subordonnée*></span><span class="sxs-lookup"><span data-stu-id="94065-340">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="94065-341">Utilisation : quand le qualificateur **propagé** est utilisé, le qualificateur de [**clé**](key-qualifier.md) doit être spécifié avec la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="94065-341">Usage: When the **Propagated** qualifier is used, the [**Key**](key-qualifier.md) qualifier must be specified with a value of **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**En lecture**</span><span class="sxs-lookup"><span data-stu-id="94065-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read**</span></span>
</dt> <dd>

<span data-ttu-id="94065-343">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-343">Data type: **boolean**</span></span>

<span data-ttu-id="94065-344">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="94065-344">Applies to: properties</span></span>

<span data-ttu-id="94065-345">Indique si la propriété est lisible.</span><span class="sxs-lookup"><span data-stu-id="94065-345">Indicates whether the property is readable.</span></span> <span data-ttu-id="94065-346">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="94065-346">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="94065-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Required**</span></span>
</dt> <dd>

<span data-ttu-id="94065-348">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-348">Data type: **boolean**</span></span>

<span data-ttu-id="94065-349">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="94065-349">Applies to: properties</span></span>

<span data-ttu-id="94065-350">Indique si une valeur non null est requise pour la propriété.</span><span class="sxs-lookup"><span data-stu-id="94065-350">Indicates whether a non-null value is required for the property.</span></span> <span data-ttu-id="94065-351">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-351">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Faisant**</span><span class="sxs-lookup"><span data-stu-id="94065-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="94065-353">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-353">Data type: **string**</span></span>

<span data-ttu-id="94065-354">S’applique à : classes, associations, indications, schémas</span><span class="sxs-lookup"><span data-stu-id="94065-354">Applies to: classes, associations, indications, schemas</span></span>

<span data-ttu-id="94065-355">Numéro de révision mineure de l’objet de schéma.</span><span class="sxs-lookup"><span data-stu-id="94065-355">Minor revision number of the schema object.</span></span> <span data-ttu-id="94065-356">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-356">The default is **NULL**.</span></span>

<span data-ttu-id="94065-357">Utilisation : le qualificateur de **version** doit être présent pour fournir le numéro de version principale lorsque le qualificateur de **révision** est utilisé.</span><span class="sxs-lookup"><span data-stu-id="94065-357">Usage: The **Version** qualifier must be present to supply the major version number when the **Revision** qualifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="94065-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schéma**</span><span class="sxs-lookup"><span data-stu-id="94065-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schema**</span></span>
</dt> <dd>

<span data-ttu-id="94065-359">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-359">Data type: **string**</span></span>

<span data-ttu-id="94065-360">S’applique à : propriétés, méthodes</span><span class="sxs-lookup"><span data-stu-id="94065-360">Applies to: properties, methods</span></span>

<span data-ttu-id="94065-361">Nom du schéma dans lequel la fonctionnalité est définie.</span><span class="sxs-lookup"><span data-stu-id="94065-361">Name of the schema in which the feature is defined.</span></span> <span data-ttu-id="94065-362">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-362">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Code**</span><span class="sxs-lookup"><span data-stu-id="94065-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Source**</span></span>
</dt> <dd>

<span data-ttu-id="94065-364">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-364">Data type: **string**</span></span>

<span data-ttu-id="94065-365">S’applique à : classes, associations, indications, références</span><span class="sxs-lookup"><span data-stu-id="94065-365">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="94065-366">Emplacement d’une instance.</span><span class="sxs-lookup"><span data-stu-id="94065-366">Location of an instance.</span></span> <span data-ttu-id="94065-367">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-367">The default is **NULL**.</span></span>

<span data-ttu-id="94065-368">La valeur du qualificateur est <*namespacetype*>://<*namespacehandle*>.</span><span class="sxs-lookup"><span data-stu-id="94065-368">The qualifier's value is <*namespacetype*>://<*namespacehandle*>.</span></span>

<span data-ttu-id="94065-369">Utilisation : le qualificateur **source** ne peut pas être utilisé avec le qualificateur **SourceType** .</span><span class="sxs-lookup"><span data-stu-id="94065-369">Usage: The **Source** qualifier cannot be used with the **SourceType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="94065-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**Telle**</span><span class="sxs-lookup"><span data-stu-id="94065-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span></span>
</dt> <dd>

<span data-ttu-id="94065-371">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-371">Data type: **string**</span></span>

<span data-ttu-id="94065-372">S’applique à : classes, associations, indications, références</span><span class="sxs-lookup"><span data-stu-id="94065-372">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="94065-373">Type d’emplacement d’une instance.</span><span class="sxs-lookup"><span data-stu-id="94065-373">Type of location of an instance.</span></span> <span data-ttu-id="94065-374">La valeur de ce qualificateur est <> *NamespaceType* .</span><span class="sxs-lookup"><span data-stu-id="94065-374">The value of this qualifier is <*namespacetype*>.</span></span> <span data-ttu-id="94065-375">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-375">The default is **NULL**.</span></span>

<span data-ttu-id="94065-376">Utilisation : le qualificateur **SourceType** ne peut pas être utilisé avec le qualificateur **source** .</span><span class="sxs-lookup"><span data-stu-id="94065-376">Usage: The **SourceType** qualifier cannot be used with the **Source** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="94065-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span><span class="sxs-lookup"><span data-stu-id="94065-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span></span>
</dt> <dd>

<span data-ttu-id="94065-378">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-378">Data type: **boolean**</span></span>

<span data-ttu-id="94065-379">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="94065-379">Applies to: classes</span></span>

<span data-ttu-id="94065-380">Indique si la classe prend en charge la création d’instances de.</span><span class="sxs-lookup"><span data-stu-id="94065-380">Indicates whether the class supports the creation of instances.</span></span> <span data-ttu-id="94065-381">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-381">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="94065-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span></span>
</dt> <dd>

<span data-ttu-id="94065-383">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-383">Data type: **boolean**</span></span>

<span data-ttu-id="94065-384">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="94065-384">Applies to: classes</span></span>

<span data-ttu-id="94065-385">Indique si la classe prend en charge la suppression des instances de.</span><span class="sxs-lookup"><span data-stu-id="94065-385">Indicates whether the class supports the deletion of instances.</span></span> <span data-ttu-id="94065-386">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-386">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**</span><span class="sxs-lookup"><span data-stu-id="94065-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="94065-388">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-388">Data type: **boolean**</span></span>

<span data-ttu-id="94065-389">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="94065-389">Applies to: classes</span></span>

<span data-ttu-id="94065-390">Indique si la classe prend en charge la modification (mise à jour) des instances de.</span><span class="sxs-lookup"><span data-stu-id="94065-390">Indicates whether the class supports the modification (updating) of instances.</span></span> <span data-ttu-id="94065-391">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-391">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminaux**</span><span class="sxs-lookup"><span data-stu-id="94065-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**</span></span>
</dt> <dd>

<span data-ttu-id="94065-393">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-393">Data type: **boolean**</span></span>

<span data-ttu-id="94065-394">S’applique à : classes</span><span class="sxs-lookup"><span data-stu-id="94065-394">Applies to: classes</span></span>

<span data-ttu-id="94065-395">Indique si la classe peut avoir des sous-classes.</span><span class="sxs-lookup"><span data-stu-id="94065-395">Indicates whether the class can have subclasses.</span></span> <span data-ttu-id="94065-396">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-396">The default is **FALSE**.</span></span>

<span data-ttu-id="94065-397">Si une sous-classe est déclarée, le compilateur génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="94065-397">If a subclass is declared, the compiler generates an error.</span></span>

<span data-ttu-id="94065-398">Utilisation : ce qualificateur ne peut pas coexister avec le qualificateur **abstract** .</span><span class="sxs-lookup"><span data-stu-id="94065-398">Usage: This qualifier cannot coexist with the **Abstract** qualifier.</span></span> <span data-ttu-id="94065-399">Si les qualificateurs **Terminal** et **abstract** sont tous les deux spécifiés, le compilateur génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="94065-399">If both the **Terminal** and **Abstract** qualifiers are specified, the compiler generates an error.</span></span>

</dd> <dt>

<span data-ttu-id="94065-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Sections**</span><span class="sxs-lookup"><span data-stu-id="94065-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Units**</span></span>
</dt> <dd>

<span data-ttu-id="94065-401">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-401">Data type: **string**</span></span>

<span data-ttu-id="94065-402">S’applique à : propriétés, méthodes, paramètres</span><span class="sxs-lookup"><span data-stu-id="94065-402">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="94065-403">Type d’unité dans laquelle l’élément de données associé est exprimé.</span><span class="sxs-lookup"><span data-stu-id="94065-403">Type of unit in which the associated data item is expressed.</span></span> <span data-ttu-id="94065-404">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-404">The default is **NULL**.</span></span>

<span data-ttu-id="94065-405">Par exemple, un élément de données de taille peut avoir la valeur « octets » pour les **unités**.</span><span class="sxs-lookup"><span data-stu-id="94065-405">For example, a size data item might have a value of "bytes" for **Units**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span><span class="sxs-lookup"><span data-stu-id="94065-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span></span>
</dt> <dd>

<span data-ttu-id="94065-407">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="94065-407">Data type: **string array**</span></span>

<span data-ttu-id="94065-408">S’applique à : propriétés, méthodes, paramètres</span><span class="sxs-lookup"><span data-stu-id="94065-408">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="94065-409">Ensemble de valeurs autorisées pour une propriété, un type de retour de méthode ou un paramètre de méthode.</span><span class="sxs-lookup"><span data-stu-id="94065-409">Set of permissible values for a property, method return type, or method parameter.</span></span> <span data-ttu-id="94065-410">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-410">The default is **NULL**.</span></span>

<span data-ttu-id="94065-411">Utilisation : ce qualificateur peut être utilisé seul ou en combinaison avec le qualificateur **values** .</span><span class="sxs-lookup"><span data-stu-id="94065-411">Usage: This qualifier can be used alone or in combination with the **Values** qualifier.</span></span> <span data-ttu-id="94065-412">En cas d’utilisation en association avec le qualificateur **values** , l’emplacement de la valeur dans le tableau **ValueMap** fournit l’emplacement de l’entrée correspondante dans le tableau **values** .</span><span class="sxs-lookup"><span data-stu-id="94065-412">When used in combination with the **Values** qualifier, the location of the value in the **ValueMap** array provides the location of the corresponding entry in the **Values** array.</span></span> <span data-ttu-id="94065-413">Utilisez le qualificateur **ValueMap** uniquement avec des valeurs de chaîne et d’entier.</span><span class="sxs-lookup"><span data-stu-id="94065-413">Use the **ValueMap** qualifier only with string and integer values.</span></span> <span data-ttu-id="94065-414">La syntaxe de la représentation d’une valeur entière dans le tableau de mappage des valeurs est digit \[ + \| = \] \[ \* digit \] .</span><span class="sxs-lookup"><span data-stu-id="94065-414">The syntax for representing an integer value in the value map array is \[+\|=\]digit\[\*digit\].</span></span> <span data-ttu-id="94065-415">Le contenu, le nombre maximal de chiffres et la valeur représentée sont limités par le type de la propriété associée.</span><span class="sxs-lookup"><span data-stu-id="94065-415">The content, maximum number of digits, and represented value are constrained by the type of the associated property.</span></span> <span data-ttu-id="94065-416">Par exemple, UInt8 ne peut pas être signé, doit être inférieur à quatre chiffres et doit représenter une valeur inférieure à 256.</span><span class="sxs-lookup"><span data-stu-id="94065-416">For example, uint8 may not be signed, must be less than four digits, and must represent a value less than 256.</span></span>

</dd> <dt>

<span data-ttu-id="94065-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Valeurs**</span><span class="sxs-lookup"><span data-stu-id="94065-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Values**</span></span>
</dt> <dd>

<span data-ttu-id="94065-418">Type de données : **tableau de chaînes**</span><span class="sxs-lookup"><span data-stu-id="94065-418">Data type: **string array**</span></span>

<span data-ttu-id="94065-419">S’applique à : propriétés, méthodes, paramètres</span><span class="sxs-lookup"><span data-stu-id="94065-419">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="94065-420">Ensemble de valeurs traduisant une valeur entière en une chaîne associée.</span><span class="sxs-lookup"><span data-stu-id="94065-420">Set of values translating an integer value into an associated string.</span></span> <span data-ttu-id="94065-421">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-421">The default is **NULL**.</span></span>

<span data-ttu-id="94065-422">Cette propriété spécifie également un tableau de valeurs de chaîne à mapper à une propriété d’énumération.</span><span class="sxs-lookup"><span data-stu-id="94065-422">This property also specifies an array of string values to be mapped to an enumeration property.</span></span> <span data-ttu-id="94065-423">Ce qualificateur peut être appliqué à une propriété de type entier ou à une propriété de type chaîne, et le mappage peut être implicite ou explicite.</span><span class="sxs-lookup"><span data-stu-id="94065-423">This qualifier can be applied to either an integer property or a string property, and the mapping can be implicit or explicit.</span></span> <span data-ttu-id="94065-424">Si le mappage est implicite, les valeurs de propriété de type entier ou chaîne représentent des positions ordinales dans le tableau de **valeurs** .</span><span class="sxs-lookup"><span data-stu-id="94065-424">If the mapping is implicit, integer or string property values represent ordinal positions in the **Values** array.</span></span> <span data-ttu-id="94065-425">Si le mappage est explicite, la propriété doit être un entier et les valeurs de propriété valides sont répertoriées dans le tableau défini par le qualificateur **ValueMap** .</span><span class="sxs-lookup"><span data-stu-id="94065-425">If the mapping is explicit, the property must be an integer, and valid property values are listed in the array defined by the **ValueMap** qualifier.</span></span> <span data-ttu-id="94065-426">Pour plus d’informations, consultez [mappage des valeurs](value-map.md).</span><span class="sxs-lookup"><span data-stu-id="94065-426">For more information, see [Value Map](value-map.md).</span></span>

<span data-ttu-id="94065-427">Si aucun qualificateur **ValueMap** n’est présent, le tableau de **valeurs** est indexé (relatif à zéro) à l’aide de la valeur dans la propriété, le type de retour de méthode ou le paramètre de méthode associé.</span><span class="sxs-lookup"><span data-stu-id="94065-427">If a **ValueMap** qualifier is not present, the **Values** array is indexed (zero-relative) by using the value in the associated property, method return type, or method parameter.</span></span> <span data-ttu-id="94065-428">Si un qualificateur **ValueMap** est présent, l’index des valeurs est défini par l’emplacement de la valeur de la propriété dans le mappage des valeurs.</span><span class="sxs-lookup"><span data-stu-id="94065-428">If a **ValueMap** qualifier is present, the values index is defined by the location of the property value in the value map.</span></span>

</dd> <dt>

<span data-ttu-id="94065-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span><span class="sxs-lookup"><span data-stu-id="94065-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="94065-430">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="94065-430">Data type: **string**</span></span>

<span data-ttu-id="94065-431">S’applique à : classes, schémas, associations, indications</span><span class="sxs-lookup"><span data-stu-id="94065-431">Applies to: classes, schemas, associations, indications</span></span>

<span data-ttu-id="94065-432">Numéro de version principale de l’objet de schéma.</span><span class="sxs-lookup"><span data-stu-id="94065-432">Major version number of the schema object.</span></span> <span data-ttu-id="94065-433">La valeur par défaut est **null**.</span><span class="sxs-lookup"><span data-stu-id="94065-433">The default is **NULL**.</span></span> <span data-ttu-id="94065-434">Le numéro de version est incrémenté lorsque des modifications sont apportées au schéma qui modifie l’interface.</span><span class="sxs-lookup"><span data-stu-id="94065-434">The version number is incremented when changes are made to the schema that alter the interface.</span></span>

</dd> <dt>

<span data-ttu-id="94065-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Très**</span><span class="sxs-lookup"><span data-stu-id="94065-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Weak**</span></span>
</dt> <dd>

<span data-ttu-id="94065-436">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-436">Data type: **boolean**</span></span>

<span data-ttu-id="94065-437">S’applique à : références</span><span class="sxs-lookup"><span data-stu-id="94065-437">Applies to: references</span></span>

<span data-ttu-id="94065-438">Indique si les clés de la classe référencée incluent les clés des autres participants de l’Association.</span><span class="sxs-lookup"><span data-stu-id="94065-438">Indicates whether the keys of the referenced class include the keys of the other participants in the association.</span></span> <span data-ttu-id="94065-439">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-439">The default is **FALSE**.</span></span>

<span data-ttu-id="94065-440">Ce qualificateur est utilisé lorsque l’identité de la classe référencée dépend de l’identité des autres participants de l’Association.</span><span class="sxs-lookup"><span data-stu-id="94065-440">This qualifier is used when the identity of the referenced class depends on the identity of the other participants in the association.</span></span> <span data-ttu-id="94065-441">Une seule référence à une classe donnée peut être faible.</span><span class="sxs-lookup"><span data-stu-id="94065-441">No more than one reference to any given class can be weak.</span></span> <span data-ttu-id="94065-442">Les autres classes de l’Association doivent définir une clé.</span><span class="sxs-lookup"><span data-stu-id="94065-442">The other classes in the association must define a key.</span></span> <span data-ttu-id="94065-443">Les clés des autres classes de l’Association sont répétées dans la classe référencée et sont marquées avec un qualificateur **propagé** .</span><span class="sxs-lookup"><span data-stu-id="94065-443">The keys of the other classes in the association are repeated in the referenced class and are tagged with a **Propagated** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="94065-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Ecrire**</span><span class="sxs-lookup"><span data-stu-id="94065-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Write**</span></span>
</dt> <dd>

<span data-ttu-id="94065-445">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-445">Data type: **boolean**</span></span>

<span data-ttu-id="94065-446">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="94065-446">Applies to: properties</span></span>

<span data-ttu-id="94065-447">Indique que les applications ou les scripts peuvent modifier la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="94065-447">Indicates that applications or scripts can change the property value.</span></span> <span data-ttu-id="94065-448">Le compte qui exécute l’application doit avoir accès à l’espace de noms qui contient des instances de la classe.</span><span class="sxs-lookup"><span data-stu-id="94065-448">The account that runs the application must have access to the namespace that contains instances of the class.</span></span> <span data-ttu-id="94065-449">L’implémentation du fournisseur peut également limiter l’accès aux données du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="94065-449">The provider implementation may also limit access to provider data.</span></span> <span data-ttu-id="94065-450">La valeur **true** indique que la propriété est lisible et accessible en écriture par les consommateurs qui sont autorisés à accéder à WMI et au fournisseur.</span><span class="sxs-lookup"><span data-stu-id="94065-450">A value of **TRUE** indicates that the property is readable and writeable by consumers that are allowed access by WMI and the provider.</span></span> <span data-ttu-id="94065-451">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-451">The default is **FALSE**.</span></span>

<span data-ttu-id="94065-452">Une propriété qui n’a pas de qualificateur d' **écriture** peut encore être accessible en écriture.</span><span class="sxs-lookup"><span data-stu-id="94065-452">A property that lacks the **Write** qualifier may still be writeable.</span></span> <span data-ttu-id="94065-453">L’implémentation du fournisseur peut autoriser la modification de toutes les propriétés dans les classes de fournisseur, que le qualificateur d' **écriture** soit présent ou non.</span><span class="sxs-lookup"><span data-stu-id="94065-453">The provider implementation may allow any properties in the provider classes to be changed, whether the **Write** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="94065-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**</span><span class="sxs-lookup"><span data-stu-id="94065-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**</span></span>
</dt> <dd>

<span data-ttu-id="94065-455">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-455">Data type: **boolean**</span></span>

<span data-ttu-id="94065-456">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="94065-456">Applies to: properties</span></span>

<span data-ttu-id="94065-457">Indique si la propriété peut être accessible en écriture lors de la création de l’instance.</span><span class="sxs-lookup"><span data-stu-id="94065-457">Indicates whether the property is writeable at instance creation.</span></span> <span data-ttu-id="94065-458">Ce qualificateur peut être utilisé conjointement avec le qualificateur **WriteAtCreate** .</span><span class="sxs-lookup"><span data-stu-id="94065-458">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="94065-459">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-459">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="94065-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**</span><span class="sxs-lookup"><span data-stu-id="94065-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="94065-461">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="94065-461">Data type: **boolean**</span></span>

<span data-ttu-id="94065-462">S’applique à : Properties</span><span class="sxs-lookup"><span data-stu-id="94065-462">Applies to: properties</span></span>

<span data-ttu-id="94065-463">Indique si la propriété est accessible en écriture à la mise à jour de l’instance.</span><span class="sxs-lookup"><span data-stu-id="94065-463">Indicates whether the property is writeable at instance update.</span></span> <span data-ttu-id="94065-464">Ce qualificateur peut être utilisé conjointement avec le qualificateur **WriteAtCreate** .</span><span class="sxs-lookup"><span data-stu-id="94065-464">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="94065-465">La valeur par défaut est **false**.</span><span class="sxs-lookup"><span data-stu-id="94065-465">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="94065-466">Exemples</span><span class="sxs-lookup"><span data-stu-id="94065-466">Examples</span></span>

<span data-ttu-id="94065-467">Pour plus d’informations sur la récupération des qualificateurs, consultez l’exemple de code PowerShell [WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) dans la Galerie technet.</span><span class="sxs-lookup"><span data-stu-id="94065-467">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

## <a name="requirements"></a><span data-ttu-id="94065-468">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94065-468">Requirements</span></span>



| <span data-ttu-id="94065-469">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94065-469">Requirement</span></span> | <span data-ttu-id="94065-470">Valeur</span><span class="sxs-lookup"><span data-stu-id="94065-470">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="94065-471">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94065-471">Minimum supported client</span></span><br/> | <span data-ttu-id="94065-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="94065-472">Windows Vista</span></span><br/>       |
| <span data-ttu-id="94065-473">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94065-473">Minimum supported server</span></span><br/> | <span data-ttu-id="94065-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="94065-474">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94065-475">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94065-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94065-476">Qualificateurs WMI</span><span class="sxs-lookup"><span data-stu-id="94065-476">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="94065-477">Ajout d’un qualificateur</span><span class="sxs-lookup"><span data-stu-id="94065-477">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




