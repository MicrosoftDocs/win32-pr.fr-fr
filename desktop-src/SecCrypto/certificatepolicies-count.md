---
description: Récupère le nombre d’objets PolicyInformation dans la collection.
ms.assetid: d4fb6bd8-4e92-4de8-9430-dd3b6262a806
title: CertificatePolicies. Count (propriété)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 405fbc928f6ff553abe3cd55d3f6e08a1aed13ef46093f912b6b08af45ec2c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771047"
---
# <a name="certificatepoliciescount-property"></a>CertificatePolicies. Count (propriété)

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour récupérer les stratégies de certificat.\]

La propriété **Count** récupère le nombre d’objets [**PolicyInformation**](policyinformation.md) dans la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
CertificatePolicies.Count As Long
```



## <a name="property-value"></a>Valeur de la propriété

Nombre d’objets [**PolicyInformation**](policyinformation.md) dans la collection. Chaque objet **PolicyInformation** représente une stratégie de certificat unique dans la collection.

## <a name="remarks"></a>Remarques

La propriété **Count** peut être utilisée pour spécifier le dernier objet [**PolicyInformation**](policyinformation.md) dans la collection lors de l’extraction d’un objet **PolicyInformation** spécifique à l’aide de la propriété [**certificatePolicies. Item**](certificatepolicies-item.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
