---
description: L' <property> élément facultatif spécifie les propriétés utilisées par le fournisseur de localisation.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: Élément Property de locationProvider (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71081b8b04ec999daa90958a29708b8efc64bee0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "106539849"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a><span data-ttu-id="d8d13-103">Élément Property de locationProvider (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="d8d13-103">property Element of locationProvider (Search Connector Schema)</span></span>

<span data-ttu-id="d8d13-104">L' <property> élément facultatif spécifie les propriétés utilisées par le fournisseur de localisation.</span><span class="sxs-lookup"><span data-stu-id="d8d13-104">The optional <property> element specifies the properties used by the location provider.</span></span> <span data-ttu-id="d8d13-105">Ces propriétés étant spécifiques à ce fournisseur de localisation, il n’existe aucun ensemble prédéfini de noms à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d8d13-105">These properties are specific to this location provider, so there is no predefined set of names to use.</span></span> <span data-ttu-id="d8d13-106">L' <property> élément a deux attributs, comme décrit dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d8d13-106">The <property> element has two attributes, as described in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8d13-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8d13-107">Syntax</span></span>


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
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



## <a name="property-element-information"></a><span data-ttu-id="d8d13-108"><property> Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="d8d13-108"><property> Element Information</span></span>



| <span data-ttu-id="d8d13-109">Élément parent</span><span class="sxs-lookup"><span data-stu-id="d8d13-109">Parent Element</span></span>                                                                                 | <span data-ttu-id="d8d13-110">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d8d13-110">Child Elements</span></span>                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [<span data-ttu-id="d8d13-111">Élément locationProvider (schéma du connecteur de recherche)</span><span class="sxs-lookup"><span data-stu-id="d8d13-111">locationProvider Element (Search Connector Schema)</span></span>](search-schema-sconn-locationprovider.md) | <span data-ttu-id="d8d13-112">, décrite dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="d8d13-112">property, described in this topic.</span></span> |



 


## <a name="property-attributes"></a><span data-ttu-id="d8d13-113"><property> Attributs</span><span class="sxs-lookup"><span data-stu-id="d8d13-113"><property> Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d8d13-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="d8d13-114">Attribute</span></span></th>
<th><span data-ttu-id="d8d13-115">Description</span><span class="sxs-lookup"><span data-stu-id="d8d13-115">Description</span></span></th>
<th><span data-ttu-id="d8d13-116">Valeurs</span><span class="sxs-lookup"><span data-stu-id="d8d13-116">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d8d13-117">name</span><span class="sxs-lookup"><span data-stu-id="d8d13-117">name</span></span></td>
<td><span data-ttu-id="d8d13-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d8d13-118">Required.</span></span> <span data-ttu-id="d8d13-119">Le nom complet de la propriété.</span><span class="sxs-lookup"><span data-stu-id="d8d13-119">The display name of the property.</span></span></td>
<td> </td>
</tr>
<tr class="even">
<td><span data-ttu-id="d8d13-120">type</span><span class="sxs-lookup"><span data-stu-id="d8d13-120">type</span></span></td>
<td><span data-ttu-id="d8d13-121">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d8d13-121">Required.</span></span> <span data-ttu-id="d8d13-122">Type de propriété.</span><span class="sxs-lookup"><span data-stu-id="d8d13-122">The type of property.</span></span></td>
<td><span data-ttu-id="d8d13-123">Any : valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d8d13-123">Any: Default.</span></span> <span data-ttu-id="d8d13-124">La valeur ne sera pas forcée par le sous-système de propriété.</span><span class="sxs-lookup"><span data-stu-id="d8d13-124">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="d8d13-125">VT_NULL est retourné par GetPropertyType.</span><span class="sxs-lookup"><span data-stu-id="d8d13-125">VT_NULL will be returned by GetPropertyType.</span></span>
<ul>
<li><span data-ttu-id="d8d13-126">NULL : il n’y a aucune valeur pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d8d13-126">Null: There is no value for this property.</span></span> <span data-ttu-id="d8d13-127">VT_NULL est retourné par GetPropertyType.</span><span class="sxs-lookup"><span data-stu-id="d8d13-127">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="d8d13-128">Chaîne : la valeur doit être un VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="d8d13-128">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="d8d13-129">Booléen : la valeur doit être un VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="d8d13-129">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="d8d13-130">Byte : la valeur doit être un VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="d8d13-130">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="d8d13-131">Buffer : la valeur doit être un VT_UI1 | Mémoire tampon d’octets VT_VECTOR.</span><span class="sxs-lookup"><span data-stu-id="d8d13-131">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="d8d13-132">Int16 : la valeur doit être un VT_I2.</span><span class="sxs-lookup"><span data-stu-id="d8d13-132">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="d8d13-133">UInt16 : la valeur doit être un VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="d8d13-133">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="d8d13-134">Int32 : la valeur doit être un VT_I4.</span><span class="sxs-lookup"><span data-stu-id="d8d13-134">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="d8d13-135">UInt32 : la valeur doit être un VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="d8d13-135">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="d8d13-136">Int64 : la valeur doit être un VT_I8.</span><span class="sxs-lookup"><span data-stu-id="d8d13-136">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="d8d13-137">UInt64 : la valeur doit être un VT_UI8</span><span class="sxs-lookup"><span data-stu-id="d8d13-137">UInt64: The value must be a VT_UI8</span></span></li>
<li><span data-ttu-id="d8d13-138">Double : la valeur doit être un VT_R8.</span><span class="sxs-lookup"><span data-stu-id="d8d13-138">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="d8d13-139">DateTime : la valeur doit être un VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="d8d13-139">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="d8d13-140">GUID : la valeur doit être un VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="d8d13-140">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="d8d13-141">Objet BLOB : la valeur doit être un VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="d8d13-141">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="d8d13-142">Objet : la valeur doit être un VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="d8d13-142">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="d8d13-143">Stream : la valeur doit être un VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="d8d13-143">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="d8d13-144">Presse-papiers : la valeur doit être un VT_CF.</span><span class="sxs-lookup"><span data-stu-id="d8d13-144">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="d8d13-145">Notes</span><span class="sxs-lookup"><span data-stu-id="d8d13-145">Remarks</span></span>

<span data-ttu-id="d8d13-146">Pour le fournisseur OpenSearch, les propriétés suivantes sont utilisées :</span><span class="sxs-lookup"><span data-stu-id="d8d13-146">For the OpenSearch provider, the following properties are used:</span></span>

-   <span data-ttu-id="d8d13-147">OpenSearchShortName : nom abrégé du service de recherche</span><span class="sxs-lookup"><span data-stu-id="d8d13-147">OpenSearchShortName: Short name of the search service</span></span>
-   <span data-ttu-id="d8d13-148">OpenSearchQueryTemplate : modèle, mis en forme selon la Convention de modèle OpenSearch, pour le service de requête</span><span class="sxs-lookup"><span data-stu-id="d8d13-148">OpenSearchQueryTemplate: Template, formatted following the OpenSearch template convention, for the query service</span></span>
-   <span data-ttu-id="d8d13-149">MaximumResultCount : (Number) nombre maximal de résultats retournés par le service de recherche</span><span class="sxs-lookup"><span data-stu-id="d8d13-149">MaximumResultCount: (number) Maximum number of results returned by the search service</span></span>
-   <span data-ttu-id="d8d13-150">LinkIsFilePath : (booléen) si la valeur est true, le fournisseur tente d’interpréter les éléments retournés en tant que fichiers, en utilisant leurs extensions pour créer le ShellItem approprié dans la vue.</span><span class="sxs-lookup"><span data-stu-id="d8d13-150">LinkIsFilePath: (Boolean) If true, the provider tries to interpret returned items as files, using their extensions to create the proper ShellItem in the view.</span></span> <span data-ttu-id="d8d13-151">Si la valeur est false, les éléments sont traités comme des raccourcis d’URL.</span><span class="sxs-lookup"><span data-stu-id="d8d13-151">If false, items are treated as URL shortcuts.</span></span>

 

 



