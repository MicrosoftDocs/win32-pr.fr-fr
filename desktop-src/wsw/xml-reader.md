---
title: lecteur XML
description: Le lecteur XML est un curseur sur une source d’entrée de XML. À son cœur, un lecteur XML lit un nœud XML à la fois, mais il existe des API d’assistance supplémentaires pour faciliter la lecture d’une séquence de nœuds.
ms.assetid: 1f99e45c-64ba-42fb-9bf0-35e27f1c5ef2
keywords:
- Services Web du lecteur XML pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d9d9c91b6594ec569536751751a3efca4c32e08
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104463934"
---
# <a name="xml-reader"></a><span data-ttu-id="54b7e-107">lecteur XML</span><span class="sxs-lookup"><span data-stu-id="54b7e-107">XML Reader</span></span>

<span data-ttu-id="54b7e-108">Le lecteur XML est un curseur sur une source d’entrée de XML.</span><span class="sxs-lookup"><span data-stu-id="54b7e-108">XML Reader is a cursor over an input source of XML.</span></span> <span data-ttu-id="54b7e-109">À son cœur, un lecteur XML lit un [nœud XML](xml-node.md) à la fois, mais il existe des API d’assistance supplémentaires pour faciliter la lecture d’une séquence de nœuds.</span><span class="sxs-lookup"><span data-stu-id="54b7e-109">At its core, an XML Reader reads one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make reading a sequence of nodes easier.</span></span>


<span data-ttu-id="54b7e-110">Les types de lecteurs suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="54b7e-110">The following types of readers input are supported:</span></span>

-   [<span data-ttu-id="54b7e-111">**Une mémoire tampon d’octets encodés**</span><span class="sxs-lookup"><span data-stu-id="54b7e-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="54b7e-112">**Un flux**</span><span class="sxs-lookup"><span data-stu-id="54b7e-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   <span data-ttu-id="54b7e-113">Une [mémoire tampon XML](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="54b7e-113">An [XML Buffer](xml-buffer.md)</span></span>

### <a name="security"></a><span data-ttu-id="54b7e-114">Sécurité</span><span class="sxs-lookup"><span data-stu-id="54b7e-114">Security</span></span>

<span data-ttu-id="54b7e-115">Le lecteur vérifie que les attributs présents sur un élément sont uniques.</span><span class="sxs-lookup"><span data-stu-id="54b7e-115">The reader will verify that the attributes present on an element are unique.</span></span> <span data-ttu-id="54b7e-116">Le temps nécessaire pour effectuer cette validation est une fonction du nombre d’attributs sur l’élément qui peut être aussi important que les [**\_ \_ \_ \_ \_ attributs max de la propriété du lecteur WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span><span class="sxs-lookup"><span data-stu-id="54b7e-116">The time required to perform this validation is a function of the number of attributes on the element which can be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="54b7e-117">Par conséquent, le traitement de documents volumineux lorsque le **\_ \_ \_ \_ nombre maximal d' \_ attributs de la propriété du lecteur WS XML** est défini sur une valeur élevée peut entraîner une attaque par déni de service.</span><span class="sxs-lookup"><span data-stu-id="54b7e-117">Therefore, processing large documents when **WS\_XML\_READER\_PROPERTY\_MAX\_ATTRIBUTES** is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="54b7e-118">Le lecteur mappera les préfixes aux espaces de noms pour chaque élément et attributs.</span><span class="sxs-lookup"><span data-stu-id="54b7e-118">The reader will map prefixes to namespaces for each element and attributes.</span></span> <span data-ttu-id="54b7e-119">Le temps nécessaire pour effectuer ce mappage est une fonction du nombre d’attributs xmlns dans la portée, ce qui peut être aussi important que le nombre [**\_ maximal d’espaces de \_ \_ \_ \_ noms des propriétés du lecteur WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span><span class="sxs-lookup"><span data-stu-id="54b7e-119">The time required to perform this mapping is a function of the number of xmlns attributes in scope which may be as large as [**WS\_XML\_READER\_PROPERTY\_MAX\_NAMESPACES**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id).</span></span> <span data-ttu-id="54b7e-120">Par conséquent, le traitement de documents volumineux lorsque cette propriété est définie sur une valeur élevée peut présenter une opportunité d’attaque par déni de service.</span><span class="sxs-lookup"><span data-stu-id="54b7e-120">Therefore, processing large documents when this property is set to a large value may present an opportunity for a denial of service attack.</span></span>

<span data-ttu-id="54b7e-121">Tandis que le lecteur s’assure que le document suit la spécification grammaticale de XML et que ses aspects se trouvent dans les quotas spécifiés, le contenu du document doit toujours être considéré comme non fiable lorsqu’il provient d’une source non fiable.</span><span class="sxs-lookup"><span data-stu-id="54b7e-121">While the reader will ensure that the document follows the grammatical specification of xml and furthermore that its aspects are within the quotas specified, the content of the document must still be considered untrusted when coming from an untrusted source.</span></span> <span data-ttu-id="54b7e-122">Les utilisateurs du lecteur doivent vérifier tous les noms d’éléments et d’attributs et les espaces de noms à l’aide de [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute), ou en inspectant manuellement les [**nœuds**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).</span><span class="sxs-lookup"><span data-stu-id="54b7e-122">Users of the reader should check all element and attribute names and namespaces using [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute), or by manually inspecting [**nodes**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).</span></span>

<span data-ttu-id="54b7e-123">D’autres situations peuvent être prises en compte, mais ne sont pas limitées à :</span><span class="sxs-lookup"><span data-stu-id="54b7e-123">Some other situations to consider include, but are not limited to:</span></span>

-   <span data-ttu-id="54b7e-124">Les éléments attendus sont peut-être manquants</span><span class="sxs-lookup"><span data-stu-id="54b7e-124">Expected elements may be missing</span></span>
-   <span data-ttu-id="54b7e-125">Des éléments inattendus peuvent apparaître</span><span class="sxs-lookup"><span data-stu-id="54b7e-125">Unexpected elements may appear</span></span>
-   <span data-ttu-id="54b7e-126">Les attributs attendus sont peut-être manquants</span><span class="sxs-lookup"><span data-stu-id="54b7e-126">Expected attributes may be missing</span></span>
-   <span data-ttu-id="54b7e-127">Des attributs inattendus peuvent apparaître</span><span class="sxs-lookup"><span data-stu-id="54b7e-127">Unexpected attributes may appear</span></span>
-   <span data-ttu-id="54b7e-128">Les éléments peuvent apparaître comme des éléments vides</span><span class="sxs-lookup"><span data-stu-id="54b7e-128">Elements may appear as empty elements</span></span>
-   <span data-ttu-id="54b7e-129">Les espaces peuvent apparaître dans des emplacements inattendus</span><span class="sxs-lookup"><span data-stu-id="54b7e-129">Whitespace may appear in unexpected places</span></span>

<span data-ttu-id="54b7e-130">Les utilisateurs du lecteur ne doivent pas allouer de la mémoire en fonction simplement des valeurs lues dans le document.</span><span class="sxs-lookup"><span data-stu-id="54b7e-130">Users of the reader should not allocate memory based simply on values read from the document.</span></span> <span data-ttu-id="54b7e-131">Examinons, par exemple, le document XML suivant :</span><span class="sxs-lookup"><span data-stu-id="54b7e-131">For example, consider the following xml document:</span></span>

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

<span data-ttu-id="54b7e-132">L’allocation d’un tableau reposant uniquement sur l’hypothèse qu’un certain nombre d’éléments suivras serait un vecteur d’attaque potentiel.</span><span class="sxs-lookup"><span data-stu-id="54b7e-132">Allocating an array based soley on the assumption that some number of elements will follow would be a potential attack vector.</span></span> <span data-ttu-id="54b7e-133">Dans ce cas, l’utilisateur du lecteur doit allouer la mémoire de façon incrémentielle à mesure que les éléments apparaissent.</span><span class="sxs-lookup"><span data-stu-id="54b7e-133">The user of the reader in this case should instead incrementally allocate the memory as the elements appear.</span></span>

<span data-ttu-id="54b7e-134">Le lecteur XML ne prend pas en charge DTD.</span><span class="sxs-lookup"><span data-stu-id="54b7e-134">XML reader does not support DTD.</span></span> <span data-ttu-id="54b7e-135">L’utilisateur du lecteur n’a pas besoin de se préoccuper de la vérification DTD.</span><span class="sxs-lookup"><span data-stu-id="54b7e-135">The user of the reader does not need to concern about DTD verification.</span></span>

<span data-ttu-id="54b7e-136">Le rappel suivant est utilisé avec les lecteurs XML :</span><span class="sxs-lookup"><span data-stu-id="54b7e-136">The following callback is used with XML readers:</span></span>

-   [<span data-ttu-id="54b7e-137">**\_rappel WS Read \_**</span><span class="sxs-lookup"><span data-stu-id="54b7e-137">**WS\_READ\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

<span data-ttu-id="54b7e-138">Les énumérations suivantes sont utilisées avec les lecteurs XML :</span><span class="sxs-lookup"><span data-stu-id="54b7e-138">The following enumerations are used with XML readers:</span></span>

-   [<span data-ttu-id="54b7e-139">**\_type d' \_ \_ encodage du lecteur XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="54b7e-139">**WS\_XML\_READER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [<span data-ttu-id="54b7e-140">**\_ \_ \_ type d’entrée du lecteur XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="54b7e-140">**WS\_XML\_READER\_INPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [<span data-ttu-id="54b7e-141">**\_ID de \_ propriété du lecteur XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="54b7e-141">**WS\_XML\_READER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

<span data-ttu-id="54b7e-142">Les fonctions suivantes sont utilisées avec les lecteurs XML :</span><span class="sxs-lookup"><span data-stu-id="54b7e-142">The following functions are used with XML readers:</span></span>

-   [<span data-ttu-id="54b7e-143">**WsCreateReader**</span><span class="sxs-lookup"><span data-stu-id="54b7e-143">**WsCreateReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [<span data-ttu-id="54b7e-144">**WsFillReader**</span><span class="sxs-lookup"><span data-stu-id="54b7e-144">**WsFillReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [<span data-ttu-id="54b7e-145">**WsFindAttribute**</span><span class="sxs-lookup"><span data-stu-id="54b7e-145">**WsFindAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [<span data-ttu-id="54b7e-146">**WsFreeReader**</span><span class="sxs-lookup"><span data-stu-id="54b7e-146">**WsFreeReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [<span data-ttu-id="54b7e-147">**WsGetNamespaceFromPrefix**</span><span class="sxs-lookup"><span data-stu-id="54b7e-147">**WsGetNamespaceFromPrefix**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [<span data-ttu-id="54b7e-148">**WsGetReaderNode**</span><span class="sxs-lookup"><span data-stu-id="54b7e-148">**WsGetReaderNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [<span data-ttu-id="54b7e-149">**WsGetReaderPosition**</span><span class="sxs-lookup"><span data-stu-id="54b7e-149">**WsGetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [<span data-ttu-id="54b7e-150">**WsGetReaderProperty**</span><span class="sxs-lookup"><span data-stu-id="54b7e-150">**WsGetReaderProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [<span data-ttu-id="54b7e-151">**WsGetXmlAttribute**</span><span class="sxs-lookup"><span data-stu-id="54b7e-151">**WsGetXmlAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [<span data-ttu-id="54b7e-152">**WsMoveReader**</span><span class="sxs-lookup"><span data-stu-id="54b7e-152">**WsMoveReader**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [<span data-ttu-id="54b7e-153">**WsReadArray**</span><span class="sxs-lookup"><span data-stu-id="54b7e-153">**WsReadArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [<span data-ttu-id="54b7e-154">**WsReadBytes**</span><span class="sxs-lookup"><span data-stu-id="54b7e-154">**WsReadBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [<span data-ttu-id="54b7e-155">**WsReadChars**</span><span class="sxs-lookup"><span data-stu-id="54b7e-155">**WsReadChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [<span data-ttu-id="54b7e-156">**WsReadCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="54b7e-156">**WsReadCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [<span data-ttu-id="54b7e-157">**WsReadEndAttribute**</span><span class="sxs-lookup"><span data-stu-id="54b7e-157">**WsReadEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [<span data-ttu-id="54b7e-158">**WsReadEndElement**</span><span class="sxs-lookup"><span data-stu-id="54b7e-158">**WsReadEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [<span data-ttu-id="54b7e-159">**WsReadNode**</span><span class="sxs-lookup"><span data-stu-id="54b7e-159">**WsReadNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [<span data-ttu-id="54b7e-160">**WsReadQualifiedName**</span><span class="sxs-lookup"><span data-stu-id="54b7e-160">**WsReadQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [<span data-ttu-id="54b7e-161">**WsReadStartAttribute**</span><span class="sxs-lookup"><span data-stu-id="54b7e-161">**WsReadStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [<span data-ttu-id="54b7e-162">**WsReadStartElement**</span><span class="sxs-lookup"><span data-stu-id="54b7e-162">**WsReadStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [<span data-ttu-id="54b7e-163">**WsReadToStartElement**</span><span class="sxs-lookup"><span data-stu-id="54b7e-163">**WsReadToStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [<span data-ttu-id="54b7e-164">**WsReadValue**</span><span class="sxs-lookup"><span data-stu-id="54b7e-164">**WsReadValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [<span data-ttu-id="54b7e-165">**WsSetInput**</span><span class="sxs-lookup"><span data-stu-id="54b7e-165">**WsSetInput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [<span data-ttu-id="54b7e-166">**WsSetInputToBuffer**</span><span class="sxs-lookup"><span data-stu-id="54b7e-166">**WsSetInputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [<span data-ttu-id="54b7e-167">**WsSetReaderPosition**</span><span class="sxs-lookup"><span data-stu-id="54b7e-167">**WsSetReaderPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [<span data-ttu-id="54b7e-168">**WsSkipNode**</span><span class="sxs-lookup"><span data-stu-id="54b7e-168">**WsSkipNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

<span data-ttu-id="54b7e-169">Le handle suivant est utilisé avec les lecteurs XML :</span><span class="sxs-lookup"><span data-stu-id="54b7e-169">The following handle is used with XML readers:</span></span>

-   [<span data-ttu-id="54b7e-170">\_lecteur XML \_ WS</span><span class="sxs-lookup"><span data-stu-id="54b7e-170">WS\_XML\_READER</span></span>](ws-xml-reader.md)

<span data-ttu-id="54b7e-171">Les structures suivantes sont utilisées avec les lecteurs XML :</span><span class="sxs-lookup"><span data-stu-id="54b7e-171">The following structures are used with XML readers:</span></span>

-   [<span data-ttu-id="54b7e-172">**\_ \_ codage binaire du lecteur WS XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="54b7e-172">**WS\_XML\_READER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [<span data-ttu-id="54b7e-173">**\_entrée de \_ \_ mémoire tampon du lecteur XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="54b7e-173">**WS\_XML\_READER\_BUFFER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [<span data-ttu-id="54b7e-174">**\_codage du \_ lecteur WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="54b7e-174">**WS\_XML\_READER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [<span data-ttu-id="54b7e-175">**\_entrée de \_ lecteur \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="54b7e-175">**WS\_XML\_READER\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [<span data-ttu-id="54b7e-176">**\_encodage \_ MTOM du lecteur XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="54b7e-176">**WS\_XML\_READER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [<span data-ttu-id="54b7e-177">**\_Propriétés du \_ lecteur \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="54b7e-177">**WS\_XML\_READER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [<span data-ttu-id="54b7e-178">**\_propriété du \_ lecteur \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="54b7e-178">**WS\_XML\_READER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [<span data-ttu-id="54b7e-179">**\_entrée de \_ flux du lecteur XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="54b7e-179">**WS\_XML\_READER\_STREAM\_INPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [<span data-ttu-id="54b7e-180">**encodage de \_ \_ texte du lecteur XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="54b7e-180">**WS\_XML\_READER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




