---
title: Canonisation XML
description: La canonisation XML résout le problème lié à la conversion d’un ensemble de nœuds XML en octets de sorte que les modifications importantes apportées au XML (telles que la modification de l’ordre des attributs dans un élément) ne modifient pas le formulaire d’octet résultant.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Services Web de canonisation XML pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8b1aa00b99b604276a479f1a47aacb5bd8b1e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842901"
---
# <a name="xml-canonicalization"></a>Canonisation XML

La canonisation XML résout le problème lié à la conversion d’un ensemble de nœuds XML en octets de sorte que les modifications importantes apportées au XML (telles que la modification de l’ordre des attributs dans un élément) ne modifient pas le formulaire d’octet résultant. Les octets obtenus à partir de la canonicalisation sont couramment utilisés pour générer une signature de chiffrement sur le contenu XML.


Les algorithmes de canonisation XML couramment utilisés normalisent les aspects suivants :

-   Encodage de caractères (UTF-8 sans préambule)
-   Sauts de ligne et autres formes de caractères
-   Ordre des attributs dans un élément
-   Formulaire d’élément vide
-   Déclaration d’espaces de noms de rendu

Les API [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) et [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) fournissent la fonctionnalité de canonisation XML lors de la lecture d’un document.

Les API [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) et [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) fournissent la fonctionnalité de canonisation XML lors de l’écriture d’un document.

Les énumérations suivantes sont utilisées avec la canonisation :

-   [**\_ \_ algorithme de canonisation WS XML \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [**\_ID de \_ propriété de canonisation WS XML \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

Les fonctions suivantes sont utilisées avec la canonisation :

-   [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

Les structures suivantes sont utilisées avec la canonisation :

-   [**\_ \_ \_ préfixes inclusives de canonisation WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [**\_propriété de \_ canonisation WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




