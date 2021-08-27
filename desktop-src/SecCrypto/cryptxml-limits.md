---
description: CryptXML définit les limites globales suivantes dans le fichier d’en-tête Cryptxml. h.
ms.assetid: 8f4dc314-76fc-40ce-a1e1-a701ae39d66d
title: Limites de CryptXML (Cryptxml. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a0dcdf5dc8f8bd9efed4dcdb15ca316ecb1645e5775f3d714f46c6835b3a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100919"
---
# <a name="cryptxml-limits"></a>Limites de CryptXML

CryptXML définit les limites globales suivantes dans le fichier d’en-tête Cryptxml. h.



| Constante/valeur                                                                                                                                                                                                                                                             | Description                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_BLOB_MAX"></span><span id="crypt_xml_blob_max"></span><dl> <dt>**Crypt \_ \_ \_ Nombre maximal d’objets BLOB XML**</dt> <dt>0x7FFFFFF8</dt> </dl>                             | Les données encodées ne peuvent pas dépasser 2 gigaoctets (Go).<br/>                                                                                                                                                                               |
| <span id="CRYPT_XML_ID_MAX"></span><span id="crypt_xml_id_max"></span><dl> <dt>**Crypt \_ \_ID XML \_ Max**</dt> <dt>256</dt> </dl>                                          | La longueur de l’ID ne peut pas dépasser 256 caractères.<br/>                                                                                                                                                                                    |
| <span id="CRYPT_XML_URI_MAX"></span><span id="crypt_xml_uri_max"></span><dl> <dt>**Crypt \_ \_URI XML \_ Max**</dt> . <dt>8 \* 1024</dt> </dl>                                   | La longueur de l’URI ne peut pas dépasser 8192 caractères.<br/>                                                                                                                                                                                  |
| <span id="CRYPT_XML_SIGNATURES_MAX"></span><span id="crypt_xml_signatures_max"></span><dl> <dt>**Crypt \_ \_ \_ Nombre maximal de signatures XML**</dt> <dt>16</dt> </dl>                   | Nombre maximal d’éléments de **signature** par défaut par document. Cette valeur peut être remplacée en spécifiant un nouveau maximum lors du passage de valeurs de propriété en tant que structures de [**\_ \_ propriété XML énigmatique**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_property) .<br/> |
| <span id="CRYPT_XML_TRANSFORM_MAX"></span><span id="crypt_xml_transform_max"></span><dl> <dt>**Crypt \_ \_Conversion XML \_ Max**</dt> . <dt>16</dt> </dl>                      | Nombre maximal de transformations, représentées par des structures d' [**\_ \_ algorithme XML énigmatiques**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm) , par référence, représentées par une structure de [**\_ \_ référence XML**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_reference) de chiffrement.<br/>          |
| <span id="CRYPT_XML_SIGNATURE_VALUE_MAX"></span><span id="crypt_xml_signature_value_max"></span><dl> <dt>**Crypt \_ \_Valeur de signature XML \_ \_ Max**</dt> <dt>2048</dt> </dl> | Longueur maximale, en octets, d’une structure [**de \_ \_ signature XML**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) de chiffrement.<br/>                                                                                                                         |
| <span id="CRYPT_XML_DIGEST_VALUE_MAX"></span><span id="crypt_xml_digest_value_max"></span><dl> <dt>**Crypt \_ \_Valeur Digest \_ XML \_ Max**</dt> <dt>128</dt> </dl>           | Longueur maximale, en octets, d’un condensé.<br/>                                                                                                                                                                                 |
| <span id="CRYPT_XML_OBJECTS_MAX"></span><span id="crypt_xml_objects_max"></span><dl> <dt>**Crypt \_ \_Objets XML \_ Max**</dt> <dt>256</dt> </dl>                           | Utilisé en interne pour spécifier le nombre maximal d’éléments **objets** autorisés par signature.<br/>                                                                                                                                |
| <span id="CRYPT_XML_REFERENCES_MAX"></span><span id="crypt_xml_references_max"></span><dl> <dt>**Crypt \_ \_Références XML \_ Max**</dt> <dt>0x7FF8</dt> </dl>               | Nombre maximal d’éléments de **référence** autorisés.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Cryptxml. h</dt> </dl> |



 

 




