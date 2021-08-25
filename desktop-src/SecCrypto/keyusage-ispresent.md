---
description: Récupère une valeur booléenne qui indique si l’extension KeyUsage est présente.
ms.assetid: d666049a-4b40-42b6-8c2d-c27a1bb4c48a
title: KeyUsage. IsPresent, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2eb962445717743512de396065304f70c31f02cfa4f3448a08a2731ed1fd377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992859"
---
# <a name="keyusageispresent-property"></a>KeyUsage. IsPresent, propriété

\[La propriété **IsPresent** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **IsPresent** récupère une valeur booléenne qui indique si l’extension [**KeyUsage**](keyusage.md) est présente.

Cette propriété est la propriété par défaut de l’objet [**KeyUsage**](keyusage.md) .

## <a name="syntax"></a>Syntaxe


```VB
KeyUsage.IsPresent As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, l’extension KeyUsage est présente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Utilisation**](keyusage.md)
</dt> </dl>

 

 
