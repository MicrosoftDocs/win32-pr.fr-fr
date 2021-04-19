---
title: Mappage de type de données entre Active Directory et LDAP
description: Le tableau suivant mappe le nom convivial de la syntaxe à l’OID de syntaxe LDAP et à la valeur ADSTYPEENUM correspondants.
ms.assetid: 07952de0-0389-473a-84ca-b5f35fdc5b1f
ms.tgt_platform: multiple
keywords:
- mappage de type de données entre Active Directory et l’ADSI LDAP
- ADSI du fournisseur de services LDAP, mappage de type de données entre Active Directory et LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45157fb7cefe1a993e6e16dffe28f101bc73759b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106517939"
---
# <a name="data-type-mapping-between-active-directory-and-ldap"></a>Mappage de type de données entre Active Directory et LDAP

Le tableau suivant mappe le nom convivial de la syntaxe à l’OID de syntaxe LDAP et à la valeur [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) correspondants.



| Nom convivial de la syntaxe              | OID de syntaxe LDAP               | Type de données ADSTYPEENUM                 |
|-----------------------------------|-------------------------------|---------------------------------------|
| AccessPointDN                     | 1.3.6.1.4.1.1466.115.121.1.2  | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| AttributeTypeDescription          | 1.3.6.1.4.1.1466.115.121.1.3  | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| Audio                             | 1.3.6.1.4.1.1466.115.121.1.4  | **\_chaîne d’octets ADSTYPE \_**            |
| Binary                            | 1.3.6.1.4.1.1466.115.121.1.5  | **\_chaîne d’octets ADSTYPE \_**            |
| BitString                         | 1.3.6.1.4.1.1466.115.121.1.6  | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| Boolean                           | 1.3.6.1.4.1.1466.115.121.1.7  | **ADSTYPE \_ booléen**                  |
| CaseExactString                   | 1.2.840.113556.1.4.1362       | **ADSTYPE \_ \_ chaîne exacte \_**      |
| CaseIgnoreString                  | 1.2.840.113556.1.4.1221       | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| Certificat                       | 1.3.6.1.4.1.1466.115.121.1.8  | **\_chaîne d’octets ADSTYPE \_**            |
| CertificateList                   | 1.3.6.1.4.1.1466.115.121.1.9  | **\_chaîne d’octets ADSTYPE \_**            |
| CertificatePair                   | 1.3.6.1.4.1.1466.115.121.1.10 | **\_chaîne d’octets ADSTYPE \_**            |
| Pays/région                    | 1.3.6.1.4.1.1466.115.121.1.11 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| DataQualitySyntax                 | 1.3.6.1.4.1.1466.115.121.1.13 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| DeliveryMethod                    | 1.3.6.1.4.1.1466.115.121.1.14 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| DirectoryString                   | 1.3.6.1.4.1.1466.115.121.1.15 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| DN                                | 1.3.6.1.4.1.1466.115.121.1.12 | **\_chaîne DN \_ ADSTYPE**               |
| DSAQualitySyntax                  | 1.3.6.1.4.1.1466.115.121.1.19 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| EnhancedGuide                     | 1.3.6.1.4.1.1466.115.121.1.21 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| FacsimileTelephoneNumber          | 1.3.6.1.4.1.1466.115.121.1.22 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| Fax                               | 1.3.6.1.4.1.1466.115.121.1.23 | **\_chaîne d’octets ADSTYPE \_**            |
| GeneralizedTime                   | 1.3.6.1.4.1.1466.115.121.1.24 | **\_heure UTC \_ ADSTYPE**                |
| Heure (seul le serveur de site le fait) | 1.3.6.1.4.1.1466.115.121.1.24 | **\_heure UTC \_ ADSTYPE**                |
| Guide                             | 1.3.6.1.4.1.1466.115.121.1.25 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| IA5String                         | 1.3.6.1.4.1.1466.115.121.1.26 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| INTEGER                           | 1.3.6.1.4.1.1466.115.121.1.27 | **\_entier ADSTYPE**                  |
| INTEGER8 (pas dans LDAP, NTDS)      | 1.2.840.113556.1.4.906        | **\_entier long \_ ADSTYPE**           |
| JPEG                              | 1.3.6.1.4.1.1466.115.121.1.28 | **\_chaîne d’octets ADSTYPE \_**            |
| MailPreference                    | 1.3.6.1.4.1.1466.115.121.1.32 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| NameAndOptionalUID                | 1.3.6.1.4.1.1466.115.121.1.34 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| NumericString                     | 1.3.6.1.4.1.1466.115.121.1.36 | **\_chaîne numérique \_ ADSTYPE**          |
| ObjectClassDescription            | 1.3.6.1.4.1.1466.115.121.1.37 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| OctetString (pas dans la RFC)          | 1.3.6.1.4.1.1466.115.121.1.40 | **\_chaîne d’octets ADSTYPE \_**            |
| OID                               | 1.3.6.1.4.1.1466.115.121.1.38 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| ORName                            | 1.2.840.113556.1.4.1221       | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| OtherMailbox                      | 1.3.6.1.4.1.1466.115.121.1.39 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| PostalAddress                     | 1.3.6.1.4.1.1466.115.121.1.41 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| PresentationAddress               | 1.3.6.1.4.1.1466.115.121.1.43 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| PrintableString                   | 1.3.6.1.4.1.1466.115.121.1.44 | **\_chaîne imprimable \_ ADSTYPE**        |
| ObjectSecurityDescriptor          | 1.2.840.113556.1.4.907        | **\_descripteur de sécurité NT ADSTYPE \_ \_** |
| TelephoneNumber                   | 1.3.6.1.4.1.1466.115.121.1.50 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| TeletexTerminalIdentifier         | 1.3.6.1.4.1.1466.115.121.1.51 | **\_chaîne d’octets ADSTYPE \_**            |
| TelexNumber                       | 1.3.6.1.4.1.1466.115.121.1.52 | **ADSTYPE \_ \_ ignorer la \_ chaîne**     |
| UTCTime                           | 1.3.6.1.4.1.1466.115.121.1.53 | **\_heure UTC \_ ADSTYPE**                |



 

 

 




