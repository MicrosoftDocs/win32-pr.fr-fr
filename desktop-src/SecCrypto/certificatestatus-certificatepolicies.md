---
description: Retourne une collection d’OID qui représente les stratégies de certificat utilisées pour créer l’objet de chaîne.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: Méthode CertificateStatus. CertificatePolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98c9e22c0cad40252cc9eebebf9aa32dc4d89b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532612"
---
# <a name="certificatestatuscertificatepolicies-method"></a>Méthode CertificateStatus. CertificatePolicies

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **certificatePolicies** retourne une collection d' [**OID**](oids.md) qui représente les stratégies de certificat utilisées pour créer l’objet de [**chaîne**](chain.md) .

## <a name="syntax"></a>Syntaxe


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Collection d' [**OID**](oids.md) . Chaque objet [**OID**](oid.md) de la collection représente un OID de stratégie de certificat.

## <a name="remarks"></a>Notes

Ajoutez des OID de stratégie de certificat au regroupement pour spécifier les stratégies de certificat à utiliser pour générer la chaîne d’approbation de certificat.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
