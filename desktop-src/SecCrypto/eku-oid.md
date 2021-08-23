---
description: Définit ou récupère une chaîne qui contient une valeur de chaîne d’OID EKU telle que définie dans wincrypt. h.
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: 'IEKU :: OID, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 49a35cb223c338573ba0a52288a1e5528820dcbd4c7589548ce31f9df46dc1e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875249"
---
# <a name="iekuoid-property"></a>IEKU :: OID, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **OID** définit ou récupère une chaîne qui contient une valeur de chaîne d’OID EKU telle que définie dans wincrypt. h.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
EKU.OID As String
```



## <a name="property-value"></a>Valeur de la propriété

Chaîne qui contient la valeur de chaîne OID de l’EKU telle que définie dans wincrypt. h.

## <a name="remarks"></a>Remarques

Cette propriété n’utilise pas l’objet [**OID**](oid.md) introduit dans CAPICOM 2,0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
