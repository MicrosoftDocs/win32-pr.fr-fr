---
description: L' <property> élément facultatif spécifie une propriété utilisée par le connecteur de recherche. Ces propriétés étant spécifiques à ce connecteur de recherche, il n’existe aucun ensemble prédéfini de noms à utiliser. Cet élément n’a pas d’éléments enfants.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Élément Property de propertyStore (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2e4cee6f26ee65ba03d9225eafcea4a03a7c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525450"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a><span data-ttu-id="3949c-105">Élément Property de propertyStore (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="3949c-105">property Element of propertyStore (Search Connector Schema)</span></span>

<span data-ttu-id="3949c-106">L' <property> élément facultatif spécifie une propriété utilisée par le connecteur de recherche.</span><span class="sxs-lookup"><span data-stu-id="3949c-106">The optional <property> element specifies a property used by the search connector.</span></span> <span data-ttu-id="3949c-107">Ces propriétés étant spécifiques à ce connecteur de recherche, il n’existe aucun ensemble prédéfini de noms à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3949c-107">These properties are specific to this search connector, so there is no predefined set of names to use.</span></span> <span data-ttu-id="3949c-108">Cet élément n’a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="3949c-108">This element has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="3949c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3949c-109">Syntax</span></span>


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="3949c-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3949c-110">Element Information</span></span>



| <span data-ttu-id="3949c-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="3949c-111">Parent Element</span></span>                                                                           | <span data-ttu-id="3949c-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3949c-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="3949c-113">Élément propertyStore (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="3949c-113">propertyStore Element (Search Connector Schema)</span></span>](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a><span data-ttu-id="3949c-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="3949c-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3949c-115">Attribut</span><span class="sxs-lookup"><span data-stu-id="3949c-115">Attribute</span></span></th>
<th><span data-ttu-id="3949c-116">Description</span><span class="sxs-lookup"><span data-stu-id="3949c-116">Description</span></span></th>
<th><span data-ttu-id="3949c-117">Valeurs</span><span class="sxs-lookup"><span data-stu-id="3949c-117">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3949c-118">name</span><span class="sxs-lookup"><span data-stu-id="3949c-118">name</span></span></td>
<td><span data-ttu-id="3949c-119">Public.</span><span class="sxs-lookup"><span data-stu-id="3949c-119">Public.</span></span> <span data-ttu-id="3949c-120">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3949c-120">Required.</span></span> <span data-ttu-id="3949c-121">Le nom complet de la propriété.</span><span class="sxs-lookup"><span data-stu-id="3949c-121">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="3949c-122">type</span><span class="sxs-lookup"><span data-stu-id="3949c-122">type</span></span></td>
<td><span data-ttu-id="3949c-123">Public.</span><span class="sxs-lookup"><span data-stu-id="3949c-123">Public.</span></span> <span data-ttu-id="3949c-124">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="3949c-124">Required.</span></span> <span data-ttu-id="3949c-125">Type de propriété.</span><span class="sxs-lookup"><span data-stu-id="3949c-125">The type of property.</span></span></td>
<td><span data-ttu-id="3949c-126">Any : valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="3949c-126">Any: Default.</span></span> <span data-ttu-id="3949c-127">La valeur ne sera pas forcée par le sous-système de propriété.</span><span class="sxs-lookup"><span data-stu-id="3949c-127">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="3949c-128">VT_NULL est retourné par GetPropertyType.</span><span class="sxs-lookup"><span data-stu-id="3949c-128">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="3949c-129">NULL : il n’y a aucune valeur pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="3949c-129">Null: There is no value for this property.</span></span> <span data-ttu-id="3949c-130">VT_NULL est retourné par GetPropertyType.</span><span class="sxs-lookup"><span data-stu-id="3949c-130">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="3949c-131">Chaîne : la valeur doit être un VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="3949c-131">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="3949c-132">Booléen : la valeur doit être un VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="3949c-132">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="3949c-133">Byte : la valeur doit être un VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="3949c-133">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="3949c-134">Buffer : la valeur doit être un VT_UI1 | Mémoire tampon d’octets VT_VECTOR.</span><span class="sxs-lookup"><span data-stu-id="3949c-134">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="3949c-135">Int16 : la valeur doit être un VT_I2.</span><span class="sxs-lookup"><span data-stu-id="3949c-135">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="3949c-136">UInt16 : la valeur doit être un VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="3949c-136">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="3949c-137">Int32 : la valeur doit être un VT_I4.</span><span class="sxs-lookup"><span data-stu-id="3949c-137">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="3949c-138">UInt32 : la valeur doit être un VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="3949c-138">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="3949c-139">Int64 : la valeur doit être un VT_I8.</span><span class="sxs-lookup"><span data-stu-id="3949c-139">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="3949c-140">UInt64 : la valeur doit être un VT_UI8</span><span class="sxs-lookup"><span data-stu-id="3949c-140">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="3949c-141">Double : la valeur doit être un VT_R8.</span><span class="sxs-lookup"><span data-stu-id="3949c-141">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="3949c-142">DateTime : la valeur doit être un VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="3949c-142">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="3949c-143">GUID : la valeur doit être un VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="3949c-143">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="3949c-144">Objet BLOB : la valeur doit être un VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="3949c-144">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="3949c-145">Objet : la valeur doit être un VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="3949c-145">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="3949c-146">Stream : la valeur doit être un VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="3949c-146">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="3949c-147">Presse-papiers : la valeur doit être un VT_CF.</span><span class="sxs-lookup"><span data-stu-id="3949c-147">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3949c-148">schéma</span><span class="sxs-lookup"><span data-stu-id="3949c-148">schema</span></span></td>
<td><span data-ttu-id="3949c-149">Public.</span><span class="sxs-lookup"><span data-stu-id="3949c-149">Public.</span></span> <span data-ttu-id="3949c-150">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="3949c-150">Optional.</span></span> <span data-ttu-id="3949c-151">Schéma dans lequel la propriété est définie.</span><span class="sxs-lookup"><span data-stu-id="3949c-151">The schema where the property is defined.</span></span></td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="3949c-152">Notes</span><span class="sxs-lookup"><span data-stu-id="3949c-152">Remarks</span></span>

<span data-ttu-id="3949c-153">Les connecteurs de recherche OpenSearch peuvent utiliser la propriété OpenSearchHTMLRolloverTemplate.</span><span class="sxs-lookup"><span data-stu-id="3949c-153">OpenSearch search connectors can use the OpenSearchHTMLRolloverTemplate property.</span></span> <span data-ttu-id="3949c-154">Cette propriété identifie un modèle mis en forme selon la Convention de modèle OpenSearch.</span><span class="sxs-lookup"><span data-stu-id="3949c-154">This property identifies a template that is formatted following the OpenSearch template convention.</span></span> <span data-ttu-id="3949c-155">Le modèle OpenSearchHTMLRolloverTemplate est utilisé lorsque l’utilisateur clique sur le bouton « Rechercher sur le site Web » dans la barre de commandes.</span><span class="sxs-lookup"><span data-stu-id="3949c-155">The OpenSearchHTMLRolloverTemplate template is used when the user clicks on the "Search on website" button in the command bar.</span></span>

## <a name="example"></a><span data-ttu-id="3949c-156">Exemple</span><span class="sxs-lookup"><span data-stu-id="3949c-156">Example</span></span>

<span data-ttu-id="3949c-157">L’exemple suivant illustre un <propertyStore> élément avec deux <property> éléments.</span><span class="sxs-lookup"><span data-stu-id="3949c-157">The following example shows a <propertyStore> element with two <property> elements.</span></span>


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



