---
description: Définit un compteur.
ms.assetid: 8f1338c0-7ea6-4d0c-af71-51012973e4a0
title: Type complexe de compteur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d591d4c23b626eaf2e2bfb10b528ff7c054507df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524222"
---
# <a name="counter-complex-type"></a><span data-ttu-id="07315-103">Type complexe de compteur</span><span class="sxs-lookup"><span data-stu-id="07315-103">counter Complex Type</span></span>

<span data-ttu-id="07315-104">Définit un compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-104">Defines a counter.</span></span>

``` syntax
<xs:complexType name="counter">
    <xs:choice
        minOccurs="0"
        maxOccurs="1"
    >
        <xs:element name="counterAttributes"
            type="man:counterAttributes"
        >
            <xs:key name="uniqueCounterAttributeName">
                <xs:selector
                    xpath="./man:counterAttribute"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="id"
        type="man:UInt32Type"
        use="required"
     />
    <xs:attribute name="uri"
        type="xs:anyURI"
        use="required"
     />
    <xs:attribute name="name"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:maxLength
                    value="1023"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="description"
        type="xs:string"
        use="optional"
     />
    <xs:attribute name="type"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="perf_counter_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer"
                 />
                <xs:enumeration
                    value="perf_counter_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_large_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_100ns_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_obj_time_queuelen_type"
                 />
                <xs:enumeration
                    value="perf_counter_bulk_count"
                 />
                <xs:enumeration
                    value="perf_counter_text"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount"
                 />
                <xs:enumeration
                    value="perf_counter_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_counter_large_rawcount_hex"
                 />
                <xs:enumeration
                    value="perf_sample_fraction"
                 />
                <xs:enumeration
                    value="perf_sample_counter"
                 />
                <xs:enumeration
                    value="perf_counter_timer_inv"
                 />
                <xs:enumeration
                    value="perf_sample_base"
                 />
                <xs:enumeration
                    value="perf_average_timer"
                 />
                <xs:enumeration
                    value="perf_average_base"
                 />
                <xs:enumeration
                    value="perf_average_bulk"
                 />
                <xs:enumeration
                    value="perf_obj_time_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer"
                 />
                <xs:enumeration
                    value="perf_counter_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_counter_multi_base"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer"
                 />
                <xs:enumeration
                    value="perf_100nsec_multi_timer_inv"
                 />
                <xs:enumeration
                    value="perf_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_large_raw_fraction"
                 />
                <xs:enumeration
                    value="perf_raw_base"
                 />
                <xs:enumeration
                    value="perf_large_raw_base"
                 />
                <xs:enumeration
                    value="perf_elapsed_time"
                 />
                <xs:enumeration
                    value="perf_counter_delta"
                 />
                <xs:enumeration
                    value="perf_counter_large_delta"
                 />
                <xs:enumeration
                    value="perf_precision_system_timer"
                 />
                <xs:enumeration
                    value="perf_precision_100ns_timer"
                 />
                <xs:enumeration
                    value="perf_precision_object_timer"
                 />
                <xs:enumeration
                    value="perf_counter_composite"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="baseID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="detailLevel"
        use="required"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="standard"
                 />
                <xs:enumeration
                    value="advanced"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="defaultScale"
        use="optional"
        default="0"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:integer"
            >
                <xs:minInclusive
                    value="-10"
                 />
                <xs:maxInclusive
                    value="10"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="aggregate"
        use="optional"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="sum"
                 />
                <xs:enumeration
                    value="avg"
                 />
                <xs:enumeration
                    value="max"
                 />
                <xs:enumeration
                    value="min"
                 />
                <xs:enumeration
                    value="undefined"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="perfTimeID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="perfFreqID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="multiCounterID"
        type="man:UInt32Type"
        use="optional"
     />
    <xs:attribute name="struct"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="field"
        type="man:CSymbolType"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="07315-105">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="07315-105">Child elements</span></span>



| <span data-ttu-id="07315-106">Élément</span><span class="sxs-lookup"><span data-stu-id="07315-106">Element</span></span>               | <span data-ttu-id="07315-107">Type</span><span class="sxs-lookup"><span data-stu-id="07315-107">Type</span></span>                                                                                 | <span data-ttu-id="07315-108">Description</span><span class="sxs-lookup"><span data-stu-id="07315-108">Description</span></span>                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07315-109">**counterAttributes**</span><span class="sxs-lookup"><span data-stu-id="07315-109">**counterAttributes**</span></span> | [<span data-ttu-id="07315-110">**homme : counterAttributes**</span><span class="sxs-lookup"><span data-stu-id="07315-110">**man:counterAttributes**</span></span>](performance-counters-counterattributes-complex-type.md) | <span data-ttu-id="07315-111">Répertorie les attributs uniques qui spécifient le mode d’affichage des données de compteur dans une application consommateur.</span><span class="sxs-lookup"><span data-stu-id="07315-111">Lists the unique attributes that specify how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="07315-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="07315-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="07315-113">Nom</span><span class="sxs-lookup"><span data-stu-id="07315-113">Name</span></span></th>
<th><span data-ttu-id="07315-114">Type</span><span class="sxs-lookup"><span data-stu-id="07315-114">Type</span></span></th>
<th><span data-ttu-id="07315-115">Description</span><span class="sxs-lookup"><span data-stu-id="07315-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="07315-116">aggregate</span><span class="sxs-lookup"><span data-stu-id="07315-116">aggregate</span></span></td>

<td><span data-ttu-id="07315-117">Fonction d’agrégation à appliquer si l’attribut <strong>instances</strong> de <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> est GlobalAggregate, multipleAggregate ou globalAggregateHistory.</span><span class="sxs-lookup"><span data-stu-id="07315-117">The aggregation function to apply if the <strong>instances</strong> attribute of <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> is globalAggregate, multipleAggregate, or globalAggregateHistory.</span></span> <span data-ttu-id="07315-118">Vous pouvez appliquer les fonctions d’agrégation suivantes :</span><span class="sxs-lookup"><span data-stu-id="07315-118">The following are the possible aggregation functions that you can apply:</span></span><br/> <dl> <span data-ttu-id="07315-119"><dt><span id="max"></span><span id="MAX"></span>Max</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-119"><dt><span id="max"></span><span id="MAX"></span>max</dt> </span></span><dd> <span data-ttu-id="07315-120">La valeur de compteur maximale est retournée.</span><span class="sxs-lookup"><span data-stu-id="07315-120">The maximum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="07315-121"><dt><span id="min"></span><span id="MIN"></span>min</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-121"><dt><span id="min"></span><span id="MIN"></span>min</dt> </span></span><dd> <span data-ttu-id="07315-122">La valeur de compteur minimale est retournée.</span><span class="sxs-lookup"><span data-stu-id="07315-122">The minimum counter value is returned.</span></span><br/> </dd> <span data-ttu-id="07315-123"><dt><span id="avg"></span><span id="AVG"></span>AVG</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-123"><dt><span id="avg"></span><span id="AVG"></span>avg</dt> </span></span><dd> <span data-ttu-id="07315-124">La valeur moyenne du compteur est retournée.</span><span class="sxs-lookup"><span data-stu-id="07315-124">The average counter value is returned.</span></span><br/> </dd> <span data-ttu-id="07315-125"><dt><span id="sum"></span><span id="SUM"></span>checksum</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-125"><dt><span id="sum"></span><span id="SUM"></span>sum</dt> </span></span><dd> <span data-ttu-id="07315-126">La somme des valeurs de compteur est retournée.</span><span class="sxs-lookup"><span data-stu-id="07315-126">The sum of the counter values is returned.</span></span><br/> </dd> <span data-ttu-id="07315-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>non défini</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-127"><dt><span id="undefined"></span><span id="UNDEFINED"></span>undefined</dt> </span></span><dd> <span data-ttu-id="07315-128">Ne pas agréger ce compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-128">Do not aggregate this counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07315-129">baseID</span><span class="sxs-lookup"><span data-stu-id="07315-129">baseID</span></span></td>
<td><span data-ttu-id="07315-130"><a href="performance-counters-uint32type-simple-type.md"><strong>homme : UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="07315-130"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="07315-131">Identificateur d’un autre compteur dans le même ensemble de compteurs, dont la valeur est utilisée pour calculer la valeur de ce compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-131">The identifier of another counter within the same counter set, whose value is used to calculate this counter's value.</span></span> <span data-ttu-id="07315-132">Les types de compteurs suivants requièrent un compteur de base :</span><span class="sxs-lookup"><span data-stu-id="07315-132">The following counter types require a base counter:</span></span><br/> <dl> <span data-ttu-id="07315-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-133"><dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> </span></span><dd> <span data-ttu-id="07315-134">Requiert le compteur de base PERF_AVERAGE_BASE.</span><span class="sxs-lookup"><span data-stu-id="07315-134">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="07315-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-135"><dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> </span></span><dd> <span data-ttu-id="07315-136">Requiert le compteur de base PERF_AVERAGE_BASE.</span><span class="sxs-lookup"><span data-stu-id="07315-136">Requires the PERF_AVERAGE_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="07315-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-137"><dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> </span></span><dd> <span data-ttu-id="07315-138">Requiert le compteur de base PERF_COUNTER_MULTI_BASE.</span><span class="sxs-lookup"><span data-stu-id="07315-138">Requires the PERF_COUNTER_MULTI_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="07315-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-139"><dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="07315-140">Requiert le compteur de base PERF_LARGE_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="07315-140">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="07315-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-141"><dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> </span></span><dd> <span data-ttu-id="07315-142">Requiert le compteur de base PERF_LARGE_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="07315-142">Requires the PERF_LARGE_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="07315-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-143"><dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> </span></span><dd> <span data-ttu-id="07315-144">Requiert le compteur de base PERF_RAW_BASE.</span><span class="sxs-lookup"><span data-stu-id="07315-144">Requires the PERF_RAW_BASE base counter.</span></span><br/> </dd> <span data-ttu-id="07315-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-145"><dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> </span></span><dd> <span data-ttu-id="07315-146">Requiert le compteur de base PERF_SAMPLE_BASE.</span><span class="sxs-lookup"><span data-stu-id="07315-146">Requires the PERF_SAMPLE_BASE base counter.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07315-147">defaultScale</span><span class="sxs-lookup"><span data-stu-id="07315-147">defaultScale</span></span></td>

<td><span data-ttu-id="07315-148">Facteur d’échelle à appliquer à la valeur de compteur (facteur \* valeur de compteur).</span><span class="sxs-lookup"><span data-stu-id="07315-148">The scale factor to apply to the counter value (factor \* counter value).</span></span> <span data-ttu-id="07315-149">La valeur par défaut est zéro si aucune échelle n’est appliquée.</span><span class="sxs-lookup"><span data-stu-id="07315-149">The default is zero if no scale is applied.</span></span> <span data-ttu-id="07315-150">Les valeurs valides sont comprises entre 10 et 10 (0,0000000001 à 1 milliard).</span><span class="sxs-lookup"><span data-stu-id="07315-150">Valid values range from  10 to 10 (0.0000000001 to 1000000000).</span></span> <span data-ttu-id="07315-151">Si cette valeur est égale à zéro, la valeur de mise à l’échelle est 1 ; Si cette valeur est 1, la valeur de l’échelle est 10 ; Si cette valeur est 1, la valeur de l’échelle est. 10 ; et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="07315-151">If this value is zero, the scale value is 1; if this value is 1, the scale value is 10; if this value is  1, the scale value is .10; and so on.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07315-152">description</span><span class="sxs-lookup"><span data-stu-id="07315-152">description</span></span></td>
<td><span data-ttu-id="07315-153"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="07315-153"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="07315-154">Brève description du compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-154">A short description of the counter.</span></span> <span data-ttu-id="07315-155">Vous n’avez pas besoin de spécifier cet attribut si le compteur comprend l’attribut <a href="performance-counters-counterattribute-complex-type.md"><strong>nodisplay</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="07315-155">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07315-156">detailLevel</span><span class="sxs-lookup"><span data-stu-id="07315-156">detailLevel</span></span></td>

<td><span data-ttu-id="07315-157">Spécifie le public cible pour les détails du compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-157">Specifies the target audience for the counter details.</span></span> <span data-ttu-id="07315-158">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="07315-158">The following are the possible values:</span></span><br/> <dl> <span data-ttu-id="07315-159"><dt><span id="standard"></span><span id="STANDARD"></span>hiver</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-159"><dt><span id="standard"></span><span id="STANDARD"></span>standard</dt> </span></span><dd> <span data-ttu-id="07315-160">Affichez des détails sur le compteur qu’un utilisateur classique peut comprendre.</span><span class="sxs-lookup"><span data-stu-id="07315-160">Display details about the counter that a typical user would understand.</span></span><br/> </dd> <span data-ttu-id="07315-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>détaillées</dt> </span><span class="sxs-lookup"><span data-stu-id="07315-161"><dt><span id="advanced"></span><span id="ADVANCED"></span>advanced</dt> </span></span><dd> <span data-ttu-id="07315-162">Affichez des détails sur le compteur que seul un utilisateur expérimenté peut comprendre.</span><span class="sxs-lookup"><span data-stu-id="07315-162">Display details about the counter that only an advanced user would understand.</span></span><br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07315-163">field</span><span class="sxs-lookup"><span data-stu-id="07315-163">field</span></span></td>
<td><span data-ttu-id="07315-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>homme : CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="07315-164"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="07315-165">Nom d’un champ dans le struct qui contient la valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-165">The name of a field within the struct that contains the counter value.</span></span> <span data-ttu-id="07315-166">Cet attribut n’est pas autorisé pour les fournisseurs en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="07315-166">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07315-167">id</span><span class="sxs-lookup"><span data-stu-id="07315-167">id</span></span></td>
<td><span data-ttu-id="07315-168"><a href="performance-counters-uint32type-simple-type.md"><strong>homme : UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="07315-168"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="07315-169">Numéro unique qui identifie le compteur au sein de l’ensemble de compteurs.</span><span class="sxs-lookup"><span data-stu-id="07315-169">A unique number that identifies the counter within the counter set.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07315-170">multiCounterID</span><span class="sxs-lookup"><span data-stu-id="07315-170">multiCounterID</span></span></td>
<td><span data-ttu-id="07315-171"><a href="performance-counters-uint32type-simple-type.md"><strong>homme : UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="07315-171"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="07315-172">Identificateur d’un autre compteur dans le même ensemble de compteurs, dont la valeur de multiplicateur est utilisée pour calculer la valeur de ce compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-172">The identifier of another counter within the same counter set, whose multiplier value is used to calculate this counter's value.</span></span> <span data-ttu-id="07315-173">Les types de compteurs suivants requièrent une valeur de multiplicateur.</span><span class="sxs-lookup"><span data-stu-id="07315-173">The following counter types require a multiplier value.</span></span> <span data-ttu-id="07315-174">Le compteur référencé doit être de type PERF_COUNTER_RAWCOUNT.</span><span class="sxs-lookup"><span data-stu-id="07315-174">The referenced counter must be of type PERF_COUNTER_RAWCOUNT.</span></span><br/>
<ul>
<li><span data-ttu-id="07315-175">PERF_COUNTER_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="07315-175">PERF_COUNTER_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="07315-176">PERF_COUNTER_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="07315-176">PERF_COUNTER_MULTI_TIMER_INV</span></span></li>
<li><span data-ttu-id="07315-177">PERF_100NSEC_MULTI_TIMER</span><span class="sxs-lookup"><span data-stu-id="07315-177">PERF_100NSEC_MULTI_TIMER</span></span></li>
<li><span data-ttu-id="07315-178">PERF_100NSEC_MULTI_TIMER_INV</span><span class="sxs-lookup"><span data-stu-id="07315-178">PERF_100NSEC_MULTI_TIMER_INV</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07315-179">name</span><span class="sxs-lookup"><span data-stu-id="07315-179">name</span></span></td>

<td><span data-ttu-id="07315-180">Nom du compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-180">The name of the counter.</span></span> <span data-ttu-id="07315-181">Le nom doit être unique et contenir moins de 1 024 caractères.</span><span class="sxs-lookup"><span data-stu-id="07315-181">The name must be unique and less than 1,024 characters.</span></span> <span data-ttu-id="07315-182">Cette valeur respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="07315-182">The name is case-sensitive.</span></span> <span data-ttu-id="07315-183">Vous n’avez pas besoin de spécifier cet attribut si le compteur comprend l’attribut <a href="performance-counters-counterattribute-complex-type.md"><strong>nodisplay</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="07315-183">You do not have to specify this attribute if the counter includes the <a href="performance-counters-counterattribute-complex-type.md"><strong>noDisplay</strong></a> attribute.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07315-184">perfFreqID</span><span class="sxs-lookup"><span data-stu-id="07315-184">perfFreqID</span></span></td>
<td><span data-ttu-id="07315-185"><a href="performance-counters-uint32type-simple-type.md"><strong>homme : UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="07315-185"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="07315-186">Identificateur d’un autre compteur dans le même ensemble de compteurs, dont la valeur de fréquence est utilisée pour calculer la valeur de ce compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-186">The identifier of another counter within the same counter set, whose frequency value is used to calculate this counter's value.</span></span> <span data-ttu-id="07315-187">Les types de compteurs suivants requièrent une fréquence.</span><span class="sxs-lookup"><span data-stu-id="07315-187">The following counter types require a frequency.</span></span> <span data-ttu-id="07315-188">Le type de compteur PERF_COUNTER_LARGE_RAWCOUNT contient la valeur d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="07315-188">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="07315-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="07315-189">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="07315-190">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="07315-190">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="07315-191">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="07315-191">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="07315-192">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="07315-192">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07315-193">perfTimeID</span><span class="sxs-lookup"><span data-stu-id="07315-193">perfTimeID</span></span></td>
<td><span data-ttu-id="07315-194"><a href="performance-counters-uint32type-simple-type.md"><strong>homme : UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="07315-194"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="07315-195">Identificateur d’un autre compteur dans le même ensemble de compteurs, dont la valeur d’horodatage est utilisée pour calculer la valeur de ce compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-195">The identifier of another counter within the same counter set, whose time stamp value is used to calculate this counter's value.</span></span> <span data-ttu-id="07315-196">Les types de compteurs suivants requièrent un horodatage.</span><span class="sxs-lookup"><span data-stu-id="07315-196">The following counter types require a time stamp.</span></span> <span data-ttu-id="07315-197">Le type de compteur PERF_COUNTER_LARGE_RAWCOUNT contient la valeur d’horodatage.</span><span class="sxs-lookup"><span data-stu-id="07315-197">The PERF_COUNTER_LARGE_RAWCOUNT counter type contains the time stamp value.</span></span><br/>
<ul>
<li><span data-ttu-id="07315-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span><span class="sxs-lookup"><span data-stu-id="07315-198">PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</span></span></li>
<li><span data-ttu-id="07315-199">PERF_ELAPSED_TIME</span><span class="sxs-lookup"><span data-stu-id="07315-199">PERF_ELAPSED_TIME</span></span></li>
<li><span data-ttu-id="07315-200">PERF_OBJ_TIME_TIMER</span><span class="sxs-lookup"><span data-stu-id="07315-200">PERF_OBJ_TIME_TIMER</span></span></li>
<li><span data-ttu-id="07315-201">PERF_PRECISION_OBJECT_TIMER</span><span class="sxs-lookup"><span data-stu-id="07315-201">PERF_PRECISION_OBJECT_TIMER</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07315-202">struct</span><span class="sxs-lookup"><span data-stu-id="07315-202">struct</span></span></td>
<td><span data-ttu-id="07315-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>homme : CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="07315-203"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="07315-204">Nom d’un élément de struct qui contient cette valeur de compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-204">The name of a struct element that contains this counter value.</span></span> <span data-ttu-id="07315-205">Cet attribut n’est pas autorisé pour les fournisseurs en mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="07315-205">This attribute is not allowed for user-mode providers.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07315-206">symbole</span><span class="sxs-lookup"><span data-stu-id="07315-206">symbol</span></span></td>
<td><span data-ttu-id="07315-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>homme : CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="07315-207"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="07315-208">Nom symbolique qui identifie le compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-208">A symbolic name that identifies the counter.</span></span> <span data-ttu-id="07315-209">L’outil <a href="ctrpp.md">CTRPP</a> crée une constante que vous pouvez utiliser lors de l’appel de fonctions qui requièrent un identificateur de compteur (par exemple, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="07315-209">The <a href="ctrpp.md">CTRPP</a> tool creates a constant that you can use when calling functions that require a counter identifier (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>).</span></span> <span data-ttu-id="07315-210">Le nom de la constante est le nom symbolique.</span><span class="sxs-lookup"><span data-stu-id="07315-210">The name of the constant is the symbolic name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="07315-211">type</span><span class="sxs-lookup"><span data-stu-id="07315-211">type</span></span></td>

<td><span data-ttu-id="07315-212">Nom du type de compteur.</span><span class="sxs-lookup"><span data-stu-id="07315-212">The name of the counter type.</span></span> <span data-ttu-id="07315-213">Pour connaître les valeurs possibles, consultez le bloc de syntaxe ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="07315-213">For possible values, see the above syntax block.</span></span> <span data-ttu-id="07315-214">Pour plus d’informations sur chaque type, consultez <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">types de compteurs</a> dans le Guide de déploiement de Windows 2003.</span><span class="sxs-lookup"><span data-stu-id="07315-214">For details of each type, see <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">Counter Types</a> in the Windows 2003 Deployment Guide.</span></span> <span data-ttu-id="07315-215">Le nom respecte la casse. Utilisez des minuscules.</span><span class="sxs-lookup"><span data-stu-id="07315-215">The name is case-sensitive use lowercase.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="07315-216">URI</span><span class="sxs-lookup"><span data-stu-id="07315-216">uri</span></span></td>
<td><span data-ttu-id="07315-217"><strong>xs:anyURI</strong></span><span class="sxs-lookup"><span data-stu-id="07315-217"><strong>xs:anyURI</strong></span></span></td>
<td><span data-ttu-id="07315-218">Identificateur de ressource uniforme unique qui permet aux utilisateurs de récupérer des valeurs de compteur à partir de n’importe quel emplacement.</span><span class="sxs-lookup"><span data-stu-id="07315-218">A unique uniform resource identifier that lets users retrieve counter values from any location.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="07315-219">Notes</span><span class="sxs-lookup"><span data-stu-id="07315-219">Remarks</span></span>

<span data-ttu-id="07315-220">Pour assurer la compatibilité descendante, chaque compteur de l’ensemble de compteurs doit spécifier les mêmes valeurs **perfFreqID** et **perfTimeID** .</span><span class="sxs-lookup"><span data-stu-id="07315-220">To provide backwards-compatibility, each counter in the counter set should specify the same **perfFreqID** and **perfTimeID** values.</span></span>

## <a name="requirements"></a><span data-ttu-id="07315-221">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07315-221">Requirements</span></span>



| <span data-ttu-id="07315-222">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07315-222">Requirement</span></span> | <span data-ttu-id="07315-223">Valeur</span><span class="sxs-lookup"><span data-stu-id="07315-223">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="07315-224">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07315-224">Minimum supported client</span></span><br/> | <span data-ttu-id="07315-225">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07315-225">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="07315-226">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="07315-226">Minimum supported server</span></span><br/> | <span data-ttu-id="07315-227">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="07315-227">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

