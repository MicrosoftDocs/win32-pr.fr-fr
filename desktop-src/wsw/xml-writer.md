---
title: Enregistreur XML
description: Le Writer XML est une API pour l’émission de données XML. À son cœur, un Writer XML écrit un nœud XML à la fois, mais il existe des API d’assistance supplémentaires pour faciliter l’écriture d’une séquence de nœuds.
ms.assetid: 69d50793-1d5b-4fc7-bf69-128f8e23a98d
keywords:
- Services Web de l’enregistreur XML pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085a02b3aca33ffa3b31e4579d47068a683ee4d8
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "106543418"
---
# <a name="xml-writer"></a><span data-ttu-id="d4794-107">Enregistreur XML</span><span class="sxs-lookup"><span data-stu-id="d4794-107">XML Writer</span></span>

<span data-ttu-id="d4794-108">Le Writer XML est une API pour l’émission de données XML.</span><span class="sxs-lookup"><span data-stu-id="d4794-108">XML Writer is an API for emitting XML.</span></span> <span data-ttu-id="d4794-109">À son cœur, un Writer XML écrit un [nœud XML](xml-node.md) à la fois, mais il existe des API d’assistance supplémentaires pour faciliter l’écriture d’une séquence de nœuds.</span><span class="sxs-lookup"><span data-stu-id="d4794-109">At its core, an XML Writer writes one [XML Node](xml-node.md) at a time, but there are additional helper APIs to make writing a sequence of nodes easier.</span></span>


<span data-ttu-id="d4794-110">Les types de sortie de writer suivants sont pris en charge :</span><span class="sxs-lookup"><span data-stu-id="d4794-110">The following types of writer output are supported:</span></span>

-   [<span data-ttu-id="d4794-111">**Une mémoire tampon d’octets encodés**</span><span class="sxs-lookup"><span data-stu-id="d4794-111">**An in-memory buffer of encoded bytes**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="d4794-112">**Un flux**</span><span class="sxs-lookup"><span data-stu-id="d4794-112">**A stream**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   <span data-ttu-id="d4794-113">Une [mémoire tampon XML](xml-buffer.md)</span><span class="sxs-lookup"><span data-stu-id="d4794-113">An [XML Buffer](xml-buffer.md)</span></span>

<span data-ttu-id="d4794-114">Les rappels suivants sont utilisés avec l’enregistreur XML :</span><span class="sxs-lookup"><span data-stu-id="d4794-114">The following callbacks are used with the XML writer:</span></span>

-   [<span data-ttu-id="d4794-115">**\_rappel de \_ chaîne \_ dynamique WS**</span><span class="sxs-lookup"><span data-stu-id="d4794-115">**WS\_DYNAMIC\_STRING\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [<span data-ttu-id="d4794-116">**rappel de WS \_ pull \_ octets \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-116">**WS\_PULL\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [<span data-ttu-id="d4794-117">**\_rappel d' \_ octets WS Push \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-117">**WS\_PUSH\_BYTES\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [<span data-ttu-id="d4794-118">**\_rappel d’écriture WS \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-118">**WS\_WRITE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

<span data-ttu-id="d4794-119">Les énumérations suivantes sont utilisées avec l’enregistreur XML :</span><span class="sxs-lookup"><span data-stu-id="d4794-119">The following enumerations are used with the XML writer:</span></span>

-   [<span data-ttu-id="d4794-120">**jeu de caractères WS \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-120">**WS\_CHARSET**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [<span data-ttu-id="d4794-121">**\_type d' \_ encodage de l’enregistreur XML WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-121">**WS\_XML\_WRITER\_ENCODING\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [<span data-ttu-id="d4794-122">**TYPE de sortie de l' \_ enregistreur XML WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-122">**WS\_XML\_WRITER\_OUTPUT\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [<span data-ttu-id="d4794-123">**\_ID de \_ propriété du Writer XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-123">**WS\_XML\_WRITER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

<span data-ttu-id="d4794-124">Les fonctions suivantes sont utilisées avec l’enregistreur XML :</span><span class="sxs-lookup"><span data-stu-id="d4794-124">The following functions are used with the XML writer:</span></span>

-   [<span data-ttu-id="d4794-125">**WsCopyNode**</span><span class="sxs-lookup"><span data-stu-id="d4794-125">**WsCopyNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [<span data-ttu-id="d4794-126">**WsCreateWriter**</span><span class="sxs-lookup"><span data-stu-id="d4794-126">**WsCreateWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [<span data-ttu-id="d4794-127">**WsFlushWriter**</span><span class="sxs-lookup"><span data-stu-id="d4794-127">**WsFlushWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [<span data-ttu-id="d4794-128">**WsFreeWriter**</span><span class="sxs-lookup"><span data-stu-id="d4794-128">**WsFreeWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [<span data-ttu-id="d4794-129">**WsGetPrefixFromNamespace**</span><span class="sxs-lookup"><span data-stu-id="d4794-129">**WsGetPrefixFromNamespace**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [<span data-ttu-id="d4794-130">**WsGetWriterPosition**</span><span class="sxs-lookup"><span data-stu-id="d4794-130">**WsGetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [<span data-ttu-id="d4794-131">**WsGetWriterProperty**</span><span class="sxs-lookup"><span data-stu-id="d4794-131">**WsGetWriterProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [<span data-ttu-id="d4794-132">**WsMoveWriter**</span><span class="sxs-lookup"><span data-stu-id="d4794-132">**WsMoveWriter**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [<span data-ttu-id="d4794-133">**WsPullBytes**</span><span class="sxs-lookup"><span data-stu-id="d4794-133">**WsPullBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [<span data-ttu-id="d4794-134">**WsPushBytes**</span><span class="sxs-lookup"><span data-stu-id="d4794-134">**WsPushBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [<span data-ttu-id="d4794-135">**WsSetOutput**</span><span class="sxs-lookup"><span data-stu-id="d4794-135">**WsSetOutput**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [<span data-ttu-id="d4794-136">**WsSetOutputToBuffer**</span><span class="sxs-lookup"><span data-stu-id="d4794-136">**WsSetOutputToBuffer**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [<span data-ttu-id="d4794-137">**WsSetWriterPosition**</span><span class="sxs-lookup"><span data-stu-id="d4794-137">**WsSetWriterPosition**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [<span data-ttu-id="d4794-138">**WsWriteArray**</span><span class="sxs-lookup"><span data-stu-id="d4794-138">**WsWriteArray**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [<span data-ttu-id="d4794-139">**WsWriteBytes**</span><span class="sxs-lookup"><span data-stu-id="d4794-139">**WsWriteBytes**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [<span data-ttu-id="d4794-140">**WsWriteChars**</span><span class="sxs-lookup"><span data-stu-id="d4794-140">**WsWriteChars**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [<span data-ttu-id="d4794-141">**WsWriteCharsUtf8**</span><span class="sxs-lookup"><span data-stu-id="d4794-141">**WsWriteCharsUtf8**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [<span data-ttu-id="d4794-142">**WsWriteEndAttribute**</span><span class="sxs-lookup"><span data-stu-id="d4794-142">**WsWriteEndAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [<span data-ttu-id="d4794-143">**WsWriteEndCData**</span><span class="sxs-lookup"><span data-stu-id="d4794-143">**WsWriteEndCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [<span data-ttu-id="d4794-144">**WsWriteEndElement**</span><span class="sxs-lookup"><span data-stu-id="d4794-144">**WsWriteEndElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [<span data-ttu-id="d4794-145">**WsWriteNode**</span><span class="sxs-lookup"><span data-stu-id="d4794-145">**WsWriteNode**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [<span data-ttu-id="d4794-146">**WsWriteQualifiedName**</span><span class="sxs-lookup"><span data-stu-id="d4794-146">**WsWriteQualifiedName**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [<span data-ttu-id="d4794-147">**WsWriteStartAttribute**</span><span class="sxs-lookup"><span data-stu-id="d4794-147">**WsWriteStartAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [<span data-ttu-id="d4794-148">**WsWriteStartCData**</span><span class="sxs-lookup"><span data-stu-id="d4794-148">**WsWriteStartCData**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [<span data-ttu-id="d4794-149">**WsWriteStartElement**</span><span class="sxs-lookup"><span data-stu-id="d4794-149">**WsWriteStartElement**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [<span data-ttu-id="d4794-150">**WsWriteText**</span><span class="sxs-lookup"><span data-stu-id="d4794-150">**WsWriteText**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [<span data-ttu-id="d4794-151">**WsWriteValue**</span><span class="sxs-lookup"><span data-stu-id="d4794-151">**WsWriteValue**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [<span data-ttu-id="d4794-152">**WsWriteXmlnsAttribute**</span><span class="sxs-lookup"><span data-stu-id="d4794-152">**WsWriteXmlnsAttribute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

<span data-ttu-id="d4794-153">Le handle suivant est utilisé avec l’enregistreur XML :</span><span class="sxs-lookup"><span data-stu-id="d4794-153">The following handle is used with the XML writer:</span></span>

-   [<span data-ttu-id="d4794-154">\_enregistreur XML \_ WS</span><span class="sxs-lookup"><span data-stu-id="d4794-154">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)

<span data-ttu-id="d4794-155">Les structures suivantes sont utilisées avec l’enregistreur XML :</span><span class="sxs-lookup"><span data-stu-id="d4794-155">The following structures are used with the XML writer:</span></span>

-   [<span data-ttu-id="d4794-156">**\_encodage \_ binaire du Writer XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-156">**WS\_XML\_WRITER\_BINARY\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [<span data-ttu-id="d4794-157">**sortie de la \_ \_ \_ mémoire tampon de l’enregistreur XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-157">**WS\_XML\_WRITER\_BUFFER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [<span data-ttu-id="d4794-158">**encodage d' \_ enregistreur XML WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-158">**WS\_XML\_WRITER\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [<span data-ttu-id="d4794-159">**\_encodage \_ MTOM WS XML Writer \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-159">**WS\_XML\_WRITER\_MTOM\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [<span data-ttu-id="d4794-160">**sortie de l' \_ enregistreur XML WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-160">**WS\_XML\_WRITER\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [<span data-ttu-id="d4794-161">**\_Propriétés du \_ writer \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="d4794-161">**WS\_XML\_WRITER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [<span data-ttu-id="d4794-162">**\_propriété du \_ writer \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="d4794-162">**WS\_XML\_WRITER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [<span data-ttu-id="d4794-163">**\_sortie du \_ flux du Writer XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-163">**WS\_XML\_WRITER\_STREAM\_OUTPUT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [<span data-ttu-id="d4794-164">**encodage de \_ \_ texte du Writer XML \_ WS \_**</span><span class="sxs-lookup"><span data-stu-id="d4794-164">**WS\_XML\_WRITER\_TEXT\_ENCODING**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




