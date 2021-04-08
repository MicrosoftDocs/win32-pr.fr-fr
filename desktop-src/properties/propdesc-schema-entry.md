---
description: Cette rubrique présente le schéma de description de propriété utilisé par le système de propriétés de Shell.
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: Présentation du schéma de description de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51d9e7c2b6fb4b599f977c0c49ad1cb2514fe8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034283"
---
# <a name="understanding-the-property-description-schema"></a><span data-ttu-id="23492-103">Présentation du schéma de description de propriété</span><span class="sxs-lookup"><span data-stu-id="23492-103">Understanding the Property Description Schema</span></span>

<span data-ttu-id="23492-104">Cette rubrique présente le schéma de description de propriété utilisé par le système de propriétés de Shell.</span><span class="sxs-lookup"><span data-stu-id="23492-104">This topic introduces the property description schema used by the Shell property system.</span></span>

<span data-ttu-id="23492-105">L’introduction de nouvelles fonctionnalités pour Windows Vista et versions ultérieures nécessitait l’extension du système de propriétés de Shell existant pour :</span><span class="sxs-lookup"><span data-stu-id="23492-105">The introduction of new features for Windows Vista and later required that the existing Shell property system be extended to:</span></span>

-   <span data-ttu-id="23492-106">Prendre en charge un système de description de propriété riche et extensible qui fournit des informations sur les propriétés, y compris les noms d’affichage, le type, le type d’affichage, le comportement de tri et de groupe et d’autres attributs nécessaires pour présenter et utiliser les propriétés.</span><span class="sxs-lookup"><span data-stu-id="23492-106">Support a rich and extensible property description system that provides information about properties including display names, type, display type, sort and group behavior, and other attributes needed to present and operate over the properties.</span></span>
-   <span data-ttu-id="23492-107">Prenez en charge une liste de types de propriété (associée à l’interface utilisateur qui peut modifier ces types dans différents affichages, tels que ListView, volet de visualisation, boîtes de dialogue de propriétés, etc.) qui peuvent être associées à différentes propriétés.</span><span class="sxs-lookup"><span data-stu-id="23492-107">Support a stock list of property types (combined with UI that can edit those types in different views like the listview, preview pane, property dialogs, and so on) that can be associated with various properties.</span></span>
-   <span data-ttu-id="23492-108">Fournissez des listes de description de la propriété, qui définissent l’ensemble des propriétés affichées dans différents affichages.</span><span class="sxs-lookup"><span data-stu-id="23492-108">Supply property description lists, which define the set of properties displayed in various views.</span></span>
-   <span data-ttu-id="23492-109">Fournir une interface simplifiée, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), afin que les gestionnaires de propriétés puissent être écrits plus facilement et que les propriétés puissent être conservées dans des fichiers.</span><span class="sxs-lookup"><span data-stu-id="23492-109">Provide a simplified interface, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), so property handlers can be written more easily and so properties can be persisted to files.</span></span>
-   <span data-ttu-id="23492-110">Prise en charge des gestionnaires de propriétés non-fichiers pour exposer des propriétés dans la vue.</span><span class="sxs-lookup"><span data-stu-id="23492-110">Support for non-file property handlers to expose properties in the view.</span></span>

<span data-ttu-id="23492-111">Ces fonctionnalités sont obtenues sur une architecture qui fournit un accès abstrait aux propriétés d’un élément de Shell.</span><span class="sxs-lookup"><span data-stu-id="23492-111">These features are achieved on an architecture that provides abstract access to the properties of a Shell item.</span></span> <span data-ttu-id="23492-112">Cette abstraction est appelée système de propriétés de Shell.</span><span class="sxs-lookup"><span data-stu-id="23492-112">This abstraction is called the Shell property system.</span></span>

-   [<span data-ttu-id="23492-113">Qu’est-ce que le schéma de description de propriété ?</span><span class="sxs-lookup"><span data-stu-id="23492-113">What Is the Property Description Schema?</span></span>](#what-is-the-property-description-schema)
-   [<span data-ttu-id="23492-114">Pourquoi utiliser un schéma ?</span><span class="sxs-lookup"><span data-stu-id="23492-114">Why Use a Schema?</span></span>](#why-use-a-schema)
-   [<span data-ttu-id="23492-115">Quelles sont les principales parties du schéma ?</span><span class="sxs-lookup"><span data-stu-id="23492-115">What Are the Major Schema Parts?</span></span>](#what-are-the-major-schema-parts)
-   [<span data-ttu-id="23492-116">Modifications pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="23492-116">Changes for Windows 7</span></span>](#changes-for-windows-7)
-   [<span data-ttu-id="23492-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23492-117">Related topics</span></span>](#related-topics)

## <a name="what-is-the-property-description-schema"></a><span data-ttu-id="23492-118">Qu’est-ce que le schéma de description de propriété ?</span><span class="sxs-lookup"><span data-stu-id="23492-118">What Is the Property Description Schema?</span></span>

<span data-ttu-id="23492-119">Le sous-système de schéma se compose des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="23492-119">The schema subsystem consists of the following:</span></span>

-   <span data-ttu-id="23492-120">Un ou plusieurs fichiers de schéma. propDesc qui définissent les descriptions des propriétés.</span><span class="sxs-lookup"><span data-stu-id="23492-120">One or more .propdesc schema files that define property descriptions.</span></span> <span data-ttu-id="23492-121">Le schéma de description de propriété est défini dans une collection de fichiers de schéma XML (à l’aide de l’extension de fichier. propDesc) au moment de l’exécution sur le système.</span><span class="sxs-lookup"><span data-stu-id="23492-121">The property description schema is defined in a collection of XML schema files (using the .propdesc file extension) at runtime on the system.</span></span> <span data-ttu-id="23492-122">Ces fichiers sont chargés en différé quand une partie du système de propriétés les requiert.</span><span class="sxs-lookup"><span data-stu-id="23492-122">These files are lazy-loaded when a part of the property system requires them.</span></span>
-   <span data-ttu-id="23492-123">Cache de schéma en mémoire utilisé pour stocker les fichiers de schéma analysés, qui incluent toutes les descriptions de propriété introduites dans le sous-système.</span><span class="sxs-lookup"><span data-stu-id="23492-123">An in-memory schema cache used to store the parsed schema files, which include all property descriptions introduced to the subsystem.</span></span> <span data-ttu-id="23492-124">Il n’est pas nécessaire de réanalyser les fichiers de configuration. propDesc qui décrivent le schéma.</span><span class="sxs-lookup"><span data-stu-id="23492-124">There is no need to reparse the .propdesc config files that describe the schema.</span></span> <span data-ttu-id="23492-125">Pour plus d’informations, consultez [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)et [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span><span class="sxs-lookup"><span data-stu-id="23492-125">For more information, see [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema), and [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).</span></span>
-   <span data-ttu-id="23492-126">Objet de sous-système qui implémente [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), qui est utilisé pour obtenir ou utiliser des descriptions de propriété.</span><span class="sxs-lookup"><span data-stu-id="23492-126">A subsystem object that implements [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), which is used to obtain or work with property descriptions.</span></span>
-   <span data-ttu-id="23492-127">Objet de sous-système qui implémente [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), qui est utilisé pour informer et utiliser en fonction d’une description de propriété.</span><span class="sxs-lookup"><span data-stu-id="23492-127">A subsystem object that implements [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), which is used to inform and operate based on a property description.</span></span>
-   <span data-ttu-id="23492-128">Objet de sous-système qui implémente [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), qui est utilisé comme collection de descriptions de propriété.</span><span class="sxs-lookup"><span data-stu-id="23492-128">A subsystem object that implements [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which is used as a collection of property descriptions.</span></span>

> [!Note]  
> <span data-ttu-id="23492-129">Vous devez ajouter `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` à l’élément de schéma racine de vos fichiers. propDesc.</span><span class="sxs-lookup"><span data-stu-id="23492-129">You must add `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` to the root schema element of your .propdesc files.</span></span>

 

## <a name="why-use-a-schema"></a><span data-ttu-id="23492-130">Pourquoi utiliser un schéma ?</span><span class="sxs-lookup"><span data-stu-id="23492-130">Why Use a Schema?</span></span>

<span data-ttu-id="23492-131">Les propriétés, par elles-mêmes, ne sont pas de type sécurisé.</span><span class="sxs-lookup"><span data-stu-id="23492-131">Properties, by themselves, are not type-safe.</span></span> <span data-ttu-id="23492-132">Un composant peut assigner une valeur numérique à la propriété System. Author, ou un horodatage [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) à la propriété System. Music. AlbumTitle, et, sans aucune autre mise en application ou aide, les magasins de propriétés l’autorisent.</span><span class="sxs-lookup"><span data-stu-id="23492-132">A component can assign a numerical value to the System.Author property, or a [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) date-stamp to the System.Music.AlbumTitle property, and, without any further enforcement or guidance, the property stores will allow it.</span></span> <span data-ttu-id="23492-133">Nous avons donc besoin d’une notion de « schematize » des propriétés, qui nous amène au sous-système de schéma.</span><span class="sxs-lookup"><span data-stu-id="23492-133">So, we needed a notion to "schematize" the properties, which brings us to the schema subsystem.</span></span>

## <a name="what-are-the-major-schema-parts"></a><span data-ttu-id="23492-134">Quelles sont les principales parties du schéma ?</span><span class="sxs-lookup"><span data-stu-id="23492-134">What Are the Major Schema Parts?</span></span>

<span data-ttu-id="23492-135">Le schéma de description de propriété utilisé par le système de propriétés de Shell est constitué d’un seul élément [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) , ainsi que d’un attribut *SchemaVersion* , qui indique la version de ce format de définition de schéma.</span><span class="sxs-lookup"><span data-stu-id="23492-135">The property description schema used by the Shell property system is composed of a single [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) element, as well as a *schemaVersion* attribute, which indicates the version of this schema definition format.</span></span> <span data-ttu-id="23492-136">Remarque : la valeur doit être « 1,0 ».</span><span class="sxs-lookup"><span data-stu-id="23492-136">Note: value must be "1.0".</span></span>


```
<!-- schema -->
    <xs:element name="schema">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescriptionList" minOccurs="1" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="schemaVersion"  type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



<span data-ttu-id="23492-137">Le [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) est composé d’un ou plusieurs éléments [PropertyDescription](./propdesc-schema-propertydescription.md) , ainsi que *d’attributs de serveur et de serveur* de *publication* .</span><span class="sxs-lookup"><span data-stu-id="23492-137">The [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) is composed of one or more [propertyDescription](./propdesc-schema-propertydescription.md) elements, as well as *publisher* and *product* attributes.</span></span>


```
<!-- propertyDescriptionList -->
    <xs:element name="propertyDescriptionList">
      <xs:complexType>
        <xs:sequence>
          <xs:element ref="propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product"   type="xs:string"/>
      </xs:complexType>
    </xs:element>
```



<span data-ttu-id="23492-138">Un [PropertyDescription](./propdesc-schema-propertydescription.md) est composé d’un [searchInfo](./propdesc-schema-searchinfo.md) et de zéro ou d’un élément [labelInfo](./propdesc-schema-labelinfo.md), [TypeInfo](./propdesc-schema-typeinfo.md)et [displayInfo](./propdesc-schema-displayinfo.md) , ainsi que des attributs *formatID*, *propID*, *propstr* et *Name* .</span><span class="sxs-lookup"><span data-stu-id="23492-138">A [propertyDescription](./propdesc-schema-propertydescription.md) is composed of one [searchInfo](./propdesc-schema-searchinfo.md) and zero or one [labelInfo](./propdesc-schema-labelinfo.md), [typeInfo](./propdesc-schema-typeinfo.md), and [displayInfo](./propdesc-schema-displayinfo.md) elements, as well as *formatID*, *propID*, *propstr*, and *name* attributes.</span></span>

<span data-ttu-id="23492-139">Il doit y avoir un élément [PropertyDescription](./propdesc-schema-propertydescription.md) pour chaque nom de propriété canonique unique destiné à être disponible dans le système.</span><span class="sxs-lookup"><span data-stu-id="23492-139">There should be one [propertyDescription](./propdesc-schema-propertydescription.md) element for every unique canonical property name that is intended to be available in the system.</span></span> <span data-ttu-id="23492-140">Les attributs de chaîne ont une limite de 512 caractères.</span><span class="sxs-lookup"><span data-stu-id="23492-140">The string attributes have a limit of 512 characters.</span></span> <span data-ttu-id="23492-141">Les valeurs de plus de 512 caractères sont tronquées.</span><span class="sxs-lookup"><span data-stu-id="23492-141">Values longer than 512 characters are truncated.</span></span>


```
<!-- propertyDescription -->
    <xs:element name="propertyDescription">
      <xs:complexType>
        <xs:all>
          <xs:element name="description"    type="xs:string" minOccurs="0" maxOccurs="1"/>
          <xs:element ref="searchInfo"   minOccurs="1" maxOccurs="1"/>
          <xs:element ref="labelInfo"    minOccurs="0" maxOccurs="1"/>
          <xs:element ref="typeInfo"     minOccurs="0" maxOccurs="1"/>
          <xs:element ref="displayInfo"  minOccurs="0" maxOccurs="1"/>
        </xs:all>
        <xs:attribute name="formatID"  type="upcase-uuid" use="required""/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required""/>
        <xs:attribute name="name"      type="canonical-name" use="required"/>
      </xs:complexType>
    </xs:element>
```



## <a name="changes-for-windows-7"></a><span data-ttu-id="23492-142">Modifications pour Windows 7</span><span class="sxs-lookup"><span data-stu-id="23492-142">Changes for Windows 7</span></span>

<span data-ttu-id="23492-143">Le schéma de description de la propriété a été modifié pour Windows 7.</span><span class="sxs-lookup"><span data-stu-id="23492-143">The property description schema has been changed for Windows 7.</span></span> <span data-ttu-id="23492-144">Il s’agit de modifications sans rupture.</span><span class="sxs-lookup"><span data-stu-id="23492-144">These are non-breaking changes.</span></span> <span data-ttu-id="23492-145">Si un élément ou un attribut de propriété n’est plus pris en charge dans Windows 7, le système d’exploitation Windows 7 ignore l’élément ou les attributs Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="23492-145">If a property element or attribute is no longer supported in Windows 7, the Windows 7 operating system ignores the Windows Vista element or attributes.</span></span> <span data-ttu-id="23492-146">De même, Windows Vista ignore également les nouveaux attributs ou éléments de propriété de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="23492-146">Similarly, Windows Vista ignores new Windows 7 property elements or attributes as well.</span></span>

<span data-ttu-id="23492-147">Toutefois, il est recommandé de mettre à jour les propriétés personnalisées de Windows 7 pour une expérience utilisateur optimale et plus cohérente.</span><span class="sxs-lookup"><span data-stu-id="23492-147">However, updating custom properties for Windows 7 is recommended for a better and more consistent user experience.</span></span>

<span data-ttu-id="23492-148">Les nouveaux éléments et attributs sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="23492-148">The following are new elements and attributes:</span></span>

-   <span data-ttu-id="23492-149">éléments [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) et [relatedProperty](./propdesc-schema-relatedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="23492-149">[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) and [relatedProperty](./propdesc-schema-relatedproperty.md) elements</span></span>
-   <span data-ttu-id="23492-150">élément [image](./propdesc-schema-image.md)</span><span class="sxs-lookup"><span data-stu-id="23492-150">[image](./propdesc-schema-image.md) element</span></span>
-   <span data-ttu-id="23492-151">mnémoniques, attribut de l’élément [searchInfo](./propdesc-schema-searchinfo.md)</span><span class="sxs-lookup"><span data-stu-id="23492-151">mnemonics attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>
-   <span data-ttu-id="23492-152">mnémoniques, attribut de l’élément [enum](./propdesc-schema-enum.md)</span><span class="sxs-lookup"><span data-stu-id="23492-152">mnemonics attribute of the [enum](./propdesc-schema-enum.md) element</span></span>
-   <span data-ttu-id="23492-153">attribut searchRawValue de l’élément [TypeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="23492-153">searchRawValue attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

<span data-ttu-id="23492-154">Les éléments et attributs suivants ont été modifiés :</span><span class="sxs-lookup"><span data-stu-id="23492-154">The following elements and attributes have changed:</span></span>

-   <span data-ttu-id="23492-155">éléments [enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md)et [enumRange](./propdesc-schema-enumrange.md)</span><span class="sxs-lookup"><span data-stu-id="23492-155">[enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md), and [enumRange](./propdesc-schema-enumrange.md) elements</span></span>
-   <span data-ttu-id="23492-156">élément [drawControl](./propdesc-schema-drawcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="23492-156">[drawControl](./propdesc-schema-drawcontrol.md) element</span></span>
-   <span data-ttu-id="23492-157">élément [editControl](./propdesc-schema-editcontrol.md)</span><span class="sxs-lookup"><span data-stu-id="23492-157">[editControl](./propdesc-schema-editcontrol.md) element</span></span>
-   <span data-ttu-id="23492-158">attribut propID de l’élément [PropertyDescription](./propdesc-schema-propertydescription.md)</span><span class="sxs-lookup"><span data-stu-id="23492-158">propID attribute of the [propertyDescription](./propdesc-schema-propertydescription.md) element</span></span>
-   <span data-ttu-id="23492-159">attribut columnIndexType de l’élément [searchInfo](./propdesc-schema-searchinfo.md)</span><span class="sxs-lookup"><span data-stu-id="23492-159">columnIndexType attribute of the [searchInfo](./propdesc-schema-searchinfo.md) element</span></span>

<span data-ttu-id="23492-160">Les éléments et attributs suivants ont été supprimés :</span><span class="sxs-lookup"><span data-stu-id="23492-160">The following elements and attributes have been removed:</span></span>

-   <span data-ttu-id="23492-161">élément [queryControl](./propdesc-schema-querycontrol.md)</span><span class="sxs-lookup"><span data-stu-id="23492-161">[queryControl](./propdesc-schema-querycontrol.md) element</span></span>
-   <span data-ttu-id="23492-162">attribut isQueryable de l’élément [TypeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="23492-162">isQueryable attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>
-   <span data-ttu-id="23492-163">attribut includeInFullTextQuery de l’élément [TypeInfo](./propdesc-schema-typeinfo.md)</span><span class="sxs-lookup"><span data-stu-id="23492-163">includeInFullTextQuery attribute of the [typeInfo](./propdesc-schema-typeinfo.md) element</span></span>

## <a name="related-topics"></a><span data-ttu-id="23492-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23492-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23492-165">propertyDescription</span><span class="sxs-lookup"><span data-stu-id="23492-165">propertyDescription</span></span>](./propdesc-schema-propertydescription.md)
</dt> <dt>

[<span data-ttu-id="23492-166">searchInfo</span><span class="sxs-lookup"><span data-stu-id="23492-166">searchInfo</span></span>](./propdesc-schema-searchinfo.md)
</dt> <dt>

[<span data-ttu-id="23492-167">labelInfo</span><span class="sxs-lookup"><span data-stu-id="23492-167">labelInfo</span></span>](./propdesc-schema-labelinfo.md)
</dt> <dt>

[<span data-ttu-id="23492-168">typeInfo</span><span class="sxs-lookup"><span data-stu-id="23492-168">typeInfo</span></span>](./propdesc-schema-typeinfo.md)
</dt> <dt>

[<span data-ttu-id="23492-169">displayInfo</span><span class="sxs-lookup"><span data-stu-id="23492-169">displayInfo</span></span>](./propdesc-schema-displayinfo.md)
</dt> <dt>

[<span data-ttu-id="23492-170">stringFormat</span><span class="sxs-lookup"><span data-stu-id="23492-170">stringFormat</span></span>](./propdesc-schema-stringformat.md)
</dt> <dt>

[<span data-ttu-id="23492-171">booleanFormat</span><span class="sxs-lookup"><span data-stu-id="23492-171">booleanFormat</span></span>](./propdesc-schema-booleanformat.md)
</dt> <dt>

[<span data-ttu-id="23492-172">numberFormat</span><span class="sxs-lookup"><span data-stu-id="23492-172">numberFormat</span></span>](./propdesc-schema-numberformat.md)
</dt> <dt>

[<span data-ttu-id="23492-173">dateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="23492-173">dateTimeFormat</span></span>](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[<span data-ttu-id="23492-174">enumeratedList</span><span class="sxs-lookup"><span data-stu-id="23492-174">enumeratedList</span></span>](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[<span data-ttu-id="23492-175">drawControl</span><span class="sxs-lookup"><span data-stu-id="23492-175">drawControl</span></span>](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[<span data-ttu-id="23492-176">editControl</span><span class="sxs-lookup"><span data-stu-id="23492-176">editControl</span></span>](./propdesc-schema-editcontrol.md)
</dt> <dt>

[<span data-ttu-id="23492-177">filterControl</span><span class="sxs-lookup"><span data-stu-id="23492-177">filterControl</span></span>](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[<span data-ttu-id="23492-178">queryControl</span><span class="sxs-lookup"><span data-stu-id="23492-178">queryControl</span></span>](./propdesc-schema-querycontrol.md)
</dt> <dt>

[<span data-ttu-id="23492-179">image</span><span class="sxs-lookup"><span data-stu-id="23492-179">image</span></span>](./propdesc-schema-image.md)
</dt> </dl>

 

 
