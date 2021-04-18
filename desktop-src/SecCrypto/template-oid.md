---
description: Récupère un objet OID qui identifie l’objet de modèle.
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Template. OID, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a8599ac999c7d6a3e3403d94ff2c6daf0eba48b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543260"
---
# <a name="templateoid-property"></a>Template. OID, propriété

\[La propriété **OID** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez le modèle OID pour le certificat pour récupérer le modèle d’extension de certificat.\]

La propriété **OID** récupère un objet [**OID**](oid.md) qui identifie l’objet de [**modèle**](template.md) .

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Template.OID As OID
```



## <a name="property-value"></a>Valeur de la propriété

Objet [**OID**](oid.md) qui identifie l’objet de [**modèle**](template.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Modèle**](template.md)
</dt> </dl>

 

 
