---
description: Récupère l’ID d’objet du qualificateur.
ms.assetid: 58ec2af7-f085-43bc-8ea8-926cb840abe9
title: Qualifier. OID, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42c2f83d4fa8be31991a98b6fe4cfc6a741e2190cd12d54bfd5e968951472bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901049"
---
# <a name="qualifieroid-property"></a>Qualifier. OID, propriété

\[La propriété **OID** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]

La propriété **OID** récupère l’ID d’objet du qualificateur. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
Qualifier.OID As OID
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**OID**](oid.md) qui identifie le qualificateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Qualificateur**](qualifier.md)
</dt> </dl>

 

 
