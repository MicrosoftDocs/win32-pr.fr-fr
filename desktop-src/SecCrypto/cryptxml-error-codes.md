---
description: Voici les codes d’erreur au moment de l’exécution, définis dans Cryptxml. h, qui peuvent être retournés par les fonctions CryptXML.
ms.assetid: c3678767-aab3-4771-b2f2-8d79545d420d
title: Codes d’erreur CryptXML (Cryptxml. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5906c406f14081844ddce042f0e170668950e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545109"
---
# <a name="cryptxml-error-codes"></a>Codes d’erreur CryptXML

Voici les codes d’erreur au moment de l’exécution, définis dans Cryptxml. h, qui peuvent être retournés par les fonctions CryptXML.



| Constante/valeur                                                                                                                                                                                                                                                                             | Description                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_E_LARGE"></span><span id="crypt_xml_e_large"></span><dl> <dt>**Crypt \_ XML \_ E \_ grand**</dt> <dt>0x80092101L</dt> </dl>                                               | La valeur fournie est trop grande.<br/>                                                                        |
| <span id="CRYPT_XML_E_ENCODING"></span><span id="crypt_xml_e_encoding"></span><dl> <dt>**Crypt \_ 0x80092103L \_ d' \_ ENcodage XML**</dt> <dt></dt> </dl>                                      | L’encodage XML spécifié n’est pas pris en charge.<br/>                                                              |
| <span id="CRYPT_XML_E_ALGORITHM"></span><span id="crypt_xml_e_algorithm"></span><dl> <dt>**Crypt \_ \_ \_ Algorithme XML E**</dt> <dt>0x80092104L</dt> </dl>                                   | L’algorithme XML spécifié n’est pas pris en charge.<br/>                                                             |
| <span id="CRYPT_XML_E_TRANSFORM"></span><span id="crypt_xml_e_transform"></span><dl> <dt>**Crypt \_ \_ \_ Transformation XML E**</dt> <dt>0x80092105L</dt> </dl>                                   | La transformation spécifiée n’est pas prise en charge.<br/>                                                                 |
| <span id="CRYPT_XML_E_HANDLE"></span><span id="crypt_xml_e_handle"></span><dl> <dt>**Crypt \_ 0x80092106L \_ du \_ handle XML E**</dt> <dt></dt> </dl>                                            | Le handle fourni n’est pas valide.<br/>                                                                       |
| <span id="CRYPT_XML_E_OPERATION"></span><span id="crypt_xml_e_operation"></span><dl> <dt>**Crypt \_ 0x80092107L de l' \_ \_ opération XML E**</dt> <dt></dt> </dl>                                   | L’opération n’est pas valide.<br/>                                                                             |
| <span id="CRYPT_XML_E_UNRESOLVED_REFERENCE"></span><span id="crypt_xml_e_unresolved_reference"></span><dl> <dt>**Crypt \_ XML \_ E \_ \_ référence non résolue**</dt> <dt>0x80092108L</dt> </dl> | Impossible de résoudre l’élément de **référence** .<br/>                                                            |
| <span id="CRYPT_XML_E_INVALID_DIGEST"></span><span id="crypt_xml_e_invalid_digest"></span><dl> <dt>**Crypt \_ XML \_ E \_ 0x80092109L \_ condensé non valide**</dt> <dt></dt> </dl>                   | La valeur Digest n’est pas valide.<br/>                                                                          |
| <span id="CRYPT_XML_E_INVALID_SIGNATURE"></span><span id="crypt_xml_e_invalid_signature"></span><dl> <dt>**Crypt \_ XML 0x8009210AL de \_ \_ \_ signature non valide**</dt> <dt></dt> </dl>          | La valeur de la signature n’est pas valide.<br/>                                                                       |
| <span id="CRYPT_XML_E_HASH_FAILED"></span><span id="crypt_xml_e_hash_failed"></span><dl> <dt>**Crypt \_ \_Échec du \_ hachage \_ E XML**</dt> <dt>0x8009210BL</dt> </dl>                            | Impossible de créer ou de calculer le hachage.<br/>                                                                 |
| <span id="CRYPT_XML_E_SIGN_FAILED"></span><span id="crypt_xml_e_sign_failed"></span><dl> <dt>**Crypt \_ Échec de la \_ \_ signature \_ E XML**</dt> <dt>0x8009210CL</dt> </dl>                            | L’opération de signature de chiffrement a échoué.<br/>                                                           |
| <span id="CRYPT_XML_E_VERIFY_FAILED"></span><span id="crypt_xml_e_verify_failed"></span><dl> <dt>**Crypt \_ \_ \_ \_ Échec de la vérification du code XML E**</dt> <dt>0x8009210DL</dt> </dl>                      | Échec de la vérification de la signature.<br/>                                                                      |
| <span id="CRYPT_XML_E_TOO_MANY_SIGNATURES"></span><span id="crypt_xml_e_too_many_signatures"></span><dl> <dt>**Crypt \_ XML \_ E \_ trop \_ de \_ signatures**</dt> <dt>0x8009210EL</dt> </dl>   | Le nombre d’éléments de **signature** dans le document a dépassé la limite maximale autorisée pour le traitement.<br/> |
| <span id="CRYPT_XML_E_INVALID_KEYVALUE"></span><span id="crypt_xml_e_invalid_keyvalue"></span><dl> <dt>**Crypt \_ XML \_ E \_ \_ valeur de KeyValue non valide**</dt> <dt>0x8009210FL</dt> </dl>             | La valeur de clé fournie n’est pas valide.<br/>                                                           |
| <span id="CRYPT_XML_E_UNEXPECTED_XML"></span><span id="crypt_xml_e_unexpected_xml"></span><dl> <dt>**Crypt \_ XML \_ E \_ 0x80092110L \_ XML inattendu**</dt> <dt></dt> </dl>                   | Du code XML non valide ou inattendu a été rencontré.<br/>                                                              |
| <span id="CRYPT_XML_E_SIGNER"></span><span id="crypt_xml_e_signer"></span><dl> <dt>**Crypt \_ 0x80092111L \_ du \_ signataire E XML**</dt> <dt></dt> </dl>                                            | Impossible de trouver la clé du signataire.<br/>                                                                      |
| <span id="CRYPT_XML_E_NON_UNIQUE_ID"></span><span id="crypt_xml_e_non_unique_id"></span><dl> <dt>**Crypt \_ \_ \_ \_ \_ ID non unique XML**</dt> <dt>0x80092112L</dt> </dl>                     | Un attribut d' **ID** non unique a été trouvé.<br/>                                                                 |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Cryptxml. h</dt> </dl> |



 

 




