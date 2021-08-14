---
description: Contient des informations sur la façon de construire une chaîne d’approbation de certificat.
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: Objet CertificateStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c0c228a06da9d0a4dd93491908af0c0a2d0693125be57b675ca64e10378f253
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769998"
---
# <a name="certificatestatus-object"></a>Objet CertificateStatus

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L’objet **CertificateStatus** contient des informations sur la façon de construire une chaîne d’approbation de certificat.

## <a name="members"></a>Membres

L’objet **CertificateStatus** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **CertificateStatus** a ces méthodes.



| Méthode                                                               | Description                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationPolicies**](certificatestatus-applicationpolicies.md) | Retourne une collection d' [**OID**](oids.md) qui représente les OID de stratégie d’application.<br/>                                           |
| [**CertificatePolicies**](certificatestatus-certificatepolicies.md) | Retourne une collection d' [**OID**](oids.md) qui représente les OID de stratégie de certificat utilisés pendant la génération de la chaîne.<br/>                |
| [**EKU**](certificatestatus-eku.md)                                 | Retourne l’objet [**EKU**](eku.md) utilisé pour définir les éléments EKU à vérifier lors de l’établissement de l’état de validité d’un certificat.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **CertificateStatus** a ces propriétés.



| Propriété                                                                        | Type d’accès           | Description                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificats**](certificatestatus-certificates.md)<br/>               | Lecture/écriture<br/> | Définit ou récupère la collection de certificats qui peuvent être utilisés pour créer la chaîne de certificats.<br/> **CAPICOM 2.0.0.3 et versions antérieures :** La propriété des [**certificats**](certificatestatus-certificates.md) n’est pas prise en charge.<br/>                    |
| [**CheckFlag**](certificatestatus-checkflag.md)<br/>                     | Lecture/écriture<br/> | Indicateur de contrôle de validité. Les valeurs peuvent être jointes à l’aide d’un opérateur **or** logique. L’indicateur de vérification par défaut est [**CAPICOM \_ vérifier \_ en \_ ligne**](capicom-check-flag.md).<br/>                                                                                     |
| [**Résultat**](certificatestatus-result.md)<br/>                           | Lecture seule<br/>  | Indique si le certificat est valide. La validité du certificat est vérifiée à l’aide de la valeur actuelle de la propriété [**CheckFlag**](certificatestatus-checkflag.md) et des paramètres de stratégie du certificat. Il s’agit de la propriété par défaut.<br/> |
| [**UrlRetrievalTimeout**](certificatestatus-urlretrievaltimeout.md)<br/> | Lecture/écriture<br/> | Définit ou récupère la durée pendant laquelle une URL est déterminée pour être inaccessible.<br/>                                                                                                                                                                     |
| [**VerificationTime**](certificatestatus-verificationtime.md)<br/>       | Lecture/écriture<br/> | Définit ou récupère l’heure à laquelle le certificat a été vérifié.<br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a>Remarques

Impossible de créer l’objet **CertificateStatus** .

L’objet **CertificateStatus** est retourné par la méthode [**Certificate. IsValid**](certificate-isvalid.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**Mutation**](chain.md)
</dt> </dl>

 

 
