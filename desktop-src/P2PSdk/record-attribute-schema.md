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
# <a name="record-attribute-schema"></a><span data-ttu-id="7ff10-103">Schéma d’attribut d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="7ff10-103">Record Attribute Schema</span></span>

<span data-ttu-id="7ff10-104">Les enregistrements peuvent avoir des attributs spécifiques à l’application qui sont une séquence de paires nom/valeur représentées sous la forme d’une chaîne XML dans le membre **pszAttributes** de la structure d' [**\_ enregistrement d’homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record) .</span><span class="sxs-lookup"><span data-stu-id="7ff10-104">Records can have application-specific attributes that are a sequence of name or value pairs represented as an XML string in the **pszAttributes** member of the [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record) structure.</span></span> <span data-ttu-id="7ff10-105">Les attributs sont utilisés pour filtrer une recherche d’enregistrements initiée par des appels à [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), qui prend un filtre de recherche XML spécifié dans le [format de requête de recherche d’enregistrements](record-search-query-format.md) en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="7ff10-105">The attributes are used to filter a record search initiated by calls to [**PeerGroupSearchRecords**](/windows/desktop/api/P2P/nf-p2p-peergroupsearchrecords), which takes an XML search filter specified in [Record Search Query Format](record-search-query-format.md) as a parameter.</span></span>

<span data-ttu-id="7ff10-106">Un attribut d’enregistrement peut être de l’un des trois types suivants :</span><span class="sxs-lookup"><span data-stu-id="7ff10-106">A record attribute can be one of the following three types:</span></span>

-   <span data-ttu-id="7ff10-107">**int** est une valeur entière.</span><span class="sxs-lookup"><span data-stu-id="7ff10-107">**int** is an integer value.</span></span>
-   <span data-ttu-id="7ff10-108">la **Date** est une valeur DateTime représentée dans l’un des formats standard décrits dans [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime) .</span><span class="sxs-lookup"><span data-stu-id="7ff10-108">**date** is a datetime value represented as one of the standard formats described at [https://www.w3.org/TR/NOTE-datetime](https://www.w3.org/TR/NOTE-datetime).</span></span>
-   <span data-ttu-id="7ff10-109">la **chaîne** est une valeur de chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="7ff10-109">**string** is a Unicode string value.</span></span>

<span data-ttu-id="7ff10-110">La liste suivante identifie les noms d’attributs spécifiques qui sont réservés par l’infrastructure homologue :</span><span class="sxs-lookup"><span data-stu-id="7ff10-110">The following list identifies the specific attribute names that are reserved by the Peer Infrastructure:</span></span>

-   <span data-ttu-id="7ff10-111">**peerlastmodifiedby**</span><span class="sxs-lookup"><span data-stu-id="7ff10-111">**peerlastmodifiedby**</span></span>
-   <span data-ttu-id="7ff10-112">**peercreatorid**</span><span class="sxs-lookup"><span data-stu-id="7ff10-112">**peercreatorid**</span></span>
-   <span data-ttu-id="7ff10-113">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="7ff10-113">**peerlastmodificationtime**</span></span>
-   <span data-ttu-id="7ff10-114">**peerrecordid**</span><span class="sxs-lookup"><span data-stu-id="7ff10-114">**peerrecordid**</span></span>
-   <span data-ttu-id="7ff10-115">**peerrecordtype**</span><span class="sxs-lookup"><span data-stu-id="7ff10-115">**peerrecordtype**</span></span>
-   <span data-ttu-id="7ff10-116">**peercreationtime**</span><span class="sxs-lookup"><span data-stu-id="7ff10-116">**peercreationtime**</span></span>
-   <span data-ttu-id="7ff10-117">**peerlastmodificationtime**</span><span class="sxs-lookup"><span data-stu-id="7ff10-117">**peerlastmodificationtime**</span></span>

## <a name="example-of-defining-record-attributes"></a><span data-ttu-id="7ff10-118">Exemple de définition d’attributs d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="7ff10-118">Example of Defining Record Attributes</span></span>

<span data-ttu-id="7ff10-119">L’exemple de schéma suivant montre comment définir des attributs d’enregistrement :</span><span class="sxs-lookup"><span data-stu-id="7ff10-119">The following schema example shows you how to define record attributes:</span></span>

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
> <span data-ttu-id="7ff10-120">Les noms d’attributs doivent être des séquences de caractères alphanumériques.</span><span class="sxs-lookup"><span data-stu-id="7ff10-120">Attribute names must be sequences of alphanumeric characters.</span></span> <span data-ttu-id="7ff10-121">Les caractères spéciaux tels que les tirets (« - ») et les traits de soulignement (« \_ ») ne sont pas autorisés dans un nom d’attribut.</span><span class="sxs-lookup"><span data-stu-id="7ff10-121">Special characters like hyphens ("-") and underscores ("\_") are not allowed in an attribute name.</span></span>

 

<span data-ttu-id="7ff10-122">L’exemple suivant de séquence d’attribut XML contient les attributs **AuthenticationType** et **AuthExpires** personnalisés qui s’affichent dans le membre **pszAttributes** de l' [**\_ enregistrement homologue**](/windows/desktop/api/P2P/ns-p2p-peer_record).</span><span class="sxs-lookup"><span data-stu-id="7ff10-122">The following example of an XML attribute sequence contains the custom **AuthenticationType** and **AuthExpires** attributes that appear in the **pszAttributes** member of [**PEER\_RECORD**](/windows/desktop/api/P2P/ns-p2p-peer_record).</span></span>

``` syntax
<attributes>
  <attribute name="AuthenticationType" type="string">Kerberos</attribute><attribute name="AuthExpires" type="date">2002-01-31</attribute>
<attributes>
```

 

 



