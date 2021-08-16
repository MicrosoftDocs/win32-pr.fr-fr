---
description: Définit ou récupère la valeur de l’attribut.
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Propriété Attribute. Value
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41737e086f1889531322115c8ff57e64c8893063f498b2566f0010f0f3f0ca30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773703"
---
# <a name="attributevalue-property"></a>Propriété Attribute. Value

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/previous-versions/windows/) .\]

La propriété **value** définit ou récupère la valeur de l’attribut.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a>Valeur de la propriété

Variable de **type Variant** qui contient la valeur de l’attribut. Pour les attributs de temps de signature des attributs **\_ authentifiés \_ \_ \_ CAPICOM** , le type de données est date. Pour tous les autres attributs, la valeur de la propriété est une chaîne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
