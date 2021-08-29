---
description: Représente une chaîne d’approbation de certificat.
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Chaîne (objet)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 861f3233c4b089dc62e56977dd2d55c59fae71aed799fa73958421a111c1ccd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876949"
---
# <a name="chain-object"></a>Chaîne (objet)

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

L’objet **chaîne** représente une chaîne d’approbation de certificat.

Cet objet fournit des propriétés et des méthodes pour générer une chaîne d’approbation de certificat afin de vérifier la validité des certificats. La chaîne est créée à l’aide de la valeur de la propriété [**CertificateStatus. CheckFlag**](certificatestatus-checkflag.md) et des paramètres de stratégie d’un objet [**CertificateStatus**](certificatestatus.md) .

L’objet **chaîne** expose les interfaces suivantes :

-   **IChain2**: introduit dans CAPICOM 2,0.
-   **IChain**: introduit dans CAPICOM 1,0.

## <a name="when-to-use"></a>Quand l’utiliser

L’objet de **chaîne** est utilisé pour effectuer les tâches suivantes :

-   Créer une chaîne d’approbation de certificat.
-   Obtenez les OID de toutes les stratégies d’application et de certificat valides pour la chaîne.
-   Vérifiez l’état des certificats dans la chaîne.
-   Obtenir des informations d’erreur étendues.
-   Récupérez la collection de certificats dans la chaîne.

## <a name="members"></a>Membres

L’objet de **chaîne** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet de **chaîne** a ces méthodes.



| Méthode                                                   | Description                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationPolicies**](chain-applicationpolicies.md) | Retourne une collection d' [**OID**](oids.md) qui représente les OID de stratégie d’application valides pour la chaîne.<br/> (Héritée de **ChainIChain2**)                                                                                                                                                          |
| [**Build**](chain-build.md)                             | Génère une chaîne de vérification de certificat à partir d’un certificat de fin vers le [*certificat racine*](../secgloss/r-gly.md)approuvé, en retournant une valeur booléenne qui indique la validité globale de la chaîne.<br/> (Héritée de **ChainIChain2IChain**) |
| [**CertificatePolicies**](chain-certificatepolicies.md) | Retourne une collection d' [**OID**](oids.md) qui représente les OID de stratégie de certificat valides pour la chaîne.<br/> (Héritée de **ChainIChain2**)                                                                                                                                                          |
| [**ExtendedErrorInfo**](chain-extendederrorinfo.md)     | Retourne une chaîne qui contient des informations d’erreur supplémentaires sur l’entrée indexée.<br/> (Héritée de **ChainIChain2**)                                                                                                                                                                                 |



 

### <a name="properties"></a>Propriétés

L’objet de **chaîne** a ces propriétés.



| Propriété                                              | Type d’accès          | Description                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Certificats**](chain-certificates.md)<br/> | Lecture seule<br/> | Récupère une collection de [**certificats**](certificates.md) qui représente les certificats dans la chaîne. Il s’agit de la propriété par défaut.<br/> (Héritée de **ChainIChain2IChain**) |
| [**Statut**](chain-status.md)<br/>             | Lecture seule<br/> | Récupère l’état de validité de la chaîne ou d’un certificat spécifique dans la chaîne.<br/> (Héritée de **ChainIChain2IChain**)                                                       |



 

## <a name="remarks"></a>Remarques

L’objet de **chaîne** peut être créé et il est sécurisé pour les scripts. Le ProgID de l’objet **chaîne** est «CAPICOM. Chaîne. 2».

**CAPICOM 1. *x*:** le ProgID de l’objet **chaîne** est CAPICOM. Chaîne. 1.

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
</dt> </dl>

 

 
