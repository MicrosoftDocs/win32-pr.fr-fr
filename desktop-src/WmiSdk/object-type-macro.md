---
description: La macro de TYPE objet contient des clauses obligatoires et facultatives qui décrivent les caractéristiques de base d’un objet MIB. Le fournisseur SNMP convertit une MIB en parties correspondantes de la macro de TYPE objet.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: Macro de TYPE objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111962"
---
# <a name="object-type-macro"></a><span data-ttu-id="ad04b-104">Macro de TYPE objet</span><span class="sxs-lookup"><span data-stu-id="ad04b-104">OBJECT-TYPE Macro</span></span>

<span data-ttu-id="ad04b-105">La macro de TYPE objet contient des clauses obligatoires et facultatives qui décrivent les caractéristiques de base d’un objet MIB.</span><span class="sxs-lookup"><span data-stu-id="ad04b-105">The OBJECT-TYPE macro contains mandatory and optional clauses that describe the basic characteristics of a MIB object.</span></span> <span data-ttu-id="ad04b-106">Le fournisseur SNMP convertit une MIB en parties correspondantes de la macro de TYPE objet.</span><span class="sxs-lookup"><span data-stu-id="ad04b-106">The SNMP Provider converts an MIB to the corresponding parts of the OBJECT-TYPE macro.</span></span>

> [!Note]  
> <span data-ttu-id="ad04b-107">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ad04b-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="ad04b-108">Composants</span><span class="sxs-lookup"><span data-stu-id="ad04b-108">Components</span></span>

<dl> <dt>

<span data-ttu-id="ad04b-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>Objet MIB</span><span class="sxs-lookup"><span data-stu-id="ad04b-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB object</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-110">Objet qui contient la plupart des données en question.</span><span class="sxs-lookup"><span data-stu-id="ad04b-110">Object that contains most of the data in question.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descripteur d’objet</span><span class="sxs-lookup"><span data-stu-id="ad04b-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-112">Nom unique ou descripteur d’objet identifiant chaque objet MIB.</span><span class="sxs-lookup"><span data-stu-id="ad04b-112">Unique name or object descriptor identifying each MIB object.</span></span> <span data-ttu-id="ad04b-113">Chaque descripteur d’objet MIB correspond exactement à un nom de propriété CIM.</span><span class="sxs-lookup"><span data-stu-id="ad04b-113">Each MIB object descriptor maps exactly to a CIM property name.</span></span> <span data-ttu-id="ad04b-114">Par exemple, **ifIndex** se traduit par **ifIndex**.</span><span class="sxs-lookup"><span data-stu-id="ad04b-114">For example, **ifIndex** translates to **ifIndex**.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[Clause de syntaxe](syntax-clause.md)</span><span class="sxs-lookup"><span data-stu-id="ad04b-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[SYNTAX Clause](syntax-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-116">Définit les données et le type d’un objet MIB.</span><span class="sxs-lookup"><span data-stu-id="ad04b-116">Defines the data and type of an MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX (clause)](index-clause.md)</span><span class="sxs-lookup"><span data-stu-id="ad04b-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX clause](index-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-118">Définit une clé pour la sélection d’une ligne de table unique.</span><span class="sxs-lookup"><span data-stu-id="ad04b-118">Defines a key for selecting a unique table row.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>Clauses d’augmentation</span><span class="sxs-lookup"><span data-stu-id="ad04b-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>AUGMENTS clause</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-120">Indique que la collection de tables qu’elle spécifie peut être considérée comme une extension d’une autre collection de tables et peut remplacer la clause INDEX dans SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="ad04b-120">Indicates that the table collection it specifies can be considered an extension of another table collection, and can replace the INDEX clause in SNMPv2.</span></span> <span data-ttu-id="ad04b-121">Les collections référencées par la clause d’AUGMENTATIONs peuvent être combinées avec l’autre collection de tables pour former une seule collection.</span><span class="sxs-lookup"><span data-stu-id="ad04b-121">The collections referred to by the AUGMENTS clause can be combined with the other table collection to form one collection.</span></span> <span data-ttu-id="ad04b-122">La collection résultante partage les propriétés de clé primaire spécifiées dans la dernière collection de tables de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="ad04b-122">The resulting collection shares the primary key properties specified in the last table collection in the chain.</span></span>

<span data-ttu-id="ad04b-123">Dans ce cas, les règles de mappage précédentes spécifiées pour la clause INDEX sont appliquées à la dernière collection de tables de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="ad04b-123">In this case, the previous mapping rules specified for the INDEX clause are applied to the last table collection in the chain.</span></span> <span data-ttu-id="ad04b-124">La collection d’objets est ensuite mappée à une définition de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="ad04b-124">The collection of objects then maps to one CIM class definition.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>Clause de l’identificateur d’objet</span><span class="sxs-lookup"><span data-stu-id="ad04b-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>OBJECT-IDENTIFIER clause</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-126">Contient un identificateur d’objet unique pour un objet MIB.</span><span class="sxs-lookup"><span data-stu-id="ad04b-126">Contains a unique object identifier for an MIB object.</span></span> <span data-ttu-id="ad04b-127">Cet identificateur d’objet est mappé à l' **\_ identificateur d’objet** du QUALIFICATEUR de propriété CIM.</span><span class="sxs-lookup"><span data-stu-id="ad04b-127">This object identifier maps to the CIM property qualifier **object\_identifier**.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Clauses Access et MAX-ACCESS](access-and-max-access-clauses.md)</span><span class="sxs-lookup"><span data-stu-id="ad04b-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[ACCESS and MAX-ACCESS Clauses](access-and-max-access-clauses.md)</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-129">Définissez les droits d’accès à l’objet MIB.</span><span class="sxs-lookup"><span data-stu-id="ad04b-129">Define the access rights to the MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION (clause)</span><span class="sxs-lookup"><span data-stu-id="ad04b-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-131">Fournit une description textuelle de l’objet, qui correspond à la **Description** du qualificateur de propriété CIM.</span><span class="sxs-lookup"><span data-stu-id="ad04b-131">Provides a text description of the object, which maps to the CIM property qualifier **Description**.</span></span> <span data-ttu-id="ad04b-132">Cette clause peut être vide.</span><span class="sxs-lookup"><span data-stu-id="ad04b-132">This clause may be empty.</span></span>

<span data-ttu-id="ad04b-133">Chaque objet **table** et **entrée** d’une définition de table SNMP contient également une clause Description, qui peut également être vide.</span><span class="sxs-lookup"><span data-stu-id="ad04b-133">Each **TABLE** and **ENTRY** object in an SNMP table definition also contains a DESCRIPTION clause, which also may be empty.</span></span> <span data-ttu-id="ad04b-134">Les clauses de TABLE et de DESCRIPTION d’entrée sont concaténées et le résultat est mappé à la **Description** du qualificateur de classe CIM.</span><span class="sxs-lookup"><span data-stu-id="ad04b-134">The TABLE and ENTRY DESCRIPTION clauses are concatenated and the result maps to the CIM class qualifier **Description**.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Clause STATUs</span><span class="sxs-lookup"><span data-stu-id="ad04b-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-136">Indique si l’objet doit être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ad04b-136">Indicates whether the object must be supported.</span></span> <span data-ttu-id="ad04b-137">Lorsque la valeur de la clause STATUs est **obsolète**, le fournisseur ignore l’objet MIB du mappage.</span><span class="sxs-lookup"><span data-stu-id="ad04b-137">When the value of the STATUS clause is **obsolete**, the provider discards the MIB object from the mapping.</span></span> <span data-ttu-id="ad04b-138">Dans le cas contraire, la clause STATUs correspond à l' **État** de qualificateur de propriété CIM.</span><span class="sxs-lookup"><span data-stu-id="ad04b-138">Otherwise, the STATUS clause maps to the CIM property qualifier **Status**.</span></span>

<span data-ttu-id="ad04b-139">Pour SNMPv1, la valeur par défaut de l' **État** est **obligatoire** ou **facultative**, mais le qualificateur peut contenir une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="ad04b-139">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="ad04b-140">Pour SNMPv2C, la valeur par défaut de l' **État** est **en cours** ou **déconseillée**, mais le qualificateur peut contenir une autre valeur.</span><span class="sxs-lookup"><span data-stu-id="ad04b-140">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL, clause</span><span class="sxs-lookup"><span data-stu-id="ad04b-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL clause</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-142">Affecte une valeur par défaut à une variable dans une ligne de table logique et mappe à la chaîne de qualificateur de propriété CIM **defval**.</span><span class="sxs-lookup"><span data-stu-id="ad04b-142">Assigns a default value to a variable in a logical table row, and maps to the string CIM property qualifier **Defval**.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>RÉFÉRENCE (clause)</span><span class="sxs-lookup"><span data-stu-id="ad04b-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-144">Fait référence à un autre document qui contient plus d’informations sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="ad04b-144">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="ad04b-145">Cette clause est mappée à la **référence** de qualificateur de propriété CIM, qui est de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="ad04b-145">This clause maps to the CIM property qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="ad04b-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>UNITs, clause</span><span class="sxs-lookup"><span data-stu-id="ad04b-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>UNITS clause</span></span>
</dt> <dd>

<span data-ttu-id="ad04b-147">Fournit une définition précise de ce que l’objet représente.</span><span class="sxs-lookup"><span data-stu-id="ad04b-147">Provides a precise definition of what the object represents.</span></span> <span data-ttu-id="ad04b-148">Cette clause mappe aux **unités** de qualificateur de propriété CIM, qui est de type chaîne.</span><span class="sxs-lookup"><span data-stu-id="ad04b-148">This clause maps to the CIM property qualifier **Units**, which is of type string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad04b-149">Notes</span><span class="sxs-lookup"><span data-stu-id="ad04b-149">Remarks</span></span>

<span data-ttu-id="ad04b-150">La macro de TYPE objet décrit les caractéristiques de base d’un objet MIB individuel.</span><span class="sxs-lookup"><span data-stu-id="ad04b-150">The OBJECT-TYPE macro describes the basic characteristics of an individual MIB object.</span></span> <span data-ttu-id="ad04b-151">Un ensemble de macros de TYPE objet peut être considéré comme un groupe d’objets connexes.</span><span class="sxs-lookup"><span data-stu-id="ad04b-151">A set of OBJECT-TYPE macros can be considered as a group of related objects.</span></span> <span data-ttu-id="ad04b-152">Dans SNMPv2C, utilisez la macro de groupe d’objets pour regrouper de manière formelle des ensembles d’objets connexes dans une collection.</span><span class="sxs-lookup"><span data-stu-id="ad04b-152">In SNMPv2C, use the OBJECT-GROUP macro to formally group sets of related objects into a collection.</span></span> <span data-ttu-id="ad04b-153">Toutefois, il n’existe aucun mécanisme formel pour créer des collections dans SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="ad04b-153">However, there is no formal mechanism for creating collections in SNMPv1.</span></span> <span data-ttu-id="ad04b-154">Dans le cadre du fournisseur SNMP, la macro de groupe d’objets est ignorée, mais vous pouvez inventer des relations et fabriquer des collections.</span><span class="sxs-lookup"><span data-stu-id="ad04b-154">For the purposes of the SNMP Provider, the OBJECT-GROUP macro is ignored, but you can invent grouping relationships and fabricate collections.</span></span>

 

 



