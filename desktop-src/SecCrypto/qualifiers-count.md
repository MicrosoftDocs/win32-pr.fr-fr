---
description: Récupère le nombre d’objets qualificateurs dans la collection.
ms.assetid: 9dafb83a-ff7f-4317-8ed4-2a46dcebf409
title: Qualifiers. Count, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fd4cfe0d600c99251db77b1764edb83353b01143fc5179c1efc29673e30e734
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900945"
---
# <a name="qualifierscount-property"></a>Qualifiers. Count, propriété

\[La propriété **Count** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section relative à la configuration requise. Utilisez plutôt la [**classe X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) en appelant le constructeur qui prend un OID comme paramètre, puis utilisez l’OID pour les stratégies de certificat pour traiter les qualificateurs qui font partie des informations de stratégie dans l’extension des stratégies de certificat.\]

La propriété **Count** récupère le nombre d’objets [**qualificateurs**](qualifier.md) dans la collection.

## <a name="syntax"></a>Syntaxe


```VB
Qualifiers.Count As Long
```



## <a name="property-value"></a>Valeur de la propriété

Nombre d’objets [**qualificateurs**](qualifier.md) dans la collection.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Qualificateurs**](qualifiers.md)
</dt> </dl>

 

 
