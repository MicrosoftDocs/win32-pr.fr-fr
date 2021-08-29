---
description: Récupère l’objet PolicyInformation qui représente la stratégie indexée. Il s’agit de la propriété par défaut.
ms.assetid: 0143629a-97cf-43f4-8f96-774f0f5cfeca
title: CertificatePolicies. Item, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 001a0cd8e6bab9c6be998f78d467c5b446c639cff994a91865ed99c77ca71caa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877919"
---
# <a name="certificatepoliciesitem-property"></a>CertificatePolicies. Item, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour récupérer les stratégies de certificat.\]

La propriété **Item** récupère l’objet [**PolicyInformation**](policyinformation.md) qui représente la stratégie indexée. Il s’agit de la propriété par défaut.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
CertificatePolicies.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**PolicyInformation**](policyinformation.md) qui représente la stratégie indexée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
