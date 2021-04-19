---
description: Représente un certificat numérique unique.
ms.assetid: da95312b-cc9f-44f0-9517-0b28c5fcfb61
title: Objet de certificat
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1360b197f0d7f5e0579a5378a37047e6a117a9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545928"
---
# <a name="certificate-object"></a>Objet de certificat

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L’objet **Certificate** représente un seul [*certificat numérique*](../secgloss/d-gly.md).

L’objet **certificat** expose les interfaces suivantes :

-   **ICertificate** : introduit dans CAPICOM 1,0.
-   **ICertificate2** : introduit dans CAPICOM 2,0.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet **certificat** est utilisé pour effectuer les tâches suivantes :

-   Charger les données de certificat, y compris la clé privée, à partir d’un fichier.
-   Obtient des informations à partir du certificat.
-   Retourne les contraintes de base, l’utilisation améliorée de la clé, les propriétés étendues, les extensions, l’utilisation de la clé, la clé publique et les objets de modèle associés au certificat.
-   Déterminez si le certificat est valide et vérifiez la disponibilité d’accès de la clé privée du sujet du certificat.
-   Affichez le certificat.
-   Importez et exportez le certificat.
-   Enregistrez le certificat dans un fichier.
-   Récupérez ou définissez les propriétés qui décrivent le certificat.

## <a name="members"></a>Membres

L’objet **certificat** a les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **certificat** a ces méthodes.



| Méthode                                                       | Description                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BasicConstraints**](certificate-basicconstraints.md)     | Retourne un objet [**basicConstraints**](basicconstraints.md) qui représente l’extension de contraintes de base du certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**)                                                   |
| [**Vidéo**](certificate-display.md)                       | Affiche un certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**)                                                                                                                                                             |
| [**Exporter**](certificate-export.md)                         | Copie un certificat dans une chaîne encodée. La chaîne encodée peut être écrite dans un fichier ou importée dans un nouvel objet de **certificat** .<br/> (Héritée de **CertificateICertificate2ICertificate**)                                               |
| [**ExtendedKeyUsage**](certificate-extendedkeyusage.md)     | Retourne un objet [**ExtendedKeyUsage**](extendedkeyusage.md) qui indique les utilisations de clés étendues valides du certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**)                                                       |
| [**ExtendedProperties**](certificate-extendedproperties.md) | Retourne une collection des propriétés étendues du certificat.<br/> (Héritée de **CertificateICertificate2**)                                                                                                                             |
| [**Extensions**](certificate-extensions.md)                 | Retourne une collection des extensions associées au certificat.<br/> (Héritée de **CertificateICertificate2**)                                                                                                                         |
| [**GetInfo**](certificate-getinfo.md)                       | Récupère les informations du certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**)                                                                                                                                         |
| [**HasPrivateKey**](certificate-hasprivatekey.md)           | Détermine si le certificat a une [*clé privée*](../secgloss/p-gly.md) qui lui est associée.<br/> (Héritée de **CertificateICertificate2ICertificate**)                                    |
| [**Importer**](certificate-import.md)                         | Importe un certificat précédemment encodé à partir d’une chaîne dans l’objet **certificat** .<br/> (Héritée de **CertificateICertificate2ICertificate**)                                                                                             |
| [**IsValid**](certificate-isvalid.md)                       | Crée une chaîne de vérification de certificat pour un certificat et retourne un objet [**CertificateStatus**](certificatestatus.md) qui contient l’état de validité du certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**) |
| [**Utilisation**](certificate-keyusage.md)                     | Retourne un objet [**KeyUsage**](keyusage.md) qui indique l’utilisation valide de la clé du certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**)                                                                                |
| [**Load**](certificate-load.md)                             | Importe un certificat à partir d’un fichier.<br/> (Héritée de **CertificateICertificate2**)                                                                                                                                                              |
| [**PublicKey**](certificate-publickey.md)                   | Retourne un objet [**PublicKey**](publickey.md) .<br/> (Héritée de **CertificateICertificate2**)                                                                                                                                                |
| [**Enregistrer**](certificate-save.md)                             | Enregistre le certificat dans un fichier.<br/> (Héritée de **CertificateICertificate2**)                                                                                                                                                                |
| [**Modèle**](certificate-template.md)                     | Retourne le modèle associé au certificat.<br/> (Héritée de **CertificateICertificate2**)                                                                                                                                           |



 

### <a name="properties"></a>Propriétés

L’objet **certificat** a ces propriétés.



| Propriété                                                      | Type d’accès           | Description                                                                                                                                          |
|:--------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Archivé**](certificate-archived.md)<br/>           | Lecture/écriture<br/> | Définit ou récupère une valeur booléenne qui indique si le certificat est archivé.<br/> (Héritée de **CertificateICertificate2**)       |
| [**IssuerName**](certificate-issuername.md)<br/>       | Lecture seule<br/>  | Récupère une chaîne qui contient le nom de l’émetteur du certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**)            |
| [**PrivateKey**](certificate-privatekey.md)<br/>       | Lecture/écriture<br/> | Définit ou récupère la clé privée associée au certificat.<br/> (Héritée de **CertificateICertificate2**)                          |
| [**SerialNumber**](certificate-serialnumber.md)<br/>   | Lecture seule<br/>  | Récupère une chaîne qui contient le numéro de série du certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**)                 |
| [**SubjectName**](certificate-subjectname.md)<br/>     | Lecture seule<br/>  | Récupère une chaîne qui contient le nom de l’objet du certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**)           |
| [**D**](certificate-thumbprint.md)<br/>       | Lecture seule<br/>  | Récupère une chaîne hexadécimale qui contient le hachage SHA-1 du certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**) |
| [**ValidFromDate**](certificate-validfromdate.md)<br/> | Lecture seule<br/>  | Récupère la date de début de validité du certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**)               |
| [**ValidToDate**](certificate-validtodate.md)<br/>     | Lecture seule<br/>  | Récupère la date de fin de validité du certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**)                  |
| [**Version**](certificate-version.md)<br/>             | Lecture seule<br/>  | Récupère le numéro de version du certificat.<br/> (Héritée de **CertificateICertificate2ICertificate**)                                |



 

## <a name="remarks"></a>Notes

L’objet de **certificat** peut être créé et il est sécurisé pour l’écriture de scripts. Le ProgID de l’objet **certificat** est «CAPICOM. Certificate. 2».

**CAPICOM 1. *x*:** le ProgID de l’objet **certificat** est «CAPICOM. Certificate. 1».

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
