---
description: Cette rubrique présente le schéma de description de propriété utilisé par le système de propriétés de Shell.
ms.assetid: cac93c31-d90d-4116-b846-0cf593d1d56e
title: Présentation du schéma de description de propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85dbb0f20c5c4a206069e80aa308a26908bf90ee0d00cf80712a342e834411e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554559"
---
# <a name="understanding-the-property-description-schema"></a>Présentation du schéma de description de propriété

Cette rubrique présente le schéma de description de propriété utilisé par le système de propriétés de Shell.

l’introduction de nouvelles fonctionnalités pour Windows Vista et versions ultérieures nécessitait l’extension du système de propriétés de Shell existant pour :

-   Prendre en charge un système de description de propriété riche et extensible qui fournit des informations sur les propriétés, y compris les noms d’affichage, le type, le type d’affichage, le comportement de tri et de groupe et d’autres attributs nécessaires pour présenter et utiliser les propriétés.
-   Prenez en charge une liste de types de propriété (associée à l’interface utilisateur qui peut modifier ces types dans différents affichages, tels que ListView, volet de visualisation, boîtes de dialogue de propriétés, etc.) qui peuvent être associées à différentes propriétés.
-   Fournissez des listes de description de la propriété, qui définissent l’ensemble des propriétés affichées dans différents affichages.
-   Fournir une interface simplifiée, [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore), afin que les gestionnaires de propriétés puissent être écrits plus facilement et que les propriétés puissent être conservées dans des fichiers.
-   Prise en charge des gestionnaires de propriétés non-fichiers pour exposer des propriétés dans la vue.

Ces fonctionnalités sont obtenues sur une architecture qui fournit un accès abstrait aux propriétés d’un élément de Shell. Cette abstraction est appelée système de propriétés de Shell.

-   [Qu’est-ce que le schéma de description de propriété ?](#what-is-the-property-description-schema)
-   [Pourquoi utiliser un schéma ?](#why-use-a-schema)
-   [Quelles sont les principales parties du schéma ?](#what-are-the-major-schema-parts)
-   [modifications pour Windows 7](#changes-for-windows-7)
-   [Rubriques connexes](#related-topics)

## <a name="what-is-the-property-description-schema"></a>Qu’est-ce que le schéma de description de propriété ?

Le sous-système de schéma se compose des éléments suivants :

-   Un ou plusieurs fichiers de schéma. propDesc qui définissent les descriptions des propriétés. Le schéma de description de propriété est défini dans une collection de fichiers de schéma XML (à l’aide de l’extension de fichier. propDesc) au moment de l’exécution sur le système. Ces fichiers sont chargés en différé quand une partie du système de propriétés les requiert.
-   Cache de schéma en mémoire utilisé pour stocker les fichiers de schéma analysés, qui incluent toutes les descriptions de propriété introduites dans le sous-système. Il n’est pas nécessaire de réanalyser les fichiers de configuration. propDesc qui décrivent le schéma. Pour plus d’informations, consultez [**PSRegisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema), [**PSUnregisterPropertySchema**](/windows/win32/api/propsys/nf-propsys-psunregisterpropertyschema)et [**PSRefreshPropertySchema**](/windows/win32/api/propsys/nf-propsys-psrefreshpropertyschema).
-   Objet de sous-système qui implémente [**IPropertySystem**](/windows/win32/api/propsys/nn-propsys-ipropertysystem), qui est utilisé pour obtenir ou utiliser des descriptions de propriété.
-   Objet de sous-système qui implémente [**IPropertyDescription**](/windows/win32/api/propsys/nn-propsys-ipropertydescription), qui est utilisé pour informer et utiliser en fonction d’une description de propriété.
-   Objet de sous-système qui implémente [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), qui est utilisé comme collection de descriptions de propriété.

> [!Note]  
> Vous devez ajouter `xmlns=http://schemas.microsoft.com/windows/2006/propertydescription` à l’élément de schéma racine de vos fichiers. propDesc.

 

## <a name="why-use-a-schema"></a>Pourquoi utiliser un schéma ?

Les propriétés, par elles-mêmes, ne sont pas de type sécurisé. Un composant peut affecter une valeur numérique à la propriété System. Author ou à un horodatage [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) sur le système. Musique. La propriété AlbumTitle et, sans aucune autre contrainte ou aide, les magasins de propriétés l’autorisent. Nous avons donc besoin d’une notion de « schematize » des propriétés, qui nous amène au sous-système de schéma.

## <a name="what-are-the-major-schema-parts"></a>Quelles sont les principales parties du schéma ?

Le schéma de description de propriété utilisé par le système de propriétés de Shell est constitué d’un seul élément [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) , ainsi que d’un attribut *SchemaVersion* , qui indique la version de ce format de définition de schéma. Remarque : la valeur doit être « 1,0 ».


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



Le [propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md) est composé d’un ou plusieurs éléments [PropertyDescription](./propdesc-schema-propertydescription.md) , ainsi que *d’attributs de serveur et de serveur* de *publication* .


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



Un [PropertyDescription](./propdesc-schema-propertydescription.md) est composé d’un [searchInfo](./propdesc-schema-searchinfo.md) et de zéro ou d’un élément [labelInfo](./propdesc-schema-labelinfo.md), [TypeInfo](./propdesc-schema-typeinfo.md)et [displayInfo](./propdesc-schema-displayinfo.md) , ainsi que des attributs *formatID*, *propID*, *propstr* et *Name* .

Il doit y avoir un élément [PropertyDescription](./propdesc-schema-propertydescription.md) pour chaque nom de propriété canonique unique destiné à être disponible dans le système. Les attributs de chaîne ont une limite de 512 caractères. Les valeurs de plus de 512 caractères sont tronquées.


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



## <a name="changes-for-windows-7"></a>modifications pour Windows 7

le schéma de description de la propriété a été modifié pour Windows 7. Il s’agit de modifications sans rupture. si un élément ou un attribut de propriété n’est plus pris en charge dans Windows 7, le système d’exploitation Windows 7 ignore l’élément ou les attributs Windows Vista. de même, Windows Vista ignore également les nouveaux attributs ou éléments de propriété de Windows 7.

toutefois, il est recommandé de mettre à jour les propriétés personnalisées de Windows 7 pour une expérience utilisateur optimale et plus cohérente.

Les nouveaux éléments et attributs sont les suivants :

-   éléments [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) et [relatedProperty](./propdesc-schema-relatedproperty.md)
-   élément [image](./propdesc-schema-image.md)
-   mnémoniques, attribut de l’élément [searchInfo](./propdesc-schema-searchinfo.md)
-   mnémoniques, attribut de l’élément [enum](./propdesc-schema-enum.md)
-   attribut searchRawValue de l’élément [TypeInfo](./propdesc-schema-typeinfo.md)

Les éléments et attributs suivants ont été modifiés :

-   éléments [enumeratedList](./propdesc-schema-enumeratedlist.md), [enum](./propdesc-schema-enum.md)et [enumRange](./propdesc-schema-enumrange.md)
-   élément [drawControl](./propdesc-schema-drawcontrol.md)
-   élément [editControl](./propdesc-schema-editcontrol.md)
-   attribut propID de l’élément [PropertyDescription](./propdesc-schema-propertydescription.md)
-   attribut columnIndexType de l’élément [searchInfo](./propdesc-schema-searchinfo.md)

Les éléments et attributs suivants ont été supprimés :

-   élément [queryControl](./propdesc-schema-querycontrol.md)
-   attribut isQueryable de l’élément [TypeInfo](./propdesc-schema-typeinfo.md)
-   attribut includeInFullTextQuery de l’élément [TypeInfo](./propdesc-schema-typeinfo.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> </dl>

 

 
