---
title: Mémoire tampon XML
description: Une mémoire tampon XML fournit un stockage en mémoire efficace pour les données XML arbitraires.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- Services Web de tampon XML pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd4e4725f2ad3345dcef7c33b694a8e327f4d8a6c43fbce39f9c57babfa467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192335"
---
# <a name="xml-buffer"></a>Mémoire tampon XML

Une mémoire tampon XML fournit un stockage en mémoire efficace pour les données XML arbitraires.


Pour lire des données à partir d’une mémoire tampon XML, utilisez un [lecteur XML](xml-reader.md) et appelez [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) avec la mémoire tampon XML. Le lecteur sera positionné au début du document.

Pour insérer des données dans une mémoire tampon, utilisez un [Writer XML](xml-writer.md) et appelez [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) avec la mémoire tampon XML. Le writer sera positionné à la fin du document.

Une fois qu’un lecteur a été défini sur une mémoire tampon XML, en plus de toutes les API de lecture XML, [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) peut être utilisé pour parcourir le lecteur à travers le document. [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) et [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) peuvent également être utilisés pour enregistrer une position dans le document et y revenir ultérieurement.

Une fois qu’un enregistreur a été défini sur une mémoire tampon XML, en plus de toutes les API du Writer XML, [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) peut être utilisé pour parcourir l’enregistreur dans le document. [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) et [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) peuvent également être utilisés pour enregistrer une position dans le document et y revenir ultérieurement. Le writer insère toujours des données avant le nœud auquel il est positionné.

Les nœuds peuvent être supprimés de la mémoire tampon XML en obtenant la position du nœud à l’aide de [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) ou [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) , puis en appelant [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) avec cette position. Pour les éléments, cette opération supprimera l’élément, tous ses enfants, y compris son élément de fin correspondant.

Une position est représentée par la valeur de la [**\_ \_ \_ position du nœud XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position). Les positions sont spécifiques à une mémoire tampon XML particulière et sont uniquement valides tant que la mémoire tampon XML est valide.

Les énumérations suivantes sont utilisées avec les mémoires tampons XML :

-   [**\_passage \_ de WS à**](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [**\_ID de \_ propriété de tampon XML \_ WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

Les fonctions suivantes sont utilisées avec les mémoires tampons XML :

-   [**WsCreateXmlBuffer**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

Le handle suivant est utilisé avec les mémoires tampons XML :

-   [\_ \_ mémoire tampon XML WS](ws-xml-buffer.md)

Les structures suivantes sont utilisées avec les tampons XML :

-   [**\_propriété de \_ tampon \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [**\_position du \_ nœud \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




