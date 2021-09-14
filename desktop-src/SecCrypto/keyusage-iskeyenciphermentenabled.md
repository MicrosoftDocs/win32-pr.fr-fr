---
description: Récupère une valeur booléenne qui indique si le bit keyEncipherment est défini.
ms.assetid: 2bdce181-3de7-4dc1-8059-1e1ca96c0d2d
title: KeyUsage. IsKeyEnciphermentEnabled, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage.IsKeyEnciphermentEnabled
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db34737954b0627953758ebc1c5bf7a64b45b1b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228936"
---
# <a name="keyusageiskeyenciphermentenabled-property"></a>KeyUsage. IsKeyEnciphermentEnabled, propriété

\[La propriété **IsKeyEnciphermentEnabled** peut être utilisée dans les systèmes d’exploitation spécifiés dans la section Configuration requise. Utilisez plutôt la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) dans l’espace de noms [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propriété **IsKeyEnciphermentEnabled** récupère une valeur booléenne qui indique si le bit KeyEncipherment est défini.

## <a name="syntax"></a>Syntaxe


```VB
KeyUsage.IsKeyEnciphermentEnabled As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

Si la **valeur est true**, le bit KeyEncipherment est défini.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|----------------------------|----------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Utilisation**](keyusage.md)
</dt> </dl>

 

 
