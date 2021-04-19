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
# <a name="counter-complex-type"></a>Type complexe de compteur

Définit un compteur.

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

## <a name="child-elements"></a>Éléments enfants



| Élément               | Type                                                                                 | Description                                                                                                      |
|-----------------------|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| **counterAttributes** | [**homme : counterAttributes**](performance-counters-counterattributes-complex-type.md) | Répertorie les attributs uniques qui spécifient le mode d’affichage des données de compteur dans une application consommateur.<br/> |



## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>aggregate</td>

<td>Fonction d’agrégation à appliquer si l’attribut <strong>instances</strong> de <a href="performance-counters-counterset-complex-type.md"><strong>counterSet</strong></a> est GlobalAggregate, multipleAggregate ou globalAggregateHistory. Vous pouvez appliquer les fonctions d’agrégation suivantes :<br/> <dl> <dt><span id="max"></span><span id="MAX"></span>Max</dt> <dd> La valeur de compteur maximale est retournée.<br/> </dd> <dt><span id="min"></span><span id="MIN"></span>min</dt> <dd> La valeur de compteur minimale est retournée.<br/> </dd> <dt><span id="avg"></span><span id="AVG"></span>AVG</dt> <dd> La valeur moyenne du compteur est retournée.<br/> </dd> <dt><span id="sum"></span><span id="SUM"></span>checksum</dt> <dd> La somme des valeurs de compteur est retournée.<br/> </dd> <dt><span id="undefined"></span><span id="UNDEFINED"></span>non défini</dt> <dd> Ne pas agréger ce compteur.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>baseID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>homme : UInt32Type</strong></a></td>
<td>Identificateur d’un autre compteur dans le même ensemble de compteurs, dont la valeur est utilisée pour calculer la valeur de ce compteur. Les types de compteurs suivants requièrent un compteur de base :<br/> <dl> <dt><span id="PERF_AVERAGE_TIMER"></span><span id="perf_average_timer"></span>PERF_AVERAGE_TIMER</dt> <dd> Requiert le compteur de base PERF_AVERAGE_BASE.<br/> </dd> <dt><span id="PERF_AVERAGE_BULK"></span><span id="perf_average_bulk"></span>PERF_AVERAGE_BULK</dt> <dd> Requiert le compteur de base PERF_AVERAGE_BASE.<br/> </dd> <dt><span id="PERF_COUNTER_MULTI_TIMER_INV"></span><span id="perf_counter_multi_timer_inv"></span>PERF_COUNTER_MULTI_TIMER_INV</dt> <dd> Requiert le compteur de base PERF_COUNTER_MULTI_BASE.<br/> </dd> <dt><span id="PERF_LARGE_RAW_FRACTION"></span><span id="perf_large_raw_fraction"></span>PERF_LARGE_RAW_FRACTION</dt> <dd> Requiert le compteur de base PERF_LARGE_RAW_BASE.<br/> </dd> <dt><span id="PERF_PRECISION_100NS_TIMER"></span><span id="perf_precision_100ns_timer"></span>PERF_PRECISION_100NS_TIMER</dt> <dd> Requiert le compteur de base PERF_LARGE_RAW_BASE.<br/> </dd> <dt><span id="PERF_RAW_FRACTION"></span><span id="perf_raw_fraction"></span>PERF_RAW_FRACTION</dt> <dd> Requiert le compteur de base PERF_RAW_BASE.<br/> </dd> <dt><span id="PERF_SAMPLE_FRACTION"></span><span id="perf_sample_fraction"></span>PERF_SAMPLE_FRACTION</dt> <dd> Requiert le compteur de base PERF_SAMPLE_BASE.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td>defaultScale</td>

<td>Facteur d’échelle à appliquer à la valeur de compteur (facteur * valeur de compteur). La valeur par défaut est zéro si aucune échelle n’est appliquée. Les valeurs valides sont comprises entre 10 et 10 (0,0000000001 à 1 milliard). Si cette valeur est égale à zéro, la valeur de mise à l’échelle est 1 ; Si cette valeur est 1, la valeur de l’échelle est 10 ; Si cette valeur est 1, la valeur de l’échelle est. 10 ; et ainsi de suite.<br/></td>
</tr>
<tr class="even">
<td>description</td>
<td><strong>xs:string</strong></td>
<td>Brève description du compteur. Vous n’avez pas besoin de spécifier cet attribut si le compteur comprend l’attribut <a href="performance-counters-counterattribute-complex-type.md"><strong>nodisplay</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td>detailLevel</td>

<td>Spécifie le public cible pour les détails du compteur. Les valeurs possibles sont les suivantes :<br/> <dl> <dt><span id="standard"></span><span id="STANDARD"></span>hiver</dt> <dd> Affichez des détails sur le compteur qu’un utilisateur classique peut comprendre.<br/> </dd> <dt><span id="advanced"></span><span id="ADVANCED"></span>détaillées</dt> <dd> Affichez des détails sur le compteur que seul un utilisateur expérimenté peut comprendre.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td>field</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>homme : CSymbolType</strong></a></td>
<td>Nom d’un champ dans le struct qui contient la valeur de compteur. Cet attribut n’est pas autorisé pour les fournisseurs en mode utilisateur.<br/></td>
</tr>
<tr class="odd">
<td>id</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>homme : UInt32Type</strong></a></td>
<td>Numéro unique qui identifie le compteur au sein de l’ensemble de compteurs.<br/></td>
</tr>
<tr class="even">
<td>multiCounterID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>homme : UInt32Type</strong></a></td>
<td>Identificateur d’un autre compteur dans le même ensemble de compteurs, dont la valeur de multiplicateur est utilisée pour calculer la valeur de ce compteur. Les types de compteurs suivants requièrent une valeur de multiplicateur. Le compteur référencé doit être de type PERF_COUNTER_RAWCOUNT.<br/>
<ul>
<li>PERF_COUNTER_MULTI_TIMER</li>
<li>PERF_COUNTER_MULTI_TIMER_INV</li>
<li>PERF_100NSEC_MULTI_TIMER</li>
<li>PERF_100NSEC_MULTI_TIMER_INV</li>
</ul></td>
</tr>
<tr class="odd">
<td>name</td>

<td>Nom du compteur. Le nom doit être unique et contenir moins de 1 024 caractères. Cette valeur respecte la casse. Vous n’avez pas besoin de spécifier cet attribut si le compteur comprend l’attribut <a href="performance-counters-counterattribute-complex-type.md"><strong>nodisplay</strong></a> .<br/></td>
</tr>
<tr class="even">
<td>perfFreqID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>homme : UInt32Type</strong></a></td>
<td>Identificateur d’un autre compteur dans le même ensemble de compteurs, dont la valeur de fréquence est utilisée pour calculer la valeur de ce compteur. Les types de compteurs suivants requièrent une fréquence. Le type de compteur PERF_COUNTER_LARGE_RAWCOUNT contient la valeur d’horodatage.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="odd">
<td>perfTimeID</td>
<td><a href="performance-counters-uint32type-simple-type.md"><strong>homme : UInt32Type</strong></a></td>
<td>Identificateur d’un autre compteur dans le même ensemble de compteurs, dont la valeur d’horodatage est utilisée pour calculer la valeur de ce compteur. Les types de compteurs suivants requièrent un horodatage. Le type de compteur PERF_COUNTER_LARGE_RAWCOUNT contient la valeur d’horodatage.<br/>
<ul>
<li>PERF_COUNTER_OBJECT_TIME_QUEUELEN_TYPE</li>
<li>PERF_ELAPSED_TIME</li>
<li>PERF_OBJ_TIME_TIMER</li>
<li>PERF_PRECISION_OBJECT_TIMER</li>
</ul></td>
</tr>
<tr class="even">
<td>struct</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>homme : CSymbolType</strong></a></td>
<td>Nom d’un élément de struct qui contient cette valeur de compteur. Cet attribut n’est pas autorisé pour les fournisseurs en mode utilisateur.<br/></td>
</tr>
<tr class="odd">
<td>symbole</td>
<td><a href="performance-counters-csymboltype-simple-type.md"><strong>homme : CSymbolType</strong></a></td>
<td>Nom symbolique qui identifie le compteur. L’outil <a href="ctrpp.md">CTRPP</a> crée une constante que vous pouvez utiliser lors de l’appel de fonctions qui requièrent un identificateur de compteur (par exemple, <a href="/windows/desktop/api/Perflib/nf-perflib-perfincrementulongcountervalue"><strong>PerfIncrementULongCounterValue</strong></a>). Le nom de la constante est le nom symbolique.<br/></td>
</tr>
<tr class="even">
<td>type</td>

<td>Nom du type de compteur. Pour connaître les valeurs possibles, consultez le bloc de syntaxe ci-dessus. Pour plus d’informations sur chaque type, consultez <a href="/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)">types de compteurs</a> dans le Guide de déploiement de Windows 2003. Le nom respecte la casse. Utilisez des minuscules. <br/></td>
</tr>
<tr class="odd">
<td>URI</td>
<td><strong>xs:anyURI</strong></td>
<td>Identificateur de ressource uniforme unique qui permet aux utilisateurs de récupérer des valeurs de compteur à partir de n’importe quel emplacement.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Notes

Pour assurer la compatibilité descendante, chaque compteur de l’ensemble de compteurs doit spécifier les mêmes valeurs **perfFreqID** et **perfTimeID** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

