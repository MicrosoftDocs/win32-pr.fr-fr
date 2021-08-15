---
description: Retourne une collection d’OID qui représente les stratégies d’application utilisées pour créer l’objet de chaîne.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: Méthode CertificateStatus. ApplicationPolicies
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5a27bc08f658e317b41380b2dabd9aadc13e8b50bd4985c0fd13211fa81fd507
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770439"
---
# <a name="certificatestatusapplicationpolicies-method"></a>Méthode CertificateStatus. ApplicationPolicies

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **ApplicationPolicies** retourne une collection d' [**OID**](oids.md) qui représente les stratégies d’application utilisées pour créer l’objet de [**chaîne**](chain.md) .

## <a name="syntax"></a>Syntaxe


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Collection d' [**OID**](oids.md) . Chaque objet [**OID**](oid.md) de la collection représente un OID de stratégie d’application.

## <a name="remarks"></a>Remarques

Ajoutez des OID de stratégie d’application au regroupement pour spécifier les stratégies d’application qui doivent être utilisées pour générer la chaîne d’approbation de certificat. Si la collection contient au moins un objet [**OID**](oid.md) , l’objet [**EKU**](eku.md) renvoyé par la méthode [**CertificateStatus. EKU**](certificatestatus-eku.md) est ignoré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
