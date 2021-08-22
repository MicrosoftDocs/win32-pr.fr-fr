---
description: Retourne une valeur booléenne qui indique si l’extension EKU est présente. Il s’agit de la propriété par défaut.
ms.assetid: d7568525-1054-47e1-a176-f154792f9589
title: ExtendedKeyUsage. IsPresent, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43c561e6c848380326151af12aebf584fb53eb7332c8e6c0d61074da03f7d3de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007337"
---
# <a name="extendedkeyusageispresent-property"></a>ExtendedKeyUsage. IsPresent, propriété

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista et Windows XP. Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **IsPresent** retourne une valeur booléenne qui indique si l’extension EKU est présente. Il s’agit de la propriété par défaut.

## <a name="syntax"></a>Syntaxe


```VB
ExtendedKeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, l’extension EKU est présente.

## <a name="requirements"></a>Configuration requise



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

 

 
