---
description: Récupère le nombre d’objets attribute dans la collection.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Attributes. Count, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537540"
---
# <a name="attributescount-property"></a>Attributes. Count, propriété

\[CAPICOM est un composant uniquement de 32 bits qui peut être utilisé dans les systèmes d’exploitation suivants : Windows Server 2008, Windows Vista, Windows XP. Utilisez plutôt la [**classe CryptographicAttributeObjectCollection**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) dans l’espace de noms [**System. Security. Cryptography**](/previous-versions/windows/) .\]

La propriété **Count** récupère le nombre d’objets [**attribute**](attribute.md) dans la collection.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
Attributes.Count As Long
```



## <a name="property-value"></a>Valeur de la propriété

Nombre d’objets [**attribute**](attribute.md) dans la collection. Chaque objet d' **attribut** représente un attribut unique dans la collection.

## <a name="remarks"></a>Notes

La propriété **Count** peut être utilisée pour spécifier le dernier objet d' [**attribut**](attribute.md) dans la collection lors de la récupération d’un objet **attribut** spécifique à l’aide de la propriété Attributes [**. Item**](attributes-item.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de la prise en charge des clients<br/> | Windows Vista<br/>                                                               |
| Fin de la prise en charge des serveurs<br/> | Windows Server 2008<br/>                                                         |
| Composant redistribuable<br/>       | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs**](attributes.md)
</dt> </dl>

 

 
