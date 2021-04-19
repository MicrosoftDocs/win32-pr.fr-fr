---
description: Contient une clause de syntaxe qui définit les données et le type de l’objet MIB.
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: Clause de syntaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525721"
---
# <a name="syntax-clause"></a><span data-ttu-id="48e38-103">Clause de syntaxe</span><span class="sxs-lookup"><span data-stu-id="48e38-103">SYNTAX Clause</span></span>

<span data-ttu-id="48e38-104">La macro [de type objet](object-type-macro.md) contient une clause de syntaxe qui définit les données et le type de l’objet MIB.</span><span class="sxs-lookup"><span data-stu-id="48e38-104">The [OBJECT-TYPE](object-type-macro.md) macro contains a SYNTAX clause that defines the data and type for the MIB object.</span></span> <span data-ttu-id="48e38-105">Alors que le fournisseur SNMP observe des règles générales pour le mappage des clauses SYNTAXIQUEs, le fournisseur suit également des règles spécifiques à plusieurs types de données.</span><span class="sxs-lookup"><span data-stu-id="48e38-105">While the SNMP Provider observes general rules for mapping SYNTAX clauses, the provider also follows rules specific to several data types.</span></span>

> [!Note]  
> <span data-ttu-id="48e38-106">Pour plus d’informations sur l’installation du fournisseur, consultez [configuration de l’environnement SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="48e38-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="48e38-107">Les règles de mappage suivantes s’appliquent à tous les types de données décrits dans le tableau ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="48e38-107">The following mapping rules apply to all of the data types described in the table below:</span></span>

-   <span data-ttu-id="48e38-108">La représentation textuelle de la clause syntaxique correspond à la **\_ Convention textuelle** de QUALIFICATEUR de propriété CIM.</span><span class="sxs-lookup"><span data-stu-id="48e38-108">The textual representation of the SYNTAX clause maps to the CIM property qualifier **textual\_convention**.</span></span>
-   <span data-ttu-id="48e38-109">La définition de type nommé dans la clause syntaxique correspond à la syntaxe de l' **objet \_** QUALIFICATEUR de propriété CIM.</span><span class="sxs-lookup"><span data-stu-id="48e38-109">The named type definition in the SYNTAX clause maps to the CIM property qualifier **object\_syntax**.</span></span> <span data-ttu-id="48e38-110">Ce mappage diffère selon le type de données.</span><span class="sxs-lookup"><span data-stu-id="48e38-110">This mapping differs depending on the data type.</span></span> <span data-ttu-id="48e38-111">Pour plus d’informations, consultez les descriptions de mappage.</span><span class="sxs-lookup"><span data-stu-id="48e38-111">For more information, see the mapping descriptions.</span></span>
-   <span data-ttu-id="48e38-112">Le type SNMP utilisé lors de l’encodage des frames de protocole SNMPv1 et SNMPv2C est mappé à l' **encodage** de qualificateur de propriété CIM.</span><span class="sxs-lookup"><span data-stu-id="48e38-112">The SNMP type used when encoding SNMPv1 and SNMPv2C protocol frames maps to the CIM property qualifier **encoding**.</span></span>
-   <span data-ttu-id="48e38-113">Le qualificateur de propriété CIM **CimType** contient la représentation textuelle qui met en forme la valeur de protocole CIM sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="48e38-113">The CIM property qualifier **cimtype** contains the textual representation that formats the underlying CIM protocol value.</span></span>

<span data-ttu-id="48e38-114">Le tableau suivant répertorie les types de données qui ont des règles spécifiques qui régissent le comportement du mappage du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="48e38-114">The following table lists data types that have specific rules that govern the provider mapping behavior.</span></span>



| <span data-ttu-id="48e38-115">Type de données SNMP</span><span class="sxs-lookup"><span data-stu-id="48e38-115">SNMP data type</span></span>                                     | <span data-ttu-id="48e38-116">Description</span><span class="sxs-lookup"><span data-stu-id="48e38-116">Description</span></span>                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48e38-117">Type primitif</span><span class="sxs-lookup"><span data-stu-id="48e38-117">Primitive type</span></span>](#primitive-type)                  | <span data-ttu-id="48e38-118">L’un des types de données de base définis dans la structure des documents SMI (Management Information) RFC 1213 et RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="48e38-118">One of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span>                                                                                                                            |
| [<span data-ttu-id="48e38-119">Convention textuelle</span><span class="sxs-lookup"><span data-stu-id="48e38-119">Textual convention</span></span>](textual-convention-macro.md) | <span data-ttu-id="48e38-120">Définition de type générée par le biais de l’utilisation explicite de la macro de **Convention textuelle** SNMPv2C ou générée par le biais de l’utilisation d’un type nommé.</span><span class="sxs-lookup"><span data-stu-id="48e38-120">Type definition generated through the explicit use of the SNMPv2C **TEXTUAL-CONVENTION** macro or generated through the use of a named type.</span></span> <span data-ttu-id="48e38-121">Une convention textuelle attribue un nom et, dans certains cas, une plage de valeurs à un type de données existant.</span><span class="sxs-lookup"><span data-stu-id="48e38-121">A textual convention assigns a name and, in some cases, a range of values to an existing data type.</span></span> |
| [<span data-ttu-id="48e38-122">Type nommé</span><span class="sxs-lookup"><span data-stu-id="48e38-122">Named type</span></span>](#named-type)                          | <span data-ttu-id="48e38-123">Référence nommée à un type primitif, une convention textuelle ou un type restreint.</span><span class="sxs-lookup"><span data-stu-id="48e38-123">Named reference to a primitive type, textual convention, or constrained type.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="48e38-124">Type restreint</span><span class="sxs-lookup"><span data-stu-id="48e38-124">Constrained type</span></span>](#constrained-type)              | <span data-ttu-id="48e38-125">Type primitif, type nommé ou Convention textuelle qui a été limitée par un mécanisme de sous-typage défini dans les documents SMI RFC 1213 et RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="48e38-125">Primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span>                                                                                      |



 

## <a name="primitive-type"></a><span data-ttu-id="48e38-126">Type primitif</span><span class="sxs-lookup"><span data-stu-id="48e38-126">Primitive Type</span></span>

<span data-ttu-id="48e38-127">Le type primitif est l’un des types de données de base définis dans la structure des documents SMI (Management Information) RFC 1213 et RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="48e38-127">The primitive type is one of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="48e38-128">Les types primitifs SNMP sont mappés à des types définis par CIM.</span><span class="sxs-lookup"><span data-stu-id="48e38-128">SNMP primitive types map to CIM-defined types.</span></span> <span data-ttu-id="48e38-129">Le tableau suivant répertorie le mappage qui se produit lorsque la clause de syntaxe fait explicitement référence à un type primitif pour SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="48e38-129">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv1.</span></span> <span data-ttu-id="48e38-130">La **\_ Convention textuelle**, **l’encodage** et les qualificateurs de la **\_ syntaxe d’objet** sont toujours identiques au type MIB et la valeur par défaut est toujours **null**.</span><span class="sxs-lookup"><span data-stu-id="48e38-130">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="48e38-131">Type MIB</span><span class="sxs-lookup"><span data-stu-id="48e38-131">MIB type</span></span>         | <span data-ttu-id="48e38-132">Type de variante CIM</span><span class="sxs-lookup"><span data-stu-id="48e38-132">CIM variant type</span></span> | <span data-ttu-id="48e38-133">valeur CimType</span><span class="sxs-lookup"><span data-stu-id="48e38-133">cimtype value</span></span> |
|------------------|------------------|---------------|
| <span data-ttu-id="48e38-134">INTEGER</span><span class="sxs-lookup"><span data-stu-id="48e38-134">INTEGER</span></span>          | <span data-ttu-id="48e38-135">VT \_</span><span class="sxs-lookup"><span data-stu-id="48e38-135">VT\_I4</span></span>           | <span data-ttu-id="48e38-136">**sint32**</span><span class="sxs-lookup"><span data-stu-id="48e38-136">**sint32**</span></span>    |
| <span data-ttu-id="48e38-137">OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="48e38-137">OCTETSTRING</span></span>      | <span data-ttu-id="48e38-138">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="48e38-138">VT\_BSTR</span></span>         | <span data-ttu-id="48e38-139">**string**</span><span class="sxs-lookup"><span data-stu-id="48e38-139">**string**</span></span>    |
| <span data-ttu-id="48e38-140">OBJECTIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="48e38-140">OBJECTIDENTIFIER</span></span> | <span data-ttu-id="48e38-141">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="48e38-141">VT\_BSTR</span></span>         | <span data-ttu-id="48e38-142">**string**</span><span class="sxs-lookup"><span data-stu-id="48e38-142">**string**</span></span>    |
| <span data-ttu-id="48e38-143">NULL</span><span class="sxs-lookup"><span data-stu-id="48e38-143">NULL</span></span>             | <span data-ttu-id="48e38-144">VT \_ null</span><span class="sxs-lookup"><span data-stu-id="48e38-144">VT\_NULL</span></span>         | <span data-ttu-id="48e38-145">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="48e38-145">Not supported</span></span> |
| <span data-ttu-id="48e38-146">IpAddress</span><span class="sxs-lookup"><span data-stu-id="48e38-146">IpAddress</span></span>        | <span data-ttu-id="48e38-147">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="48e38-147">VT\_BSTR</span></span>         | <span data-ttu-id="48e38-148">**string**</span><span class="sxs-lookup"><span data-stu-id="48e38-148">**string**</span></span>    |
| <span data-ttu-id="48e38-149">Compteur</span><span class="sxs-lookup"><span data-stu-id="48e38-149">Counter</span></span>          | <span data-ttu-id="48e38-150">VT \_</span><span class="sxs-lookup"><span data-stu-id="48e38-150">VT\_I4</span></span>           | <span data-ttu-id="48e38-151">**uint32**</span><span class="sxs-lookup"><span data-stu-id="48e38-151">**uint32**</span></span>    |
| <span data-ttu-id="48e38-152">Jauge</span><span class="sxs-lookup"><span data-stu-id="48e38-152">Gauge</span></span>            | <span data-ttu-id="48e38-153">VT \_</span><span class="sxs-lookup"><span data-stu-id="48e38-153">VT\_I4</span></span>           | <span data-ttu-id="48e38-154">**uint32**</span><span class="sxs-lookup"><span data-stu-id="48e38-154">**uint32**</span></span>    |
| <span data-ttu-id="48e38-155">Graduations</span><span class="sxs-lookup"><span data-stu-id="48e38-155">TimeTicks</span></span>        | <span data-ttu-id="48e38-156">VT \_</span><span class="sxs-lookup"><span data-stu-id="48e38-156">VT\_I4</span></span>           | <span data-ttu-id="48e38-157">**uint32**</span><span class="sxs-lookup"><span data-stu-id="48e38-157">**uint32**</span></span>    |
| <span data-ttu-id="48e38-158">Opaque</span><span class="sxs-lookup"><span data-stu-id="48e38-158">Opaque</span></span>           | <span data-ttu-id="48e38-159">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="48e38-159">VT\_BSTR</span></span>         | <span data-ttu-id="48e38-160">**string**</span><span class="sxs-lookup"><span data-stu-id="48e38-160">**string**</span></span>    |
| <span data-ttu-id="48e38-161">NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="48e38-161">NetworkAddress</span></span>   | <span data-ttu-id="48e38-162">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="48e38-162">VT\_BSTR</span></span>         | <span data-ttu-id="48e38-163">**string**</span><span class="sxs-lookup"><span data-stu-id="48e38-163">**string**</span></span>    |



 

<span data-ttu-id="48e38-164">Le fournisseur ignore la macro de TYPE objet lorsque la clause de syntaxe fait référence à la **valeur null**, soit explicitement, soit par le biais d’une assignation de type nommée.</span><span class="sxs-lookup"><span data-stu-id="48e38-164">The provider ignores the OBJECT-TYPE macro when the SYNTAX clause refers to **NULL**, either explicitly or through a named type assignment.</span></span> <span data-ttu-id="48e38-165">Le tableau suivant répertorie le mappage qui se produit lorsque la clause de syntaxe fait explicitement référence à un type primitif pour SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="48e38-165">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv2.</span></span> <span data-ttu-id="48e38-166">La **\_ Convention textuelle**, **l’encodage** et les qualificateurs de la **\_ syntaxe d’objet** sont toujours identiques au type MIB et la valeur par défaut est toujours **null**.</span><span class="sxs-lookup"><span data-stu-id="48e38-166">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="48e38-167">Type MIB</span><span class="sxs-lookup"><span data-stu-id="48e38-167">MIB type</span></span>          | <span data-ttu-id="48e38-168">Type de variante CIM</span><span class="sxs-lookup"><span data-stu-id="48e38-168">CIM variant type</span></span> | <span data-ttu-id="48e38-169">valeur CimType</span><span class="sxs-lookup"><span data-stu-id="48e38-169">cimtype value</span></span> |
|-------------------|------------------|---------------|
| <span data-ttu-id="48e38-170">INTEGER</span><span class="sxs-lookup"><span data-stu-id="48e38-170">INTEGER</span></span>           | <span data-ttu-id="48e38-171">VT \_</span><span class="sxs-lookup"><span data-stu-id="48e38-171">VT\_I4</span></span>           | <span data-ttu-id="48e38-172">**sint32**</span><span class="sxs-lookup"><span data-stu-id="48e38-172">**sint32**</span></span>    |
| <span data-ttu-id="48e38-173">CHAÎNE D’OCTETS</span><span class="sxs-lookup"><span data-stu-id="48e38-173">OCTET STRING</span></span>      | <span data-ttu-id="48e38-174">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="48e38-174">VT\_BSTR</span></span>         | <span data-ttu-id="48e38-175">**string**</span><span class="sxs-lookup"><span data-stu-id="48e38-175">**string**</span></span>    |
| <span data-ttu-id="48e38-176">IDENTIFICATEUR D’OBJET</span><span class="sxs-lookup"><span data-stu-id="48e38-176">OBJECT IDENTIFIER</span></span> | <span data-ttu-id="48e38-177">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="48e38-177">VT\_BSTR</span></span>         | <span data-ttu-id="48e38-178">**string**</span><span class="sxs-lookup"><span data-stu-id="48e38-178">**string**</span></span>    |
| <span data-ttu-id="48e38-179">IpAddress</span><span class="sxs-lookup"><span data-stu-id="48e38-179">IpAddress</span></span>         | <span data-ttu-id="48e38-180">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="48e38-180">VT\_BSTR</span></span>         | <span data-ttu-id="48e38-181">**string**</span><span class="sxs-lookup"><span data-stu-id="48e38-181">**string**</span></span>    |
| <span data-ttu-id="48e38-182">Counter32</span><span class="sxs-lookup"><span data-stu-id="48e38-182">Counter32</span></span>         | <span data-ttu-id="48e38-183">VT \_</span><span class="sxs-lookup"><span data-stu-id="48e38-183">VT\_I4</span></span>           | <span data-ttu-id="48e38-184">**uint32**</span><span class="sxs-lookup"><span data-stu-id="48e38-184">**uint32**</span></span>    |
| <span data-ttu-id="48e38-185">Gauge32</span><span class="sxs-lookup"><span data-stu-id="48e38-185">Gauge32</span></span>           | <span data-ttu-id="48e38-186">VT \_</span><span class="sxs-lookup"><span data-stu-id="48e38-186">VT\_I4</span></span>           | <span data-ttu-id="48e38-187">**uint32**</span><span class="sxs-lookup"><span data-stu-id="48e38-187">**uint32**</span></span>    |
| <span data-ttu-id="48e38-188">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="48e38-188">Unsigned32</span></span>        | <span data-ttu-id="48e38-189">VT \_</span><span class="sxs-lookup"><span data-stu-id="48e38-189">VT\_I4</span></span>           | <span data-ttu-id="48e38-190">**uint32**</span><span class="sxs-lookup"><span data-stu-id="48e38-190">**uint32**</span></span>    |
| <span data-ttu-id="48e38-191">Integer32</span><span class="sxs-lookup"><span data-stu-id="48e38-191">Integer32</span></span>         | <span data-ttu-id="48e38-192">VT \_</span><span class="sxs-lookup"><span data-stu-id="48e38-192">VT\_I4</span></span>           | <span data-ttu-id="48e38-193">**sint32**</span><span class="sxs-lookup"><span data-stu-id="48e38-193">**sint32**</span></span>    |
| <span data-ttu-id="48e38-194">Counter64</span><span class="sxs-lookup"><span data-stu-id="48e38-194">Counter64</span></span>         | <span data-ttu-id="48e38-195">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="48e38-195">VT\_BSTR</span></span>         | <span data-ttu-id="48e38-196">**uint64**</span><span class="sxs-lookup"><span data-stu-id="48e38-196">**uint64**</span></span>    |
| <span data-ttu-id="48e38-197">Graduations</span><span class="sxs-lookup"><span data-stu-id="48e38-197">TimeTicks</span></span>         | <span data-ttu-id="48e38-198">VT \_</span><span class="sxs-lookup"><span data-stu-id="48e38-198">VT\_I4</span></span>           | <span data-ttu-id="48e38-199">**uint32**</span><span class="sxs-lookup"><span data-stu-id="48e38-199">**uint32**</span></span>    |
| <span data-ttu-id="48e38-200">Opaque</span><span class="sxs-lookup"><span data-stu-id="48e38-200">Opaque</span></span>            | <span data-ttu-id="48e38-201">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="48e38-201">VT\_BSTR</span></span>         | <span data-ttu-id="48e38-202">**string**</span><span class="sxs-lookup"><span data-stu-id="48e38-202">**string**</span></span>    |



 

## <a name="named-type"></a><span data-ttu-id="48e38-203">Type nommé</span><span class="sxs-lookup"><span data-stu-id="48e38-203">Named Type</span></span>

<span data-ttu-id="48e38-204">Les types nommés SNMP sont mappés à des types définis par CIM.</span><span class="sxs-lookup"><span data-stu-id="48e38-204">SNMP named types map to CIM-defined types.</span></span> <span data-ttu-id="48e38-205">Quand la clause de syntaxe fait référence à un [type primitif](#primitive-type), une [Convention textuelle](textual-convention-macro.md)ou un [type restreint](#constrained-type) via une dérivation d’assignation de type, utilisez ces types pour déterminer quelles procédures de mappage s’appliquent.</span><span class="sxs-lookup"><span data-stu-id="48e38-205">When the SYNTAX clause refers to a [primitive type](#primitive-type), [textual convention](textual-convention-macro.md), or [constrained type](#constrained-type) through a type assignment derivation, use the those types to determine which mapping procedures apply.</span></span>

-   <span data-ttu-id="48e38-206">Si, par dérivation des règles d’assignation de type, vous rencontrez une définition de type avec restriction :</span><span class="sxs-lookup"><span data-stu-id="48e38-206">If, through derivation of the type assignment rules, you encounter a constrained type definition:</span></span>

    -   <span data-ttu-id="48e38-207">Et si, par une dérivation plus poussée, vous rencontrez l’une des conventions textuelles listées dans la [macro de Convention textuelle](textual-convention-macro.md), appliquez les règles de mappage pour les types restreints et les conventions textuelles.</span><span class="sxs-lookup"><span data-stu-id="48e38-207">And if, through further derivation, you encounter one of the textual conventions listed in [TEXTUAL-CONVENTION Macro](textual-convention-macro.md), then apply the mapping rules for constrained types and textual conventions.</span></span>
    -   <span data-ttu-id="48e38-208">Sinon, si vous rencontrez l’un des types primitifs listés dans l’un des tableaux de types primitifs, appliquez les règles de mappage pour les types primitifs et les types confrontés.</span><span class="sxs-lookup"><span data-stu-id="48e38-208">Otherwise, if you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types and constrained types.</span></span>

-   <span data-ttu-id="48e38-209">Si vous rencontrez l’une des conventions textuelles listées dans la [ \_ macro de Convention textuelle](textual-convention-macro.md), appliquez les règles de mappage pour les conventions textuelles.</span><span class="sxs-lookup"><span data-stu-id="48e38-209">If you encounter one of the textual conventions listed in [TEXTUAL\_CONVENTION Macro](textual-convention-macro.md), apply the mapping rules for textual conventions.</span></span>
-   <span data-ttu-id="48e38-210">Si vous rencontrez l’un des types primitifs listés dans une table de types primitifs, appliquez les règles de mappage pour les types primitifs.</span><span class="sxs-lookup"><span data-stu-id="48e38-210">If you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types.</span></span>

> [!Note]  
> <span data-ttu-id="48e38-211">Les classes qui contiennent des types de propriété qui ne sont pas conformes au mappage décrit ci-dessus ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="48e38-211">Classes containing property types that do not conform to the mapping described above are not valid.</span></span> <span data-ttu-id="48e38-212">Dans ce cas, le fournisseur retourne une erreur si et quand le fournisseur demande la récupération d’une définition de classe lors de l’exécution d’une fonction de récupération d’instance.</span><span class="sxs-lookup"><span data-stu-id="48e38-212">In this case, the provider returns an error if and when the provider requests the retrieval of a class definition while executing an instance retrieval function.</span></span>

 

## <a name="constrained-type"></a><span data-ttu-id="48e38-213">Type restreint</span><span class="sxs-lookup"><span data-stu-id="48e38-213">Constrained Type</span></span>

<span data-ttu-id="48e38-214">Un type restreint est un type primitif, un type nommé ou une convention textuelle qui a été limitée par un mécanisme de sous-typage défini dans les documents SMI RFC 1213 et RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="48e38-214">A constrained type is a primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="48e38-215">Quand un sous-typage se produit, des qualificateurs CIM supplémentaires sont requis pour spécifier les valeurs de sous-type.</span><span class="sxs-lookup"><span data-stu-id="48e38-215">When subtyping occurs, additional CIM qualifiers are required to specify the subtype values.</span></span> <span data-ttu-id="48e38-216">La définition de type nommé dans la clause de syntaxe mappe textuellement à la syntaxe d' **objet \_** QUALIFICATEUR de propriété CIM jusqu’à, mais n’inclut pas les contraintes du sous-type.</span><span class="sxs-lookup"><span data-stu-id="48e38-216">The named-type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax** up to, but not including the constraints of the subtype.</span></span>

<span data-ttu-id="48e38-217">Les sous-types peuvent respecter l’un des formats suivants :</span><span class="sxs-lookup"><span data-stu-id="48e38-217">Subtypes may follow any of the following formats:</span></span>

-   <span data-ttu-id="48e38-218">ENTIER énuméré</span><span class="sxs-lookup"><span data-stu-id="48e38-218">Enumerated INTEGER</span></span>

    <span data-ttu-id="48e38-219">L' **énumération** du qualificateur de propriété CIM spécifie les valeurs énumérées.</span><span class="sxs-lookup"><span data-stu-id="48e38-219">The CIM property qualifier **enumeration** specifies the enumerated values.</span></span> <span data-ttu-id="48e38-220">Ce qualificateur est représenté sous la forme d’une chaîne contenant une liste séparée par des virgules de valeurs entières 32 bits signées.</span><span class="sxs-lookup"><span data-stu-id="48e38-220">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="48e38-221">Le tableau suivant répertorie les types de mappages.</span><span class="sxs-lookup"><span data-stu-id="48e38-221">The following table lists the mapping types.</span></span> <span data-ttu-id="48e38-222">La valeur par défaut est toujours **null**.</span><span class="sxs-lookup"><span data-stu-id="48e38-222">The default value is always **NULL**.</span></span>



| <span data-ttu-id="48e38-223">Type MIB avec restriction</span><span class="sxs-lookup"><span data-stu-id="48e38-223">Constrained MIB type</span></span> | <span data-ttu-id="48e38-224">Type de variante CIM</span><span class="sxs-lookup"><span data-stu-id="48e38-224">CIM variant type</span></span> | <span data-ttu-id="48e38-225">Qualificateurs CIM</span><span class="sxs-lookup"><span data-stu-id="48e38-225">CIM qualifiers</span></span>                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48e38-226">ENTIER énuméré</span><span class="sxs-lookup"><span data-stu-id="48e38-226">Enumerated INTEGER</span></span>   | <span data-ttu-id="48e38-227">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="48e38-227">VT\_BSTR</span></span>         | <span data-ttu-id="48e38-228">**\_ Convention textuelle**: enumeratedinteger</span><span class="sxs-lookup"><span data-stu-id="48e38-228">**textual\_convention**: enumeratedinteger</span></span><br/> <span data-ttu-id="48e38-229">**encodage**: entier</span><span class="sxs-lookup"><span data-stu-id="48e38-229">**encoding**: INTEGER</span></span><br/> <span data-ttu-id="48e38-230">**CimType**: chaîne</span><span class="sxs-lookup"><span data-stu-id="48e38-230">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="48e38-231">BITS</span><span class="sxs-lookup"><span data-stu-id="48e38-231">BITS</span></span>

    <span data-ttu-id="48e38-232">Les **bits** de qualificateur de propriété CIM spécifient les valeurs énumérées.</span><span class="sxs-lookup"><span data-stu-id="48e38-232">The CIM property qualifier **bits** specifies the enumerated values.</span></span> <span data-ttu-id="48e38-233">Ce qualificateur est représenté sous la forme d’une chaîne contenant une liste séparée par des virgules de valeurs entières 32 bits signées.</span><span class="sxs-lookup"><span data-stu-id="48e38-233">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="48e38-234">Le tableau suivant répertorie les types de mappages.</span><span class="sxs-lookup"><span data-stu-id="48e38-234">The following table lists the mapping types.</span></span> <span data-ttu-id="48e38-235">La valeur par défaut est toujours **null**.</span><span class="sxs-lookup"><span data-stu-id="48e38-235">The default value is always **NULL**.</span></span>



| <span data-ttu-id="48e38-236">Type MIB avec restriction</span><span class="sxs-lookup"><span data-stu-id="48e38-236">Constrained MIB type</span></span> | <span data-ttu-id="48e38-237">Type de variante CIM</span><span class="sxs-lookup"><span data-stu-id="48e38-237">CIM variant type</span></span>      | <span data-ttu-id="48e38-238">Qualificateurs CIM</span><span class="sxs-lookup"><span data-stu-id="48e38-238">CIM qualifiers</span></span>                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48e38-239">BITS</span><span class="sxs-lookup"><span data-stu-id="48e38-239">BITS</span></span>                 | <span data-ttu-id="48e38-240">matrice VT de \_ matrice VT \| \_</span><span class="sxs-lookup"><span data-stu-id="48e38-240">VT\_ARRAY \| VT\_BSTR</span></span> | <span data-ttu-id="48e38-241">**\_ Convention textuelle**: bits</span><span class="sxs-lookup"><span data-stu-id="48e38-241">**textual\_convention**: bits</span></span><br/> <span data-ttu-id="48e38-242">**encodage**: OCTETSTRING</span><span class="sxs-lookup"><span data-stu-id="48e38-242">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="48e38-243">**CimType**: chaîne</span><span class="sxs-lookup"><span data-stu-id="48e38-243">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="48e38-244">Longueur variable</span><span class="sxs-lookup"><span data-stu-id="48e38-244">Variable-length</span></span>

    <span data-ttu-id="48e38-245">Quand la clause de syntaxe fait référence à un type primitif, à un type nommé ou à une convention textuelle qui est sous-typée sous la forme d’une chaîne d’OCTET de longueur variable ou opaque, la **\_ longueur variable** de QUALIFICATEUR de propriété CIM spécifie les valeurs minimales, maximales et de longueur fixe associées à la définition de type.</span><span class="sxs-lookup"><span data-stu-id="48e38-245">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a variable-length OCTET STRING or Opaque, the CIM property qualifier **variable\_length** specifies the minimum, maximum, and fixed-length values associated with the type definition.</span></span> <span data-ttu-id="48e38-246">Ce qualificateur est implémenté sous forme de chaîne au format suivant, où les valeurs de longueur variable sont représentées par des entiers non signés 32 bits.</span><span class="sxs-lookup"><span data-stu-id="48e38-246">This qualifier is implemented as a string in the following format where the variable-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   <span data-ttu-id="48e38-247">Longueur fixe</span><span class="sxs-lookup"><span data-stu-id="48e38-247">Fixed-length</span></span>

    <span data-ttu-id="48e38-248">Quand la clause de syntaxe fait référence à un type primitif, à un type nommé ou à une convention textuelle qui est sous-typée sous la forme d’une chaîne d’OCTET de longueur fixe ou opaque, la **\_ longueur fixe** du QUALIFICATEUR de propriété CIM spécifie la valeur de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="48e38-248">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a fixed-length OCTET STRING or Opaque, the CIM property qualifier **fixed\_length** specifies the fixed-length value.</span></span> <span data-ttu-id="48e38-249">Ce qualificateur est représenté sous la forme d’une valeur entière non signée 32 bits.</span><span class="sxs-lookup"><span data-stu-id="48e38-249">This qualifier is represented as an unsigned 32-bit integer value.</span></span>

-   <span data-ttu-id="48e38-250">Plage</span><span class="sxs-lookup"><span data-stu-id="48e38-250">Range</span></span>

    <span data-ttu-id="48e38-251">Quand la clause de syntaxe fait référence à un type primitif, à un type nommé ou à une convention textuelle qui est sous-typée comme un entier ou une jauge de valeur fixe ou de plage, la **\_ valeur de variable** de QUALIFICATEUR de propriété CIM spécifie les valeurs comprises dans la plage et fixes associées à la définition de type.</span><span class="sxs-lookup"><span data-stu-id="48e38-251">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a ranged or fixed-value INTEGER or Gauge, the CIM property qualifier **variable\_value** specifies the ranged and fixed values associated with the type definition.</span></span> <span data-ttu-id="48e38-252">Ce qualificateur est implémenté sous forme de chaîne au format suivant, où les valeurs de longueur fixe et de plage sont représentées sous la forme d’entiers non signés 32 bits.</span><span class="sxs-lookup"><span data-stu-id="48e38-252">This qualifier is implemented as a string in the following format where the range and fixed-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a><span data-ttu-id="48e38-253">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="48e38-253">Example Code</span></span>

<span data-ttu-id="48e38-254">L’exemple suivant décrit un sous-type d’entier énuméré.</span><span class="sxs-lookup"><span data-stu-id="48e38-254">The following example describes an enumerated INTEGER subtype.</span></span>

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

<span data-ttu-id="48e38-255">Cet exemple est mappé à :</span><span class="sxs-lookup"><span data-stu-id="48e38-255">This example maps to:</span></span>

``` syntax
enumeration("up(1),down(2),testing(3)")
```

<span data-ttu-id="48e38-256">L’exemple de code suivant décrit un sous-type BITS.</span><span class="sxs-lookup"><span data-stu-id="48e38-256">The following code example describes a BITS subtype.</span></span>

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

<span data-ttu-id="48e38-257">L’exemple de code suivant est mappé à :</span><span class="sxs-lookup"><span data-stu-id="48e38-257">The following code example maps to:</span></span>

``` syntax
bits("up(1),down(2),testing(3)")
```

<span data-ttu-id="48e38-258">L’exemple de code suivant décrit un sous-type de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="48e38-258">The following code example describes a variable-length subtype.</span></span>

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

<span data-ttu-id="48e38-259">Cet exemple est mappé à :</span><span class="sxs-lookup"><span data-stu-id="48e38-259">This example maps to:</span></span>

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

<span data-ttu-id="48e38-260">L’exemple suivant décrit un sous-type de longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="48e38-260">The following example describes a fixed-length subtype.</span></span>

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

<span data-ttu-id="48e38-261">Cet exemple est mappé à :</span><span class="sxs-lookup"><span data-stu-id="48e38-261">This example maps to:</span></span>

``` syntax
fixed_length(6)
```

<span data-ttu-id="48e38-262">L’exemple suivant décrit un sous-type de plage.</span><span class="sxs-lookup"><span data-stu-id="48e38-262">The following example describes a range subtype.</span></span>

``` syntax
Status := INTEGER (10..20|8)
```

<span data-ttu-id="48e38-263">Cet exemple est mappé à :</span><span class="sxs-lookup"><span data-stu-id="48e38-263">This example maps to:</span></span>

``` syntax
variable_value("10..20,8")
```

 

 




