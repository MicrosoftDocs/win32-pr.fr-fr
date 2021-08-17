---
description: Retourne l’objet EKU utilisé pour générer l’objet de chaîne.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: Méthode CertificateStatus. EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 63ddc2cd793c786cff1f7c5bb983cdba525fb52f940723f826ab4b44b89bf1ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770289"
---
# <a name="certificatestatuseku-method"></a>Méthode CertificateStatus. EKU

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**structure X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La méthode **EKU** retourne l’objet [**EKU**](eku.md) utilisé pour créer l’objet de [**chaîne**](chain.md) .

## <a name="syntax"></a>Syntaxe


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un objet [**EKU**](eku.md) qui indique le paramètre d’utilisation de la clé étendue du [*certificat*](../secgloss/c-gly.md). Le paramètre EKU établit l’utilisation valide d’un certificat. Un seul objet **EKU** peut être défini pour chaque certificat.

## <a name="remarks"></a>Remarques

La méthode [**CertificateStatus. ApplicationPolicies**](certificatestatus-applicationpolicies.md) fournit les mêmes fonctionnalités que cette méthode, mais permet de spécifier un grand nombre de paramètres au lieu d’un seul. Si la collection d' [**OID**](oids.md) retournée par la méthode **ApplicationPolicies** contient un ou plusieurs objets [**OID**](oid.md) , l’objet [**EKU**](eku.md) retourné par cette méthode est ignoré. Utilisez la méthode **ApplicationPolicies** à la place de cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CertificateStatus**](certificatestatus.md)
</dt> <dt>

[**Objets de chiffrement**](cryptography-objects.md)
</dt> <dt>

[**EKU**](eku.md)
</dt> </dl>

 

 
