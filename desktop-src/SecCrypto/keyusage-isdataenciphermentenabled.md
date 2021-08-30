---
description: Récupère une valeur booléenne qui indique si le bit dataEncipherment est défini.
ms.assetid: 9b29a76f-1494-4db3-a5d7-69fe631ca1dd
title: KeyUsage. IsDataEnciphermentEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDataEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1ca5e71de36503406e5cc45f136fc7e86eb3ec2cc0324d4a1a75d81cf1bc6fa4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100779"
---
# <a name="keyusageisdataenciphermentenabled-property"></a>KeyUsage. IsDataEnciphermentEnabled, propriété

\[La propriété **IsDataEnciphermentEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **IsDataEnciphermentEnabled** récupère une valeur booléenne qui indique si le bit DataEncipherment est défini.

## <a name="syntax"></a>Syntaxe


```VB
KeyUsage.IsDataEnciphermentEnabled As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, le bit DataEncipherment est défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Utilisation**](keyusage.md)
</dt> </dl>

 

 
