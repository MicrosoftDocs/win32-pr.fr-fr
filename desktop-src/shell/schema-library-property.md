---
description: L' <property> élément spécifie une propriété utilisée par la bibliothèque. Ces propriétés étant spécifiques à la bibliothèque, il n’existe aucun ensemble prédéfini de noms de propriétés à utiliser. Cet élément est facultatif et n’a pas d’éléments enfants.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: Property, élément (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b269e8914cf1f5da92d96e1922f7347a161daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991105"
---
# <a name="property-element-library-schema"></a><span data-ttu-id="6c81b-105">Property, élément (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="6c81b-105">property Element (Library Schema)</span></span>

<span data-ttu-id="6c81b-106">L' <property> élément spécifie une propriété utilisée par la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="6c81b-106">The <property> element specifies a property used by the library.</span></span> <span data-ttu-id="6c81b-107">Ces propriétés étant spécifiques à la bibliothèque, il n’existe aucun ensemble prédéfini de noms de propriétés à utiliser.</span><span class="sxs-lookup"><span data-stu-id="6c81b-107">These properties are specific to the library, so there is no predefined set of property names to use.</span></span> <span data-ttu-id="6c81b-108">Cet élément est facultatif et n’a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="6c81b-108">This element is optional and has no child elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c81b-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c81b-109">Syntax</span></span>

``` syntax
<!-- property -->
<xs:element name="property" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension base="xs:anyType">
                <xs:attribute name="name" type="canonical-name" use="required"/>
                    <xs:simpleType name="canonical-name">
                        <xs:restriction base="xs:string">
                            <xs:maxLength value="63"/>
                            <xs:pattern value="[0-9A-Za-z.]*"/>
                        </xs:restriction>
                    </xs:simpleType>
                <xs:attribute name="type"/>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a><span data-ttu-id="6c81b-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6c81b-110">Element Information</span></span>



| <span data-ttu-id="6c81b-111">Élément parent</span><span class="sxs-lookup"><span data-stu-id="6c81b-111">Parent Element</span></span>                                                             | <span data-ttu-id="6c81b-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6c81b-112">Child Elements</span></span> |
|----------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="6c81b-113">Élément propertyStore (schéma de bibliothèque)</span><span class="sxs-lookup"><span data-stu-id="6c81b-113">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md) | <span data-ttu-id="6c81b-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="6c81b-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="6c81b-115">Attributs</span><span class="sxs-lookup"><span data-stu-id="6c81b-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c81b-116">Attribut</span><span class="sxs-lookup"><span data-stu-id="6c81b-116">Attribute</span></span></th>
<th><span data-ttu-id="6c81b-117">Description</span><span class="sxs-lookup"><span data-stu-id="6c81b-117">Description</span></span></th>
<th><span data-ttu-id="6c81b-118">Valeurs</span><span class="sxs-lookup"><span data-stu-id="6c81b-118">Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c81b-119">name</span><span class="sxs-lookup"><span data-stu-id="6c81b-119">name</span></span></td>
<td><span data-ttu-id="6c81b-120">Public.</span><span class="sxs-lookup"><span data-stu-id="6c81b-120">Public.</span></span> <span data-ttu-id="6c81b-121">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6c81b-121">Required.</span></span> <span data-ttu-id="6c81b-122">Le nom complet de la propriété.</span><span class="sxs-lookup"><span data-stu-id="6c81b-122">The display name of the property.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6c81b-123">type</span><span class="sxs-lookup"><span data-stu-id="6c81b-123">type</span></span></td>
<td><span data-ttu-id="6c81b-124">Public.</span><span class="sxs-lookup"><span data-stu-id="6c81b-124">Public.</span></span> <span data-ttu-id="6c81b-125">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6c81b-125">Required.</span></span> <span data-ttu-id="6c81b-126">Type de propriété.</span><span class="sxs-lookup"><span data-stu-id="6c81b-126">The type of property.</span></span></td>
<td><ul>
<li><span data-ttu-id="6c81b-127">Any : valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="6c81b-127">Any: Default.</span></span> <span data-ttu-id="6c81b-128">La valeur ne sera pas forcée par le sous-système de propriété.</span><span class="sxs-lookup"><span data-stu-id="6c81b-128">The value will not be coerced by the property subsystem.</span></span> <span data-ttu-id="6c81b-129">VT_NULL est retourné par GetPropertyType.</span><span class="sxs-lookup"><span data-stu-id="6c81b-129">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="6c81b-130">NULL : il n’y a aucune valeur pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="6c81b-130">Null: There is no value for this property.</span></span> <span data-ttu-id="6c81b-131">VT_NULL est retourné par GetPropertyType.</span><span class="sxs-lookup"><span data-stu-id="6c81b-131">VT_NULL will be returned by GetPropertyType.</span></span></li>
<li><span data-ttu-id="6c81b-132">Chaîne : la valeur doit être un VT_LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="6c81b-132">String: The value must be a VT_LPWSTR.</span></span></li>
<li><span data-ttu-id="6c81b-133">Booléen : la valeur doit être un VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="6c81b-133">Boolean: The value must be a VT_BOOL.</span></span></li>
<li><span data-ttu-id="6c81b-134">Byte : la valeur doit être un VT_UI1.</span><span class="sxs-lookup"><span data-stu-id="6c81b-134">Byte: The value must be a VT_UI1.</span></span></li>
<li><span data-ttu-id="6c81b-135">Buffer : la valeur doit être un VT_UI1 | Mémoire tampon d’octets VT_VECTOR.</span><span class="sxs-lookup"><span data-stu-id="6c81b-135">Buffer: The value must be a VT_UI1 | VT_VECTOR buffer of bytes.</span></span></li>
<li><span data-ttu-id="6c81b-136">Int16 : la valeur doit être un VT_I2.</span><span class="sxs-lookup"><span data-stu-id="6c81b-136">Int16: The value must be a VT_I2.</span></span></li>
<li><span data-ttu-id="6c81b-137">UInt16 : la valeur doit être un VT_UI2.</span><span class="sxs-lookup"><span data-stu-id="6c81b-137">UInt16: The value must be a VT_UI2.</span></span></li>
<li><span data-ttu-id="6c81b-138">Int32 : la valeur doit être un VT_I4.</span><span class="sxs-lookup"><span data-stu-id="6c81b-138">Int32: The value must be a VT_I4.</span></span></li>
<li><span data-ttu-id="6c81b-139">UInt32 : la valeur doit être un VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="6c81b-139">UInt32: The value must be a VT_UI4.</span></span></li>
<li><span data-ttu-id="6c81b-140">Int64 : la valeur doit être un VT_I8.</span><span class="sxs-lookup"><span data-stu-id="6c81b-140">Int64: The value must be a VT_I8.</span></span></li>
<li><span data-ttu-id="6c81b-141">UInt64 : la valeur doit être un VT_UI8.</span><span class="sxs-lookup"><span data-stu-id="6c81b-141">UInt64: The value must be a VT_UI8.</span></span></li>
<li><span data-ttu-id="6c81b-142">Double : la valeur doit être un VT_R8.</span><span class="sxs-lookup"><span data-stu-id="6c81b-142">Double: The value must be a VT_R8.</span></span></li>
<li><span data-ttu-id="6c81b-143">DateTime : la valeur doit être un VT_FILETIME.</span><span class="sxs-lookup"><span data-stu-id="6c81b-143">DateTime: The value must be a VT_FILETIME.</span></span></li>
<li><span data-ttu-id="6c81b-144">GUID : la valeur doit être un VT_CLSID.</span><span class="sxs-lookup"><span data-stu-id="6c81b-144">Guid: The value must be a VT_CLSID.</span></span></li>
<li><span data-ttu-id="6c81b-145">Objet BLOB : la valeur doit être un VT_BLOB.</span><span class="sxs-lookup"><span data-stu-id="6c81b-145">Blob: The value must be a VT_BLOB.</span></span></li>
<li><span data-ttu-id="6c81b-146">Objet : la valeur doit être un VT_UNKNOWN.</span><span class="sxs-lookup"><span data-stu-id="6c81b-146">Object: The value must be a VT_UNKNOWN.</span></span></li>
<li><span data-ttu-id="6c81b-147">Stream : la valeur doit être un VT_STREAM.</span><span class="sxs-lookup"><span data-stu-id="6c81b-147">Stream: The value must be a VT_STREAM.</span></span></li>
<li><span data-ttu-id="6c81b-148">Presse-papiers : la valeur doit être un VT_CF.</span><span class="sxs-lookup"><span data-stu-id="6c81b-148">Clipboard: The value must be a VT_CF.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="6c81b-149">Notes</span><span class="sxs-lookup"><span data-stu-id="6c81b-149">Remarks</span></span>

<span data-ttu-id="6c81b-150">La configuration requise pour l’élément <nom canonique> correspond à la configuration requise pour Windows Search et le système de propriétés Windows.</span><span class="sxs-lookup"><span data-stu-id="6c81b-150">The requirements for the <canonical-name> element match the requirements for Windows Search and the Windows property system.</span></span> <span data-ttu-id="6c81b-151">La chaîne doit être de type canonique.</span><span class="sxs-lookup"><span data-stu-id="6c81b-151">The string must be of type canonical-type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c81b-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6c81b-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c81b-153">Schéma de description de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6c81b-153">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="6c81b-154">Schémas de propriété</span><span class="sxs-lookup"><span data-stu-id="6c81b-154">Property Schemas</span></span>](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[<span data-ttu-id="6c81b-155">Schéma de la description du connecteur de recherche</span><span class="sxs-lookup"><span data-stu-id="6c81b-155">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
