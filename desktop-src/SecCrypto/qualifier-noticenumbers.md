---
description: Récupère la collection de numéros d’avis de l’utilisateur.
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: Qualifier. NoticeNumbers, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ef9b2c4c70e011cc33f0aa9d9f2bbcc9f530bec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542403"
---
# <a name="qualifiernoticenumbers-property"></a>Qualifier. NoticeNumbers, propriété

\[La propriété **NoticeNumbers** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]

La propriété **NoticeNumbers** récupère la collection de numéros d’avis de l’utilisateur. Cette propriété peut être vide.

## <a name="syntax"></a>Syntaxe


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a>Valeur de la propriété

Collection de numéros d’avis de l’utilisateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Qualificateur**](qualifier.md)
</dt> </dl>

 

 
