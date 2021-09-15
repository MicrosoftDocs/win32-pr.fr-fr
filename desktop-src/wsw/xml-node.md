---
title: Nœud XML
description: Un nœud XML représente un élément XML unique, par exemple, un élément de début et ses attributs, un élément de fin, du texte ou \ 0034 ; typé \ 0034 ; contenu de texte, tel qu’un entier ou un tableau d’octets. Les données d’un nœud varient en fonction du \_ type de \_ nœud XML WS \_ .
ms.assetid: c514c542-029b-46d1-a796-1f132a41b2ad
keywords:
- Services Web de nœud XML pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac212205fac02db0ee87d8acbe0b123ffcead921
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521988"
---
# <a name="xml-node"></a>Nœud XML

Un nœud XML représente un élément XML unique, par exemple, un élément de début et ses attributs, un élément de fin, du texte ou un contenu de texte « typé », tel qu’un entier ou un tableau d’octets. Les données d’un nœud varient en fonction du [**\_ type de \_ nœud \_ XML WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).


L’exemple suivant illustre un document XML spécifique à l’encodage représenté par des structures indépendantes de l’encodage.

``` syntax
<p:PurchaseOrder xmlns:p="http://tempuri.org" p:id="3891">
    <p:Buyer>Joe</p:Buyer>
</p:PurchaseOrder>
```

``` syntax
WS_XML_STRING purchaseOrder = WS_XML_STRING_VALUE("PurchaseOrder");
WS_XML_STRING id            = WS_XML_STRING_VALUE("id");
WS_XML_STRING prefix        = WS_XML_STRING_VALUE("p");
WS_XML_STRING ns            = WS_XML_STRING_VALUE("http://tempuri.org");

WS_XML_ATTRIBUTE xmlnsAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ TRUE,
    /* prefix      */ &prefix,
    /* localName   */ NULL,
    /* ns          */ &ns,
    /* value       */ NULL
};
WS_XML_INT32_TEXT idText =
{
    /* text  */ { WS_XML_TEXT_TYPE_INT32 },
    /* value */ 3891
};
WS_XML_ATTRIBUTE idAttribute =
{
    /* singleQuote */ FALSE,
    /* isXmlNs     */ FALSE,
    /* prefix      */ &prefix,
    /* localName   */ &id,
    /* ns          */ &ns,
    /* value       */ &idText.text,
};
WS_XML_ATTRIBUTE* attributes[2] =
{
    &xmlnsAttribute,
    &idAttribute
};
WS_XML_ELEMENT_NODE elementNode =
{
    /* node           */ { WS_XML_NODE_TYPE_ELEMENT },
    /* prefix         */ &prefix,
    /* localName      */ &purchaseOrder,
    /* ns             */ &ns,
    /* attributeCount */ 2,
    /* attributes     */ attributes,
    /* isEmpty        */ FALSE,
    /* array          */ NULL,
};
WS_XML_UTF8_TEXT joeText =
{
    /* text  */ { WS_XML_TEXT_TYPE_UTF8 },
    /* value */ WS_XML_STRING_VALUE("Joe")
};
WS_XML_TEXT_NODE textNode =
{
    /* node */ { WS_XML_NODE_TYPE_TEXT },
    /* text */ &joeText.text
};
WS_XML_NODE endElementNode =
{
    WS_XML_NODE_TYPE_END_ELEMENT
};
WS_XML_NODE* nodes[3] =
{
    &elementNode.node,
    &textNode.node,
    &endElementNode
};
```

Les énumérations suivantes sont utilisées avec les nœuds XML :

-   [**\_type de valeur WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [**\_type de \_ nœud \_ XML WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [**\_type de \_ texte \_ XML WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

Les fonctions suivantes sont utilisées avec les nœuds XML :

-   [**WsTrimXmlWhitespace**](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [**WsVerifyXmlNCName**](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [**WsXmlStringEquals**](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

Les macros suivantes sont utilisées avec les nœuds XML :

-   [**\_valeur du \_ dictionnaire de chaînes XML \_ WS \_**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   [**\_chaîne XML \_ WS \_ null**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))
-   [**\_valeur de \_ chaîne WS XML \_**](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

Les structures suivantes sont utilisées avec les nœuds XML :

-   [**\_attribut XML \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [**\_ \_ Texte base64 WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [**\_ \_ texte bool XML \_ bool**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [**\_nœud de \_ Commentaires \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [**\_texte de \_ date/heure XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [**\_ \_ texte décimal WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [**\_dictionnaire XML \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [**\_ \_ texte double WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [**\_nœud d' \_ élément \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [**\_ \_ texte flottant WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [**\_texte du \_ GUID WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [**\_ \_ Texte Int32 XML \_ Int32**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [**\_ \_ Texte Int64 XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [**\_texte de \_ liste \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [**\_nœud XML \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [**\_QName XML \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [**\_ \_ texte QName XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [**\_chaîne XML \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [**\_texte XML \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [**\_nœud de \_ texte \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [**\_texte de \_ TIMESPAN \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [**\_Texte WS XML \_ UINT64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [**\_texte de \_ l' \_ ID \_ unique WS XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [**WS \_ XML \_ , \_ texte UTF16**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [**\_ \_ Texte UTF8 XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 