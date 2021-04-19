---
description: Fournit des services qui permettent aux développeurs d’applications d’ajouter la sécurité basée sur le chiffrement aux applications.
ms.assetid: 9a2add82-53f9-49ed-b20c-019f95e7d260
title: Informations de référence sur CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b828f3b5b35e3e0ef799529f866c23416c8df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545140"
---
# <a name="capicom-reference"></a>Informations de référence sur CAPICOM

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt le .NET Framework pour implémenter des fonctionnalités de sécurité. Pour plus d’informations, consultez [alternatives à l’utilisation de](alternatives-to-using-capicom.md)CAPICOM.\]

Le client COM CAPICOM fournit des services qui permettent aux développeurs d’applications d’ajouter la sécurité basée sur le [*chiffrement*](../secgloss/c-gly.md) aux applications. CryptoAPI intègre des fonctionnalités pour l’authentification à l’aide de [*signatures numériques*](../secgloss/d-gly.md), l’enveloppement des messages et le chiffrement et le déchiffrement des données.



| Category                    | Description                                                                                                                |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Objets du magasin de certificats   | Objets disponibles pour l’utilisation des magasins de certificats et des certificats dans ces magasins.                                       |
| Objets de signature numérique   | Objets utilisés pour signer numériquement des données et pour vérifier les signatures numériques.                                                      |
| Objets de données enveloppés      | Objets utilisés pour créer des messages de données enveloppés pour la confidentialité et pour déchiffrer des données dans des messages enveloppés.                      |
| Objets de chiffrement de données     | Objets utilisés pour chiffrer les données et déchiffrer les données chiffrées.                                                                |
| Objets auxiliaires           | Objets utilisés pour modifier les comportements par défaut et pour gérer les certificats, les magasins de certificats et les messages de l’interface utilisateur. |
| Interfaces d’interopérabilité | Interfaces qui permettent aux dérivations de CryptoAPI de fonctionner conjointement avec CAPICOM 2,0.                                          |
| Types d’énumération           | Types énumération utilisés avec CAPICOM.                                                                                       |



 

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
| [**ExtendedProperty**](extendedproperty.md)       | Représente une propriété étendue Microsoft.                                                                               |
| [**Extension**](extension.md)                     | Représente une extension de certificat unique.                                                                              |
| [**Extensions**](extensions.md)                   | Représente une collection d’objets d' [**extension**](extension.md) .                                                      |
| [**PrivateKey**](privatekey.md)                   | Représente une clé privée.                                                                                               |
| [**PublicKey**](publickey.md)                     | Représente une clé publique dans un objet de [**certificat**](certificate.md) .                                                 |
| [**Magasin**](store.md)                             | Fournit les propriétés et les méthodes permettant de choisir, gérer et utiliser les magasins de certificats et les certificats dans ces magasins. |
| [**Modèle**](template.md)                       | Représente le modèle d’extension de certificat du certificat.                                                       |



 

## <a name="digital-signature-objects"></a>Objets de signature numérique

Les objets suivants sont exportés pour signer numériquement les données et pour vérifier les signatures numériques.



| Object                           | Description                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Fournit des fonctionnalités pour signer du contenu avec une signature numérique Authenticode. |
| [**SignedData**](signeddata.md) | Objet utilisé pour signer des données et vérifier la signature sur les données signées.               |
| [**Signataire**](signer.md)         | Informations sur un seul signataire de données, y compris le certificat du signataire.           |
| [**Signataires**](signers.md)       | Collection d’objets [**signataires**](signer.md) .                                    |



 

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
| [**OID**](oid.md)                             | Représente un identificateur d’objet qui est utilisé par plusieurs propriétés CAPICOM.                                                                     |
| [**OID**](oids.md)                           | Représente une collection d’objets [**OID**](oid.md) .                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Fournit l’accès aux OID de stratégie d’une extension.                                                                                             |
| [**Qualificateur**](qualifier.md)                 | Représente un pointeur CPS (certification Practice Statement) ou un qualificateur d’avis utilisateur.                                                           |
| [**Qualificateurs**](qualifiers.md)               | Représente une collection de qualificateurs.                                                                                                          |
| [**Paramètres**](settings.md)                   | Active ou désactive les boîtes de dialogue pour demander l’identité de l’expéditeur ou du signataire si cette identité n’est pas spécifiée.                                     |
| [**Services**](utilities.md)                 | Fournit des fonctionnalités pour les tâches courantes.                                                                                                        |



 

## <a name="interoperability-interfaces"></a>Interfaces d’interopérabilité

Les interfaces suivantes permettent aux dérivations de CryptoAPI de fonctionner conjointement avec CAPICOM 2,0.



| Interface                              | Description                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Fournit l’accès au contexte d’un objet de [**certificat**](certificate.md) CAPICOM X. 509v3. Ce contexte permet d’utiliser le certificat CAPICOM dans d’autres dérivations de CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Fournit l’accès au contexte d’un objet de [**magasin**](store.md) CAPICOM. Ce contexte permet d’utiliser le magasin de certificats CAPICOM dans d’autres dérivations de CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Fournit l’accès au contexte d’un objet de [**chaîne**](chain.md) CAPICOM. Ce contexte autorise l’utilisation de la chaîne d’approbation de certificat CAPICOM dans d’autres dérivations de CryptoAPI.         |



 

## <a name="enumeration-types"></a>Types d’énumération

CAPICOM définit les types d’énumération suivants :

-   [**\_emplacement de recherche d' \_ active \_ Directory \_ CAPICOM**](capicom-active-directory-search-location.md)
-   [**CAPICOM ( \_ attribut)**](capicom-attribute.md)
-   [**TYPE d’informations du \_ certificat CAPICOM \_ \_**](capicom-cert-info-type.md)
-   [**TYPE de recherche de \_ certificat CAPICOM \_ \_**](capicom-certificate-find-type.md)
-   [**\_ \_ option include du certificat \_ CAPICOM**](capicom-certificate-include-option.md)
-   [**TYPE d’enregistrement du \_ certificat CAPICOM \_ \_ \_**](capicom-certificate-save-as-type.md)
-   [**\_ \_ type d’enregistrement certificats \_ CAPICOM \_**](capicom-certificates-save-as-type.md)
-   [**\_indicateur de vérification CAPICOM \_**](capicom-check-flag.md)
-   [**\_utilisation améliorée de la EKU**](capicom-eku.md)
-   [**\_type d’encodage \_ CAPICOM**](capicom-encoding-type.md)
-   [**\_algorithme de chiffrement CAPICOM \_**](capicom-encryption-algorithm.md)
-   [**longueur de la \_ clé de chiffrement CAPICOM \_ \_**](capicom-encryption-key-length.md)
-   [**\_code d’erreur CAPICOM \_**](capicom-error-code.md)
-   [**\_indicateur d’exportation CAPICOM \_**](capicom-export-flag.md)
-   [**\_algorithme de hachage \_ CAPICOM**](capicom-hash-algorithm.md)
-   [**emplacement de la \_ clé \_ CAPICOM**](capicom-key-location.md)
-   [**\_spécification de clé CAPICOM \_**](capicom-key-spec.md)
-   [**indicateur de stockage de \_ clé CAPICOM \_ \_**](capicom-key-storage-flag.md)
-   [**\_OID CAPICOM**](capicom-oid.md)
-   [**\_propid propid**](capicom-propid.md)
-   [**TYPE de preuve pour CAPICOM \_ \_**](capicom-prov-type.md)
-   [**\_type de secret CAPICOM \_**](capicom-secret-type.md)
-   [**\_indicateur de vérification des données signées CAPICOM \_ \_ \_**](capicom-signed-data-verify-flag.md)
-   [**\_emplacement du magasin CAPICOM \_**](capicom-store-location.md)
-   [**MODE d’ouverture du \_ magasin CAPICOM \_ \_**](capicom-store-open-mode.md)
-   [**TYPE d’enregistrement du \_ magasin CAPICOM \_ \_ \_**](capicom-store-save-as-type.md)

 

 
