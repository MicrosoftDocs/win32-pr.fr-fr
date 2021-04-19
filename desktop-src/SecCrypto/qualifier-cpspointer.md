---
description: Récupère l’URI qui pointe vers une déclaration CPS (certification Practice Statement) publiée par l’autorité de certification.
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: Qualifier. CPSPointer, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db16e8faa25fc929e884358fcd885943adc17e32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521680"
---
# <a name="qualifiercpspointer-property"></a>Qualifier. CPSPointer, propriété

\[La propriété **CPSPointer** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]

La propriété **CPSPointer** récupère l’URI qui pointe vers une déclaration CPS (certification Practice Statement) publiée par l’autorité de certification.

## <a name="syntax"></a>Syntaxe


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a>Valeur de la propriété

URI qui pointe vers un CPS publié par l’autorité de certification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Qualificateur**](qualifier.md)
</dt> </dl>

 

 
