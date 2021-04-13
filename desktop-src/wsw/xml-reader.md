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
# <a name="xml-reader"></a>lecteur XML

Le lecteur XML est un curseur sur une source d’entrée de XML. À son cœur, un lecteur XML lit un [nœud XML](xml-node.md) à la fois, mais il existe des API d’assistance supplémentaires pour faciliter la lecture d’une séquence de nœuds.


Les types de lecteurs suivants sont pris en charge :

-   [**Une mémoire tampon d’octets encodés**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**Un flux**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   Une [mémoire tampon XML](xml-buffer.md)

### <a name="security"></a>Sécurité

Le lecteur vérifie que les attributs présents sur un élément sont uniques. Le temps nécessaire pour effectuer cette validation est une fonction du nombre d’attributs sur l’élément qui peut être aussi important que les [**\_ \_ \_ \_ \_ attributs max de la propriété du lecteur WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Par conséquent, le traitement de documents volumineux lorsque le **\_ \_ \_ \_ nombre maximal d' \_ attributs de la propriété du lecteur WS XML** est défini sur une valeur élevée peut entraîner une attaque par déni de service.

Le lecteur mappera les préfixes aux espaces de noms pour chaque élément et attributs. Le temps nécessaire pour effectuer ce mappage est une fonction du nombre d’attributs xmlns dans la portée, ce qui peut être aussi important que le nombre [**\_ maximal d’espaces de \_ \_ \_ \_ noms des propriétés du lecteur WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id). Par conséquent, le traitement de documents volumineux lorsque cette propriété est définie sur une valeur élevée peut présenter une opportunité d’attaque par déni de service.

Tandis que le lecteur s’assure que le document suit la spécification grammaticale de XML et que ses aspects se trouvent dans les quotas spécifiés, le contenu du document doit toujours être considéré comme non fiable lorsqu’il provient d’une source non fiable. Les utilisateurs du lecteur doivent vérifier tous les noms d’éléments et d’attributs et les espaces de noms à l’aide de [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement), [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute), ou en inspectant manuellement les [**nœuds**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node).

D’autres situations peuvent être prises en compte, mais ne sont pas limitées à :

-   Les éléments attendus sont peut-être manquants
-   Des éléments inattendus peuvent apparaître
-   Les attributs attendus sont peut-être manquants
-   Des attributs inattendus peuvent apparaître
-   Les éléments peuvent apparaître comme des éléments vides
-   Les espaces peuvent apparaître dans des emplacements inattendus

Les utilisateurs du lecteur ne doivent pas allouer de la mémoire en fonction simplement des valeurs lues dans le document. Examinons, par exemple, le document XML suivant :

``` syntax
<array count='1000000'>
   <!-- malicious document provider didn't actually provide 1000000 array items -->
</array>
```

L’allocation d’un tableau reposant uniquement sur l’hypothèse qu’un certain nombre d’éléments suivras serait un vecteur d’attaque potentiel. Dans ce cas, l’utilisateur du lecteur doit allouer la mémoire de façon incrémentielle à mesure que les éléments apparaissent.

Le lecteur XML ne prend pas en charge DTD. L’utilisateur du lecteur n’a pas besoin de se préoccuper de la vérification DTD.

Le rappel suivant est utilisé avec les lecteurs XML :

-   [**\_rappel WS Read \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)

Les énumérations suivantes sont utilisées avec les lecteurs XML :

-   [**\_type d' \_ \_ encodage du lecteur XML WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_encoding_type)
-   [**\_ \_ \_ type d’entrée du lecteur XML WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_input_type)
-   [**\_ID de \_ propriété du lecteur XML \_ WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_reader_property_id)

Les fonctions suivantes sont utilisées avec les lecteurs XML :

-   [**WsCreateReader**](/windows/desktop/api/WebServices/nf-webservices-wscreatereader)
-   [**WsFillReader**](/windows/desktop/api/WebServices/nf-webservices-wsfillreader)
-   [**WsFindAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsfindattribute)
-   [**WsFreeReader**](/windows/desktop/api/WebServices/nf-webservices-wsfreereader)
-   [**WsGetNamespaceFromPrefix**](/windows/desktop/api/WebServices/nf-webservices-wsgetnamespacefromprefix)
-   [**WsGetReaderNode**](/windows/desktop/api/WebServices/nf-webservices-wsgetreadernode)
-   [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition)
-   [**WsGetReaderProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderproperty)
-   [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute)
-   [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader)
-   [**WsReadArray**](/windows/desktop/api/WebServices/nf-webservices-wsreadarray)
-   [**WsReadBytes**](/windows/desktop/api/WebServices/nf-webservices-wsreadbytes)
-   [**WsReadChars**](/windows/desktop/api/WebServices/nf-webservices-wsreadchars)
-   [**WsReadCharsUtf8**](/windows/desktop/api/WebServices/nf-webservices-wsreadcharsutf8)
-   [**WsReadEndAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadendattribute)
-   [**WsReadEndElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadendelement)
-   [**WsReadNode**](/windows/desktop/api/WebServices/nf-webservices-wsreadnode)
-   [**WsReadQualifiedName**](/windows/desktop/api/WebServices/nf-webservices-wsreadqualifiedname)
-   [**WsReadStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartattribute)
-   [**WsReadStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadstartelement)
-   [**WsReadToStartElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadtostartelement)
-   [**WsReadValue**](/windows/desktop/api/WebServices/nf-webservices-wsreadvalue)
-   [**WsSetInput**](/windows/desktop/api/WebServices/nf-webservices-wssetinput)
-   [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer)
-   [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition)
-   [**WsSkipNode**](/windows/desktop/api/WebServices/nf-webservices-wsskipnode)

Le handle suivant est utilisé avec les lecteurs XML :

-   [\_lecteur XML \_ WS](ws-xml-reader.md)

Les structures suivantes sont utilisées avec les lecteurs XML :

-   [**\_ \_ codage binaire du lecteur WS XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_binary_encoding)
-   [**\_entrée de \_ \_ mémoire tampon du lecteur XML WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_buffer_input)
-   [**\_codage du \_ lecteur WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_encoding)
-   [**\_entrée de \_ lecteur \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_input)
-   [**\_encodage \_ MTOM du lecteur XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_mtom_encoding)
-   [**\_Propriétés du \_ lecteur \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_properties)
-   [**\_propriété du \_ lecteur \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_property)
-   [**\_entrée de \_ flux du lecteur XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_stream_input)
-   [**encodage de \_ \_ texte du lecteur XML \_ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_reader_text_encoding)

 

 




