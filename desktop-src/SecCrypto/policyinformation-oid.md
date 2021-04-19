---
description: Récupère l’OID de la stratégie. Il s’agit de la propriété par défaut.
ms.assetid: c78bbbcb-befd-491c-afbd-80c3ba124d29
title: PolicyInformation. OID, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9acab40130ef6c55bf014058b3e5a6d935ed8a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527998"
---
# <a name="policyinformationoid-property"></a>PolicyInformation. OID, propriété

\[La propriété **OID** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les informations de stratégie dans l’extension des stratégies de certificat.\]

La propriété **OID** récupère l’OID de la stratégie. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
PolicyInformation.OID As OID
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur d’objet de la stratégie en tant qu’objet [**OID**](oid.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PolicyInformation**](policyinformation.md)
</dt> </dl>

 

 
