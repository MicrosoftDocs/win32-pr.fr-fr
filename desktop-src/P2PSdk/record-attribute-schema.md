---
description: Les enregistrements peuvent avoir des attributs spécifiques à l’application qui sont une séquence de paires nom/valeur représentées sous la forme d’une chaîne XML dans le membre pszAttributes de la structure d’enregistrement d’HOMOLOGUe \_ .
ms.assetid: 2991af9b-da32-4915-b4d6-575e3faac04e
title: Schéma d’attribut d’enregistrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa8c4c8b00b09e9c8cb988088af645e9f9c967
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520115"
---
# <a name="record-attribute-schema"></a>Schéma d’attribut d’enregistrement

Les enregistrements peuvent avoir des attributs spécifiques à l’application qui sont une séquence de paires nom/valeur représentées sous la forme d’une chaîne XML dans le membre **pszAttributes** de la structure d' [**\_ enregistrement d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Les attributs sont utilisés pour filtrer une recherche d’enregistrements initiée par des appels à [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), qui prend un filtre de recherche XML spécifié dans le [format de requête de recherche d’enregistrements](record-search-query-format.md) en tant que paramètre.

Un attribut d’enregistrement peut être de l’un des trois types suivants :

-   **int** est une valeur entière.
-   la **Date** est une valeur DateTime représentée dans l’un des formats standard décrits dans [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .
-   la **chaîne** est une valeur de chaîne Unicode.

La liste suivante identifie les noms d’attributs spécifiques qui sont réservés par l’infrastructure homologue :

-   **peerlastmodifiedby**
-   **peercreatorid**
-   **peerlastmodificationtime**
-   **peerrecordid**
-   **peerrecordtype**
-   **peercreationtime**
-   **peerlastmodificationtime**

## <a name="example-of-defining-record-attributes"></a>Exemple de définition d’attributs d’enregistrement

L’exemple de schéma suivant montre comment définir des attributs d’enregistrement :

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema">
   <xs:simpleType name="alphanum">
       <xs:restriction base="xs:string">
          <xs:pattern value="\c+" />
       </xs:restriction>
   </xs:simpleType>
   <xs:complexType name="attributeType">
       <xs:simpleContent>
          <xs:extension base="xs:string">
                <xs:attribute name="name" type="alphanum" />
                <xs:attribute name="type">
                    <xs:simpleType>
                        <xs:restriction base="alphanum">
                           <xs:enumeration value="string"/>
                           <xs:enumeration value="date"/>
                           <xs:enumeration value="int"/>
                        </xs:restriction>
                    </xs:simpleType>
                </xs:attribute>
           </xs:extension>
       </xs:simpleContent>
    </xs:complexType>
    <xs:element name="attributes">
       <xs:complexType>
           <xs:sequence>
                <xs:element name="attribute" type="attributeType" minOccurs="0" maxOccurs="unbounded" />
           </xs:sequence>
       </xs:complexType>
    </xs:element>
</xs:schema>  
```

> [!Note]  
> Les noms d’attributs doivent être des séquences de caractères alphanumériques. Les caractères spéciaux tels que les tirets (« - ») et les traits de soulignement (« \_ ») ne sont pas autorisés dans un nom d’attribut.

 

L’exemple suivant de séquence d’attribut XML contient les attributs **AuthenticationType** et **AuthExpires** personnalisés qui s’affichent dans le membre **pszAttributes** de l' [**\_ enregistrement homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record).

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



