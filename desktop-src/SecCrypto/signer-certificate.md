---
description: Définit ou récupère l’objet de certificat qui représente le certificat d’un signataire des données.
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: Signature. Certificate, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5c91a2b508370fd9f59df4b2228895372ce8ee1ec502a5d6111c527c4d00e7ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117973619"
---
# <a name="signercertificate-property"></a>Signature. Certificate, propriété

\[La propriété **certificat** est disponible pour une utilisation dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe CmsSigner**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propriété **Certificate** définit ou récupère l’objet [**certificat**](certificate.md) qui représente le certificat d’un signataire des données. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a>Valeur de la propriété

Objet de [**certificat**](certificate.md) qui représente le certificat d’un signataire des données.

## <a name="remarks"></a>Remarques

Lorsque la valeur de cette propriété est réinitialisée, directement ou indirectement, l’intégralité de l' [*État*](../secgloss/s-gly.md) de l’objet est réinitialisée.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Signataire**](signer.md)
</dt> </dl>

 

 
