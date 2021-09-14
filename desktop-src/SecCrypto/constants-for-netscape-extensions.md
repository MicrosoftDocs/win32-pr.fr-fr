---
description: Utilisé avec les opérations d’encodage et de décodage.
ms.assetid: 713c95ae-e5d0-416c-ba0c-4b5399aa8a33
title: Constantes pour les extensions Netscape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06999a879d0d289bb95cdb8ba5506200154d60e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229020"
---
# <a name="constants-for-netscape-extensions"></a>Constantes pour les extensions Netscape

Les extensions Netscape suivantes sont utilisées avec les opérations d’encodage et de décodage. Les constantes prédéfinies et les chaînes de l’identificateur d’objet de Netscape ne sont pas utilisées directement avec les fonctions d’encodage ou de décodage, [**CryptEncodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobject), [**CryptEncodeObjectEx**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobjectex), [**CryptSignAndEncodeCertificate**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate), [**CryptDecodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobject)ou [**CryptDecodeObjectEx**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex). Au lieu de cela, ces extensions requièrent l’utilisation du *lpszStructType* affiché.

Pour obtenir des informations supplémentaires qui s’appliquent à certaines extensions Netscape, consultez les remarques qui suivent le tableau.



| Identificateurs d’objet d’extension de certificat Netscape                      | *lpszStructType*                                           | *PvStructInfo* correspondant                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| szOID \_ Netscape \_ base \_ URL « 2.16.840.1.113730.1.2 »<br/>           | X509 \_ toute chaîne \_ ou \_ Unicode x509 \_ toute \_ chaîne<br/> | [**Certificat \_ \_valeur de nom**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Le membre **dwValueType** est défini sur CERT \_ RDN \_ IA5 \_ String. Le membre **pbData** du membre de **valeur** pointe vers une \_ chaîne IA5 ajoutée au début de toutes les adresses URL relatives dans un certificat. Cette extension peut être considérée comme une optimisation pour réduire la taille des extensions d’URL.                                                                                                       |
| URL de la \_ stratégie d’autorité de certification Netscape szOID \_ \_ \_ « 2.16.840.1.113730.1.8 »<br/>     | X509 \_ toute chaîne \_ ou \_ Unicode x509 \_ toute \_ chaîne<br/> | [**Certificat \_ \_valeur de nom**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Le membre **dwValueType** est défini sur CERT \_ RDN \_ IA5 \_ String. Le membre **pbData** du membre de **valeur** pointe vers une \_ chaîne IA5, l’URL relative ou absolue de la page Web décrivant les stratégies sous lesquelles le certificat a été émis.                                                                                                                                                            |
| \_URL de RÉvocation de l’autorité de certification Netscape szOID \_ \_ \_ « 2.16.840.1.113730.1.4 »<br/> | X509 \_ toute chaîne \_ ou \_ Unicode x509 \_ toute \_ chaîne<br/> | [**Certificat \_ \_valeur de nom**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Le membre **dwValueType** est défini sur CERT \_ RDN \_ IA5 \_ String. Le membre **pbData** du membre de **valeur** pointe vers une \_ chaîne IA5 qui est l’URL relative ou absolue utilisée pour vérifier l’état de révocation des certificats signés par l' [*autorité de certification*](../secgloss/c-gly.md) à laquelle le certificat actuel appartient. |
| \_URL de renouvellement du certificat Netscape szOID \_ \_ \_ « 2.16.840.1.113730.1.7 »<br/>  | X509 \_ toute chaîne \_ ou \_ Unicode x509 \_ toute \_ chaîne<br/> | [**Certificat \_ \_valeur de nom**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Le membre **dwValueType** est défini sur CERT \_ RDN \_ IA5 \_ String. Le membre **pbData** du membre de **valeur** pointe vers une \_ chaîne IA5 qui est l’URL relative ou absolue d’un formulaire de renouvellement de certificat.                                                                                                                                                                                                     |
| szOID de la \_ \_ séquence de certificats Netscape \_ « 2.16.840.1.113730.2.5 »<br/>      | \_ \_ \_ séquence d’informations de contenu PKCS \_ de \_ any                     | [**CRYPTer \_ \_ \_ les informations \_ de contenu de \_ tout**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)                                                                                                                                                                                                                                                                                                                                                                |
| szOID \_ \_ type de certificat Netscape \_ « 2.16.840.1.113730.1.1 »<br/>          | \_Bits x509                                                 | [**BLOB de chiffrement \_ binaire \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_bit_blob)                                                                                                                                                                                                                                                                                                                                                                                                           |
| szOID \_ - \_ Commentaire Netscape « 2.16.840.1.113730.1.13 »<br/>            | X509 \_ toute chaîne \_ ou \_ Unicode x509 \_ toute \_ chaîne<br/> | [**Certificat \_ \_valeur de nom**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Le membre **dwValueType** est défini sur CERT \_ RDN \_ IA5 \_ String. Le membre **pbData** du membre de **valeur** pointe vers une \_ chaîne IA5 qui est un commentaire à afficher lorsque le certificat est affiché.                                                                                                                                                                                                         |
| \_URL de \_ révocation Netscape de szOID \_ « 2.16.840.1.113730.1.3 »<br/>     | X509 \_ toute chaîne \_ ou \_ Unicode x509 \_ toute \_ chaîne<br/> | [**Certificat \_ \_valeur de nom**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Le membre **dwValueType** est défini sur CERT \_ RDN \_ IA5 \_ String. Le membre **pbData** du membre de **valeur** pointe vers une \_ chaîne IA5 qui est une URL relative ou absolue utilisée pour vérifier l’état de révocation du certificat.                                                                                                                                                                              |
| szOID \_ \_ nom du serveur Netscape SSL \_ \_ « 2.16.840.1.113730.1.12 »<br/>  | X509 \_ toute chaîne \_ ou \_ Unicode x509 \_ toute \_ chaîne<br/> | [**Certificat \_ \_valeur de nom**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Le membre **dwValueType** est défini sur CERT \_ RDN \_ IA5 \_ String. Le membre **pbData** du membre de **valeur** pointe vers une \_ chaîne IA5 qui est une expression d’interpréteur de commandes utilisée pour faire correspondre le nom d’hôte du serveur SSL à l’aide de ce certificat.                                                                                                                                                                       |



 

Pour toutes les fonctions d’encodage qui utilisent soit la \_ chaîne x509 Any \_ , soit la chaîne X5O9 \_ Unicode \_ Any \_ String **lpszStructType**, la chaîne x509 \_ Any \_ String est utilisée si le format de chaîne du membre **pbData** du membre **value** est [*ASCII*](../secgloss/a-gly.md), et x509 \_ Unicode \_ Any \_ String est utilisé si le format de chaîne est Unicode. Dans le cas Unicode, la chaîne doit être convertie en une \_ chaîne IA5 avant l’encodage en définissant le membre **dwValueType** de la structure de [**\_ \_ valeur de nom de certificat**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value) sur CERT \_ RDN \_ IA5 \_ String.

Pour les fonctions de décodage, l’utilisateur sélectionne le format de la chaîne de sortie. Utilisez x509 \_ n’importe quelle \_ chaîne si le format de chaîne souhaité est ASCII, et x509 \_ Unicode \_ Any \_ String si le format de chaîne souhaité est Unicode.

Pour l’extension d’URL de renouvellement de certificat \_ Netscape szOID \_ \_ \_ , la structure de données contient une URL relative ou absolue qui pointe vers un formulaire de renouvellement de certificat. Le formulaire de renouvellement est accessible avec une méthode HTTP obtenue à l’aide d’une URL qui est la concaténation de l’URL de renouvellement et du numéro de série du certificat. Le numéro de série du certificat est encodé sous la forme d’une chaîne de chiffres hexadécimaux ASCII. Par exemple, si Netscape-base-URL est l’URL de l'*autorité de certification* https:///, que Netscape-CERT-Renewal-URL est cgi-bin/Check-Renew. cgi ? et que le numéro de série du certificat est 173420, l’URL obtenue est : https://URL de l'*autorité de certification*/cgi-bin/Check-Renew.cgi ? 02a56c. Le document renvoyé doit être un formulaire HTML qui permettra à l’utilisateur de demander un renouvellement de son certificat.

Pour l' \_ extension de \_ séquence de certificat Netscape szOID \_ à l’aide de l' \_ \_ encodage ASN x509, le certificat est encodé sous la forme d’une \_ \_ structure d’informations de contenu PKCS encapsulant une séquence de any. La valeur du membre **ContentType** est **pszObjId**, tandis que le champ Content est la structure suivante :

SequenceOfAny :: = séquence de ANY

Les [**\_ \_ objets BLOB der**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))de chiffrer dans la [**\_ \_ \_ séquence d’informations de chiffrement \_ de \_ n’importe quel**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)point membre **rgValue** du point de vue des certificats X509 encodés.

Pour \_ \_ les extensions de type de certificat Netscape szOID \_ , les bits suivants sont définis.



| Valeur en bits | Type correspondant                      |
|-----------|-----------------------------------------|
| 0x80      | \_type de \_ certificat d’authentification du client Netscape SSL \_ \_ \_ |
| 0x40      | \_type de \_ \_ certificat d’authentification serveur SSL \_ Netscape \_ |
| 0x04      | TYPE de certificat de l' \_ \_ autorité de certification SSL \_ de Netscape \_           |



 

Pour les \_ extensions d' \_ URL de révocation Netscape szOID \_ , une URL relative ou absolue peut être utilisée pour vérifier l’état de révocation d’un certificat. La vérification de la révocation sera effectuée en tant que méthode HTTP obtenir à l’aide d’une URL qui est la concaténation de la révocation-URL et du numéro de série du certificat. Le numéro de série du certificat est encodé sous la forme d’une chaîne de chiffres hexadécimaux ASCII. Par exemple, si Netscape-base-URL est https : \/ /www.certs-r-US.com/, l’URL Netscape-Revocation-URL est cgi-bin/Check-Rev. cgi ? et le numéro de série du certificat est 173420, l’URL obtenue est : https : \/ /www.certs-r-US.com/cgi-bin/Check-Rev.cgi ?02a56c.

Le serveur doit retourner un document avec le type de contenu application/x-Netscape-révocation. Le document doit contenir un seul chiffre ASCII, « 1 » si le certificat n’est pas valide actuellement, et « 0 » s’il est actuellement valide.

Notez que pour toutes les URL qui incluent le numéro de série du certificat, le numéro de série est encodé sous la forme d’une chaîne composée d’un nombre pair de chiffres hexadécimaux. Si le nombre de chiffres significatifs est impair, la chaîne aura un zéro non significatif unique pour garantir la génération d’un nombre pair de chiffres.

 

 
