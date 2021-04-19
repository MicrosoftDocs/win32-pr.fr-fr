---
description: Récupère une valeur booléenne qui indique si le bit encipherOnly est défini.
ms.assetid: 60d79ea4-4968-49e0-8d16-873fbcbd951c
title: KeyUsage. IsEncipherOnlyEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsEncipherOnlyEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8a473797f989d18e090af33f08274ecede2630b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541259"
---
# <a name="keyusageisencipheronlyenabled-property"></a>KeyUsage. IsEncipherOnlyEnabled, propriété

\[La propriété **IsEncipherOnlyEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **IsEncipherOnlyEnabled** récupère une valeur booléenne qui indique si le bit encipherOnly est défini.

## <a name="syntax"></a>Syntaxe


```VB
KeyUsage.IsEncipherOnlyEnabled As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, le bit encipherOnly est défini.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Utilisation**](keyusage.md)
</dt> </dl>

 

 
