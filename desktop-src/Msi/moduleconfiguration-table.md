---
description: La table ModuleConfiguration identifie les attributs configurables du module. Cette table n’est pas fusionnée dans la base de données.
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: Table ModuleConfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa187c10b5d3376a9bec78eb897b4982445ff01f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203404"
---
# <a name="moduleconfiguration-table"></a><span data-ttu-id="992c2-104">Table ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="992c2-104">ModuleConfiguration Table</span></span>

<span data-ttu-id="992c2-105">La table ModuleConfiguration identifie les attributs configurables du module.</span><span class="sxs-lookup"><span data-stu-id="992c2-105">The ModuleConfiguration table identifies the configurable attributes of the module.</span></span> <span data-ttu-id="992c2-106">Cette table n’est pas fusionnée dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="992c2-106">This table is not merged into the database.</span></span>

<span data-ttu-id="992c2-107">La table ModuleConfiguration contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="992c2-107">The ModuleConfiguration table has the following columns.</span></span>



| <span data-ttu-id="992c2-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="992c2-108">Column</span></span>       | <span data-ttu-id="992c2-109">Type</span><span class="sxs-lookup"><span data-stu-id="992c2-109">Type</span></span>                         | <span data-ttu-id="992c2-110">Clé</span><span class="sxs-lookup"><span data-stu-id="992c2-110">Key</span></span> | <span data-ttu-id="992c2-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="992c2-111">Nullable</span></span> |
|--------------|------------------------------|-----|----------|
| <span data-ttu-id="992c2-112">Nom</span><span class="sxs-lookup"><span data-stu-id="992c2-112">Name</span></span>         | [<span data-ttu-id="992c2-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="992c2-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="992c2-114">O</span><span class="sxs-lookup"><span data-stu-id="992c2-114">Y</span></span>   | <span data-ttu-id="992c2-115">N</span><span class="sxs-lookup"><span data-stu-id="992c2-115">N</span></span>        |
| <span data-ttu-id="992c2-116">Format</span><span class="sxs-lookup"><span data-stu-id="992c2-116">Format</span></span>       | [<span data-ttu-id="992c2-117">Integer</span><span class="sxs-lookup"><span data-stu-id="992c2-117">Integer</span></span>](integer.md)       | <span data-ttu-id="992c2-118">N</span><span class="sxs-lookup"><span data-stu-id="992c2-118">N</span></span>   | <span data-ttu-id="992c2-119">N</span><span class="sxs-lookup"><span data-stu-id="992c2-119">N</span></span>        |
| <span data-ttu-id="992c2-120">Type</span><span class="sxs-lookup"><span data-stu-id="992c2-120">Type</span></span>         | [<span data-ttu-id="992c2-121">Text</span><span class="sxs-lookup"><span data-stu-id="992c2-121">Text</span></span>](text.md)             | <span data-ttu-id="992c2-122">N</span><span class="sxs-lookup"><span data-stu-id="992c2-122">N</span></span>   | <span data-ttu-id="992c2-123">O</span><span class="sxs-lookup"><span data-stu-id="992c2-123">Y</span></span>        |
| <span data-ttu-id="992c2-124">ContextData</span><span class="sxs-lookup"><span data-stu-id="992c2-124">ContextData</span></span>  | [<span data-ttu-id="992c2-125">Text</span><span class="sxs-lookup"><span data-stu-id="992c2-125">Text</span></span>](text.md)             | <span data-ttu-id="992c2-126">N</span><span class="sxs-lookup"><span data-stu-id="992c2-126">N</span></span>   | <span data-ttu-id="992c2-127">O</span><span class="sxs-lookup"><span data-stu-id="992c2-127">Y</span></span>        |
| <span data-ttu-id="992c2-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="992c2-128">DefaultValue</span></span> | [<span data-ttu-id="992c2-129">Text</span><span class="sxs-lookup"><span data-stu-id="992c2-129">Text</span></span>](text.md)             | <span data-ttu-id="992c2-130">N</span><span class="sxs-lookup"><span data-stu-id="992c2-130">N</span></span>   | <span data-ttu-id="992c2-131">O</span><span class="sxs-lookup"><span data-stu-id="992c2-131">Y</span></span>        |
| <span data-ttu-id="992c2-132">Attributs</span><span class="sxs-lookup"><span data-stu-id="992c2-132">Attributes</span></span>   | [<span data-ttu-id="992c2-133">Integer</span><span class="sxs-lookup"><span data-stu-id="992c2-133">Integer</span></span>](integer.md)       | <span data-ttu-id="992c2-134">N</span><span class="sxs-lookup"><span data-stu-id="992c2-134">N</span></span>   | <span data-ttu-id="992c2-135">O</span><span class="sxs-lookup"><span data-stu-id="992c2-135">Y</span></span>        |
| <span data-ttu-id="992c2-136">DisplayName</span><span class="sxs-lookup"><span data-stu-id="992c2-136">DisplayName</span></span>  | [<span data-ttu-id="992c2-137">Text</span><span class="sxs-lookup"><span data-stu-id="992c2-137">Text</span></span>](text.md)             | <span data-ttu-id="992c2-138">N</span><span class="sxs-lookup"><span data-stu-id="992c2-138">N</span></span>   | <span data-ttu-id="992c2-139">O</span><span class="sxs-lookup"><span data-stu-id="992c2-139">Y</span></span>        |
| <span data-ttu-id="992c2-140">Description</span><span class="sxs-lookup"><span data-stu-id="992c2-140">Description</span></span>  | [<span data-ttu-id="992c2-141">Text</span><span class="sxs-lookup"><span data-stu-id="992c2-141">Text</span></span>](text.md)             | <span data-ttu-id="992c2-142">N</span><span class="sxs-lookup"><span data-stu-id="992c2-142">N</span></span>   | <span data-ttu-id="992c2-143">O</span><span class="sxs-lookup"><span data-stu-id="992c2-143">Y</span></span>        |
| <span data-ttu-id="992c2-144">HelpLocation</span><span class="sxs-lookup"><span data-stu-id="992c2-144">HelpLocation</span></span> | [<span data-ttu-id="992c2-145">Text</span><span class="sxs-lookup"><span data-stu-id="992c2-145">Text</span></span>](text.md)             | <span data-ttu-id="992c2-146">N</span><span class="sxs-lookup"><span data-stu-id="992c2-146">N</span></span>   | <span data-ttu-id="992c2-147">O</span><span class="sxs-lookup"><span data-stu-id="992c2-147">Y</span></span>        |
| <span data-ttu-id="992c2-148">HelpKeyword</span><span class="sxs-lookup"><span data-stu-id="992c2-148">HelpKeyword</span></span>  | [<span data-ttu-id="992c2-149">Text</span><span class="sxs-lookup"><span data-stu-id="992c2-149">Text</span></span>](text.md)             | <span data-ttu-id="992c2-150">N</span><span class="sxs-lookup"><span data-stu-id="992c2-150">N</span></span>   | <span data-ttu-id="992c2-151">O</span><span class="sxs-lookup"><span data-stu-id="992c2-151">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="992c2-152">Colonnes</span><span class="sxs-lookup"><span data-stu-id="992c2-152">Columns</span></span>

<dl> <dt>

<span data-ttu-id="992c2-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme</span><span class="sxs-lookup"><span data-stu-id="992c2-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="992c2-154">Ce champ définit le nom de l’élément configurable.</span><span class="sxs-lookup"><span data-stu-id="992c2-154">This field defines the name of the configurable item.</span></span> <span data-ttu-id="992c2-155">Ce nom est référencé dans le modèle de mise en forme dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="992c2-155">This name is referenced in the formatting template in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="992c2-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Format</span><span class="sxs-lookup"><span data-stu-id="992c2-156"><span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Format</span></span>
</dt> <dd>

<span data-ttu-id="992c2-157">Cette colonne spécifie le format des données en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="992c2-157">This column specifies the format of the data being changed.</span></span>



| <span data-ttu-id="992c2-158">Format</span><span class="sxs-lookup"><span data-stu-id="992c2-158">Format</span></span>                                       | <span data-ttu-id="992c2-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="992c2-159">Value</span></span> |
|----------------------------------------------|-------|
| [<span data-ttu-id="992c2-160">Text</span><span class="sxs-lookup"><span data-stu-id="992c2-160">Text</span></span>](text-format-types.md)                | <span data-ttu-id="992c2-161">0</span><span class="sxs-lookup"><span data-stu-id="992c2-161">0</span></span>     |
| [<span data-ttu-id="992c2-162">Clé</span><span class="sxs-lookup"><span data-stu-id="992c2-162">Key</span></span>](key-format-types.md)                  | <span data-ttu-id="992c2-163">1</span><span class="sxs-lookup"><span data-stu-id="992c2-163">1</span></span>     |
| [<span data-ttu-id="992c2-164">Integer</span><span class="sxs-lookup"><span data-stu-id="992c2-164">Integer</span></span>](integer-format-types.md)          | <span data-ttu-id="992c2-165">2</span><span class="sxs-lookup"><span data-stu-id="992c2-165">2</span></span>     |
| [<span data-ttu-id="992c2-166">Format de champ de champ</span><span class="sxs-lookup"><span data-stu-id="992c2-166">Bitfield Format</span></span>](bitfield-format-types.md) | <span data-ttu-id="992c2-167">3</span><span class="sxs-lookup"><span data-stu-id="992c2-167">3</span></span>     |



 

</dd> <dt>

<span data-ttu-id="992c2-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer</span><span class="sxs-lookup"><span data-stu-id="992c2-168"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>Type</span></span>
</dt> <dd>

<span data-ttu-id="992c2-169">Cette colonne spécifie le type des données en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="992c2-169">This column specifies the type for the data being changed.</span></span> <span data-ttu-id="992c2-170">Ce type est utilisé pour fournir un contexte pour toute interface utilisateur et n’est pas utilisé dans le processus de fusion.</span><span class="sxs-lookup"><span data-stu-id="992c2-170">This type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="992c2-171">Les valeurs valides pour cette colonne dépendent de la valeur dans la colonne format.</span><span class="sxs-lookup"><span data-stu-id="992c2-171">The valid values for this column depend on the value in the Format column.</span></span>

</dd> <dt>

<span data-ttu-id="992c2-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData</span><span class="sxs-lookup"><span data-stu-id="992c2-172"><span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData</span></span>
</dt> <dd>

<span data-ttu-id="992c2-173">Cette colonne spécifie un contexte sémantique pour les données demandées.</span><span class="sxs-lookup"><span data-stu-id="992c2-173">This column specifies a semantic context for the requested data.</span></span> <span data-ttu-id="992c2-174">Le type est utilisé pour fournir un contexte pour toute interface utilisateur et n’est pas utilisé dans le processus de fusion.</span><span class="sxs-lookup"><span data-stu-id="992c2-174">The type is used to provide a context for any user-interface and is not used in the merge process.</span></span> <span data-ttu-id="992c2-175">Les valeurs valides pour cette colonne dépendent des valeurs dans les colonnes format et type.</span><span class="sxs-lookup"><span data-stu-id="992c2-175">The valid values for this column depend on the values in the Format and Type columns.</span></span>

</dd> <dt>

<span data-ttu-id="992c2-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue</span><span class="sxs-lookup"><span data-stu-id="992c2-176"><span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue</span></span>
</dt> <dd>

<span data-ttu-id="992c2-177">Cette colonne spécifie une valeur par défaut pour l’élément de cet enregistrement si l’outil de fusion refuse de fournir une valeur.</span><span class="sxs-lookup"><span data-stu-id="992c2-177">This column specifies a default value for the item in this record if the merge tool declines to provide a value.</span></span> <span data-ttu-id="992c2-178">Cette valeur doit avoir le format, le type et le contexte de l’élément.</span><span class="sxs-lookup"><span data-stu-id="992c2-178">This value must have the format, type, and context of the item.</span></span> <span data-ttu-id="992c2-179">S’il s’agit d’un élément de format « clé », la clé étrangère doit être une clé valide dans les tables du module.</span><span class="sxs-lookup"><span data-stu-id="992c2-179">If this is a "Key" format item, the foreign key must be a valid key into the tables of the module.</span></span> <span data-ttu-id="992c2-180">La valeur NULL peut être une valeur valide pour cette colonne en fonction de l’élément.</span><span class="sxs-lookup"><span data-stu-id="992c2-180">Null may be a valid value for this column depending on the item.</span></span> <span data-ttu-id="992c2-181">Pour les éléments de format « clé », cette valeur est au [format spécial CMSM](cmsm-special-format.md).</span><span class="sxs-lookup"><span data-stu-id="992c2-181">For "Key" format items, this value is in [CMSM special format](cmsm-special-format.md).</span></span> <span data-ttu-id="992c2-182">Pour tous les autres types, la valeur est traitée littéralement.</span><span class="sxs-lookup"><span data-stu-id="992c2-182">For all other types, the value is treated literally.</span></span>

<span data-ttu-id="992c2-183">Les auteurs de modules doivent s’assurer que le module est valide dans son état par défaut.</span><span class="sxs-lookup"><span data-stu-id="992c2-183">Module authors must ensure that the module is valid in its default state.</span></span> <span data-ttu-id="992c2-184">Cela permet de s’assurer que les versions de Mergemod.dll antérieures à la version 2,0 peuvent toujours utiliser le module dans son état par défaut.</span><span class="sxs-lookup"><span data-stu-id="992c2-184">This ensures that versions of Mergemod.dll earlier than version 2.0 can still use the module in its default state.</span></span>

</dd> <dt>

<span data-ttu-id="992c2-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs</span><span class="sxs-lookup"><span data-stu-id="992c2-185"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="992c2-186">Cette colonne est un champ de bits contenant des attributs pour cet élément configurable.</span><span class="sxs-lookup"><span data-stu-id="992c2-186">This column is a bit field containing attributes for this configurable item.</span></span> <span data-ttu-id="992c2-187">NULL équivaut à 0.</span><span class="sxs-lookup"><span data-stu-id="992c2-187">Null is equivalent to 0.</span></span> <span data-ttu-id="992c2-188">Tous les autres éléments de cette colonne sont réservés pour une utilisation ultérieure et doivent avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="992c2-188">All other bits in this column are reserved for future use and must be 0.</span></span>



| <span data-ttu-id="992c2-189">Nom</span><span class="sxs-lookup"><span data-stu-id="992c2-189">Name</span></span>                             | <span data-ttu-id="992c2-190">Decimal</span><span class="sxs-lookup"><span data-stu-id="992c2-190">Decimal</span></span> | <span data-ttu-id="992c2-191">Valeur hexadécimale</span><span class="sxs-lookup"><span data-stu-id="992c2-191">Hexadecimal</span></span> | <span data-ttu-id="992c2-192">Description</span><span class="sxs-lookup"><span data-stu-id="992c2-192">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="992c2-193">msmConfigurableOptionKeyNoOrphan</span><span class="sxs-lookup"><span data-stu-id="992c2-193">msmConfigurableOptionKeyNoOrphan</span></span> | <span data-ttu-id="992c2-194">1</span><span class="sxs-lookup"><span data-stu-id="992c2-194">1</span></span>       | <span data-ttu-id="992c2-195">0x00000001</span><span class="sxs-lookup"><span data-stu-id="992c2-195">0x00000001</span></span>  | <span data-ttu-id="992c2-196">Cet attribut s’applique uniquement aux enregistrements qui répertorient une clé étrangère dans une table de module dans leur champ DefaultValue.</span><span class="sxs-lookup"><span data-stu-id="992c2-196">This attribute only applies to records that list a foreign key to a module table in their DefaultValue field.</span></span> <span data-ttu-id="992c2-197">L’outil de fusion ignore l’attribut pour tous les formats autres que les [types de format de clé](key-format-types.md).</span><span class="sxs-lookup"><span data-stu-id="992c2-197">The merge tool ignores the attribute for any formats other than the [Key Format Types](key-format-types.md).</span></span> <span data-ttu-id="992c2-198">Les éléments qui ne sont pas répertoriés dans la [table ModuleSubstitution](modulesubstitution-table.md) sont exclus de la vérification suivante.</span><span class="sxs-lookup"><span data-stu-id="992c2-198">Items not listed in the [ModuleSubstitution table](modulesubstitution-table.md) are excluded from the following check.</span></span> <span data-ttu-id="992c2-199">L’outil de fusion ne fusionne pas la ligne référencée par la colonne DefaultValue dans la base de données cible si les conditions suivantes sont respectées après avoir effectué toutes les options de configuration.</span><span class="sxs-lookup"><span data-stu-id="992c2-199">The merge tool does not merge the row referenced by the DefaultValue column into the target database if the following conditions are satisfied after completing all configuration options.</span></span><br/> <span data-ttu-id="992c2-200">Chaque ligne de la table ModuleConfiguration avec la même valeur DefaultValue a le msmConfigurationItemsKeyNoOrphan défini.</span><span class="sxs-lookup"><span data-stu-id="992c2-200">Every row in the ModuleConfiguration table with the same DefaultValue has the msmConfigurationItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="992c2-201">Aucune ligne n’utilise DefaultValue, car l’outil de création a refusé de fournir une valeur.</span><span class="sxs-lookup"><span data-stu-id="992c2-201">No rows use the DefaultValue because the authoring tool declined to provide a value.</span></span><br/> <span data-ttu-id="992c2-202">L’outil de fusion fusionne la ligne si l’une des conditions suivantes est satisfaite.</span><span class="sxs-lookup"><span data-stu-id="992c2-202">The merge tool merges the row if any of the following conditions are satisfied.</span></span><br/> <span data-ttu-id="992c2-203">L’outil de fusion recherche toutes les lignes qui n’ont pas de msmConfigItemsKeyNoOrphan définie.</span><span class="sxs-lookup"><span data-stu-id="992c2-203">The merge tool finds any row that does not have msmConfigItemsKeyNoOrphan set.</span></span><br/> <span data-ttu-id="992c2-204">Si l’outil de fusion détecte une ligne à l’aide de DefaultValue, car l’outil de création a refusé de fournir une valeur.</span><span class="sxs-lookup"><span data-stu-id="992c2-204">If the merge tool finds any row using DefaultValue because the authoring tool declined to provide a value.</span></span><br/> |
| <span data-ttu-id="992c2-205">msmConfigurableOptionNonNullable</span><span class="sxs-lookup"><span data-stu-id="992c2-205">msmConfigurableOptionNonNullable</span></span> | <span data-ttu-id="992c2-206">2</span><span class="sxs-lookup"><span data-stu-id="992c2-206">2</span></span>       | <span data-ttu-id="992c2-207">0x00000002</span><span class="sxs-lookup"><span data-stu-id="992c2-207">0x00000002</span></span>  | <span data-ttu-id="992c2-208">Lorsque cet attribut est défini, la valeur NULL n’est pas une réponse valide pour cet élément.</span><span class="sxs-lookup"><span data-stu-id="992c2-208">When this attribute is set, null is not a valid response for this item.</span></span> <span data-ttu-id="992c2-209">Cet attribut n’a aucun effet pour les types de [format entier](integer-format-types.md) ou les [types de format de champ](bitfield-format-types.md)de type de champ.</span><span class="sxs-lookup"><span data-stu-id="992c2-209">This attribute has no effect for [Integer Format Types](integer-format-types.md) or [Bitfield Format Types](bitfield-format-types.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="992c2-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>NomComplet</span><span class="sxs-lookup"><span data-stu-id="992c2-210"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>DisplayName</span></span>
</dt> <dd>

<span data-ttu-id="992c2-211">Cette colonne fournit une brève description de cet élément que l’outil de création peut utiliser dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="992c2-211">This column provides a short description of this item that the authoring tool may use in the user interface.</span></span> <span data-ttu-id="992c2-212">Cette colonne ne peut pas être localisée.</span><span class="sxs-lookup"><span data-stu-id="992c2-212">This column may not be localized.</span></span> <span data-ttu-id="992c2-213">Affectez la valeur null à cette colonne pour que le module demande que l’outil de création n’expose pas cette propriété dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="992c2-213">Set this column to null to have the module is request that the authoring tool not expose this property in the UI.</span></span> <span data-ttu-id="992c2-214">L’outil peut ignorer la valeur de ce champ.</span><span class="sxs-lookup"><span data-stu-id="992c2-214">The tool may disregard the value in this field.</span></span>

</dd> <dt>

<span data-ttu-id="992c2-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive</span><span class="sxs-lookup"><span data-stu-id="992c2-215"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="992c2-216">Cette colonne fournit une description de cet élément que l’outil de création peut utiliser dans les éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="992c2-216">This column provides a description of this item that the authoring tool may use in UI elements.</span></span> <span data-ttu-id="992c2-217">Cette chaîne peut être localisée par la transformation de langage du module.</span><span class="sxs-lookup"><span data-stu-id="992c2-217">This string may be localized by the module's language transform.</span></span> <span data-ttu-id="992c2-218">Cette colonne peut être null.</span><span class="sxs-lookup"><span data-stu-id="992c2-218">This column may be null.</span></span>

</dd> <dt>

<span data-ttu-id="992c2-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span><span class="sxs-lookup"><span data-stu-id="992c2-219"><span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation</span></span>
</dt> <dd>

<span data-ttu-id="992c2-220">Cette colonne fournit le nom d’un fichier d’aide (sans l’extension. chm) ou une liste délimitée par des points-virgules des espaces de noms d’aide.</span><span class="sxs-lookup"><span data-stu-id="992c2-220">This column provides either the name of a help file (without the .chm extension) or a semicolon delimited list of help namespaces.</span></span> <span data-ttu-id="992c2-221">Cette colonne peut être null si aucune aide n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="992c2-221">This column can be null if no help is available.</span></span> <span data-ttu-id="992c2-222">Cette colonne peut être NULL uniquement si la colonne HelpKeyword a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="992c2-222">This column can be null only if the HelpKeyword column is null.</span></span>

</dd> <dt>

<span data-ttu-id="992c2-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span><span class="sxs-lookup"><span data-stu-id="992c2-223"><span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword</span></span>
</dt> <dd>

<span data-ttu-id="992c2-224">Cette colonne fournit un mot clé dans le fichier d’aide ou l’espace de noms de la colonne HelpLocation.</span><span class="sxs-lookup"><span data-stu-id="992c2-224">This column provides a keyword into the help file or namespace from the HelpLocation column.</span></span> <span data-ttu-id="992c2-225">L’interprétation de ce mot clé dépend de la colonne HelpLocation.</span><span class="sxs-lookup"><span data-stu-id="992c2-225">The interpretation of this keyword depends on the HelpLocation column.</span></span> <span data-ttu-id="992c2-226">Cette colonne peut être null.</span><span class="sxs-lookup"><span data-stu-id="992c2-226">This column may be null.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="992c2-227">Notes</span><span class="sxs-lookup"><span data-stu-id="992c2-227">Remarks</span></span>

<span data-ttu-id="992c2-228">La table ModuleConfiguration est utilisée par les [modules de fusion configurables](configurable-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="992c2-228">The ModuleConfiguration table is used by [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="992c2-229">Mergemod.dll 2,0 ou version ultérieure est requis pour créer un module de fusion configurable.</span><span class="sxs-lookup"><span data-stu-id="992c2-229">Mergemod.dll 2.0 or later is required to create a configurable merge module.</span></span>

<span data-ttu-id="992c2-230">Pour garantir la compatibilité avec les versions antérieures de Mergemod.dll, la table ModuleConfiguration et la [table ModuleSubstitution](modulesubstitution-table.md) doivent être ajoutées à la [table ModuleIgnoreTable](moduleignoretable-table.md) de chaque module.</span><span class="sxs-lookup"><span data-stu-id="992c2-230">To ensure compatibility with older versions of Mergemod.dll, the ModuleConfiguration table and [ModuleSubstitution table](modulesubstitution-table.md) should be added to the [ModuleIgnoreTable table](moduleignoretable-table.md) of every module.</span></span>

## <a name="validation"></a><span data-ttu-id="992c2-231">Validation</span><span class="sxs-lookup"><span data-stu-id="992c2-231">Validation</span></span>

<dl>

[<span data-ttu-id="992c2-232">ICE03</span><span class="sxs-lookup"><span data-stu-id="992c2-232">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="992c2-233">ICE06</span><span class="sxs-lookup"><span data-stu-id="992c2-233">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="992c2-234">ICE25</span><span class="sxs-lookup"><span data-stu-id="992c2-234">ICE25</span></span>](ice25.md)  
[<span data-ttu-id="992c2-235">ICE45</span><span class="sxs-lookup"><span data-stu-id="992c2-235">ICE45</span></span>](ice45.md)  
</dl>

 

 




