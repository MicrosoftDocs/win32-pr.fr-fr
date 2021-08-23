---
description: Récupère une valeur booléenne qui indique si le bit decipherOnly est défini.
ms.assetid: 69d8649d-c7bc-438b-afdd-6c9d2627cd72
title: KeyUsage. IsDecipherOnlyEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsDecipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e46a2d5fb04b54922081bc7c15ab4cfdcbe7536974720d39472ac0af8c64fca5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622309"
---
# <a name="keyusageisdecipheronlyenabled-property"></a>KeyUsage. IsDecipherOnlyEnabled, propriété

\[La propriété **IsDecipherOnlyEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **IsDecipherOnlyEnabled** récupère une valeur booléenne qui indique si le bit decipherOnly est défini.

## <a name="syntax"></a>Syntaxe


```VB
KeyUsage.IsDecipherOnlyEnabled As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, le bit decipherOnly est défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Utilisation**](keyusage.md)
</dt> </dl>

 

 
