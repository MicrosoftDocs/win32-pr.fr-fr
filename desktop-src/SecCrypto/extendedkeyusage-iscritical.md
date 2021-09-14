---
description: Retourne une valeur booléenne qui indique si l’extension d’utilisation améliorée de la clé est marquée comme critique.
ms.assetid: f6d2a2e0-512b-44f2-a7d9-9ad661398aa8
title: ExtendedKeyUsage. IsCritical, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5331922567af3b9a34517ab5059fa03ad9904270
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127118885"
---
# <a name="extendedkeyusageiscritical-property"></a>ExtendedKeyUsage. IsCritical, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **IsCritical** retourne une valeur booléenne qui indique si l’extension d’utilisation améliorée de la clé est marquée comme critique.

## <a name="syntax"></a>Syntaxe


```VB
ExtendedKeyUsage.IsCritical As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, l’extension d’utilisation améliorée de la clé est marquée comme critique.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ExtendedKeyUsage**](extendedkeyusage.md)
</dt> </dl>

 

 
