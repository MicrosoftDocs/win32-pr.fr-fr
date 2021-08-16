---
description: Ajoute un objet d’attribut à la collection.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Attributes. Add, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5639a4bed96dcf4cef315b4550cd2982778d6ecc68024364f06eb377cbd8b0d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773514"
---
# <a name="attributesadd-method"></a>Attributes. Add, méthode

\[capicom est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/previous-versions/windows/) .\]

La méthode **Add** ajoute un objet [**attribut**](attribute.md) à la collection.

## <a name="syntax"></a>Syntaxe


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Attribut* \[ dans\]
</dt> <dd>

Objet d' [**attribut**](attribute.md) à ajouter à la fin de la collection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur. Une application qui utilise cette méthode doit contenir du code pour gérer une exception levée par cette méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | capicom 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets de chiffrement](cryptography-objects.md)
</dt> <dt>

[**Attributs**](attributes.md)
</dt> </dl>

 

 
