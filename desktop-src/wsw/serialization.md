---
title: Sérialisation
description: La sérialisation est le processus d’écriture de valeurs dans les structures de données C (structs, tableaux et valeurs primitives) en tant qu’élément XML. La désérialisation est le processus inverse.
ms.assetid: aa092156-30ae-4f8a-baa2-450f38a78153
keywords:
- Services Web de sérialisation pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f986c6cec9a035424aaafe1c51f4dc0d3ee014
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104211198"
---
# <a name="serialization"></a>Sérialisation

La sérialisation est le processus d’écriture de valeurs dans les structures de données C (structs, tableaux et valeurs primitives) en tant qu’élément XML. La désérialisation est le processus inverse.


La sérialisation est le processus d’écriture de valeurs dans les structures de données C (structures, tableaux et valeurs primitives) en tant qu’élément XML. La désérialisation est le processus inverse.

Les deux processus reposent sur une description du mappage entre les structures de données C et XML.

![Diagramme montrant comment la sérialisation et la désérialisation reposent sur une description du mappage entre les structures de données C et XML.](images/xmlmapping.png)

Pour sérialiser une valeur, l’application appelle [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement), [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute) ou [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype).

Pour désérialiser une valeur, l’application appelle [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement), [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute) ou [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype).

## <a name="security"></a>Sécurité

Le [lecteur XML](xml-reader.md) est utilisé dans le processus de désérialisation. Reportez-vous à la section sécurité dans le lecteur XML pour obtenir des informations de sécurité liées à XML.

Le désérialiseur continue à désérialiser les données jusqu’à ce qu’il ait terminé de lire l’élément en cours de désérialisation. Le processus de désérialisation échoue lorsqu’il rencontre un document XML qui n’est pas conforme à la description des données désérialisées. À ce stade, le lecteur XML utilisé devient non valide et une erreur est retournée.

Par défaut, la désérialisation est stricte. Certaines conditions provoquant l’échec de la désérialisation incluent, sans s’y limiter, les conditions suivantes :

-   Éléments attendus manquants
-   Des champs d’élément inattendus apparaissent entre les éléments requis
-   Contenu de l’élément supplémentaire après les champs obligatoires, à moins que le **WS_STRUCT_IGNORE_TRAILING_ELEMENT_CONTENT**
-   Attributs inattendus, sauf si l’indicateur [**WS \_ struct \_ ignore les \_ \_ attributs non gérés**](https://msdn.microsoft.com/library/Dd323454(v=VS.85).aspx) est spécifié
-   Valeur de type de données inattendue en dehors de la plage spécifiée
-   Le nombre d’éléments répétitifs est en dehors de la plage spécifiée

La sérialisation d’une grande quantité de données peut entraîner une allocation excessive de la mémoire et peut entraîner une attaque par déni de service. L’utilisateur qui désérialise les données doit spécifier un objet segment de mémoire pour allouer les données, et l’utilisateur peut utiliser la limite d’allocation du tas pour empêcher une attaque d’allocation de mémoire.

La prise en charge de plage pour les types de données, notamment la longueur maximale pour les chaînes, le nombre maximal d’éléments dans le tableau, etc. permet à l’utilisateur de contrôler la taille maximale des différents types de données. L’utilisateur peut spécifier une plage dans la description ou le schéma des données pour limiter la taille maximale des différentes données.

Une valeur de chaîne contenant un zéro incorporé est prise en charge dans les formats de transmission (texte, binaire, MTOM). Lors de la désérialisation d’une chaîne avec un zéro incorporé, l’utilisateur doit utiliser une chaîne comptée (WS \_ String) afin que le zéro ne confonde pas le calcul de la longueur de la chaîne. Si une valeur de chaîne contenant un zéro incorporé est désérialisée dans un champ qui attend une chaîne se terminant par zéro, une erreur est retournée et la désérialisation échoue. Si Wsutil est utilisé pour générer des descriptions de données, l’option/String : WS \_ String doit être utilisée si la chaîne avec un zéro incorporé est attendue.

Les rappels suivants sont utilisés avec la sérialisation :

-   [**rappel de comparaison de la \_ durée WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**\_rappel de \_ type WS Read \_**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**\_rappel de \_ type WS Write \_**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

Les énumérations suivantes sont utilisées avec la sérialisation :

-   [**\_mappage de champs WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_field_mapping)
-   [**\_options de champ WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_encoding_type)
-   [**\_option WS Read \_**](/windows/desktop/api/WebServices/ne-webservices-ws_read_option)
-   [**\_type WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type)
-   [**\_mappage de type WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_type_mapping)
-   [**\_option d’écriture WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_write_option)

Les fonctions suivantes sont utilisées avec la sérialisation :

-   [**WsReadAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsreadattribute)
-   [**WsReadElement**](/windows/desktop/api/WebServices/nf-webservices-wsreadelement)
-   [**WsReadType**](/windows/desktop/api/WebServices/nf-webservices-wsreadtype)
-   [**WsWriteAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswriteattribute)
-   [**WsWriteElement**](/windows/desktop/api/WebServices/nf-webservices-wswriteelement)
-   [**WsWriteType**](/windows/desktop/api/WebServices/nf-webservices-wswritetype)

Les structures suivantes sont utilisées avec la sérialisation :

-   [**Description de l' \_ attribut WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_attribute_description)
-   [**\_Description WS bool \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bool_description)
-   [**Description de WS \_ octets \_**](/windows/desktop/api/WebServices/ns-webservices-ws_bytes_description)
-   [**\_Description du \_ tableau WS Byte \_**](/windows/desktop/api/WebServices/ns-webservices-ws_byte_array_description)
-   [**\_Description du \_ tableau de caractères WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_char_array_description)
-   [**\_Description du \_ type \_ personnalisé WS**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_type_description)
-   [**Description de WS \_ DateTime \_**](/windows/desktop/api/WebServices/ns-webservices-ws_datetime_description)
-   [**Description de WS \_ Decimal \_**](/windows/desktop/api/WebServices/ns-webservices-ws_decimal_description)
-   [**\_valeur par défaut de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_default_value)
-   [**Description de WS \_ double \_**](/windows/desktop/api/WebServices/ns-webservices-ws_double_description)
-   [**Description de la \_ durée WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_duration_description)
-   [**Description de l' \_ élément WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_element_description)
-   [**Description de l' \_ adresse du point de terminaison WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address_description)
-   [**Description de WS \_ enum \_**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_description)
-   [**\_valeur d’énumération WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_enum_value)
-   [**Description de l' \_ erreur WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_description)
-   [**\_Description du champ WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_field_description)
-   [**\_Description WS float \_**](/windows/desktop/api/WebServices/ns-webservices-ws_float_description)
-   [**\_Description du GUID WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_guid_description)
-   [**\_Description WS Int16 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int16_description)
-   [**\_Description WS Int32 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int32_description)
-   [**\_Description WS Int64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int64_description)
-   [**Description de WS \_ INT8 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_int8_description)
-   [**\_plage d’éléments WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_item_range)
-   [**Description de la \_ chaîne WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_string_description)
-   [**Description de WS \_ struct \_**](/windows/desktop/api/WebServices/ns-webservices-ws_struct_description)
-   [**\_Description WS TIMESPAN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_timespan_description)
-   [**Description de WS \_ UINT16 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint16_description)
-   [**Description de WS \_ UInt32 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint32_description)
-   [**\_Description WS UINT64 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint64_description)
-   [**Description de WS \_ UINT8 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_uint8_description)
-   [**Description de WS \_ Union \_**](/windows/desktop/api/WebServices/ns-webservices-ws_union_description)
-   [**\_Description du \_ champ WS Union \_**](/windows/desktop/api/WebServices/ns-webservices-ws_union_field_description)
-   [**Description de l' \_ ID unique de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_unique_id_description)
-   [**\_Description du \_ tableau WS UTF8 \_**](/windows/desktop/api/WebServices/ns-webservices-ws_utf8_array_description)
-   [**Description de WS \_ void \_**](/windows/desktop/api/WebServices/ns-webservices-ws_void_description)
-   [**Description de WS \_ WSZ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_wsz_description)
-   [**\_Description du \_ QName \_ XML WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_qname_description)
-   [**Description de la \_ chaîne XML WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_string_description)

 

 




