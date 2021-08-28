---
description: L' &lt; élément de propriété facultatif &gt; spécifie une propriété utilisée par le connecteur de recherche. Ces propriétés étant spécifiques à ce connecteur de recherche, il n’existe aucun ensemble prédéfini de noms à utiliser. Cet élément n’a pas d’éléments enfants.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Élément Property de propertyStore (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ad97c22ac87d67fdec0d007d4333bffe16aad1
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886775"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a>Élément Property de propertyStore (schéma du connecteur de recherche)

L' &lt; élément de propriété facultatif &gt; spécifie une propriété utilisée par le connecteur de recherche. Ces propriétés étant spécifiques à ce connecteur de recherche, il n’existe aucun ensemble prédéfini de noms à utiliser. Cet élément n’a pas d’éléments enfants.

## <a name="syntax"></a>Syntaxe


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



## <a name="element-information"></a>Informations sur les éléments



| Élément parent                                                                           | Éléments enfants |
|------------------------------------------------------------------------------------------|----------------|
| [Élément propertyStore (schéma du connecteur de recherche)](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a>Attributs




| Attribut | Description | Valeurs | 
|-----------|-------------|--------|
| name | Public. Obligatoire. Le nom complet de la propriété. |   | 
| type | Public. Obligatoire. Type de propriété. | Any : valeur par défaut. La valeur ne sera pas forcée par le sous-système de propriété. VT_NULL est retourné par GetPropertyType.<ul><li>NULL : il n’y a aucune valeur pour cette propriété. VT_NULL est retourné par GetPropertyType.</li><li>Chaîne : la valeur doit être un VT_LPWSTR.</li><li>Booléen : la valeur doit être un VT_BOOL.</li><li>Byte : la valeur doit être un VT_UI1.</li><li>Buffer : la valeur doit être un VT_UI1 | Mémoire tampon d’octets VT_VECTOR.</li><li>Int16 : la valeur doit être un VT_I2.</li><li>UInt16 : la valeur doit être un VT_UI2.</li><li>Int32 : la valeur doit être un VT_I4.</li><li>UInt32 : la valeur doit être un VT_UI4.</li><li>Int64 : la valeur doit être un VT_I8.</li><li>UInt64 : la valeur doit être un VT_UI8</li><li>Double : la valeur doit être un VT_R8.</li><li>DateTime : la valeur doit être un VT_FILETIME.</li><li>GUID : la valeur doit être un VT_CLSID.</li><li>Objet BLOB : la valeur doit être un VT_BLOB.</li><li>Objet : la valeur doit être un VT_UNKNOWN.</li><li>Stream : la valeur doit être un VT_STREAM.</li><li>Presse-papiers : la valeur doit être un VT_CF.</li></ul> | 
| schéma | Public. Facultatif. Schéma dans lequel la propriété est définie. |   | 




 

## <a name="remarks"></a>Remarques

OpenSearch les connecteurs de recherche peuvent utiliser la propriété OpenSearchHTMLRolloverTemplate. cette propriété identifie un modèle mis en forme selon la convention de modèle OpenSearch. Le modèle OpenSearchHTMLRolloverTemplate est utilisé lorsque l’utilisateur clique sur le bouton « Rechercher sur le site Web » dans la barre de commandes.

## <a name="example"></a>Exemple

L’exemple suivant montre un &lt; &gt; élément propertyStore avec deux &lt; éléments de propriété &gt; .


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



