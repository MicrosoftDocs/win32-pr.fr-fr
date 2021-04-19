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
# <a name="xml-writer"></a>Enregistreur XML

Le Writer XML est une API pour l’émission de données XML. À son cœur, un Writer XML écrit un [nœud XML](xml-node.md) à la fois, mais il existe des API d’assistance supplémentaires pour faciliter l’écriture d’une séquence de nœuds.


Les types de sortie de writer suivants sont pris en charge :

-   [**Une mémoire tampon d’octets encodés**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**Un flux**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   Une [mémoire tampon XML](xml-buffer.md)

Les rappels suivants sont utilisés avec l’enregistreur XML :

-   [**\_rappel de \_ chaîne \_ dynamique WS**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**rappel de WS \_ pull \_ octets \_**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**\_rappel d' \_ octets WS Push \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**\_rappel d’écriture WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)

Les énumérations suivantes sont utilisées avec l’enregistreur XML :

-   [**jeu de caractères WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_charset)
-   [**\_type d' \_ encodage de l’enregistreur XML WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_encoding_type)
-   [**TYPE de sortie de l' \_ enregistreur XML WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_output_type)
-   [**\_ID de \_ propriété du Writer XML \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_writer_property_id)

Les fonctions suivantes sont utilisées avec l’enregistreur XML :

-   [**WsCopyNode**](/windows/desktop/api/WebServices/nf-webservices-wscopynode)
-   [**WsCreateWriter**](/windows/desktop/api/WebServices/nf-webservices-wscreatewriter)
-   [**WsFlushWriter**](/windows/desktop/api/WebServices/nf-webservices-wsflushwriter)
-   [**WsFreeWriter**](/windows/desktop/api/WebServices/nf-webservices-wsfreewriter)
-   [**WsGetPrefixFromNamespace**](/windows/desktop/api/WebServices/nf-webservices-wsgetprefixfromnamespace)
-   [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition)
-   [**WsGetWriterProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterproperty)
-   [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter)
-   [**WsPullBytes**](/windows/desktop/api/WebServices/nf-webservices-wspullbytes)
-   [**WsPushBytes**](/windows/desktop/api/WebServices/nf-webservices-wspushbytes)
-   [**WsSetOutput**](/windows/desktop/api/WebServices/nf-webservices-wssetoutput)
-   [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer)
-   [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition)
-   [**WsWriteArray**](/windows/desktop/api/WebServices/nf-webservices-wswritearray)
-   [**WsWriteBytes**](/windows/desktop/api/WebServices/nf-webservices-wswritebytes)
-   [**WsWriteChars**](/windows/desktop/api/WebServices/nf-webservices-wswritechars)
-   [**WsWriteCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wswritecharsutf8)
-   [**WsWriteEndAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteendattribute)
-   [**WsWriteEndCData**](/windows/desktop/api/WebServices/nf-webservices-wswriteendcdata)
-   [**WsWriteEndElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteendelement)
-   [**WsWriteNode**](/windows/desktop/api/WebServices/nf-webservices-wswritenode)
-   [**WsWriteQualifiedName**](/windows/desktop/api/WebServices/nf-webservices-wswritequalifiedname)
-   [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute)
-   [**WsWriteStartCData**](/windows/desktop/api/WebServices/nf-webservices-wswritestartcdata)
-   [**WsWriteStartElement**](/windows/desktop/api/WebServices/nf-webservices-wswritestartelement)
-   [**WsWriteText**](/windows/desktop/api/WebServices/nf-webservices-wswritetext)
-   [**WsWriteValue**](/windows/desktop/api/WebServices/nf-webservices-wswritevalue)
-   [**WsWriteXmlnsAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritexmlnsattribute)

Le handle suivant est utilisé avec l’enregistreur XML :

-   [\_enregistreur XML \_ WS](ws-xml-writer.md)

Les structures suivantes sont utilisées avec l’enregistreur XML :

-   [**\_encodage \_ binaire du Writer XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_binary_encoding)
-   [**sortie de la \_ \_ \_ mémoire tampon de l’enregistreur XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_buffer_output)
-   [**encodage d' \_ enregistreur XML WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_encoding)
-   [**\_encodage \_ MTOM WS XML Writer \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_mtom_encoding)
-   [**sortie de l' \_ enregistreur XML WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_output)
-   [**\_Propriétés du \_ writer \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_properties)
-   [**\_propriété du \_ writer \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_property)
-   [**\_sortie du \_ flux du Writer XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_stream_output)
-   [**encodage de \_ \_ texte du Writer XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_writer_text_encoding)

 

 




