---
description: Les propriétés de nom sont des propriétés de certificats et de demandes de certificat qui représentent des données relatives à l’objet, c’est-à-dire le propriétaire du certificat ou la personne pour laquelle un certificat est demandé.
ms.assetid: c32756f7-4431-410e-ab3a-c7b748a43829
title: Propriétés du nom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28765f0c278678ed5bdca9ef8547c1c6dc85ca7b6b343b229441b4b777eac688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425309"
---
# <a name="name-properties"></a>Propriétés du nom

Les propriétés de nom sont des propriétés de certificats et de demandes de certificat qui représentent des données relatives à l’objet, c’est-à-dire le propriétaire du certificat ou la personne pour laquelle un certificat est demandé. Chaque propriété Name est identifiée par un nom de propriété. Ces noms ne sont pas localisables ; Toutefois, les propriétés de nom correspondent généralement à une colonne de base de données de services de certificats. vous pouvez utiliser le composant logiciel enfichable MMC Autorité de certification, l’outil de ligne de commande « certutil-Schema » ou la méthode [**IEnumCERTVIEWCOLUMN :: GetDisplayName**](/windows/desktop/api/Certview/nf-certview-ienumcertviewcolumn-getdisplayname) pour afficher les versions localisées des noms de colonne de base de données.

Le nom de la propriété (mais pas les alias) peut avoir « subject ». comme préfixe facultatif. Par exemple, pour faire référence au nom commun du sujet, vous pouvez utiliser « CommonName » ou « subject. CommonName ».

En plus de son nom, chaque propriété a un certain nombre d’alias que les services de certificats reconnaissent en tant que noms de remplacement pour la propriété. Notez que les [*identificateurs d’objet*](../secgloss/o-gly.md) (OID) sont des alias acceptables, comme les **\_ \* *constantes szOID _. Ces constantes sont des définitions (dans wincrypt. h) qui représentent les OID. Par exemple, _* szOID \_ \_ nom commun** est défini en tant que « 2.5.4.3 ». Par conséquent, vous pouvez utiliser les constantes **szOID \_ \*** comme alias à la place des OID qu’ils représentent.



| Nom de la propriété                 | Alias                                                                                                                                                        | Type de données                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| « Subject. CommonName »          | « CommonName » « CN »<br/> "2.5.4.3"<br/> **\_nom commun \_ szOID**<br/>                                                                           | **Chaîne** (maximum 64 chars)  | Pour les certificats utilisateur, le nom complet de la personne. Pour les certificats d’ordinateur, le ***/** _chemin d’accès nom d'_ hôte complet * utilisé dans les recherches DNS (Domain Name System) (par exemple, *hostname ***.** _Exemple_* _. com_*).<br/>                                                                                                                                                                                                                                                                        |
| « Subject. Country »             | "Pays" "C"<br/> 2.5.4.6<br/> **\_nom du pays szOID \_**<br/>                                                                              | **Chaîne** (2 caractères max.)    | Pays ou région du sujet. Il s’agit d’un code de pays/région à deux caractères [*X. 500*](../secgloss/x-gly.md) (par exemple, pour États-Unis ou ca pour le Canada).<br/> La plupart de ces codes à deux caractères sont définis dans la norme ISO 3166. en outre, le code des paramètres régionaux actuels est disponible via un appel à la fonction Windows [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) (en spécifiant un *LCType* de paramètres régionaux \_ SISO3166CTRYNAME).<br/> |
| « Subject. DeviceSerialNumber »  | "DeviceSerialNumber" "2.5.4.5"<br/> **Numéro de série de l' \_ appareil szOID \_ \_**<br/>                                                                         | **Chaîne** (max 1024 caractères) | Numéro de série de l’appareil.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| « Subject. DomainComponent »     | « DomainComponent » « DC »<br/> "0.9.2342.19200300.100.1.25"<br/> **\_composant de domaine szOID \_**<br/>                                              | **Chaîne** (max 128 caractères)  | Composant d’un nom DNS (Domain Name System).                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| « Subject.EMail »               | « E-mail » « E »<br/> "1.2.840.113549.1.9.1"<br/> **szOID \_ RSA \_ emailaddr**<br/>                                                                  | **Chaîne** (max 128 caractères)  | Adresse de messagerie (par exemple, « someone@example.com »).                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| « Subject. GivenName »           | "GivenName" "G"<br/> "2.5.4.42"<br/> **szOID \_ \_ nom donné**<br/>                                                                             | **Chaîne** (16 caractères max.)   | Prénom du sujet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| « Subject.Initials »            | « Initiales » « I »<br/> "2.5.4.43"<br/> **\_initiales szOID**<br/>                                                                                 | **Chaîne** (5 caractères max.)    | Initiales de l’objet (facultatif).                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| « Subject. localité »            | « Localité » « L »<br/> "2.5.4.7"<br/> **nom de la \_ localité szOID \_**<br/>                                                                            | **Chaîne** (max 128 caractères)  | Nom de la ville du sujet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| « Subject. Organization »        | « Organisation » « org »<br/> Sorties<br/> 2.5.4.10<br/> **nom de l' \_ organisation szOID \_**<br/>                                                  | **Chaîne** (max 64 caractères)   | Nom légal de l’organisation du sujet.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| « Subject. unité »             | "Unité" "unité"<br/> OrganizationalUnit<br/> Organisation<br/> 2.5.4.11<br/> **nom de l' \_ unité d’organisation szOID \_ \_**<br/> | **Chaîne** (max 64 caractères)   | Nom de la sous-organisation ou du service du sujet.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| « Subject. State »               | « État » « ST »<br/> X<br/> 2.5.4.8<br/> **\_ \_ nom de l’État ou de la \_ province \_ szOID**<br/>                                                    | **Chaîne** (max 128 caractères)  | Nom complet de l’État ou de la province du sujet (par exemple, Californie).                                                                                                                                                                                                                                                                                                                                                                                                                         |
| « Subject. StreetAddress »       | « StreetAddress » « rue »<br/> "2.5.4.9"<br/> **\_adresse postale szOID \_**<br/>                                                                 | **Chaîne** (30 caractères maximum)   | Rue ou zone de commande du sujet.                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| « Subject. Surname »             | « Nom » « SN »<br/> "2.5.4.4"<br/> **nom de szOID sur \_ \_**<br/>                                                                                 | **Chaîne** (max 40 caractères)   | Nom de l’objet.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| « Subject. title »               | "Titre" "T"<br/> "2.5.4.12"<br/> **\_titre szOID**<br/>                                                                                       | **Chaîne** (max 64 caractères)   | Titre de la personne qui a demandé le certificat (facultatif).                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| « Subject. UnstructuredAddress » | "UnstructuredAddress" "1.2.840.113549.1.9.8"<br/> **szOID \_ RSA \_ unstructAddr**<br/>                                                                | **Chaîne** (max 1024 caractères) | Adresse non structurée.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| « Subject. UnstructuredName »    | "UnstructuredName" "1.2.840.113549.1.9.2"<br/> **szOID \_ RSA \_ unstructName**<br/>                                                                   | **Chaîne** (max 1024 caractères) | Nom non structuré.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

Les propriétés suivantes sont associées à l’objet, bien qu’elles ne soient pas des propriétés de nom. Le module de stratégie ne peut pas définir ces propriétés directement.



| Propriété                    | Type de données                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| « Request. DistinguishedName » | **Chaîne** (max 8192 caractères) | [*Nom unique relatif*](../secgloss/r-gly.md) de la demande, représentation textuelle du sujet dans la demande. Cette représentation est constituée de propriétés de nom, par exemple, « CN = MyName, OU = MonService, C = US ». L’application de services de certificats définit cette propriété avant d’appeler le module de stratégie, en appelant [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) à l’aide de l’objet du RawRequest. |
| « Request. RawName »           | **Binaire** (maximum 4096 octets) | Objet [*BLOB*](../secgloss/b-gly.md) d’objets binaires ASN. 1 ( [*Abstract Syntax Notation One*](../secgloss/a-gly.md) ) extrait de la requête. L’application des services de certificats définit cette propriété avant d’appeler le module de stratégie. sa valeur est déterminée par l’objet du RawRequest.                                                                                     |
| DistinguishedName         | **Chaîne** (max 8192 caractères) | Nom unique relatif du certificat, représentation textuelle du sujet dans le certificat. Cette représentation est constituée de propriétés de nom, par exemple, « CN = MyName, OU = MonService, C = US ». L’application de services de certificats définit cette propriété après avoir appelé le module de stratégie, en appelant [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) à l’aide de RawName.                                                                                                               |
| "RawName"                   | **Binaire** (maximum 4096 octets) | Objet [*BLOB*](../secgloss/b-gly.md) d’objets binaires ASN. 1 utilisé pour construire le certificat. L’application des services de certificats définit cette propriété après avoir appelé le module de stratégie. sa valeur est déterminée par les valeurs de propriétés de nom spécifiques (subject. CommonName, etc.) comme indiqué par le SubjectTemplate.                                                                                                                                        |



 

Les composants de [*nom unique relatif*](../secgloss/r-gly.md) apparaissent dans la propriété DistinguishedName et l’ordre dans lequel ils apparaissent sont contrôlés par la valeur de Registre « SubjectTemplate » contenue dans la clé de Registre suivante :

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            CertSvc
               Configuration
                  CaName
```

Lorsque les services de certificats analysent les noms d' [*attributs*](../secgloss/a-gly.md) , il ignore les espaces, les traits d’Union (signes moins) et la casse. Par exemple, les valeurs « AttributeName1 », « attribut nom1 » et « attribute-nom1 » sont toutes équivalentes. Pour les valeurs d’attribut, les services de certificats ignorent les espaces blancs de début et de fin.

Toutes les propriétés précédentes, à l’exception de DistinguishedName, RawName et subject. Country, prennent en charge la syntaxe à valeurs multiples à l’aide d’un caractère de saut de ligne. Le séparateur de saut de ligne ne peut pas être désactivé ou modifié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du certificat](certificate-properties.md)
</dt> <dt>

[**ICertServerExit::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> <dt>

[**ICertServerExit::GetRequestProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getrequestproperty)
</dt> <dt>

[**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerPolicy::GetRequestProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getrequestproperty)
</dt> <dt>

[**ICertServerPolicy::SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty)
</dt> </dl>

 

 
