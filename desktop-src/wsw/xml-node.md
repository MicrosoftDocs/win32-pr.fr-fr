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
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "106511329"
---
# <a name="xml-node"></a><span data-ttu-id="829fe-107">Nœud XML</span><span class="sxs-lookup"><span data-stu-id="829fe-107">XML Node</span></span>

<span data-ttu-id="829fe-108">Un nœud XML représente un élément XML unique, par exemple, un élément de début et ses attributs, un élément de fin, du texte ou un contenu de texte « typé », tel qu’un entier ou un tableau d’octets.</span><span class="sxs-lookup"><span data-stu-id="829fe-108">An XML Node represents a single piece of XML, for example, a start element and its attributes, an end element, text, or "typed" text content such as an integer or byte array.</span></span> <span data-ttu-id="829fe-109">Les données d’un nœud varient en fonction du [**\_ type de \_ nœud \_ XML WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span><span class="sxs-lookup"><span data-stu-id="829fe-109">The data in a node varies according to the [**WS\_XML\_NODE\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type).</span></span>


<span data-ttu-id="829fe-110">L’exemple suivant illustre un document XML spécifique à l’encodage représenté par des structures indépendantes de l’encodage.</span><span class="sxs-lookup"><span data-stu-id="829fe-110">The following shows an example of an encoding specific xml document represented with encoding independent structures.</span></span>

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

<span data-ttu-id="829fe-111">Les énumérations suivantes sont utilisées avec les nœuds XML :</span><span class="sxs-lookup"><span data-stu-id="829fe-111">The following enumerations are used with XML nodes:</span></span>

-   [<span data-ttu-id="829fe-112">**\_type de valeur WS \_**</span><span class="sxs-lookup"><span data-stu-id="829fe-112">**WS\_VALUE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_value_type)
-   [<span data-ttu-id="829fe-113">**\_type de \_ nœud \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-113">**WS\_XML\_NODE\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_node_type)
-   [<span data-ttu-id="829fe-114">**\_type de \_ texte \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-114">**WS\_XML\_TEXT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_text_type)

<span data-ttu-id="829fe-115">Les fonctions suivantes sont utilisées avec les nœuds XML :</span><span class="sxs-lookup"><span data-stu-id="829fe-115">The following functions are used with XML nodes:</span></span>

-   [<span data-ttu-id="829fe-116">**WsTrimXmlWhitespace**</span><span class="sxs-lookup"><span data-stu-id="829fe-116">**WsTrimXmlWhitespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wstrimxmlwhitespace)
-   [<span data-ttu-id="829fe-117">**WsVerifyXmlNCName**</span><span class="sxs-lookup"><span data-stu-id="829fe-117">**WsVerifyXmlNCName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsverifyxmlncname)
-   [<span data-ttu-id="829fe-118">**WsXmlStringEquals**</span><span class="sxs-lookup"><span data-stu-id="829fe-118">**WsXmlStringEquals**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsxmlstringequals)

<span data-ttu-id="829fe-119">Les macros suivantes sont utilisées avec les nœuds XML :</span><span class="sxs-lookup"><span data-stu-id="829fe-119">The following macros are used with XML nodes:</span></span>

-   [<span data-ttu-id="829fe-120">**\_valeur du \_ dictionnaire de chaînes XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="829fe-120">**WS\_XML\_STRING\_DICTIONARY\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_dictionary_value)
-   <span data-ttu-id="829fe-121">[**\_chaîne XML \_ WS \_ null**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="829fe-121">[**WS\_XML\_STRING\_NULL**](/previous-versions/windows/desktop/legacy/dd323562(v=vs.85))</span></span>
-   [<span data-ttu-id="829fe-122">**\_valeur de \_ chaîne WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="829fe-122">**WS\_XML\_STRING\_VALUE**</span></span>](/windows/desktop/api/WebServices/nf-webservices-ws_xml_string_value)

<span data-ttu-id="829fe-123">Les structures suivantes sont utilisées avec les nœuds XML :</span><span class="sxs-lookup"><span data-stu-id="829fe-123">The following structures are used with XML nodes:</span></span>

-   [<span data-ttu-id="829fe-124">**\_attribut XML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-124">**WS\_XML\_ATTRIBUTE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_attribute)
-   [<span data-ttu-id="829fe-125">**\_ \_ Texte base64 WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="829fe-125">**WS\_XML\_BASE64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_base64_text)
-   [<span data-ttu-id="829fe-126">**\_ \_ texte bool XML \_ bool**</span><span class="sxs-lookup"><span data-stu-id="829fe-126">**WS\_XML\_BOOL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_bool_text)
-   [<span data-ttu-id="829fe-127">**\_nœud de \_ Commentaires \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-127">**WS\_XML\_COMMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_comment_node)
-   [<span data-ttu-id="829fe-128">**\_texte de \_ date/heure XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="829fe-128">**WS\_XML\_DATETIME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_datetime_text)
-   [<span data-ttu-id="829fe-129">**\_ \_ texte décimal WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="829fe-129">**WS\_XML\_DECIMAL\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_decimal_text)
-   [<span data-ttu-id="829fe-130">**\_dictionnaire XML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-130">**WS\_XML\_DICTIONARY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_dictionary)
-   [<span data-ttu-id="829fe-131">**\_ \_ texte double WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="829fe-131">**WS\_XML\_DOUBLE\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_double_text)
-   [<span data-ttu-id="829fe-132">**\_nœud d' \_ élément \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-132">**WS\_XML\_ELEMENT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_element_node)
-   [<span data-ttu-id="829fe-133">**\_ \_ texte flottant WS \_ XML**</span><span class="sxs-lookup"><span data-stu-id="829fe-133">**WS\_XML\_FLOAT\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_float_text)
-   [<span data-ttu-id="829fe-134">**\_texte du \_ GUID WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="829fe-134">**WS\_XML\_GUID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_guid_text)
-   [<span data-ttu-id="829fe-135">**\_ \_ Texte Int32 XML \_ Int32**</span><span class="sxs-lookup"><span data-stu-id="829fe-135">**WS\_XML\_INT32\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int32_text)
-   [<span data-ttu-id="829fe-136">**\_ \_ Texte Int64 XML \_**</span><span class="sxs-lookup"><span data-stu-id="829fe-136">**WS\_XML\_INT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_int64_text)
-   [<span data-ttu-id="829fe-137">**\_texte de \_ liste \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-137">**WS\_XML\_LIST\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_list_text)
-   [<span data-ttu-id="829fe-138">**\_nœud XML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-138">**WS\_XML\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node)
-   [<span data-ttu-id="829fe-139">**\_QName XML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-139">**WS\_XML\_QNAME**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname)
-   [<span data-ttu-id="829fe-140">**\_ \_ texte QName XML \_**</span><span class="sxs-lookup"><span data-stu-id="829fe-140">**WS\_XML\_QNAME\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_text)
-   [<span data-ttu-id="829fe-141">**\_chaîne XML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-141">**WS\_XML\_STRING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string)
-   [<span data-ttu-id="829fe-142">**\_texte XML \_ WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-142">**WS\_XML\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text)
-   [<span data-ttu-id="829fe-143">**\_nœud de \_ texte \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-143">**WS\_XML\_TEXT\_NODE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_text_node)
-   [<span data-ttu-id="829fe-144">**\_texte de \_ TIMESPAN \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="829fe-144">**WS\_XML\_TIMESPAN\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_timespan_text)
-   [<span data-ttu-id="829fe-145">**\_Texte WS XML \_ UINT64 \_**</span><span class="sxs-lookup"><span data-stu-id="829fe-145">**WS\_XML\_UINT64\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_uint64_text)
-   [<span data-ttu-id="829fe-146">**\_texte de \_ l' \_ ID \_ unique WS XML**</span><span class="sxs-lookup"><span data-stu-id="829fe-146">**WS\_XML\_UNIQUE\_ID\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_unique_id_text)
-   [<span data-ttu-id="829fe-147">**WS \_ XML \_ , \_ texte UTF16**</span><span class="sxs-lookup"><span data-stu-id="829fe-147">**WS\_XML\_UTF16\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf16_text)
-   [<span data-ttu-id="829fe-148">**\_ \_ Texte UTF8 XML \_**</span><span class="sxs-lookup"><span data-stu-id="829fe-148">**WS\_XML\_UTF8\_TEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_utf8_text)

 

 