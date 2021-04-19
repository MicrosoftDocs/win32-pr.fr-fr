---
description: Décrit les erreurs du fournisseur SNMP WMI 1001 à 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Erreurs 1001 à 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa10b83c660d617bdbf37b6f119e824bbba60616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521229"
---
# <a name="errors-1001-through-1010"></a><span data-ttu-id="d8c6e-103">Erreurs 1001 à 1010</span><span class="sxs-lookup"><span data-stu-id="d8c6e-103">Errors 1001 through 1010</span></span>

<span data-ttu-id="d8c6e-104">Décrit les erreurs du fournisseur SNMP WMI 1001 à 1010.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-104">Describes WMI SNMP provider errors 1001 through 1010.</span></span>

[<span data-ttu-id="d8c6e-105">Erreur irrécupérable 1001</span><span class="sxs-lookup"><span data-stu-id="d8c6e-105">Fatal Error 1001</span></span>](#fatal-error-1001)

[<span data-ttu-id="d8c6e-106">Erreur irrécupérable 1002</span><span class="sxs-lookup"><span data-stu-id="d8c6e-106">Fatal Error 1002</span></span>](#fatal-error-1002)

[<span data-ttu-id="d8c6e-107">Erreur irrécupérable 1003</span><span class="sxs-lookup"><span data-stu-id="d8c6e-107">Fatal Error 1003</span></span>](#fatal-error-1003)

[<span data-ttu-id="d8c6e-108">AVERTISSEMENT 1004</span><span class="sxs-lookup"><span data-stu-id="d8c6e-108">Warning 1004</span></span>](#warning-1004)

[<span data-ttu-id="d8c6e-109">AVERTISSEMENT 1005</span><span class="sxs-lookup"><span data-stu-id="d8c6e-109">Warning 1005</span></span>](#warning-1005)

[<span data-ttu-id="d8c6e-110">Erreur irrécupérable 1006</span><span class="sxs-lookup"><span data-stu-id="d8c6e-110">Fatal Error 1006</span></span>](#fatal-error-1006)

[<span data-ttu-id="d8c6e-111">Erreur irrécupérable 1008</span><span class="sxs-lookup"><span data-stu-id="d8c6e-111">Fatal Error 1008</span></span>](#fatal-error-1008)

## <a name="fatal-error-1001"></a><span data-ttu-id="d8c6e-112">Erreur irrécupérable 1001</span><span class="sxs-lookup"><span data-stu-id="d8c6e-112">Fatal Error 1001</span></span>

<dl> <dt>

<span data-ttu-id="d8c6e-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001,> irrécupérable : " <fileName> : <line \#> : la clause Syntax d’Object-type n’est pas résolue en types autorisés"</span><span class="sxs-lookup"><span data-stu-id="d8c6e-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, Fatal>: "<fileName>:<line\#>: SYNTAX clause of OBJECT-TYPE does not resolve to allowed types"</span></span>
</dt> <dd>

<span data-ttu-id="d8c6e-114">Erreur sémantique du module d’appel de macro de TYPE objet.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-114">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="d8c6e-115">La clause de syntaxe de la macro de TYPE objet doit être résolue en un type ou un sous-type, formé à l’aide de la spécification de taille ou de plage autorisée par le SMI ou SNMPv2C SMI.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-115">The SYNTAX clause of the OBJECT-TYPE macro must resolve to a type or subtype, formed by using the SIZE or range specification that the SNMPv1 or SNMPv2C SMI allows.</span></span> <span data-ttu-id="d8c6e-116">Si ce n’est pas le cas, l’erreur irrécupérable 1001 est signalée.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-116">If this is not the case, fatal error 1001 is reported.</span></span>

<span data-ttu-id="d8c6e-117">Cette erreur peut se produire lors de la compilation d’un MIB ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-117">This error can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

<span data-ttu-id="d8c6e-118">Les types autorisés par l’SMI SNMPv1 sont :</span><span class="sxs-lookup"><span data-stu-id="d8c6e-118">Types allowed by the SNMPv1 SMI are:</span></span>

-   <span data-ttu-id="d8c6e-119">INTEGER</span><span class="sxs-lookup"><span data-stu-id="d8c6e-119">INTEGER</span></span>
-   <span data-ttu-id="d8c6e-120">NULL</span><span class="sxs-lookup"><span data-stu-id="d8c6e-120">NULL</span></span>
-   <span data-ttu-id="d8c6e-121">CHAÎNE D’OCTETS</span><span class="sxs-lookup"><span data-stu-id="d8c6e-121">OCTET STRING</span></span>
-   <span data-ttu-id="d8c6e-122">IDENTIFICATEUR D’OBJET</span><span class="sxs-lookup"><span data-stu-id="d8c6e-122">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="d8c6e-123">NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="d8c6e-123">NetworkAddress</span></span>
-   <span data-ttu-id="d8c6e-124">IpAddress</span><span class="sxs-lookup"><span data-stu-id="d8c6e-124">IpAddress</span></span>
-   <span data-ttu-id="d8c6e-125">Compteur</span><span class="sxs-lookup"><span data-stu-id="d8c6e-125">Counter</span></span>
-   <span data-ttu-id="d8c6e-126">Jauge</span><span class="sxs-lookup"><span data-stu-id="d8c6e-126">Gauge</span></span>
-   <span data-ttu-id="d8c6e-127">Graduations</span><span class="sxs-lookup"><span data-stu-id="d8c6e-127">TimeTicks</span></span>
-   <span data-ttu-id="d8c6e-128">Opaque</span><span class="sxs-lookup"><span data-stu-id="d8c6e-128">Opaque</span></span>
-   <span data-ttu-id="d8c6e-129">DisplayString</span><span class="sxs-lookup"><span data-stu-id="d8c6e-129">DisplayString</span></span>
-   <span data-ttu-id="d8c6e-130">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="d8c6e-130">PhysAddress</span></span>

<span data-ttu-id="d8c6e-131">Les types autorisés par l’SMI SNMPv2C sont :</span><span class="sxs-lookup"><span data-stu-id="d8c6e-131">Types allowed by the SNMPv2C SMI are:</span></span>

-   <span data-ttu-id="d8c6e-132">INTEGER</span><span class="sxs-lookup"><span data-stu-id="d8c6e-132">INTEGER</span></span>
-   <span data-ttu-id="d8c6e-133">CHAÎNE D’OCTETS</span><span class="sxs-lookup"><span data-stu-id="d8c6e-133">OCTET STRING</span></span>
-   <span data-ttu-id="d8c6e-134">IDENTIFICATEUR D’OBJET</span><span class="sxs-lookup"><span data-stu-id="d8c6e-134">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="d8c6e-135">BITS</span><span class="sxs-lookup"><span data-stu-id="d8c6e-135">BITS</span></span>
-   <span data-ttu-id="d8c6e-136">Integer32</span><span class="sxs-lookup"><span data-stu-id="d8c6e-136">Integer32</span></span>
-   <span data-ttu-id="d8c6e-137">IpAddress</span><span class="sxs-lookup"><span data-stu-id="d8c6e-137">IpAddress</span></span>
-   <span data-ttu-id="d8c6e-138">Counter32</span><span class="sxs-lookup"><span data-stu-id="d8c6e-138">Counter32</span></span>
-   <span data-ttu-id="d8c6e-139">Graduations</span><span class="sxs-lookup"><span data-stu-id="d8c6e-139">TimeTicks</span></span>
-   <span data-ttu-id="d8c6e-140">Opaque</span><span class="sxs-lookup"><span data-stu-id="d8c6e-140">Opaque</span></span>
-   <span data-ttu-id="d8c6e-141">Counter64</span><span class="sxs-lookup"><span data-stu-id="d8c6e-141">Counter64</span></span>
-   <span data-ttu-id="d8c6e-142">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="d8c6e-142">Unsigned32</span></span>
-   <span data-ttu-id="d8c6e-143">DisplayString</span><span class="sxs-lookup"><span data-stu-id="d8c6e-143">DisplayString</span></span>
-   <span data-ttu-id="d8c6e-144">PhysAddress</span><span class="sxs-lookup"><span data-stu-id="d8c6e-144">PhysAddress</span></span>
-   <span data-ttu-id="d8c6e-145">MacAddress</span><span class="sxs-lookup"><span data-stu-id="d8c6e-145">MacAddress</span></span>
-   <span data-ttu-id="d8c6e-146">TruthValue</span><span class="sxs-lookup"><span data-stu-id="d8c6e-146">TruthValue</span></span>
-   <span data-ttu-id="d8c6e-147">TestAndIncr</span><span class="sxs-lookup"><span data-stu-id="d8c6e-147">TestAndIncr</span></span>
-   <span data-ttu-id="d8c6e-148">AutonomousType</span><span class="sxs-lookup"><span data-stu-id="d8c6e-148">AutonomousType</span></span>
-   <span data-ttu-id="d8c6e-149">InstancePointer</span><span class="sxs-lookup"><span data-stu-id="d8c6e-149">InstancePointer</span></span>
-   <span data-ttu-id="d8c6e-150">VariablePointer</span><span class="sxs-lookup"><span data-stu-id="d8c6e-150">VariablePointer</span></span>
-   <span data-ttu-id="d8c6e-151">RowPointer</span><span class="sxs-lookup"><span data-stu-id="d8c6e-151">RowPointer</span></span>
-   <span data-ttu-id="d8c6e-152">RowStatus</span><span class="sxs-lookup"><span data-stu-id="d8c6e-152">RowStatus</span></span>
-   <span data-ttu-id="d8c6e-153">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="d8c6e-153">TimeStamp</span></span>
-   <span data-ttu-id="d8c6e-154">TimeInterval</span><span class="sxs-lookup"><span data-stu-id="d8c6e-154">TimeInterval</span></span>
-   <span data-ttu-id="d8c6e-155">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="d8c6e-155">DateAndTime</span></span>
-   <span data-ttu-id="d8c6e-156">StorageType</span><span class="sxs-lookup"><span data-stu-id="d8c6e-156">StorageType</span></span>
-   <span data-ttu-id="d8c6e-157">Tdomain</span><span class="sxs-lookup"><span data-stu-id="d8c6e-157">Tdomain</span></span>
-   <span data-ttu-id="d8c6e-158">Taddress</span><span class="sxs-lookup"><span data-stu-id="d8c6e-158">Taddress</span></span>

</dd> </dl>

## <a name="fatal-error-1002"></a><span data-ttu-id="d8c6e-159">Erreur irrécupérable 1002</span><span class="sxs-lookup"><span data-stu-id="d8c6e-159">Fatal Error 1002</span></span>

<dl> <dt>

<span data-ttu-id="d8c6e-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002,> irrécupérable : " <fileName> : <ligne \#> : clause d’accès non valide <clause> "</span><span class="sxs-lookup"><span data-stu-id="d8c6e-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, Fatal>: "<fileName>:<line\#>: Invalid ACCESS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="d8c6e-161">Erreur sémantique du module d’appel de macro de TYPE objet.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-161">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="d8c6e-162">Pour SNMPv1, la clause d’accès de la macro de TYPE objet doit être « lecture seule », « en écriture seule », « lecture/écriture » ou « non accessible ».</span><span class="sxs-lookup"><span data-stu-id="d8c6e-162">For SNMPv1, the ACCESS clause of the OBJECT-TYPE macro must be "read-only," "write-only," "read/write," or "not-accessible."</span></span>

<span data-ttu-id="d8c6e-163">Pour SNMPv2C, la clause MAX-ACCESS doit être « lecture seule », « lecture-création », « lecture/écriture » ou « non accessible ».</span><span class="sxs-lookup"><span data-stu-id="d8c6e-163">For SNMPv2C, the MAX-ACCESS clause must be "read-only," "read-create," "read/write," or "not-accessible."</span></span>

</dd> </dl>

## <a name="fatal-error-1003"></a><span data-ttu-id="d8c6e-164">Erreur irrécupérable 1003</span><span class="sxs-lookup"><span data-stu-id="d8c6e-164">Fatal Error 1003</span></span>

<dl> <dt>

<span data-ttu-id="d8c6e-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003,> irrécupérable : " <fileName> : <ligne \#> : clause d’État non valide <clause> "</span><span class="sxs-lookup"><span data-stu-id="d8c6e-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, Fatal>: "<fileName>:<line\#>: Invalid STATUS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="d8c6e-166">Erreur sémantique du module d’appel de macro de TYPE objet.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-166">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="d8c6e-167">Pour SNMPv1, la clause STATUs d’un appel de macro de TYPE objet doit être « obligatoire », « facultatif », « obsolète » ou « déconseillé ».</span><span class="sxs-lookup"><span data-stu-id="d8c6e-167">For SNMPv1, the STATUS clause of an OBJECT-TYPE macro invocation must be "mandatory," "optional," "obsolete," or "deprecated."</span></span>

<span data-ttu-id="d8c6e-168">Pour SNMPv2C, la clause STATUs d’un appel de macro de TYPE objet doit être « Current », « Deprecated » ou « obsolete ».</span><span class="sxs-lookup"><span data-stu-id="d8c6e-168">For SNMPv2C, the STATUS clause of an OBJECT-TYPE macro invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="warning-1004"></a><span data-ttu-id="d8c6e-169">AVERTISSEMENT 1004</span><span class="sxs-lookup"><span data-stu-id="d8c6e-169">Warning 1004</span></span>

<dl> <dt>

<span data-ttu-id="d8c6e-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, avertissement> : " <fileName> : <ligne \#> : Object-type <identifier> , dont la syntaxe est résolue en l’un des types de compteurs ne se termine pas par la lettre'"</span><span class="sxs-lookup"><span data-stu-id="d8c6e-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, whose syntax resolves to one of the Counter types does not end with the letter 's' "</span></span>
</dt> <dd>

<span data-ttu-id="d8c6e-171">AVERTISSEMENT sémantique du module d’appel de macro de TYPE objet.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-171">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="d8c6e-172">L’identificateur d’un objet de la syntaxe Counter (SNMPv1) ou Counter32 et Counter64 (SNMPv2C) doit être pluriel.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-172">The identifier for an object of SYNTAX Counter (SNMPv1) or Counter32 and Counter64 (SNMPv2C) must be plural.</span></span>

<span data-ttu-id="d8c6e-173">Cet avertissement peut se produire lors de la compilation d’un MIB ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-173">This warning can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

</dd> </dl>

## <a name="warning-1005"></a><span data-ttu-id="d8c6e-174">AVERTISSEMENT 1005</span><span class="sxs-lookup"><span data-stu-id="d8c6e-174">Warning 1005</span></span>

<dl> <dt>

<span data-ttu-id="d8c6e-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, avertissement> : " <fileName> : <\#> de ligne : Object-type avec la syntaxe" Sequence of ", doit avoir une clause d’accès" inaccessible "</span><span class="sxs-lookup"><span data-stu-id="d8c6e-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, Warning>: "<fileName>:<line\#>: OBJECT-TYPE with SYNTAX "SEQUENCE OF", should have an ACCESS clause "not-accessible"</span></span>
</dt> <dd>

<span data-ttu-id="d8c6e-176">AVERTISSEMENT sémantique du module d’appel de macro de TYPE objet.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-176">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="d8c6e-177">Une ligne de table ou conceptuelle (en séquence de types d’objets de séquence ou, respectivement) doit être « non accessible ».</span><span class="sxs-lookup"><span data-stu-id="d8c6e-177">A table or conceptual row (SEQUENCE OF or SEQUENCE object types, respectively) must be "not-accessible."</span></span>

<span data-ttu-id="d8c6e-178">Cet avertissement peut se produire dans SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-178">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1006"></a><span data-ttu-id="d8c6e-179">Erreur irrécupérable 1006</span><span class="sxs-lookup"><span data-stu-id="d8c6e-179">Fatal Error 1006</span></span>

<dl> <dt>

<span data-ttu-id="d8c6e-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006,> fatale : " <fileName> : <line \#> Object-type <identifier> , qui est de la séquence de syntaxe, n’a pas d’index ou de clause d’augmentation"</span><span class="sxs-lookup"><span data-stu-id="d8c6e-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, Fatal>: "<fileName>:<line\#> OBJECT-TYPE <identifier>, which is of SYNTAX SEQUENCE, does not have an INDEX or AUGMENTS clause"</span></span>
</dt> <dd>

<span data-ttu-id="d8c6e-181">Erreur sémantique du module d’appel de macro de TYPE objet.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-181">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="d8c6e-182">Pour SNMPv1, la clause INDEX doit être présente pour une définition de TYPE objet dont la syntaxe correspond à un type de séquence.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-182">For SNMPv1, the INDEX clause must be present for an OBJECT-TYPE definition whose SYNTAX resolves to a SEQUENCE type.</span></span>

<span data-ttu-id="d8c6e-183">Pour SNMPv2C, la clause INDEX ou l’augmentation doit être présente pour une déclaration de ligne conceptuelle.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-183">For SNMPv2C, either the INDEX or the AUGMENTS clause must be present for a conceptual row declaration.</span></span>

</dd> </dl>

## <a name="fatal-error-1008"></a><span data-ttu-id="d8c6e-184">Erreur irrécupérable 1008</span><span class="sxs-lookup"><span data-stu-id="d8c6e-184">Fatal Error 1008</span></span>

<dl> <dt>

<span data-ttu-id="d8c6e-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008,> irrécupérable : " <fileName> : <ligne \#> : Object-type <identifier> , qui est de la syntaxe" Sequence "n’a pas été référencée"</span><span class="sxs-lookup"><span data-stu-id="d8c6e-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, Fatal>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, which is of SYNTAX "SEQUENCE" has not been referenced"</span></span>
</dt> <dd>

<span data-ttu-id="d8c6e-186">Erreur sémantique du module d’appel de macro de TYPE objet.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-186">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="d8c6e-187">Un TYPE d’objet avec la clause SYNTAX comme type de séquence doit figurer dans la clause syntaxique d’un seul appel de TYPE objet qui représente une déclaration de table, autrement dit un objet avec la clause SYNTAX comme une séquence de type.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-187">An OBJECT-TYPE with the SYNTAX clause as a SEQUENCE type must figure in the SYNTAX clause of exactly one OBJECT-TYPE invocation that stands for a table declaration, that is, an object with the SYNTAX clause as a SEQUENCE OF type.</span></span> <span data-ttu-id="d8c6e-188">Le \# paramètre de> de ligne <fait référence au deuxième point de référence.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-188">The <line\#> parameter refers to the second point of reference.</span></span>

<span data-ttu-id="d8c6e-189">Cette erreur peut se produire dans SNMPv1 ou SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d8c6e-189">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



