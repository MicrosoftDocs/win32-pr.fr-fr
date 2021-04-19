---
description: Récupère une collection des qualificateurs de la stratégie.
ms.assetid: aa5e2225-0a39-40bc-868c-d96f5953edaa
title: PolicyInformation. Qualifiers, propriété (IADs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PolicyInformation.Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 89f24e21acd24cbcaa021f7c668fc8c208102c0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537333"
---
# <a name="policyinformationqualifiers-property"></a>PolicyInformation. Qualifiers, propriété

\[La propriété **qualificateurs** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les informations de stratégie dans l’extension des stratégies de certificat.\]

La propriété **Qualifiers** récupère une collection des qualificateurs de la stratégie.

## <a name="syntax"></a>Syntaxe


```VB
PolicyInformation.Qualifiers As Qualifiers
```



## <a name="property-value"></a>Valeur de la propriété

Le pointeur CPS (certification Practice Statement) de la stratégie ou les qualificateurs d’avis utilisateur, en tant qu’objet [**qualificateurs**](qualifiers.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| En-tête<br/>          | <dl> <dt>IADs. h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**PolicyInformation**](policyinformation.md)
</dt> </dl>

 

 
