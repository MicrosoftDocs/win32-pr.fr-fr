---
description: Répertorie les objets fournis par CryptoAPI.
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: Objets de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea3476e7edad1d32fe1e11635bd65622d2a8375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393504"
---
# <a name="cryptography-objects"></a>Objets de chiffrement

Les objets de chiffrement sont catégorisés en fonction de l’utilisation comme suit :

-   [Objets du magasin de certificats](#certificate-store-objects)
-   [Objets de signature numérique](#digital-signature-objects)
-   [Objets de données enveloppés](#enveloped-data-objects)
-   [Objets de chiffrement de données](#data-encryption-objects)
-   [Objets auxiliaires](#auxiliary-objects)
-   [Objets d’inscription de certificat](#certificate-enrollment-objects)

## <a name="certificate-store-objects"></a>Objets du magasin de certificats

Les objets suivants fonctionnent avec les [*magasins de certificats*](../secgloss/c-gly.md) et les certificats dans ces magasins. CAPICOM prend en charge l’utilisation de l’utilisateur actuel, de l’ordinateur local, de la mémoire et des magasins de certificats de Active Directory.



| Object                                             | Description                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Certificat**](certificate.md)                 | Un seul certificat numérique.                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | Collection d’objets [**PolicyInformation**](policyinformation.md) .                                                 |
| [**Certificats**](certificates.md)               | Collection d’objets de [**certificat**](certificate.md) .                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Fournit des informations d’État sur un certificat.                                                                           |
| [**Mutation**](chain.md)                             | Crée et vérifie une chaîne de validation de certificat sur la base d’un certificat numérique.                                       |
| [**ExtendedProperties**](extendedproperties.md)   | Représente une collection d’objets [**ExtendedProperty**](extendedproperty.md) .                                        |
| [**ExtendedProperty**](extendedproperties.md)     | Représente une propriété étendue Microsoft.                                                                               |
| [**Extension**](extension.md)                     | Représente une extension de certificat unique.                                                                              |
| [**Extensions**](extensions.md)                   | Représente une collection d’objets d' [**extension**](extension.md) .                                                      |
| [**PrivateKey**](privatekey.md)                   | Représente une clé privée.                                                                                               |
| [**PublicKey**](publickey.md)                     | Représente une clé publique dans un objet de [**certificat**](certificate.md) .                                                 |
| [**Magasin**](store.md)                             | Fournit les propriétés et les méthodes permettant de choisir, gérer et utiliser les magasins de certificats et les certificats dans ces magasins. |
| [**Modèle**](template.md)                       | Représente le modèle d’extension de certificat du certificat.                                                       |



 

## <a name="digital-signature-objects"></a>Objets de signature numérique

Les objets suivants sont exportés pour signer numériquement les données et pour vérifier les signatures numériques.



| Object                           | Description                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Objet utilisé pour signer du code avec une signature numérique Authenticode et pour vérifier la signature du code signé. |
| [**SignedData**](signeddata.md) | Objet utilisé pour signer des données et vérifier la signature sur les données signées.                                        |
| [**Signataire**](signer.md)         | Informations sur un seul signataire de données, y compris le certificat du signataire.                                    |
| [**Signataires**](signers.md)       | Collection d’objets [**signataires**](signer.md) .                                                             |



 

## <a name="enveloped-data-objects"></a>Objets de données enveloppés

Les objets suivants sont exportés pour créer des messages de données enveloppés pour la confidentialité et pour déchiffrer des données dans des messages enveloppés.



| Object                                 | Description                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnvelopedData**](envelopeddata.md) | Objets utilisés pour créer, envoyer et recevoir des données enveloppées. Les données enveloppées sont chiffrées afin que seuls les destinataires prévus puissent les déchiffrer. |
| [**Destinataires**](recipients.md)       | Collection d’objets de [**certificat**](certificate.md) des destinataires prévus d’un message enveloppé.                           |



 

## <a name="data-encryption-objects"></a>Objets de chiffrement de données

L’objet suivant est exporté pour chiffrer les données arbitraires pour la confidentialité et déchiffrer les données chiffrées.



| Object                                 | Description                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**EncryptedData**](encrypteddata.md) | Objets utilisés pour chiffrer les données. Les données chiffrées dans un objet [**EncryptedData**](encrypteddata.md) peuvent être déchiffrées. |



 

## <a name="auxiliary-objects"></a>Objets auxiliaires

Les objets suivants sont exportés pour modifier les comportements par défaut d’autres objets et pour gérer les certificats, les magasins de certificats et les messages.



| Object                                         | Description                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algorithme**](algorithm.md)                 | Définit la longueur de l’algorithme et de la [*clé*](../secgloss/k-gly.md) à utiliser dans les opérations de chiffrement. |
| [**Attribut**](attribute.md)                 | Fournit une seule partie des informations ajoutées sur une signature, telles que l’heure de la signature.                                                    |
| [**Attributs**](attributes.md)               | Collection d’objets [**attribute**](attribute.md) .                                                                                           |
| [**BasicConstraints**](basicconstraints.md)   | Fournit un accès en lecture seule aux contraintes de base sur les utilisations d’un certificat.                                                                    |
| [**EKU**](eku.md)                             | Fournit l’accès aux propriétés EKU des certificats.                                                                                              |
| [**Utilisations améliorées de la clé**](ekus.md)                           | Collection d’objets [**EKU**](eku.md) .                                                                                                       |
| [**EncodedData**](encodeddata.md)             | Représente un bloc de données encodées.                                                                                                             |
| [**ExtendedKeyUsage**](extendedkeyusage.md)   | Fournit un accès en lecture seule aux propriétés d’utilisation de clé étendue des certificats.                                                                 |
| [**HashedData**](hasheddata.md)               | Fournit les fonctionnalités permettant d’appliquer un algorithme de hachage à une chaîne.                                                                               |
| [**Utilisation**](keyusage.md)                   | Fournit un accès en lecture seule aux propriétés d’utilisation de clé des certificats.                                                                              |
| [**NoticeNumbers**](noticenumbers.md)         | Représente une collection d’objets d' [**extension**](extension.md) .                                                                              |
| [**OID**](oid.md)                             | Représente un identificateur d’objet qui est utilisé par plusieurs propriétés CAPICOM.                                                                     |
| [**OID**](oids.md)                           | Représente une collection d’objets [**OID**](oid.md) .                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Fournit l’accès aux OID de stratégie d’une extension.                                                                                             |
| [**Qualificateur**](qualifier.md)                 | Représente un pointeur CPS (certification Practice Statement) ou un qualificateur d’avis utilisateur.                                                           |
| [**Qualificateurs**](qualifiers.md)               | Représente une collection de qualificateurs.                                                                                                          |
| [**Paramètres**](settings.md)                   | Active ou désactive les boîtes de dialogue pour demander l’identité de l’expéditeur ou du signataire si cette identité n’est pas spécifiée.                                     |
| [**Services**](utilities.md)                 | Fournit des fonctionnalités pour les tâches courantes.                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a>Objets d’inscription de certificat

L’objet suivant est utilisé pour l’inscription de certificats.



| Object                     | Description                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) | Objet qui représente le contrôle d’inscription de certificat. Il est principalement utilisé lors de la programmation dans Visual Basic ou dans un autre langage Automation. |



 

 

 
