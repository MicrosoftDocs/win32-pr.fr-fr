---
title: Type complexe DataDefinitionType
description: Définit un élément de données que vous souhaitez inclure avec l’événement. | Type complexe DataDefinitionType
ms.assetid: f4234e54-a5a8-48e4-941f-05107dcd3f88
keywords:
- DataDefinitionType type complexe EventLog
topic_type:
- apiref
api_name:
- DataDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19584c28a7bdf7ae01b87d1f414b9464b7b4271d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522911"
---
# <a name="datadefinitiontype-complex-type"></a><span data-ttu-id="6b0de-105">Type complexe DataDefinitionType</span><span class="sxs-lookup"><span data-stu-id="6b0de-105">DataDefinitionType Complex Type</span></span>

<span data-ttu-id="6b0de-106">Définit un élément de données que vous souhaitez inclure avec l’événement.</span><span class="sxs-lookup"><span data-stu-id="6b0de-106">Defines a data item that you want to include with the event.</span></span>

``` syntax
<xs:complexType name="DataDefinitionType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="string"
                use="required"
             />
            <xs:attribute name="inType"
                type="QName"
                use="required"
             />
            <xs:attribute name="outType"
                type="QName"
                use="optional"
             />
            <xs:attribute name="map"
                type="string"
                use="optional"
             />
            <xs:attribute name="length"
                type="LengthType"
                use="optional"
             />
            <xs:attribute name="count"
                type="CountType"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="6b0de-107">Attributs</span><span class="sxs-lookup"><span data-stu-id="6b0de-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b0de-108">Nom</span><span class="sxs-lookup"><span data-stu-id="6b0de-108">Name</span></span></th>
<th><span data-ttu-id="6b0de-109">Type</span><span class="sxs-lookup"><span data-stu-id="6b0de-109">Type</span></span></th>
<th><span data-ttu-id="6b0de-110">Description</span><span class="sxs-lookup"><span data-stu-id="6b0de-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6b0de-111">count</span><span class="sxs-lookup"><span data-stu-id="6b0de-111">count</span></span></td>
<td><span data-ttu-id="6b0de-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b0de-112"><a href="eventmanifestschema-counttype-simpletype.md"><strong>CountType</strong></a></span></span></td>
<td><span data-ttu-id="6b0de-113">Nombre d’éléments dans le tableau si l’élément de données est un tableau.</span><span class="sxs-lookup"><span data-stu-id="6b0de-113">The number of elements in the array if the data item is an array.</span></span> <span data-ttu-id="6b0de-114">Vous pouvez spécifier le nombre réel ou le nom d’un autre élément de données qui contient le nombre.</span><span class="sxs-lookup"><span data-stu-id="6b0de-114">You can specify the actual count or the name of another data item that contains the count.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b0de-115">InType</span><span class="sxs-lookup"><span data-stu-id="6b0de-115">inType</span></span></td>
<td><span data-ttu-id="6b0de-116"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="6b0de-116"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="6b0de-117">Type de données de cet élément de données.</span><span class="sxs-lookup"><span data-stu-id="6b0de-117">The data type for this data item.</span></span> <span data-ttu-id="6b0de-118">Pour obtenir la liste des types de données d’entrée prédéfinis, consultez le type complexe <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6b0de-118">For a list of predefined input data types, see the <a href="eventmanifestschema-inputtype-complextype.md"><strong>InputType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b0de-119">length</span><span class="sxs-lookup"><span data-stu-id="6b0de-119">length</span></span></td>
<td><span data-ttu-id="6b0de-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></span><span class="sxs-lookup"><span data-stu-id="6b0de-120"><a href="eventmanifestschema-lengthtype-simpletype.md"><strong>LengthType</strong></a></span></span></td>
<td><span data-ttu-id="6b0de-121">Longueur d’un élément de données de longueur variable, telle qu’un objet blob binaire.</span><span class="sxs-lookup"><span data-stu-id="6b0de-121">The length of a variable length data item, such as a binary blob.</span></span> <span data-ttu-id="6b0de-122">Pour les données binaires, spécifiez la longueur en octets et pour les données de type chaîne, spécifiez la longueur en caractères.</span><span class="sxs-lookup"><span data-stu-id="6b0de-122">For binary data, specify the length in bytes and for string data, specify the length in characters.</span></span> <span data-ttu-id="6b0de-123">Vous pouvez spécifier la longueur réelle ou le nom d’un autre élément de données qui contient la longueur.</span><span class="sxs-lookup"><span data-stu-id="6b0de-123">You can specify the actual length or the name of another data item that contains the length.</span></span><br/> <span data-ttu-id="6b0de-124">Si vous utilisez l’attribut length pour spécifier une chaîne de longueur fixe, vous devez remplir la chaîne à sa longueur fixe, ce qui permet d’utiliser le caractère de fin null à la fin (par exemple, si la longueur est de 5, la chaîne &quot; ABC &quot; doit être complétée comme &quot; ABC &quot; .</span><span class="sxs-lookup"><span data-stu-id="6b0de-124">If you use the length attribute to specify a fixed length string, you must pad the string to its fixed length allowing for the null-terminator character at the end (for example, if the length is 5, the string &quot;abc&quot; must be padded as &quot;abc &quot;.</span></span> <span data-ttu-id="6b0de-125">La longueur de chaîne doit inclure le caractère de fin null.</span><span class="sxs-lookup"><span data-stu-id="6b0de-125">The string length must include the null-terminator character.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b0de-126">carte</span><span class="sxs-lookup"><span data-stu-id="6b0de-126">map</span></span></td>
<td><span data-ttu-id="6b0de-127">string</span><span class="sxs-lookup"><span data-stu-id="6b0de-127">string</span></span></td>
<td><span data-ttu-id="6b0de-128">Nom de la carte nom/valeur à utiliser pour mapper des valeurs entières à des chaînes.</span><span class="sxs-lookup"><span data-stu-id="6b0de-128">The name of the name/value map to use to map integer values to strings.</span></span> <span data-ttu-id="6b0de-129">Le type de données de l’élément de données doit être de l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="6b0de-129">The data type of the data item must be of one of the following types:</span></span><br/>
<ul>
<li><span data-ttu-id="6b0de-130">win:UInt8</span><span class="sxs-lookup"><span data-stu-id="6b0de-130">win:UInt8</span></span></li>
<li><span data-ttu-id="6b0de-131">win:UInt16</span><span class="sxs-lookup"><span data-stu-id="6b0de-131">win:UInt16</span></span></li>
<li><span data-ttu-id="6b0de-132">win:UInt32</span><span class="sxs-lookup"><span data-stu-id="6b0de-132">win:UInt32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6b0de-133">name</span><span class="sxs-lookup"><span data-stu-id="6b0de-133">name</span></span></td>
<td><span data-ttu-id="6b0de-134">string</span><span class="sxs-lookup"><span data-stu-id="6b0de-134">string</span></span></td>
<td><span data-ttu-id="6b0de-135">Nom de l'élément de données.</span><span class="sxs-lookup"><span data-stu-id="6b0de-135">The name of the data item.</span></span> <span data-ttu-id="6b0de-136">Vous pouvez utiliser le nom pour faire référence à cet élément de données dans votre fragment XML si vous spécifiez une section <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> dans votre modèle.</span><span class="sxs-lookup"><span data-stu-id="6b0de-136">You can use the name to reference this data item in your XML fragment if you specify a <a href="eventmanifestschema-userdata-templateitemtype-element.md"><strong>UserData</strong></a> section in your template.</span></span> <span data-ttu-id="6b0de-137">Vous pouvez également faire référence à ce nom dans un attribut de longueur ou de nombre d’un autre élément de données si cet élément de données contient sa valeur de longueur ou de nombre.</span><span class="sxs-lookup"><span data-stu-id="6b0de-137">You can also reference this name in a length or count attribute of another data item if this data item contains its length or count value.</span></span><br/> <span data-ttu-id="6b0de-138"><strong>Windows Vista :</strong> Cet attribut est facultatif.</span><span class="sxs-lookup"><span data-stu-id="6b0de-138"><strong>Windows Vista:</strong> This attribute is optional.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6b0de-139">Type de</span><span class="sxs-lookup"><span data-stu-id="6b0de-139">outType</span></span></td>
<td><span data-ttu-id="6b0de-140"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="6b0de-140"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="6b0de-141">Type de données à utiliser lors du rendu de cet élément de données.</span><span class="sxs-lookup"><span data-stu-id="6b0de-141">The data type to use when rendering this data item.</span></span> <span data-ttu-id="6b0de-142">Pour obtenir la liste des types de données de sortie prédéfinis, consultez le type complexe <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6b0de-142">For a list of predefined output data types, see the <a href="eventmanifestschema-outputtype-complextype.md"><strong>OutputType</strong></a> complex type.</span></span><br/> <span data-ttu-id="6b0de-143"><strong>Windows Vista :</strong> Le type de sortie est ignoré et le service détermine le type en fonction du type d’entrée.</span><span class="sxs-lookup"><span data-stu-id="6b0de-143"><strong>Windows Vista:</strong> The output type is ignored, and the service determines the type based on the input type.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="6b0de-144">Notes</span><span class="sxs-lookup"><span data-stu-id="6b0de-144">Remarks</span></span>

<span data-ttu-id="6b0de-145">Pour les types d’entrée de longueur variable, tels que les objets BLOB binaires, vous devez utiliser l’attribut length pour spécifier explicitement la taille des données.</span><span class="sxs-lookup"><span data-stu-id="6b0de-145">For variable length input types, such as binary blobs, you must use the length attribute to explicitly specify the size of the data.</span></span> <span data-ttu-id="6b0de-146">Pour les chaînes, spécifiez l’attribut length uniquement si les chaînes ont une longueur fixe.</span><span class="sxs-lookup"><span data-stu-id="6b0de-146">For strings, specify the length attribute only if the strings are of a fixed length.</span></span>

## <a name="examples"></a><span data-ttu-id="6b0de-147">Exemples</span><span class="sxs-lookup"><span data-stu-id="6b0de-147">Examples</span></span>

<span data-ttu-id="6b0de-148">Voici quelques exemples de définitions d’éléments de données.</span><span class="sxs-lookup"><span data-stu-id="6b0de-148">The following are a few examples of the data item definitions.</span></span>


```XML
<!-- The data item is an 8-bit integer -->
<data name="binaryChar" inType="win:UInt8">
 
<!-- The data item is a single ANSI character -->
<data name="ansiChar" inType="win:UInt8" outtype="xs:string">
 
<!-- The data item is a single Unicode character -->
<data name="unicodeChar" inType="win:UInt16" outtype="xs:string">
 
<!-- The data item is an IP address that is rendered as a dot separated list of interger values -->
<data name="ipAddress" inType="win:UInt32" outtype="win:IPv4">
 
<!-- The data item is a Boolean value -->
<data name="success" inType="win:boolean">
 
<!-- The data item is a null-terminated ANSI string -->
<data name="string" inType="win:AnsiString"> 

<!-- The data item is a fixed length ANSI string -->
<data name="string" inType="win:AnsiString" length="42"> 
 
<!-- The data item is a fixed length array of null-terminated ANSI strings -->
<data name="strings" inType="win:AnsiString" count="20">
 
<!-- The data item is a fixed length array of fixed length ANSI strings -->
<data name="strings" inType="win:AnsiString" length="42" count="20">
 
<!-- The data item is a variable length array of same sized ANSI strings -->
<data name="stringLength" inType="win:UInt16">
<data name="arrayCount" inType="win:Uint16">
<data name="strings" inType="win:AnsiString" length="stringLength" count="arrayCount"> 
 
<!-- For binary data, you must specify the size.
<!-- The data item is a fixed length array of fixed length binary blobs -->
<data name="blobs" inType="win:Binary" length="42" count="20">

<!-- The data item is a fixed length binary blob -->
<data name="blob" inType="win:Binary" length="42">

<!-- The following are illegal binary data definitions -->
<!-- This definition is illegal because no length is specified -->
<data name="blob" inType="win:Binary"> 
 
<!-- This definition is illegal because you cannot determine the length of each binary blob -->
<data name="blob" inType="win:Binary" count="20"> 
 
<!-- The data item is a variable length array of structures. Each structure -->
<!-- contains an array of same sized ANSI strings --> 
<data name="arrayStructCount" inType="win:UInt16">
<struct name="countedStrings" count="arrayStructCount">
      <data name="stringLength" inType="win:UInt16">
      <data name="string" inType="win:AnsiString" length="stringLength">
</struct>
 
<!-- The data item is a time stamp that is rendered in 100ns units -->
<data name="timestamp" inType="win:UInt32" outType="win:ETWTIME">

<!-- The data item is a fixed length array of integers --> 
<data name="integers" inType="win:UInt32" count="20">

<!-- The data item is a variable length array of integers -->
<data name="arrayCount" inType="win:UInt16"> 
<data name="integers" inType="win:UInt32" count="arrayCount"> 

<!-- The following is illegal because you cannot assign a length value to a data type of a known size -->
<data name="integer" inType="win:UInt32" length="42">
```



## <a name="requirements"></a><span data-ttu-id="6b0de-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b0de-149">Requirements</span></span>



| <span data-ttu-id="6b0de-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b0de-150">Requirement</span></span> | <span data-ttu-id="6b0de-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b0de-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6b0de-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b0de-152">Minimum supported client</span></span><br/> | <span data-ttu-id="6b0de-153">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b0de-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6b0de-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b0de-154">Minimum supported server</span></span><br/> | <span data-ttu-id="6b0de-155">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b0de-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





